# Unslop 🧹

> **The Agent Skill against generic AI SaaS slop.**  
> Kill the purple gradient, delete the glossy blobs, lose the hype words, stop centering everything, and give the user one thing worth looking at.

[![Agent Skills](https://img.shields.io/badge/Agent%20Skill-SKILL.md-black?style=flat-square)](https://github.com/Syed-Haseeb97/unslop)
[![License: MIT](https://img.shields.io/badge/License-MIT-black?style=flat-square)](LICENSE)

---

## What is This?

When you prompt an AI coding agent (Claude Code, Cursor, Copilot, Codex, Antigravity) to *"build a modern landing page"*, it almost always converges on the exact same lazy statistical median:

- Cosmic dark background with giant purple & cyan `blur-3xl` blobs.
- An announcement pill capsule above the headline (`✨ v2.0 is live! Claim early access →`).
- An `h1` reading: *"Supercharge Your Workflow with Next-Gen Intelligence"* in purple/pink gradient text.
- Three shiny `rounded-full` pill buttons.
- A fake logo banner ("TRUSTED BY 10,000+ TEAMS").
- 3 cards with 48x48 rounded purple squares containing `Sparkles`, `Zap`, and `ShieldCheck` icons with lorem ipsum.
- Fake reviews from *"Sarah K., Founder at CloudScale"*.
- Everything centered, bouncing, and bobbing up and down.

**Unslop** is an open-source Agent Skill (`SKILL.md`) that re-trains your AI agents to build intentional, editorial, and mechanically honest web interfaces with real typography, authentic utility, and zero clichés.

---

## The Side-by-Side Benchmark

We built the **exact same product** (a Postgres schema migration engine) in both styles:

| Slop Cliché (Before) | Unslop Standard (After) |
| :--- | :--- |
| **Purple/Fuchsia Gradient Backgrounds** | Warm Archival Paper (`#F5F3EE`) & Crisp 1px Stone Hairlines (`#C8C2B5`) |
| **Gradient Text** (`bg-clip-text text-transparent`) | High-contrast solid charcoal ink (`#16181D`) with `Instrument Serif` italic accents |
| **Announcement Pill Capsule** above headline | Clean whitespace. Let the `h1` command the viewport |
| **Vague Hype Words** (*"Supercharge your synergy"*) | Plain English utility: *"Generate typed, zero-downtime Postgres migrations directly from your schema diffs"* |
| **Centered Everything** | Left-aligned narrative tension and asymmetric 60/40 grid layout |
| **Three Competing Shiny Buttons** | One decisive primary action button and an understated text link |
| **Fake Reviews & Vanity Logos** | Concrete benchmark metrics (p99 latency, AST parse speed) |
| **Generic Icon Square Cards** | Dense, content-first cards containing real DDL statements and rollback rules |
| **Bouncing & Floating Animations** | Static, calm, distraction-free interface on a disciplined 4-point spatial scale |
| **Decorative 3D Spheres & Blobs** | **The One Thing Worth Looking At**: An interactive live SQL schema diff inspector |

### Inspect the Demos
Open `index.html` in your browser to view the interactive split-screen comparison:
- `examples/slop.html`: The textbook 2024 AI SaaS slop page.
- `examples/unslop.html`: The editorial Unslop implementation.

---

## How to Install

### Option A: Using the `skills` CLI (Recommended)

Install directly into your project's agent configuration with one command:

```bash
npx skills add Syed-Haseeb97/unslop
```

Or install globally for all projects:

```bash
npx skills add Syed-Haseeb97/unslop -g
```

---

### Option B: Claude Code / Antigravity

Copy `SKILL.md` into your local skills directory:

```bash
mkdir -p .agents/skills/unslop
curl -fsSL https://raw.githubusercontent.com/Syed-Haseeb97/unslop/main/SKILL.md -o .agents/skills/unslop/SKILL.md
```

Or for Claude Code:

```bash
mkdir -p .claude/skills/unslop
curl -fsSL https://raw.githubusercontent.com/Syed-Haseeb97/unslop/main/SKILL.md -o .claude/skills/unslop/SKILL.md
```

---

### Option C: Cursor (`.cursorrules`)

Add the rules directly into your project's `.cursorrules` or `.cursor/rules/unslop.mdc`:

```bash
curl -fsSL https://raw.githubusercontent.com/Syed-Haseeb97/unslop/main/.cursorrules -o .cursorrules
```

---

## The Pre-Flight Agent Checklist

Whenever your agent generates code, it must verify this checklist:

- [ ] Is there any purple-to-indigo gradient anywhere in CSS or Tailwind classes? (If yes, **delete**).
- [ ] Is any text styled with `bg-clip-text text-transparent`? (If yes, **make it solid ink**).
- [ ] Are there decorative background blur balls (`blur-3xl`, `rounded-full bg-purple-500/20`)? (If yes, **delete**).
- [ ] Are there emojis in the header, logo, or navigation? (If yes, **remove**).
- [ ] Is there an announcement pill sitting above the `h1`? (If yes, **remove**).
- [ ] Are there multiple competing primary buttons in the hero? (If yes, **reduce to one main action**).
- [ ] Is the hero copy full of buzzwords like "supercharge" or "next-gen"? (If yes, **replace with plain English functionality**).
- [ ] Is every single section centered? (If yes, **rebalance with left-aligned editorial layout**).
- [ ] Are cards filled with generic icon squares and lorem ipsum? (If yes, **replace with real data, code, or UI elements**).
- [ ] Are elements bouncing, floating, or pulsing without direct user intent? (If yes, **freeze them**).
- [ ] Does the page have one genuine, high-fidelity element worth examining closely?

---

## License

MIT © [Syed Haseeb](https://github.com/Syed-Haseeb97)
