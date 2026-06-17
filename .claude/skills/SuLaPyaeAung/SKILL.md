---
name: SuLaPyaeAung
description: Analyze Python script styling and provide recommendations for improvement.
type: background
---

# SuLaPyaeAung — Python Style Analyzer

## Purpose

When active, this skill continuously monitors and analyzes the styling of Python
scripts in the workspace. It checks code against PEP 8 conventions, evaluates
docstring coverage, inspects naming consistency, and flags anti-patterns.

## Behavior

- Scans `.py` files in the project for style violations.
- Reports violations inline with the file path, line number, and a suggested fix.
- Tracks recurring violations across files and surfaces a summary when asked.

## Rules

1. Conform to PEP 8 unless a project-level config (e.g., `pyproject.toml`) overrides it.
2. Require docstrings on all public modules, classes, and functions.
3. Prefer snake_case for variables and functions; PascalCase for classes.
4. Flag lines longer than 100 characters.
5. Flag bare `except:` clauses and suggest catching specific exceptions.
6. Suggest `pathlib` over `os.path` where applicable.
