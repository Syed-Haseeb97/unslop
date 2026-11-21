---
name: unslop-web-design
description: Strict design and implementation instructions for AI agents to eliminate generic AI SaaS slop (purple gradients, glossy blobs, hype copy, pill overload, floating boxes) and build authentic, editorial, high-craft web interfaces.
license: MIT
compatibility: ">=1.0.0"
allowed-tools:
  - Read
  - Write
  - Edit
---

# Unslop Web Design: Instructions for AI Agents

> **Mission**: Build websites that feel designed by a thoughtful, opinionated human engineer and typographer—not generated from a 2023 Tailwind SaaS landing page template. Kill the clichés. Elevate the craft.

---

## 1. The Slop Quarantine (What NEVER to Do)

Every item in this list is an immediate rejection criterion:

| The Slop Pattern | Why It Fails | Mandatory Replacement |
| :--- | :--- | :--- |
| **Purple/Indigo Gradient** (`from-purple-500 to-indigo-600`) | Generic "AI vibe" shorthand that telegraphs zero creative effort. | Grounded, intentional palettes: warm archival paper, charcoal ink, deep forest green, terracotta, warm slate, or raw monochrome. |
| **Gradient Text** (`bg-clip-text text-transparent`) | Tacky, dated, impairs legibility, screams cheap template. | Crisp, solid high-contrast typography. Use italicized serif accents or subtle weight shifts for emphasis. |
| **Glossy Blobs & Blurred Orbs** (`blur-3xl`, radial glow divs) | Meaningless background filler that slows rendering and adds visual noise. | Clean negative space, subtle 1px hairline borders (`#E5E7EB` or `#C8C2B5`), or crisp architectural grid lines. |
| **Glow Effects** (`box-shadow: 0 0 40px rgba(...)`) | Fake sci-fi aesthetic masquerading as depth. | Flat elevation, 1px tactile borders, or subtle, diffuse hard-edged contact shadows (`box-shadow: 2px 2px 0px rgba(0,0,0,0.06)`). |
| **Emoji in Navigation & Headings** (🚀, ⚡, ✨, 🔥) | Infantilizes the product. Looks like a crypto pump-and-dump or student hackathon. | Clean, concise text labels. If an icon is essential, use a precise, custom stroke icon (1.5px stroke weight) with purpose. |
| **The Pill Above the Headline** ("✨ v2.0 is live! →") | Ubiquitous boilerplate capsule that pushes the actual message down. | Drop it completely. Let the `<h1>` command the top of the viewport. If news is urgent, use a discrete top bar or integrate it directly into the copy. |
| **Hype Words** ("Revolutionary", "Next-Gen", "Seamless", "Supercharge") | Empty marketing filler that erodes trust. | Plain English. State the exact mechanics, utility, and concrete output of the software. |
| **Centering Everything** (`text-center items-center mx-auto max-w-2xl`) | Lazy symmetrical stacking that feels like a presentation slide, not an interface. | Left-aligned prose, asymmetric column layouts, structured editorial grid tension, offset sidebars. |
| **Three Competing CTA Buttons** | Paralyzes the user with decision fatigue. | One single, authoritative Primary Action button. At most, one low-key text link or ghost secondary button next to it. |
| **Fake Reviews & Testimonials** (Unsplash headshots with generic quotes) | Dishonest and immediately spotted by technical users. | Remove the section entirely. Replace with real documentation, live interactive product state, architecture diagrams, or raw feature specs. |
| **Pill Corners on Everything** (`rounded-full` everywhere) | Makes an interface look like plastic bubble wrap or candy. | Purposeful, restrained geometry: `rounded-md` (6px) or `rounded-lg` (8px) for buttons and inputs; crisp 1px borders; square corners where editorial framing calls for it. |
| **Default Inter / Roboto** | The comic sans of 2024 web design through sheer over-saturation. | Distinctive typography: pair an editorial serif (`Instrument Serif`, `Newsreader`, `Fraunces`, `Playfair`) or high-character sans (`Geist`, `Cabinet Grotesk`, `Plus Jakarta Sans`, `Space Grotesk`) with a refined monospace. |
| **The "Stack Banner" / Fake Logo Cloud** ("Trusted by 10,000+ teams") | Unverifiable vanity banner taking up prime viewport real estate. | Delete it. Let the product speak for itself. |
| **Tiny All-Caps Over-Labeling** (`text-[10px] tracking-widest uppercase` everywhere) | Pretends to look technical like an arcade HUD, but just adds clutter. | Standard sentence case or title case in regular weights. Use monospace metadata only when displaying actual data (keys, timestamps, counts). |
| **Icon Box on Every Card** (32x32 rounded box with Lucide `Sparkles` or `Zap`) | Modular card monotony that conveys zero information. | Content-first cards: show real syntax code snippets, live previews, actual data tables, or direct interface controls. |
| **Bouncing & Floating Animations** (`animate-bounce`, bobbing divs) | Induces motion fatigue; signals novelty toy rather than production tool. | Zero idle motion. Use instant or snappy (100–150ms cubic-bezier) transitions strictly for direct user interactions (hover, click, focus). |

---

## 2. Core Foundations

### A. The 4-Point Spatial Discipline
Every margin, padding, height, width, and gap MUST strictly adhere to a 4-point grid:
- `4px` (`gap-1`, `p-1`) — Micro spacing, tag padding, icon-text alignment.
- `8px` (`gap-2`, `p-2`) — Compact element grouping.
- `12px` (`gap-3`, `p-3`) — Form fields, button inner padding.
- `16px` (`gap-4`, `p-4`) — Standard container padding, small card gap.
- `24px` (`gap-6`, `p-6`) — Card padding, component separations.
- `32px` (`gap-8`, `p-8`) — Major section sub-divisions.
- `48px` (`gap-12`, `py-12`) — Section breaks.
- `64px` (`py-16`) or `96px` (`py-24`) — Major page viewports.

Never invent random pixel values (`style="margin-top: 19px"`).

### B. Typography: Character & Tension
Ditch sterile, ubiquitous default sans-serif stacks. Establish real typographic hierarchy:

1. **Display & Primary Headings (`h1`, `h2`)**:
   - Use high-character, editorial fonts with structural weight:
     - `Instrument Serif` (Italic accents for emphasis, tight leading `leading-[0.95]`).
     - `Cabinet Grotesk` or `Syne` (Bold, structural modernism).
     - `Newsreader` or `Fraunces` (Literary, warm, authoritative).
2. **Body & Controls (`p`, `button`, `input`)**:
   - Highly legible, neutral workhorse:
     - `Geist` or `Plus Jakarta Sans` or clean system fallbacks.
     - Line height: `leading-relaxed` (1.6 to 1.7) for body text.
     - Color: Deep charcoal ink (`#16181D` or `#1E2024`), never washed-out medium gray on white.
3. **Data, Metrics, & Code (`code`, `pre`, `.metric`)**:
   - Monospace precision:
     - `Geist Mono`, `JetBrains Mono`, or `Space Mono`.

---

## 3. Layout: Asymmetry & Editorial Cadence

Stop placing every element in a centered `flex-col items-center text-center` column. Real design uses layout tension:

- **Left-Aligned Hierarchy**: Left-align your hero headlines, copy, and action groupings. It anchors the reader's eye naturally.
- **Split Proportions**: Instead of 50/50 split sections, use editorial 60/40 or 70/30 ratios (e.g., strong narrative on the left, interactive inspector on the right).
- **Hairline Framing**: Define structure with crisp 1px borders (`border border-neutral-200` or `#C8C2B5`), not drop shadows or blurry glow containers.

---

## 4. Copywriting: The "Say What It Does" Test

Before writing a single headline, run the **Concrete Utility Test**:

| Slop Headline (Rejected) | Concrete Reality (Approved) |
| :--- | :--- |
| "Supercharge your development workflow with AI-driven synergy." | "Generate typed Postgres migrations directly from your schema diffs." |
| "The revolutionary platform for high-velocity teams." | "Track pull request reviews, cycle times, and CI bottlenecks in one dashboard." |
| "Next-gen communication tailored for the future of work." | "End-to-end encrypted team chat with native voice transcription." |

**Rules for Copy**:
- Cut adjectives like "powerful", "magical", "effortless", "seamless", "blazing-fast".
- If a sentence can describe 50 other startups, delete it.
- State: (1) What it accepts as input, (2) What operation it performs, (3) What it outputs.

---

## 5. "The One Thing Worth Looking At" (The Hero Anchor)

Every page must have **one dominant, high-craft focal point** that rewards the user's attention. Instead of decorative fluff (floating logos, blobs, 3D spheres), provide a tangible artifact:

1. **A Live Interactive Sandbox**: A functional code playground, a real interactive query runner, or an active audio waveform generator.
2. **A High-Fidelity UI Blueprint**: A realistic, detailed interface inspection view (e.g., an authentic canvas, a complete data table with dense metrics, or a state graph).
3. **An Architectural Flow**: A clean, precision-rendered SVG pipeline diagram showing actual data movement and protocols.
4. **An Interactive Calculator/Simulator**: Inputs and live recalculated charts that directly demonstrate the product's math or savings.

---

## 6. Pre-Flight Agent Checklist (Run Before Submitting Code)

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
