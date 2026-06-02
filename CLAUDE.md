# CLAUDE.md — Forked Software

Context file for Claude Code / Cowork when working in Forked Software repos.

## What this is
Forked Software builds web apps and automates business workflows for clients.
Portfolio examples: tankstl.com, fennel.forkedsoftware.com (Fennel demo).
Work spans greenfield client apps and small internal tools.

## Default stack
- Vite + React + TypeScript + Tailwind
- Deployed to GitHub Pages with custom domains (GoDaddy DNS)
- Prefer simple, low-maintenance hosting; be skeptical of unnecessary infra
  (auth, self-hosting, managed services) unless the client genuinely needs it.

## Conventions
- TypeScript strict; no `any` without a comment justifying it.
- Components small and composable; colocate styles via Tailwind utility classes.
- Keep dependencies lean — justify every new package.
- Commit messages: imperative, scoped (e.g. `feat(fennel): add results filter`).

## Deploy notes
- GitHub Pages build → confirm `base` in `vite.config` matches the repo/domain.
- Custom domain set via CNAME + GoDaddy DNS; don't break the CNAME file on deploy.
- After a deploy, verify the live custom domain, not just the Pages URL.

## How to work with me
- Output tight and punchy — no filler, no over-explaining. Show the diff/result first.
- When proposing architecture, lead with the simplest thing that works, then note
  the upgrade path only if relevant.
- For client-facing copy or docs, voice is personal, story-driven, community-oriented —
  authentic context over credentials.
- Ask before adding auth, a backend, or paid infra to a project that doesn't have one.

## Common tasks
- `npm run dev` / `npm run build` / `npm run preview`
- Scaffolding a new client app from the default stack above
- Wiring a GitHub Pages + custom-domain deploy
- Building small workflow automations (favor readable scripts over frameworks)
