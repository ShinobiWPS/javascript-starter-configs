# Agent Guide

Use `pnpm` for workspace commands.

## Project Rules

- Use TanStack Query for server state. It's' forbidden to use React Context aside from managing state regarding Auth, User and theme. If a case happens still need a solution for centralized store, use Tanstack Store.
- Keep TypeScript strict and do not use `any`.
- Do not leave `console.log` inside code that's gonna be committed.
- Keep cross-feature imports as close to zero as possible. Promote shared logic to root `helpers/`, `utilities/`, `interfaces/`, `hooks/`, or `facade-components/`.

## Where To Look Next

- TSX rules: ``
- TypeScript rules: ``
- Architecture reference: ``

If two instructions conflict, the more specific file should win.

## TanStack Skills

- Prefer installed TanStack Intent skills from dependencies before creating new local library guidance.

## Errore Coding Convention

This codebase uses the errore.org convention. ALWAYS read and apply its skill, before editing any code.
