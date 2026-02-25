# AGENTS.md - Development Guide

Quick start guide for running the TCMS Schemas validator.

## Installation

```bash
# Install dependencies
uv pip install -r requirements.txt
```

## Running Validation

```bash
# Validate a single file with auto-detected schema
python validator.py samples/test-case/gsma_4.4.2.2_TC.yml

# Validate with explicit schema path
python validator.py samples/test-plan/data.yml schemas/tcms/test-plan.schema.json
```

## Project Structure

```
tcms-schemas/
├── validator.py              # Main validation script
├── requirements.txt          # Python dependencies
├── schemas/                  # Schema definitions
│   └── tcms/
│       ├── test-case-main.schema.json
│       ├── test-plan.schema.json
│       ├── execution-log.schema.json
│       └── verification-result.schema.json
└── samples/                  # Sample YAML files
    ├── test-case/
    │   ├── gsma_4.4.2.2_TC.yml
    │   └── gsma_4.4.2.3_TC.yml
    └── test-plan/data.yml
```

## Dependencies

- PyYAML (6.0.1) - YAML parsing
- jsonschema (4.20.0) - JSON schema validation
- click - Command-line interface framework
