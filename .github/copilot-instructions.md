# Copilot Instructions

## Build, test, and lint commands

- There are currently no `build`, `test`, or `lint` scripts in `package.json`.
- There is no single-test command because no test runner is configured in this repository.
- Use `npm install` when dependency changes need to update `package-lock.json`.

## High-level architecture

- This repository is a configuration-focused proof of concept for Renovate support around the `skills.sh` ecosystem, not an application with a `src/` tree.
- `README.md` explains the project goal: demonstrate how Renovate can manage `skills.sh` packages and serve as a reference implementation for the Renovate discussion linked there.
- `.agents` contains `skills`, which is the repository's skills-specific input. Treat it as part of the dependency surface Renovate is expected to manage.
- `package.json` and `package-lock.json` represent the npm side of the dependency story. Right now the only declared npm dependency is `express`.
- `renovate.json` is the central automation file. It currently keeps the setup intentionally small by extending only `config:recommended`.

## Key conventions

- Keep changes aligned with the repository's purpose as a minimal reference PoC; most meaningful edits belong in `README.md`, `.agents`, `package.json` / `package-lock.json`, or `renovate.json`.
- Do not assume hidden app code, CI jobs, or local tooling exist. If you introduce new automation, document it in the repository docs and update this file.
- When changing dependencies, keep the manifest and lockfile in sync.
- Preserve the README's framing around Renovate, `skills.sh`, and the linked discussion so the repository remains a clear example of that workflow.
