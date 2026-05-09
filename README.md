# Google Repo

A simple GitHub Pages workspace for experiments made with Google Gemini models.

Live site: <https://augmentedthinker.github.io/google/>  
Repository: <https://github.com/augmentedthinker/google>

## Purpose

This repo is intentionally small and easy to understand. It is not a complex application, framework, or production product. It is a public experiment hub where Gemini/OpenClaw agents can create and organize:

- standalone HTML artifacts
- simple visual demos
- session notes
- repo reference material
- lightweight documentation

The primary design goal is **clarity for weaker or smaller models**. If an agent is using this repository, it should be able to quickly answer:

1. What is this repo for?
2. Where do new artifacts go?
3. Where do session notes go?
4. Which files should be edited carefully?
5. How do I add something without breaking the site?

## Mental Model

Think of the site as a very small workspace with four public sections:

| Section | File | Purpose |
|---|---|---|
| Home | `index.html` | Explains the repo and links to the main areas. |
| Artifacts | `artifacts.html` | Gallery of generated HTML experiments and demos. |
| Session Notes | `session-notes.html` | Work-session summaries and continuity notes. |
| Markdowns | `markdowns.html` | Links to README, reference files, and workspace instruction files. |

There is no build system. There is no package manager. There is no backend. GitHub Pages serves the files directly.

## Current Model Focus

This repo is used for experiments around Google/Gemini models, including:

- `google/gemini-2.5-flash`
- `google/gemini-2.5-pro`
- `google/gemini-3.1-flash-lite-preview`

The model list may change over time. If a new model becomes the focus of the repo, update both this README and the homepage.

## Site Structure

```text
.
├── index.html                 # Homepage and orientation page
├── artifacts.html             # Artifact gallery / experiment list
├── session-notes.html         # Session note index
├── markdowns.html             # Documentation and markdown file index
├── style.css                  # Shared styling for the simple site
├── README.md                  # Main operating guide for humans and agents
├── repo-reference.md          # Short compact repo reference
├── repo-reference.html        # Browser-viewable artifact/reference page
├── session-note-*.html        # Individual session notes
├── *.html                     # Individual artifacts and experiments
├── assets/                    # Images and media assets
├── AGENTS.md                  # Agent workspace behavior instructions
├── SOUL.md                    # Assistant personality / tone context
├── USER.md                    # Human collaborator context
├── IDENTITY.md                # Assistant identity context
├── TOOLS.md                   # Local tool notes
└── HEARTBEAT.md               # Periodic-check instructions, if used
```

## Main Pages Explained

### `index.html` — Home

The homepage explains what this repo is and gives simple links to the three major sections:

- Artifacts
- Session Notes
- Markdowns

Keep this page simple. It should orient a new agent or human in under one minute.

### `artifacts.html` — Artifact Gallery

Artifacts are browser-viewable outputs from work sessions. They are usually standalone `.html` files.

Examples currently include:

- `glowing-orb.html`
- `physics-simulation.html`
- `procedural-flow.html`
- `pulse-animation.html`
- `repo-analytics.html`
- `morning-briefing.html`
- `clock.html`
- `particles.html`

When adding a new artifact:

1. Create the artifact as a standalone `.html` file in the repo root, unless it clearly belongs in a subfolder.
2. Use `style.css` if the artifact should match the site style.
3. Add a button link in `artifacts.html`.
4. Put the newest artifact near the top.
5. Make sure the linked file actually exists before committing.

Do **not** leave broken links in `artifacts.html`.

### `session-notes.html` — Session Notes

Session notes preserve continuity. They should help the next agent understand what happened without needing the entire previous conversation.

A useful session note includes:

- date/time
- short summary of work completed
- files changed
- decisions made
- known issues
- next steps

Session notes can be plain HTML files like `session-note-5.html`. Add new notes to the top of `session-notes.html`.

### `markdowns.html` — Documentation Index

This page gives browser links to important markdown and workspace files.

Recommended reading order for agents:

1. `README.md`
2. `repo-reference.md`
3. `AGENTS.md`
4. `TOOLS.md`
5. `SOUL.md`
6. `USER.md`
7. `IDENTITY.md`
8. `HEARTBEAT.md`

Use this page when a model needs to understand the repo's structure and operating context.

## Workspace Instruction Files

Several files are not normal website content. They are context files for agents.

### `AGENTS.md`

General operating instructions for agents working in this workspace.

Read this before making broad changes.

### `SOUL.md`

Assistant personality and tone context. Do not rewrite casually. If changed, mention it to Christopher.

### `USER.md`

Human collaborator context. Keep it respectful and minimal. Do not turn it into a private dossier.

### `IDENTITY.md`

High-level assistant identity context.

### `TOOLS.md`

Local notes about tools or repo-specific operating habits.

### `HEARTBEAT.md`

Optional periodic-check instructions. Keep it empty or very short unless there is a specific reason to add heartbeat tasks.

## Style Rules

The site uses one shared stylesheet: `style.css`.

Design goals:

- mobile-first
- simple navigation
- large readable buttons
- minimal visual noise
- clear explanations
- no complex dependencies

Avoid adding frameworks unless Christopher specifically asks. This repo should stay easy for smaller models to reason about.

## Link Hygiene

Before committing, check that every internal link points to an existing file.

Important internal pages:

- `index.html`
- `artifacts.html`
- `session-notes.html`
- `markdowns.html`

Common mistake: adding a button to an artifact file that was never created. If the file does not exist, either create it or remove the link.

## How to Add a New Artifact

1. Create a file named clearly, for example:
   - `neural-flow.html`
   - `gemini-layout-test.html`
   - `model-comparison-card.html`
2. Make it standalone HTML.
3. Add a link near the top of `artifacts.html`.
4. Use a clear label:
   - `2026-05-09 10:30 EDT — Neural Flow`
5. Check the page locally or through GitHub Pages after pushing.
6. If the artifact represents an important session, also add a session note.

## How to Add a New Session Note

1. Create a file like `session-note-5.html`.
2. Include:
   - title
   - date/time
   - summary
   - changed files
   - next steps
3. Add a button to the top of `session-notes.html`.
4. Keep the note useful, not verbose.

## How to Add or Update Markdown Documentation

1. Edit the relevant `.md` file.
2. If it is an important file, add it to `markdowns.html`.
3. Keep language direct and simple.
4. Prefer concrete instructions over abstract explanations.

## Operating Principles for Gemini Agents

If you are a Gemini/OpenClaw agent working in this repo:

- Prefer simple edits over clever architecture.
- Preserve the existing static-site structure.
- Do not add unnecessary dependencies.
- Do not create broken links.
- Do not delete artifacts unless Christopher asks.
- Update navigation pages when adding new pages.
- Write session notes when work creates useful continuity.
- Keep explanations short enough for weaker models to follow.
- If unsure, inspect files before guessing.

## First-Pass Cleanup Completed

This README was expanded to make the repo easier for Gemini agents to understand. The site navigation was clarified around four main areas:

- Home
- Artifacts
- Session Notes
- Markdowns

The old placeholder buttons on the homepage were replaced with meaningful links. The artifact page was cleaned so it only links to files that currently exist.

## Quick Checklist Before Committing

- [ ] Did you update the correct index page?
- [ ] Did you add links for any new files?
- [ ] Did you verify that links are not broken?
- [ ] Did you avoid unnecessary complexity?
- [ ] Did you write or update a session note if the change needs continuity?

## Short Summary

This repo is a simple public experiment site for Google Gemini model work. Keep it clean, obvious, mobile-friendly, and easy for future agents to understand.
