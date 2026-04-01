# Copilot instructions for DevOps_Shack_Ultimate_Pipeline_12_march

## High-level architecture and intent
- This repository is a *DevOps documentation/pipeline cookbook* organized by phases: `PHASE-1`, `PHASE-2`, `PHASE-3`, `PHASE-4`.
- Each phase is a sequence of infrastructure or CI/CD instructions (Jenkins, Nexus, SonarQube, K8s, etc.), not a multi-service codebase.
- Files under `PHASE-*/*.md` are authoritative source-of-truth for steps, shell scripts, and configuration commands.
- `app` is a placeholder text file, not application source code.

## What to change in this repo
- Focus on improving docs in `PHASE-*/*.md` and top-level `README.md` to be precise, reproducible, and consistent.
- Prefer adding sample commands exactly as shown in existing style (e.g., in `PHASE-1/Jenkins.md` use `bash` fenced blocks and runnable script blocks).
- Keep file organization intact: no need to create new phase directories unless explicitly asked.

## Conventions and patterns
- Existing docs use shell script snippets that can be copy/pasted (with shebangs and `chmod +x` instructions).
- Standard flow: describe objective, show script, then instructions to save and run (e.g., `install_jenkins.sh`).
- Minimal narrative in `README.md` currently, so new contributions should include clear objectives and context.

## Developer workflows
- No build/test toolchain is defined in source; guided workflow is in docs (e.g., install, configure, run Jenkins/Docker/K8s commands).
- If adding workflow docs, include expected environment (Ubuntu 22.04, root privileges, `sudo`, etc.).
- Avoid guessing unsourced CI or test commands.

## External dependencies/integration points
- `PHASE-1/Jenkins.md` references Jenkins package repo and Docker repository, so keep URLs current and verify package names.
- `PHASE-1/K8-Setup.md` likely contains Kubernetes configuration tasks; preserve step order and command fidelity.
- Follow path-based linking style (`PHASE-2/Git-Repo-Setup.md`, etc.) for internal cross-reference.

## AI behavior when editing
- Do not add generic instructions such as “write tests” unless explicitly requested; keep content practical and specific to this repository structure.
- Use concrete examples from existing files (e.g., replicate the `chmod +x install_jenkins.sh` pattern).
- Keep edits small and atomic, with clear commit semantics.

## Meta
- This file can be updated iteratively if more code appears (non-doc source) in later phases.
- If uncertain about scope, ask: “Should I add a new `PHASE-5` doc or update existing phase docs?”
