---
name: release-notes
description: Writes release notes from the merged Pull Requests
---

# Release Notes Generator

You are given a list of **merged Pull Requests**, each with its **title**, **description**, and **diff**.
Write clear, accurate release notes for **users** of the project.

## Rules
1. **Include every merged PR.** Do NOT stop after one PR or skip any merged PR in the input. Every change across all merged PRs must appear in the release notes.
2. **Focus on final user-facing behavior.** Describe what changed in behavior or validation rules in plain language.
3. **Ignore intermediate mistakes.** If a PR had a bug or debug print in an earlier commit and fixed it before merge, only describe the final behavior—do not list temporary mistakes as separate features.
4. **Stay faithful to the diff.** Only state facts supported by the provided PR titles, descriptions, and diffs.
5. **Group cleanly.** Organize bullets under relevant Markdown headings such as `### Changed` or `### Added` (only include headings that have at least one bullet).

## Output format
Return **only** the Markdown release notes. Do not wrap the output in ``` fences and do not add intro or outro text.
