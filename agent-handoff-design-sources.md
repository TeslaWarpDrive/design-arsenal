# Design tools and sources and inspiration for you to focus on: [PROJECT]

## Brief (from Bradley)

> Here's a list of design tools and sources and inspiration for you to focus on for **[PROJECT]**.

Bradley saved these from X. Treat them as the **default source material** for this project:

1. **Use them, don't just cite them.** When you pick a component library, animation kit, shader/background, font or color approach, choose from this list first. Look elsewhere only when nothing here fits, and say why.
2. **Directly usable** items (`web_ready: true`) come with an install/usage hint. Use it as given, and check the license line before you ship.
3. **Reference-only** items are galleries. Browse them for layout, footer, CTA, motion and icon ideas, then build your own version. Don't copy assets.
4. **Start with the top picks (★).** For a web page, a strong default stack is: design-taste + ai-design-skills (direction and process) → better-design tokens or ui-layouts blocks (structure) → paper-shaders or canvas-ui (one hero effect) → motion-primitives / trickle-ui-kit (motion and text reveals) → land-book, footer.design, cta.gallery, 60fps, motionin.design (inspiration).
5. **Bradley's taste:** anything a person will look at should be striking and polished, never bland. Read `bradley-design-taste.md` in this folder first.
6. **No purchases.** Several sources have paid tiers (motionin.design, Backgrounds Supply, Grainient Pro, Wonderlist, Hyperiux Pro). Use only free or open-source parts unless Bradley approves a purchase.
7. Honor `prefers-reduced-motion` and keep text contrast at WCAG AA or better over shaders and gradients.

Machine-readable copy: `agent-handoff-design-sources.json` (same data). Source: 34 bookmarks scanned, 27 resources kept.

## Sources

### Agent design skills

#### AI Design Skills (elayadesign) ★ top pick
- name: AI Design Skills (elayadesign)
- url: https://github.com/elayadesign/ai-design-skills
- category: Agent design skills
- what it is: Collection of design skills for AI coding tools (Claude Code, Cursor, Codex, Windsurf). Currently one skill, landing-page-design: intake questions, page structure, conversion copy, and a full visual system (type, spacing, radius, motion). The poster says he designed his landing pages with it plus Higgsfield, Claude and Cursor.
- when to use it: Have the agent load this skill before laying out a landing page or a one-page site.
- directly usable for a web page: yes (Agent skill (process/rules), not a runtime dependency)
- install / usage: git clone https://github.com/elayadesign/ai-design-skills.git /tmp/ai-design-skills && cp -r /tmp/ai-design-skills/skills/landing-page-design .claude/skills/  (Cursor: copy into .cursor/rules/)
- license: MIT
- stack: Markdown skill files (agent-agnostic)
- source post: https://x.com/elayadesigns/status/2114049200749175174
- note: StreetPi already used it on 2026-10-25 to make 4 layout concepts. Bradley picked 'Control center' as the app's real Home.

#### Superdesign
- name: Superdesign
- url: https://github.com/superdesigndev/superdesign
- category: Agent design skills
- what it is: 'AI Product Design Agent - Open Source' — IDE extension that generates HTML mockups/variants from prompts. Its README points to an install guide at superdesign.dev/ide-extension.
- when to use it: Quick throwaway mockup exploration only.
- directly usable for a web page: no (Mockup generator, not a page dependency)
- install / usage: Install from the Cursor/VS Code Marketplace per https://www.superdesign.dev/ide-extension
- license: AGPL-3.0 plus some files under a commercial 'Enterprise' license (Super Design License)
- stack: TypeScript, VS Code/Cursor extension
- source post: https://x.com/RoundtableSpace/status/2110255627704455591
- note: Earlier StreetPi research (2026-10-18) found the original repo marked no longer maintained, with the product moved to superdesign.dev. Avoid copying its code into a page because of the AGPL license.

#### Better Design ★ top pick
- name: Better Design
- url: https://github.com/marvkr/better-design
- category: Agent design skills
- what it is: Open-source design MCP server + shadcn/ui registry: 31 brand-grade themes (Linear, Stripe, Vercel, Notion, Apple, Supabase, Figma…), design tokens, UI principles and WCAG rules.
- when to use it: Pick a ready token set/theme for a shadcn/Tailwind page, or run its UI/WCAG review rules on a finished page.
- directly usable for a web page: yes (shadcn registry components + theme tokens + MCP server)
- install / usage: npx shadcn@latest add https://www.better-design.com/registry/<design-system>/<component>.json  (e.g. .../registry/linear/button.json). Browse at https://better-design.com/design-systems
- license: MIT
- stack: TypeScript, shadcn/ui, Tailwind, MCP
- source post: https://x.com/RoundtableSpace/status/2110255627704455591
- note: StreetPi's colors-v2 work borrowed its 'Midnight Glass' / 'Glassmorphic Dark' token layering.

#### Design Taste ★ top pick
- name: Design Taste
- url: https://github.com/madebymustafa/design-taste
- category: Agent design skills
- what it is: 24 open-source agent skills that turn taste into instructions — ten genre identities (e.g. editorial, quiet-luxury, dark-tech), each proven by a same-brief before/after demo; craft skills for details and code skills for delivery.
- when to use it: Before designing: pick a deliberate genre/direction, ban generic 'AI look' defaults, and run its pre-flight checklist.
- directly usable for a web page: yes (Agent skills (process/rules))
- install / usage: git clone https://github.com/madebymustafa/design-taste.git && ./scripts/install.sh
- license: MIT
- stack: JavaScript/CSS demos; skills are markdown
- source post: https://x.com/RoundtableSpace/status/2110255627704455591
- note: StreetPi used its taste-color skill (60-30-10, OKLCH ramps, WCAG math) as the color review checklist.

### UI kits, components & effects

#### Canvas UI ★ top pick
- name: Canvas UI
- url: https://github.com/DavidHDev/canvas-ui
- category: UI kits, components & effects
- what it is: A library of creative canvas components: real HTML with WebGL effects running over it (35 components). React, Vue, Svelte, vanilla; WebGL2 default build plus WebGPU build.
- when to use it: One hero-level ambient/WebGL effect (liquid, shader, 3D) layered over real HTML.
- directly usable for a web page: yes (shadcn-compatible registry (source copied into your repo); MCP-ready)
- install / usage: npx shadcn@latest init && npx shadcn@latest add @canvas-ui/liquid-react  (docs: https://canvasui.dev/docs/installation)
- license: MIT + Commons Clause (free in your own projects, commercial or not; you can't sell the library itself)
- stack: TypeScript; React/Vue/Svelte/vanilla; three.js for object effects
- source post: https://x.com/RoundtableSpace/status/2110255627704455591
- note: Heavy GPU work. Give it a reduced-motion fallback.

#### Paper Shaders ★ top pick
- name: Paper Shaders
- url: https://github.com/paper-design/shaders
- category: UI kits, components & effects
- what it is: Zero-dependency canvas shaders (e.g. MeshGradient, DotOrbit) installable from npm or designed in Paper; playground at shaders.paper.design.
- when to use it: Animated mesh-gradient / grain backgrounds and hero auras.
- directly usable for a web page: yes (npm package (React or vanilla))
- install / usage: npm i @paper-design/shaders-react  (vanilla: npm i @paper-design/shaders); import {MeshGradient} from '@paper-design/shaders-react'
- license: Apache-2.0
- stack: TypeScript, WebGL; React wrapper + vanilla package
- source post: https://x.com/RoundtableSpace/status/2110255627704455591
- note: StreetPi's loved Aurora palette uses this mesh-gradient recipe for its aura.

#### UI Layouts ★ top pick
- name: UI Layouts
- url: https://github.com/ui-layouts/uilayouts
- category: UI kits, components & effects
- what it is: 'Not just a library': components, effects, design tools and ready-to-use blocks (hero, feature, bento sections…) for modern interfaces.
- when to use it: Pull a ready hero/feature/bento block instead of building one from scratch.
- directly usable for a web page: yes (Copy-in React components/blocks)
- install / usage: npm install motion clsx tailwind-merge (Tailwind required), then copy components from https://www.ui-layouts.com
- license: MIT
- stack: TypeScript, React/Next, Tailwind, motion
- source post: https://x.com/RoundtableSpace/status/2110255627704455591
- note: The post's link (github.com/ui-layouts/ui-layouts) now redirects to ui-layouts/uilayouts.

#### Hyperiux Components (Hyperiux Vault)
- name: Hyperiux Components (Hyperiux Vault)
- url: https://github.com/Hyperiux-Immersion-Labs/hyperiux-components
- category: UI kits, components & effects
- what it is: Animation effects and interactive UI components for Next.js, installed by CLI (examples: phantom-image-trail, milky-way, spider-particles, immersive-full-screen-nav, rectangular-text-reveal). Free tier plus paid Pro effects.
- when to use it: Immersive, marketing-style scroll and hover effects.
- directly usable for a web page: yes (CLI that installs source into your project)
- install / usage: npx hyperiux init && npx hyperiux add <effect>  (Pro effects need npx hyperiux login)
- license: Repo MIT; GitHub description says the free effects are MPL 2.0; Pro effects are paid
- stack: TypeScript, Next.js
- source post: https://x.com/RoundtableSpace/status/2110255627704455591
- note: The post's link (github.com/Hyperiux-Immersive/Hyperiux) returns 404. This is the live repo found by search; it's very likely the same project.

#### Motion Primitives ★ top pick
- name: Motion Primitives
- url: https://github.com/ibelick/motion-primitives
- category: UI kits, components & effects
- what it is: UI kit to make beautiful, animated interfaces faster: customizable, open-source motion components built with motion and Tailwind CSS (in beta).
- when to use it: Polished micro-interactions: text effects, reveals, carousels, hover states.
- directly usable for a web page: yes (Copy-in React components)
- install / usage: See https://motion-primitives.com/docs (components are copied in; needs motion + Tailwind)
- license: MIT
- stack: TypeScript, React, motion (Framer Motion), Tailwind
- source post: https://x.com/RoundtableSpace/status/2110255627704455591

#### Cursify
- name: Cursify
- url: https://github.com/ui-layouts/cursify
- category: UI kits, components & effects
- what it is: Cursor animation library for React & Next.js.
- when to use it: A custom desktop cursor effect only. It does nothing on touch screens.
- directly usable for a web page: yes (Copy-in React components)
- install / usage: npm install motion clsx tailwind-merge, then copy from https://cursify.ui-layouts.com
- license: None stated (no license file)
- stack: TypeScript, React/Next, Tailwind, motion
- source post: https://x.com/RoundtableSpace/status/2110255627704455591
- note: With no license, treat it as reference only.

#### Trickle UI Kit ★ top pick
- name: Trickle UI Kit
- url: https://github.com/akaieuan/trickle-UI-kit
- category: UI kits, components & effects
- what it is: 47 pure-CSS text-animation primitives for React: zero runtime, SSR-safe, copy-paste install via the shadcn registry.
- when to use it: Headline and text reveals without adding a JS animation runtime.
- directly usable for a web page: yes (shadcn registry (CSS keyframes portable to vanilla))
- install / usage: npx shadcn@latest init, then add components per https://tricklekit.dev/#install
- license: MIT
- stack: TypeScript, React, Tailwind v4, shadcn
- source post: https://x.com/RoundtableSpace/status/2110255627704455591
- note: The post's link (github.com/akaieuan/trickle) returns 404. The live repo is akaieuan/trickle-UI-kit.

### Inspiration galleries

#### Inspora
- name: Inspora
- url: https://inspora.design
- category: Inspiration galleries
- what it is: A curated archive of recent visual design and creative work. (Post label: 'Creative design inspiration'.)
- when to use it: Mood and art-direction references.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://x.com/neropursue/status/2113878128061792423

#### Land-book ★ top pick
- name: Land-book
- url: https://land-book.com
- category: Inspiration galleries
- what it is: Hand-picked website design inspiration gallery, updated daily. (Post label: 'Landing page inspiration'.)
- when to use it: Landing-page layout references.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://x.com/neropursue/status/2113878128061792423

#### Landdding
- name: Landdding
- url: https://landdding.com
- category: Inspiration galleries
- what it is: Daily new web designs submitted and upvoted by a community of web designers. (Post label: 'Landing page examples'.)
- when to use it: More landing-page examples.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://x.com/neropursue/status/2113878128061792423

#### Footer ★ top pick
- name: Footer
- url: https://footer.design
- category: Inspiration galleries
- what it is: 'The only footer gallery on earth': curated website footer inspiration, sortable by type and style.
- when to use it: Designing the page footer.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://x.com/neropursue/status/2113878128061792423

#### CTA Gallery ★ top pick
- name: CTA Gallery
- url: https://cta.gallery
- category: Inspiration galleries
- what it is: Curated gallery of call-to-action designs, filterable by type (button, form, modal, newsletter, pricing…), industry and mode.
- when to use it: Designing buttons, sign-up and pricing CTAs.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://x.com/neropursue/status/2113878128061792423

#### 60fps.design ★ top pick
- name: 60fps.design
- url: https://60fps.design
- category: Inspiration galleries
- what it is: 'Endless collection of delightful details from best-in-class apps': 2,000+ app motion/interaction shots, filterable by gesture, pattern, effect and element; also has an MCP. (Post label: 'UI animation references'.)
- when to use it: Motion and micro-interaction references.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only (no reuse license)
- stack: Website
- source post: https://x.com/neropursue/status/2113878128061792423
- note: StreetPi used it as its motion reference.

#### Iconly
- name: Iconly
- url: https://iconly.design
- category: Inspiration galleries
- what it is: Browse app, game and web icons from real apps (Netflix, Flighty, Craft, ChatGPT…). (Post label: 'App icon inspiration'.)
- when to use it: App-icon and favicon references.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://x.com/neropursue/status/2113878128061792423

### Templates & premium sections

#### Motion (motionin.design) ★ top pick
- name: Motion (motionin.design)
- url: https://motionin.design
- category: Templates & premium sections
- what it is: 'Premium interactive web sections': physics-based, cursor-responsive sections (galleries, heroes, sliders, liquid-glass, WebGL). Each ships as a detailed prompt + spec file you paste into an AI coding tool. Some sections are free; the rest need $9/mo or a $99 lifetime plan. (Post label: 'Interactive web sections'.)
- when to use it: Hero/gallery interaction ideas. The free sections' specs can be fed straight to an agent.
- directly usable for a web page: yes (Agent-ready prompt/spec (free ones only, unless purchased))
- install / usage: Open a section marked Free on motionin.design and copy its prompt + spec into the agent
- license: Paid plans cover commercial/client work; free sections are marked Free
- stack: Prompt + spec files (GSAP / rAF / WebGL)
- source post: https://x.com/neropursue/status/2113878128061792423
- note: Don't buy anything without Bradley's approval.

#### Wonderlist
- name: Wonderlist
- url: https://wonderlist.design
- category: Templates & premium sections
- what it is: 127 premium website templates designed in Figma (SaaS, agency, portfolio, consulting…). (Post label: 'Premium Figma designs'.)
- when to use it: Figma layout references.
- directly usable for a web page: no (Reference / paid Figma files)
- install / usage: n/a
- license: Premium (paid)
- stack: Figma
- source post: https://x.com/neropursue/status/2113878128061792423

#### v0 Templates
- name: v0 Templates
- url: https://v0.app/templates
- category: Templates & premium sections
- what it is: v0 by Vercel community templates: apps, components and starters (landing pages, dashboards, portfolios, shader landing page, infinite scrolling images…) you can duplicate. (Post label: 'Ready-made app templates'.)
- when to use it: Fork a starter or component as a base.
- directly usable for a web page: yes (Duplicate a template in v0 / copy its code)
- install / usage: Open a template on v0.app/templates and use Duplicate
- license: Per template
- stack: React/Next.js, Tailwind, shadcn (v0)
- source post: https://x.com/neropursue/status/2113878128061792423

### Fonts, colors & backgrounds

#### Font In Logo
- name: Font In Logo
- url: https://fontinlogo.com
- category: Fonts, colors & backgrounds
- what it is: Find the fonts used by famous brand, movie, TV and game logos (verified, closest-match, or based-on), many pointing to free fonts (e.g. Netflix → Bebas Neue, Star Wars → Orbitron).
- when to use it: Picking a display face with a specific brand feel.
- directly usable for a web page: yes (Font identification. Load the named free font (e.g. Google Fonts))
- install / usage: Look up the brand, then load the named free font
- license: Varies per font (many listed as free fonts)
- stack: Website
- source post: https://x.com/neropursue/status/2113878128061792423

#### Backgrounds Supply
- name: Backgrounds Supply
- url: https://backgrounds.supply
- category: Fonts, colors & backgrounds
- what it is: 1,000+ handcrafted and AI-generated backgrounds in ~29 collections (gradients, ASCII, animated…); one-time $49; commercial use allowed, no resale. Has freebies and a 'Gradient Lab'. (Post label: 'Unique backgrounds'.)
- when to use it: Hero/section background images.
- directly usable for a web page: yes (Image assets (freebies only unless purchased))
- install / usage: Use free downloads from the Freebies page
- license: Paid commercial license; freebies available
- stack: Image/video files
- source post: https://x.com/neropursue/status/2113878128061792423
- note: Don't buy anything without Bradley's approval.

#### Grainient ★ top pick
- name: Grainient
- url: https://grainient.supply
- category: Fonts, colors & backgrounds
- what it is: Grainy and smooth gradients, animated gradients, AI backgrounds and a real-time shader gradient tool; Pro is paid, with a free tier (Freebies). (Post label: 'Gradients & animated backgrounds'.)
- when to use it: Grain texture and gradient backgrounds.
- directly usable for a web page: yes (Image assets / shader tool)
- install / usage: Use https://grainient.supply/freebies
- license: Freebies allowed for personal and commercial projects (no redistribution); Pro is paid
- stack: Image/video assets + web shader tool
- source post: https://x.com/neropursue/status/2113878128061792423
- note: StreetPi's Aurora palette uses a Grainient-style grain overlay.

### Creative & AI tools

#### Reelfolio
- name: Reelfolio
- url: https://reelfolio.io
- category: Creative & AI tools
- what it is: Turns screenshots, mockups and clips into professional video portfolio showreels, with no editing skills needed. (Post label: 'Animated project showreels'.)
- when to use it: Making a showreel video of a finished page or app.
- directly usable for a web page: no (External tool)
- install / usage: n/a
- license: Not checked
- stack: Web app
- source post: https://x.com/neropursue/status/2113878128061792423

#### VoiceStudio
- name: VoiceStudio
- url: https://github.com/debpalash/VoiceStudio
- category: Creative & AI tools
- what it is: Open-source, fully local ElevenLabs alternative: voice cloning, voice design, video dubbing, dictation, transcription and audiobook creation in 646 languages, with 14 TTS engines.
- when to use it: Local voice-over, dubbing or TTS. Not a page dependency.
- directly usable for a web page: no (Local desktop tool)
- install / usage: curl -fsSL https://voicestudio.sh/install | sh
- license: AGPL-3.0
- stack: Python; desktop app (CUDA/MLX)
- source post: https://x.com/liambraus/status/2103825720807993573
- note: The bookmarked post (Spanish) didn't link the repo. The author's own first reply did: https://x.com/liambraus/status/2103825725438505434

### Community

#### on.design
- name: on.design
- url: https://on.design
- category: Community
- what it is: Designer community. The landing page only shows 'Design, together — again' and a sign-in. (Post label: 'Designer community'.)
- when to use it: Not for page building.
- directly usable for a web page: no (n/a)
- install / usage: n/a
- license: n/a
- stack: Website (sign-in)
- source post: https://x.com/neropursue/status/2113878128061792423
- note: It's behind a sign-in, so I couldn't see more.
