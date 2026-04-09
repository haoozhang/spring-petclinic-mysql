---
name: security-assessment-merge
description: Merge CVE and CWE security assessment results into a unified security report and update report.json
---

# Security Assessment: Merge and Report

## Role

You are a **security assessment aggregator**. Your task is to read all CVE and CWE result files produced by earlier security skills, merge them into a unified security assessment report, and inject the findings into `report.json`.

> **Important:** You are a data aggregator, NOT an analyzer. Do NOT re-scan the codebase. Your sole responsibility is to read, normalize, merge, and write the security findings that were already produced by the CVE and CWE assessment skills.

## Objective

1. Read all security assessment result files from the `security/` subdirectory
2. Normalize CVE and CWE findings into a unified format
3. Generate `security-assessment.json` (machine-readable merged report)
4. Generate `security-assessment.md` (human-readable markdown report)
5. Inject a `"security"` array into the existing `report.json`

## Instructions

### Step 1: Read CVE Results

Read the CVE result file at `security/cve-assessment-result.json`.

This file is a **flat JSON array** where each element has:
```json
{
  "id": "CVE-2024-xxxx",
  "name": "Summary",
  "status": "FOUND",
  "category": "CVE",
  "severity": "mandatory|optional|potential",
  "storyPoint": 1,
  "evidence": {
    "files": ["pom.xml:42"],
    "explanation": "Markdown description..."
  }
}
```

Only include entries where `status` is `"FOUND"`.

If the file does not exist or is empty, treat CVE findings as an empty list.

### Step 2: Read CWE Results

Read all CWE result files matching `security/result-cwe-*.json`.

Each CWE file uses a **wrapper format**:
```json
{
  "input_name": "CWE - Category Name",
  "status": "success",
  "result": {
    "values": [
      {
        "id": "CWE-79",
        "name": "Cross-site Scripting",
        "status": "FOUND",
        "category": "Injection Attacks",
        "evidence": {
          "files": ["src/Controller.java"],
          "explanation": "Description..."
        }
      }
    ]
  }
}
```

Navigate to `result.values` in each file and extract entries where `status` is `"FOUND"`.

If no CWE files exist, treat CWE findings as an empty list.

### Step 3: Build the Unified Security Findings Array

Transform all FOUND CVE and CWE items into the unified format:

```json
{
  "id": "CVE-2024-xxxx or CWE-79",
  "title": "Human-readable title",
  "category": "CVE or CWE category (e.g., Injection Attacks)",
  "severity": "mandatory|optional|potential",
  "description": "Detailed description",
  "evidence": {
    "files": ["path/to/file.java"],
    "explanation": "Why this was flagged"
  },
  "storyPoint": 1
}
```

For **CVE findings**: Map `name` → `title`, use `explanation` as both `description` and `evidence.explanation`.

For **CWE findings**: Map `name` → `title`, use `explanation` as `evidence.explanation`, and construct `description` from the CWE name and category.

### Step 4: Calculate Summary Statistics

Count:
- `totalFindings`: Total number of FOUND CVE + CWE items
- `cveCount`: Number of CVE findings
- `cweCount`: Number of CWE findings
- `bySeverity`: Count of findings grouped by severity (`mandatory`, `optional`, `potential`)
- `byCategory`: Count of findings grouped by category (`CVE`, `Injection Attacks`, etc.)
- `totalRulesAssessed`: Total number of CWE checklist items across all `result-cwe-*.json` files (both FOUND and NOT_FOUND)
- `rulesPassed`: `totalRulesAssessed - cweCount`

### Step 5: Write security-assessment.json

Write the full merged report to `security/security-assessment.json`:

```json
{
  "GeneratedAt": "2026-04-09T12:00:00.0000000Z",
  "ProjectPath": ".",
  "Summary": {
    "TotalFindings": 5,
    "CveCount": 2,
    "CweCount": 3,
    "BySeverity": { "mandatory": 3, "optional": 1, "potential": 1 },
    "ByCategory": { "CVE": 2, "Injection Attacks": 2, "Code Quality": 1 },
    "TotalRulesAssessed": 59,
    "RulesPassed": 56
  },
  "CveFindings": [
    {
      "Id": "CVE-2024-xxxx",
      "Name": "Vulnerability Title",
      "Category": "CVE",
      "Severity": "mandatory",
      "StoryPoint": 1,
      "Description": "...",
      "Files": ["pom.xml:42"],
      "Explanation": "..."
    }
  ],
  "CweFindings": [
    {
      "Id": "CWE-79",
      "Name": "Cross-site Scripting",
      "Category": "Injection Attacks",
      "Severity": "optional",
      "StoryPoint": 8,
      "Description": "...",
      "Files": ["src/Controller.java"],
      "Explanation": "..."
    }
  ]
}
```

### Step 6: Write security-assessment.md

Write a human-readable markdown report to `security/security-assessment.md`:

```markdown
# Security Assessment Report

**Generated:** <timestamp>

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | N |
| CVE Vulnerabilities | N |
| CWE Vulnerabilities | N |
| Total Rules Assessed | N |
| Rules Passed | N |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | N |
| optional | N |
| potential | N |

## CVE Findings (Dependency Vulnerabilities)

### CVE-2024-xxxx: Title
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:42

<explanation>

## CWE Findings (Code-Level Vulnerabilities)

### CWE-79: Cross-site Scripting
- **Category:** Injection Attacks
- **Severity:** optional
- **Story Points:** 8
- **Files:** src/Controller.java

> <explanation>
```

If there are no findings at all, write:
```markdown
## No security vulnerabilities found.

The assessment did not detect any CVE or CWE vulnerabilities in the codebase.
```

### Step 7: Merge into report.json

**Use `jq` for safe JSON manipulation** — do NOT manually rewrite report.json.

First, write the unified findings array to a temporary file, then merge:

```bash
# Write the unified findings array
cat > security/unified-findings.json << 'SECURITY_EOF'
[
  ... unified findings array from Step 3 ...
]
SECURITY_EOF

# Merge into report.json using jq
if [ -f "report.json" ] && command -v jq &> /dev/null; then
  jq --argjson sec "$(cat security/unified-findings.json)" '. + {"security": $sec}' report.json > report.json.tmp && mv report.json.tmp report.json
elif [ -f "report.json" ]; then
  # Fallback without jq: use python or node
  python3 -c "
import json, sys
with open('report.json', 'r') as f: report = json.load(f)
with open('security/unified-findings.json', 'r') as f: security = json.load(f)
report['security'] = security
with open('report.json', 'w') as f: json.dump(report, f, indent=2)
" 2>/dev/null || echo "Warning: Could not merge security into report.json (jq and python3 unavailable)"
fi

# Clean up temp file
rm -f security/unified-findings.json
```

If `report.json` does not exist (e.g., AppCAT failed), create a minimal stub:
```json
{
  "metadata": {
    "generated_at": "<timestamp>",
    "note": "Security-only report (AppCAT was not run or failed)"
  },
  "security": [ ... ]
}
```

## Error Handling

- If no security result files exist at all, write empty reports (`security-assessment.json` with zero findings, `security-assessment.md` with "No vulnerabilities found")
- If a CWE result file is malformed, skip it and continue with the rest
- If the `report.json` merge fails, log a warning but do NOT fail the overall task — the standalone `security-assessment.json` is still valid
- Always produce all three output files (`security-assessment.json`, `security-assessment.md`, and the merged `report.json`)
