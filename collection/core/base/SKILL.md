---
name: youngmayor-base
description: Universal core standards for projects. This skill should be used on every project to enforce philosophies, structure, naming, tooling, and global anti-patterns regardless of language.
---

# Base Code Doctrine

This skill defines the non-negotiable core principles governing all code modifications and creation. These philosophies override language-specific conveniences in favor of long-term maintainability.

## The Iron Law

Code is written for **humans first, machines second**. Every architectural and syntactical decision must answer: _"Will this still make sense in 6 months?"_

## Core Principles

1. **Optimise for Readability & Maintainability:** Avoid “clever” or esoteric code. Prefer boring, predictable patterns.
2. **Clean & Lean Code:** Let the code breathe. Do not cluster unrelated lines of code together. Group related logic, separate unrelated logic with blank lines.
3. **Separation of Concerns:** Avoid monolithic (God) files. Co-locate related logic where appropriate, but prevent tight coupling.

## Naming Standards

- **Intention-Revealing:** Use highly descriptive names.
- **Verbosely Clear:** Functions should read like sentences (e.g., `calculateUserDiscount()` instead of `calcDisc()`).
- **No Abbreviations:** Unless universally understood (like `id` or `url`), do not abbreviate variables.

## Project Structure & Tooling

- **Modular Architecture:** Enforce strict layered architectures (e.g., Controllers → Services → Repositories).
- **Environment Parity:** Every project using a `.env` MUST include a `.env.example` that lists all variables with short descriptions.
- **Strict Tooling:** JS/TS projects must always utilize and enforce:
  - `npm run lint`
  - `npm run format`
  - `npm run type-check`

## UI & Styling Standards (Global)

- **Zero Hardcoded Colours:** Banned utility classes like `bg-white`, `text-gray-500`.
- **Semantic Tokens Only:** Use design-system mapped tokens (`bg-primary`, `text-foreground`, `bg-card`).
- **Centralised Themes:** A scalable product requires a scalable, centralised design system.

## Security Basics

- **Zero Trust:** Never trust client input. Always validate and sanitize at the boundary.
- **Secret Isolation:** Secrets must never be exposed to the frontend/client. Apps should _verify_ tokens, not generate them locally.
- **Fail Loud & Log:** Never silently fail or swallow errors. Always log errors and return contextually meaningful responses.

## Global Anti-Patterns [BANNED]

- **God Files:** Modules/files exceeding ~300+ lines doing multiple unrelated things.
- **Hardcoded Configurations:** Magic strings and undocumented arbitrary numbers.
- **Logic in UI:** Business logic embedded directly within UI presentation components.
- **Silent Error Handling:** `try { ... } catch (e) {}`.
- **Copy-Paste Programming:** Duplicating logic instead of abstracting.

## Quick Default Validation

Before finalizing any generation, ask yourself: _"If something feels messy here, fix it immediately."_
