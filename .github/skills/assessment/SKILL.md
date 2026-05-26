---
name: assessment
description: Run application assessment for a single repository
---

# Application Assessment

This skill performs application assessment for a single repository. It supports Java, .NET, and JavaScript/TypeScript projects.

## Input Parameters

- `workspace-path` (optional): Path to the project to assess. Defaults to the current directory (repository root) when not specified. All assessment outputs are written relative to this path (e.g. `{workspace-path}/.github/modernize/assessment/reports/report-{reportId}/report.json`). For a repository with multiple sub-projects, pass the sub-project directory path so that each sub-project's outputs are isolated.

## When to Use This Skill

Use this skill when you need to:

- Assess a Java or .NET application for cloud readiness and migration issues
- Assess a JavaScript/TypeScript project for outdated dependencies and available updates
- Generate detailed assessment reports with issue analysis and recommendations
- Understand application dependencies, frameworks, and potential migration blockers

## What This Skill Does

This skill performs a simplified assessment workflow:

1. **Check Project Type and Prerequisites**:
   - **For Java projects**: Verify that MCP tool is available ('appmod-run-assessment-action')
     - If this MCP tool is not configured, return immediately with setup instructions
     - **IMPORTANT**: For Java projects, you MUST ONLY call the 'appmod-run-assessment-action' MCP tool. Do NOT call 'appmod-precheck-assessment', 'appmod-install-appcat', 'appmod-run-assessment', or any other MCP tool. The 'appmod-run-assessment-action' tool handles everything (prerequisite checks, installation, and assessment execution) in a single call.
   - **For .NET projects**: Check if .NET SDK is available
     - No MCP tools required for .NET assessment
   - **For JavaScript/TypeScript projects**: Check if Node.js and npm are available
     - No MCP tools required for JS/TS assessment

2. **Run Assessment**:
   - **For Java projects**: Trigger AppCAT analysis via Assessment MCP server
     - Uses 'appmod-run-assessment-action' MCP tool
     - The MCP tool automatically saves the report to the versioned directory
   - **For .NET projects**: Install and run AppCAT directly
     - Install: `dotnet tool update dotnet-appcat`
     - Find all .csproj files under `{workspace-path}`
     - Join project paths with semicolons: `projectPaths="project1.csproj;project2.csproj"`
     - Run: `dotnet-appcat analyze $projectPaths --source Solution --target Any --serializer APPMODJSON --code --privacyMode Restricted --non-interactive --report {workspace-path}\.github\modernize\appcat\result\report.json`
   - **For JavaScript/TypeScript projects**: Install and run npm-check-updates
     - Install: `npm install -g npm-check-updates@19.6.3 --prefix {tool-install-dir}`
     - Run: `ncu --format group --packageFile {workspace-path}/package.json`
     - Save the output to `{workspace-path}/.github/modernize/assessment/js-assessment-report.md`
   - Analyzes code for cloud migration issues or dependency updates
   - Generates structured assessment data

3. **Save Report to Versioned Directory (.NET only)**:
   - **For Java projects**: The MCP tool automatically saves the report to `{workspace-path}/.github/modernize/assessment/reports/report-{reportId}/report.json` — no manual saving needed
   - **For .NET projects**: The report is at `{workspace-path}/.github/modernize/appcat/result/report.json`
   - Read the generated `report.json` and extract the `metadata.analysisStartTime` field
   - Format the timestamp as `yyyyMMddHHmmss` to produce the `reportId` (e.g. `2024-06-15T14:30:52Z` becomes `20240615143052`)
   - Create the versioned directory: `mkdir -p {workspace-path}/.github/modernize/assessment/reports/report-{reportId}`
   - Move the report to: `{workspace-path}/.github/modernize/assessment/reports/report-{reportId}/report.json`
   - This versioned report should be included in the pull request

## How to Use

### Prerequisites

**For Java projects**:
- MCP tool must be available: 'appmod-run-assessment-action'
- If tool is not configured, the skill will return instructions for setup
- **CRITICAL**: Only call 'appmod-run-assessment-action'. Never call 'appmod-precheck-assessment', 'appmod-install-appcat', or 'appmod-run-assessment' — these are legacy tools and must not be used.

**For .NET projects**:
- .NET SDK must be installed
- No MCP tools required - appcat will be installed and run directly via .NET CLI
- The assessment will automatically install `dotnet-appcat` tool if not already present

**For JavaScript/TypeScript projects**:
- Node.js and npm must be installed
- No MCP tools required - npm-check-updates will be installed and run directly via npm
- The assessment will automatically install `npm-check-updates` if not already present

### Triggering Assessment

Simply express the intent to assess the application. Example prompts:

- "Assess the application"
- "Run assessment for this project"

The assessment process automatically:
- Detects project language and framework within `{workspace-path}`
- **For Java**: Uses MCP tool to run AppCAT and automatically save report to versioned directory
- **For .NET**: Installs dotnet-appcat tool and runs analysis directly
- **For JavaScript/TypeScript**: Installs npm-check-updates and runs dependency analysis
- Executes comprehensive analysis
- **For Java**: Report is automatically saved to `{workspace-path}/.github/modernize/assessment/reports/report-{reportId}/report.json`
- **For .NET**: Generates report at `{workspace-path}/.github/modernize/appcat/result/report.json`
- **For JavaScript/TypeScript**: Generates report at `{workspace-path}/.github/modernize/assessment/js-assessment-report.md`

### Report Saving

**For Java projects**:
1. The 'appmod-run-assessment-action' MCP tool automatically saves the report to `{workspace-path}/.github/modernize/assessment/reports/report-{reportId}/report.json`
2. No manual report moving is needed
3. Include this versioned report in the pull request

**For .NET projects**:
1. Report is initially generated at `{workspace-path}/.github/modernize/appcat/result/report.json`
2. Read the report and extract `metadata.analysisStartTime`, format as `yyyyMMddHHmmss` to get `reportId`
3. Move the report to `{workspace-path}/.github/modernize/assessment/reports/report-{reportId}/report.json`
4. Include this versioned report in the pull request

**For JavaScript/TypeScript projects**:
1. Report is directly generated at `{workspace-path}/.github/modernize/assessment/js-assessment-report.md`
2. Include this report in the pull request

## Report Output Location

Report location depends on project type:

**For Java projects** (via MCP server):
- Automatically saved to: `{workspace-path}/.github/modernize/assessment/reports/report-{reportId}/report.json`

**For .NET projects** (direct execution):
- Initially generated at: `{workspace-path}/.github/modernize/appcat/result/report.json`
- Moved to versioned directory: `{workspace-path}/.github/modernize/assessment/reports/report-{reportId}/report.json`

**For JavaScript/TypeScript projects** (direct execution):
- Directly generated at: `{workspace-path}/.github/modernize/assessment/js-assessment-report.md`

## Success Criteria

Assessment is complete when:
- ✅ **For Java**: MCP server is available (or clear instructions provided if not)
- ✅ **For .NET**: .NET SDK is available and dotnet-appcat tool is installed
- ✅ **For JavaScript/TypeScript**: Node.js and npm are available and npm-check-updates is installed
- ✅ AppCAT analysis executes without errors (Java/.NET) or ncu analysis executes without errors (JS/TS)
- ✅ **For Java and .NET**: Report generated at `{workspace-path}/.github/modernize/assessment/reports/report-{reportId}/report.json`
- ✅ **For JavaScript/TypeScript**: Report generated at `{workspace-path}/.github/modernize/assessment/js-assessment-report.md`
- ✅ Report metadata includes assessment tool version, timestamp, and configuration

## Troubleshooting

**Prerequisites Not Met**:
- **For Java**: Verify MCP tool is available ('appmod-run-assessment-action')
  - Return immediately with setup instructions if tool is not available
  - Do not attempt to run assessment without MCP
- **For .NET**: Verify .NET SDK is installed
  - Check with `dotnet --version` command
  - Provide installation instructions if .NET SDK is missing
- **For JavaScript/TypeScript**: Verify Node.js and npm are installed
  - Check with `npm --version` command
  - Provide installation instructions if npm is missing

**Assessment Failures**:
- Unsupported project type (only Java, .NET, and JavaScript/TypeScript supported)
- **For Java**: MCP server communication errors
- **For .NET**:
  - dotnet-appcat tool installation failure
  - dotnet-appcat command execution errors
- **For JavaScript/TypeScript**:
  - npm-check-updates installation failure
  - ncu command execution errors
  - No package.json found at `{workspace-path}/package.json`
- Invalid project structure or build configuration

**Report Generation Issues**:
- **For Java**: No report.json found at `{workspace-path}/.github/modernize/assessment/reports/report-{reportId}/report.json` after MCP execution
- **For .NET**: Report not generated at `{workspace-path}/.github/modernize/appcat/result/report.json`, or `metadata.analysisStartTime` missing from report
- **For JavaScript/TypeScript**: Report not generated at `{workspace-path}/.github/modernize/assessment/js-assessment-report.md`
- Report file is corrupted or invalid JSON (Java/.NET only)

For any failure, provide clear error messages and troubleshooting steps.
