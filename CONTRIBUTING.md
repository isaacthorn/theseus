<!--
SPDX-FileCopyrightText: 2026 Isaac Thorn

SPDX-License-Identifier: CC-BY-4.0
-->

# Contributing to Theseus

## Getting started

Install [pre-commit](https://pre-commit.com/) (e.g. `sudo apt install pre-commit`), then from the repository root:

```
pre-commit install --install-hooks
```

This installs both the `pre-commit` and `commit-msg` git hooks. From then on, every commit is checked automatically; you can also run everything on demand with:

```
pre-commit run --all-files
```

## Commit messages

Commit messages must follow [Conventional Commits](https://www.conventionalcommits.org/), e.g.:

```
feat: add component graph resolver
fix: correct swap ordering in scaffolding step
docs: update contributing guide
```

This is enforced by the `commit-msg` hook.

## Code style

- C++ formatting is enforced by `clang-format` (see `.clang-format`) and applied automatically as a pre-commit hook.
- `.editorconfig` sets consistent indentation, line endings, and line length for editors that support it.

## Architecture Decision Records

Significant architectural decisions are recorded as [MADR](https://adr.github.io/madr/) 4.0.0 ADRs under [`docs/decisions`](docs/decisions). See [`0000-use-madr.md`](docs/decisions/0000-use-madr.md) for why this format was chosen.

To record a new decision:

1. Copy whichever template fits the decision's weight (`adr-template.md` for the full format, or `-minimal` for lighter-weight decisions) to `docs/decisions/NNNN-short-title.md`, using the next sequential number.
2. Fill it in and open a PR alongside (or ahead of) the change it justifies.

## Licensing (REUSE)

This project follows the [REUSE Specification](https://reuse.software/spec/) for licensing and copyright. Every file needs an SPDX copyright and license identifier, either as a header comment or as an entry in `REUSE.toml` for files that can't carry one directly.

Add a header to new files, for example:

```
// SPDX-FileCopyrightText: 2026 Isaac Thorn
//
// SPDX-License-Identifier: Apache-2.0
```

Check compliance locally with:

```
reuse lint
```

This is also enforced by a pre-commit hook.
