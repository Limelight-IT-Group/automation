# Automation

## Overview
Automation scripts, workflows and pipelines for Limelight IT Group operations and client service delivery.

## Purpose
Centralises all automation tooling used by Limelight IT — from internal ops scripts to client onboarding workflows, M365 provisioning and reporting pipelines. Built for reliability, reuse and rapid deployment.

## Structure
```
automation/
├── workflows/     # End-to-end automation workflows
├── scripts/       # Standalone automation scripts
├── templates/     # Reusable script and config templates
├── tests/         # Unit and integration tests
├── .gitignore
└── README.md
```

## Usage
Each script includes a header comment with usage instructions:
```bash
python3 scripts/<script_name>.py --help
```
Copy `.env.example` to `.env` and populate credentials before running.

## Standards
- Python 3.10+ required
- All scripts must be idempotent where possible
- Logging to stdout — no silent failures
- Secrets via environment variables only
- Tests required for any script touching production systems
- Commit messages follow Conventional Commits: `feat:` `fix:` `chore:` `docs:`

## License
MIT License — Copyright (c) 2026 Limelight IT Group