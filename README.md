# renovate-skills-example

A proof-of-concept (PoC) project demonstrating how [Renovate](https://github.com/renovatebot/renovate) can manage updates for the [skills CLI](https://github.com/vercel-labs/skills) — the open agent skills ecosystem tool.

## Background

This project was created as a PoC in response to the Renovate discussion:
**[Add support for skills.sh (vercel-labs/skills)](https://github.com/renovatebot/renovate/discussions/41841)**

The discussion explores how Renovate could automate updates for `skills.sh`, which behaves like a package executed as a CLI tool. As skills installations grow in popularity, keeping them up to date becomes important, and Renovate is the natural tool to handle this automatically.

## Purpose

The goal of this repository is to:

1. Demonstrate how Renovate can be configured to work with `skills.sh` packages.
2. Serve as a reference implementation for the approach described in the Renovate discussion above.
3. Showcase Renovate best practices via the included `renovate.json` configuration.

## Renovate Configuration

This repository includes a [`renovate.json`](./renovate.json) with recommended best practices:

- Extends from the `config:recommended` preset for sensible defaults.
- Enables the [Dependency Dashboard](https://docs.renovatebot.com/key-concepts/dashboard/) for a full overview of pending updates.
- Groups minor updates together to reduce noise.
- Enables automerge for patch-level updates to keep dependencies current with minimal manual effort.
- Limits concurrent PRs to avoid overwhelming the review queue.

## Related Links

- [Renovate Discussion #41841 — Add support for skills.sh](https://github.com/renovatebot/renovate/discussions/41841)
- [vercel-labs/skills — The CLI for the open agent skills ecosystem](https://github.com/vercel-labs/skills)
- [Renovate Documentation](https://docs.renovatebot.com)
