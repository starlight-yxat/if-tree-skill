# If-Tree Skill

A public, versioned repository for the If-Tree Skill methodology.

## What this repository is for

This repository is used to publish, version, and preserve the If-Tree Skill methodology as a public record.

Its purpose is:

- to provide a stable public timestamp for the methodology
- to keep version history clear and inspectable
- to make future citation and authorship attribution easier
- to reduce ambiguity about prior publication

## Core idea

The If-Tree Skill treats a condition tree as the natural-language form of a program.

Its core claim is:

- document and program are strictly equivalent
- condition branches plus loops are sufficient to express complete program logic
- the system must not guess missing rules
- when user-provided facts are insufficient for implementation, the document must expose explicit ERROR nodes instead of silently filling gaps

## Current document

The current methodology document is stored in:

- `if-tree-skill-v5.md`

## Scope

This repository currently focuses on:

- requirement organization
- condition-tree document structure
- axioms and responsibility boundaries
- data validation rules
- data-flow tracking
- ERROR exposure rules
- reversibility self-check

## Versioning policy

New revisions of the methodology should be committed as explicit version updates.

Recommended version pattern:

- v0.x for early public drafts
- v1.0.0 for the first stable public release

## Citation and attribution

If this repository, its methodology, or its document structure is referenced in research, software, articles, videos, or derivative documentation, attribution should point to this repository and the relevant released version.

## Author

Author: starlight-yxat

## Status

Current status: public draft
