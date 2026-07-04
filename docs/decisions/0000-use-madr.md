<!--
SPDX-FileCopyrightText: 2026 Isaac Thorn

SPDX-License-Identifier: CC-BY-4.0
-->

# Use Markdown Architectural Decision Records

## Context and Problem Statement

I want to track architectural decisions made in the course of this project. What format, structure and/or templates should these records use?

## Considered Options

- [MADR](https://adr.github.io/madr/) 4.0.0
- [Michael Nygard's template](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions)
- [Sustainable Architectural Decisions](https://www.infoq.com/articles/sustainable-architectural-design-decisions)
- Formless - No conventions for file format and structure

## Decision Outcome

Chosen option: "MADR 4.0.0", because

- Implicit assumptions should be made explicit. Design documentation is important to enable people understanding the decisions later on.
- MADR allows for structured capturing of any decision.
- The MADR format is lean and fits my development style.
- The MADR structure is comprehensible and facilitates usage & maintenance.
