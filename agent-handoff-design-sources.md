# Design tools and sources and inspiration for you to focus on: [PROJECT]

## Brief (from Bradley)

> Here's a list of design tools and sources and inspiration for you to focus on for **[PROJECT]**.

Bradley saved these from X. Treat them as the **default source material** for this project:

1. **Use them, don't just cite them.** When you pick a component library, animation kit, shader/background, font or color approach, choose from this list first. Look elsewhere only when nothing here fits, and say why.
2. **Directly usable** items (`web_ready: true`) come with an install/usage hint. Use it as given, and check the license line before you ship.
3. **Reference-only** items are galleries. Browse them for layout, footer, CTA, motion and icon ideas, then build your own version. Don't copy assets.
4. **Start with the top picks (★).** For a web page, a strong default stack is: design-taste + ai-design-skills (direction and process) → better-design tokens or ui-layouts blocks (structure) → paper-shaders or canvas-ui (one hero effect) → motion-primitives / trickle-ui-kit (motion and text reveals) → land-book, footer.design, cta.gallery, 60fps, motionin.design (inspiration). Hallmark and the official GSAP skills, added 9 Nov 2026, are the new top picks when a page needs a harder taste check or scroll-driven motion.
5. **Bradley's taste:** anything a person will look at should be striking and polished, never bland. Read `bradley-design-taste.md` in this folder first.
6. **No purchases.** Several sources have paid tiers (motionin.design, Backgrounds Supply, Grainient Pro, Wonderlist, Hyperiux Pro). Use only free or open-source parts unless Bradley approves a purchase. Shaders Pro, React Bits Pro, and Haikei Pro (marked coming soon) are paid. Leave those tiers alone.
7. Honor `prefers-reduced-motion` and keep text contrast at WCAG AA or better over shaders and gradients.

Machine-readable copy: `agent-handoff-design-sources.json` (same data). Source: bookmarks from 25 Oct 2026, plus more added 9 Nov 2026. 56 resources are in this file.

8. **Left out on purpose.** Coolors, Inter, and the broad directories (SiteInspire, One Page Love, Saaspo, WebInspoo, Landingfolio, Httpster). Scrolltide and the main Refero library, because most of each is paid. SaaS Interface ($39 once), SaaSFrame, and Page Flows. Shader Gradient, because the homepage sells a Framer plugin and the repo had no root LICENSE file. Anthropic's frontend-design skill and Emil Kowalski's skills, because Design Taste, Motion Primitives, and the new GSAP skills already cover that job.

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

#### Hallmark ★ top pick
- name: Hallmark
- url: https://github.com/Nutlope/hallmark
- category: Agent design skills
- what it is: Design skill that deals a theme from a catalog, then lints the built page in a browser for machine-made tells: eyebrow labels, a single colored word in a headline, an empty hero, a sign-up on every page.
- when to use it: Before a new page, when the risk is a generic generated layout.
- directly usable for a web page: yes (Agent skill (process/rules))
- install / usage: npx skills add nutlope/hallmark
- license: MIT
- stack: Markdown skill; Node 18+; optional Puppeteer for the browser lint
- source post: https://x.com/Y0urDumble/status/2119793194435027220
- note: Browser screenshots also need Chrome and puppeteer-core. Static checks still run without them.

#### GSAP skills ★ top pick
- name: GSAP skills
- url: https://github.com/greensock/gsap-skills
- category: Agent design skills
- what it is: Official agent skills for GSAP: core tweens, easing, timelines, ScrollTrigger, and React, Vue, and Svelte usage.
- when to use it: Any scroll-linked or timeline animation, before the agent invents a GSAP API.
- directly usable for a web page: yes (Agent skill (process/rules))
- install / usage: npx skills add https://github.com/greensock/gsap-skills
- license: MIT
- stack: Agent Skills; GSAP
- source post: https://x.com/Y0urDumble/status/2119793194435027220
- note: This is the skill, not the GSAP runtime. Install GSAP itself when the page needs it.

#### Impeccable
- name: Impeccable
- url: https://github.com/pbakaus/impeccable
- category: Agent design skills
- what it is: Installable design-quality skill. It sets a project direction, then checks the page against that direction.
- when to use it: When a page needs a written quality bar the agent reloads on later edits.
- directly usable for a web page: yes (Agent skill (process/rules))
- install / usage: npx impeccable install
- license: Apache-2.0
- stack: Markdown skill
- source post: https://x.com/Y0urDumble/status/2119793194435027220
- note: Reload the editor after install, then run the init command the installer prints.

#### Taste Skill (Leonxlnx)
- name: Taste Skill (Leonxlnx)
- url: https://github.com/Leonxlnx/taste-skill
- category: Agent design skills
- what it is: A separate taste skill from Design Taste. The frontend skill is design-taste-frontend. Leonxlnx asked for credit under Elaya's design-skills post.
- when to use it: When you want a second taste pass that is not the madebymustafa Design Taste repo.
- directly usable for a web page: yes (Agent skill (process/rules))
- install / usage: npx skills add https://github.com/Leonxlnx/taste-skill --skill design-taste-frontend
- license: MIT
- stack: Markdown skill
- source post: https://x.com/LexnLin/status/2114150089211904417
- note: Do not confuse this repo with github.com/madebymustafa/design-taste, which is already in the catalog.

#### GradientDeck
- name: GradientDeck
- url: https://github.com/VenoM9078/gradientdeck-skill
- category: Agent design skills
- what it is: Skill that writes a page plan first: what the visitor came to do, type, color, photos, and one memorable touch, saved under .gradientdeck before code.
- when to use it: Before the agent starts a page from a blank brief.
- directly usable for a web page: yes (Agent skill (process/rules))
- install / usage: npx gradientdeck install
- license: MIT. The README says free and MIT licensed.
- stack: Markdown skill
- source post: https://news.ycombinator.com/item?id=50251342
- note: Show HN, 26 Oct 2026.

#### Flawless UI/UX
- name: Flawless UI/UX
- url: https://github.com/smokeeaasd/flawless-ui-ux
- category: Agent design skills
- what it is: Design skill plus a local CLI that inspects a running URL for contrast, names, text size, overflow, broken images, and runtime errors.
- when to use it: After a page runs, as a check rather than as a component library.
- directly usable for a web page: yes (Agent skill plus a local inspect CLI)
- install / usage: npx flawless-ui-ux@latest install
- license: MIT
- stack: Markdown skill; local inspect CLI
- source post: https://news.ycombinator.com/item?id=50381846
- note: Show HN, 5 Nov 2026.

#### oil-motion
- name: oil-motion
- url: https://github.com/oil-oil/oil-motion
- category: Agent design skills
- what it is: Skill for motion that follows scroll, pointer, drag, and device tilt. It prepares generated video, green-screen clips, and sprites into a controllable timeline. It is not a CSS transition kit.
- when to use it: A product, character, or scene that should move with scroll or the pointer.
- directly usable for a web page: yes (Agent skill (process/rules))
- install / usage: npx skills add oil-oil/oil-motion
- license: MIT
- stack: Agent skill; video and sprite assets
- source post: https://x.com/Y0urDumble/status/2119793194435027220
- note: Ordinary button and layout motion should stay in CSS, Motion Primitives, or GSAP. This skill says so.

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
- note: The post's link (github.com/Hyperiux-Immersive/Hyperiux) returns 404. This is the live repo, and it looks like the same project.

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

#### AnimateIcons
- name: AnimateIcons
- url: https://animateicons.in
- category: UI kits, components & effects
- what it is: Animated icon set for React, Vue, Angular, and plain JS. The live page says 1,500 free open-source icons and shows a shadcn registry. The post that named it said 170.
- when to use it: Icons that should move on hover, instead of a static set.
- directly usable for a web page: yes (npm package and a shadcn registry)
- install / usage: npm install @animateicons/react
- license: The site says free and open source. A LICENSE file was not opened.
- stack: React, Vue, Angular, or plain JS; shadcn registry
- source post: https://x.com/csaba_kissi/status/2119791399176732731
- note: A shadcn add is also on the homepage: npx shadcn@latest add @animateicons/lu-x

#### PlopUI
- name: PlopUI
- url: https://plopui.com
- category: UI kits, components & effects
- what it is: Hand-drawn React kit: wobbly lines, crooked stickers, native elements, and WCAG AA. Each wobble is seeded so server and client match.
- when to use it: A page that should not look like a default component grid.
- directly usable for a web page: yes (shadcn registry or an npm package)
- install / usage: npx shadcn add @plopui/button
- license: MIT. The bundled Sketchpop font is SIL OFL 1.1.
- stack: TypeScript, React, shadcn registry
- source post: https://www.reddit.com/r/SideProject/comments/1xp8tli/i_built_a_handdrawn_react_ui_kit_as_a_side/
- note: Posted on r/SideProject on 6 Nov 2026. npm i @plop-ui/react is the package form.

#### Volt UI
- name: Volt UI
- url: https://github.com/Mahmoud-ctrl/volt-ui
- category: UI kits, components & effects
- what it is: React animation package: text motion, cursors, buttons, cards, loaders, and backgrounds. The README says there is no pro tier.
- when to use it: A specific motion component with one npm import.
- directly usable for a web page: yes (npm package)
- install / usage: npm install @volt-ui/react
- license: MIT
- stack: React, Motion, GSAP, Three.js
- source post: https://www.reddit.com/r/react/comments/1r6p0ap/100_react_animation_components_all_free/
- note: Docs are at https://volt-ui-two.vercel.app/components

#### GodUI
- name: GodUI
- url: https://godui.design
- category: UI kits, components & effects
- what it is: Animated shadcn components, plus a lab of more experimental pieces. Motion stays on transform, opacity, and filter. An MCP server can install them.
- when to use it: You already use shadcn and want motion copied in as source.
- directly usable for a web page: yes (shadcn registry and an MCP server)
- install / usage: npx shadcn@latest add "https://godui.design/r/dialog.json"
- license: MIT
- stack: TypeScript, React, shadcn, MCP
- source post: https://www.reddit.com/r/react/comments/1urrhru/i_built_an_opensource_collection_of_animated/

#### React Bits
- name: React Bits
- url: https://reactbits.dev
- category: UI kits, components & effects
- what it is: Free animated React components: text, cursors, reveals, and shader backgrounds, each as JavaScript or TypeScript and CSS or Tailwind. Same author as Canvas UI.
- when to use it: One free animated component from the public registry.
- directly usable for a web page: yes (shadcn registry)
- install / usage: npx shadcn@latest add @react-bits/SplitText-TS-TW
- license: MIT plus Commons Clause. Free to use in a project. You cannot sell the library itself.
- stack: React, shadcn registry
- source post: https://www.reddit.com/r/BestGitHubRepos/comments/1xkwb4i/react_bits_animated_react_components_for_websites/
- note: React Bits Pro is paid. Some pieces are adapted from Paper Shaders. Use the free registry.

#### Shaders
- name: Shaders
- url: https://github.com/shader-effects-inc/shaders
- category: UI kits, components & effects
- what it is: WebGPU shader components for React, Vue, Svelte, Solid, and plain JS. Gradients, noise, glass, light, and cursor trails. This is Shader Effects Inc, not Paper Shaders.
- when to use it: A shader component with a shared prop API, or an agent skill that knows this library.
- directly usable for a web page: yes (npm package and an agent skill)
- install / usage: npx shaders skill
- license: MIT for the engine, the repo components, and the npm package. Pro presets are a paid subscription.
- stack: TypeScript, WebGPU, npm package shaders
- source post: https://www.reddit.com/r/reactjs/comments/1wzbnmw/shaders_is_now_open_source_with_200_webgpu/
- note: Do not buy Shaders Pro without approval. Give WebGPU effects a static fallback.

#### Fancy Components
- name: Fancy Components
- url: https://www.fancycomponents.dev
- category: UI kits, components & effects
- what it is: Copy-in React text motion: letter swap, scramble, typewriter, text on a path, and reveals. Built with Tailwind and Motion, shipped as a shadcn registry.
- when to use it: A headline treatment that should be source in the repo, not a runtime you cannot read.
- directly usable for a web page: yes (shadcn registry)
- install / usage: npx shadcn add @fancy/component-name
- license: MIT
- stack: React, Tailwind, Motion, shadcn registry
- source post: https://www.reddit.com/r/shadcn/comments/1ormdg2/top_free_shadcn_ui_block_and_component_libraries/
- note: Add the @fancy registry URL to components.json first. Docs: https://www.fancycomponents.dev/docs/installation

#### Liquid Glass
- name: Liquid Glass
- url: https://glass.samasante.com
- category: UI kits, components & effects
- what it is: Real refraction for the web, with no dependencies. The homepage says it works in Safari, Firefox, and Chrome.
- when to use it: One glass surface, not a whole glass theme.
- directly usable for a web page: yes (npm package)
- install / usage: pnpm add @samasante/liquid-glass
- license: MIT
- stack: Zero-dependency package @samasante/liquid-glass
- source post: https://x.com/askwhykartik/status/2110346921042657426
- note: The homepage showed v0.1.0.

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

#### Sections
- name: Sections
- url: https://sections.wtf
- category: Inspiration galleries
- what it is: One section at a time from real products: menu, hero, features, pricing, CTA, testimonial, FAQ, footer, 404, and more.
- when to use it: You are stuck on one region of a page and Footer or CTA Gallery is the wrong slice.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://www.indiehackers.com/post/the-best-design-directories-to-show-off-your-work-e7b0c99522
- note: Named by Arian Adeli on Indie Hackers, 22 Dec 2025. The email list is optional.

#### 404s
- name: 404s
- url: https://www.404s.design
- category: Inspiration galleries
- what it is: 404 pages only. Filters cover style and industry. Each card links to that site's real 404.
- when to use it: Designing an error page.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://fountn.design/resource/404s-gallery-of-error-404-page-designs/
- note: Free to browse.

#### Navbar Gallery
- name: Navbar Gallery
- url: https://navbar.gallery
- category: Inspiration galleries
- what it is: Navigation bars from real sites: dropdown, mega menu, sidebar, search, announcement, and fullscreen. Built by the person behind Footer. The public grid numbers past 550.
- when to use it: Designing the top navigation. The Iconly photo post of nav ideas has no links. This does.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://x.com/himanshubuildss/status/2118769896591106302
- note: Free to browse. Sponsored by Mobbin. Subscribe is a newsletter, not a gate.

#### Pricing Pages
- name: Pricing Pages
- url: https://pricingpages.design
- category: Inspiration galleries
- what it is: Pricing pages only, filtered by tier cards, comparison tables, monthly switch, and usage pricing.
- when to use it: Designing a pricing section.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://pricingpages.design
- note: The homepage is the gallery.

#### Minimal Gallery
- name: Minimal Gallery
- url: https://minimal.gallery
- category: Inspiration galleries
- what it is: Curated minimal sites, tagged by portfolio, startup, one page, agency, and SaaS. Running since 2013. A weekly email is optional.
- when to use it: A quieter landing-page reference than the louder galleries.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://x.com/YassineZaanouni/status/2119700637239894349
- note: Also named by Arian Adeli on Indie Hackers, 7 Apr 2026, next to Land-book.

#### recent.design
- name: recent.design
- url: https://recent.design
- category: Inspiration galleries
- what it is: Site gallery. godly.website now redirects here.
- when to use it: Recent whole-site references.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://x.com/YassineZaanouni/status/2119700637239894349
- note: The post linked godly.website. That host redirects to this one.

#### Dead Simple Sites
- name: Dead Simple Sites
- url: https://deadsimplesites.com
- category: Inspiration galleries
- what it is: Sites chosen for being quiet: no animation and no scroll-jacking, per the gallery's own description.
- when to use it: A reference for a page that should stay still.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://www.indiehackers.com/post/the-best-design-directories-to-show-off-your-work-e7b0c99522
- note: Named by Arian Adeli on Indie Hackers, 22 Dec 2025.

#### OG Image Gallery
- name: OG Image Gallery
- url: https://www.ogimage.gallery
- category: Inspiration galleries
- what it is: Hand-picked Open Graph images, filtered by category. Open Graph Examples is the larger sibling and lists the meta tags behind each image.
- when to use it: Designing a social preview image.
- directly usable for a web page: no (Reference only)
- install / usage: n/a
- license: Viewing only
- stack: Website
- source post: https://www.indiehackers.com/post/the-best-design-directories-to-show-off-your-work-e7b0c99522
- note: The larger catalog is https://opengraphexamples.com

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

#### fffuel
- name: fffuel
- url: https://www.fffuel.co/gggrain/
- category: Fonts, colors & backgrounds
- what it is: Free in-browser SVG generators. gggrain makes grainy gradients, nnnoise makes noise, and uuunion makes mesh-like gradients.
- when to use it: A grain or noise background while the grainy-gradients demo host is paused.
- directly usable for a web page: yes (SVG export)
- install / usage: Export from https://www.fffuel.co/gggrain/
- license: Free SVG export for use on the web or in a design app. No SPDX license was stated on the generator page.
- stack: Website; SVG export
- source post: https://www.reddit.com/r/web_design/comments/1kjiq3n/where_does_one_find_or_generate_these_grainy/mro5xla/
- note: Named on r/web_design, 11 May 2025, in a thread about grainy Webflow backgrounds.

#### Haikei
- name: Haikei
- url: https://haikei.app
- category: Fonts, colors & backgrounds
- what it is: SVG background generators. The free tier is 15 generators, unlimited SVG downloads, and unlimited medium-resolution PNGs, with no signup.
- when to use it: A blob, wave, or grid background exported as SVG.
- directly usable for a web page: yes (SVG export on the free tier)
- install / usage: Export from https://haikei.app on the free tier
- license: Free tier stays free, including commercial and client work. You may not use the output to run a competing generator. Pro is marked coming soon.
- stack: Website; SVG and PNG export
- source post: https://www.reddit.com/r/SideProject/comments/18ydql9/i_launched_my_abandoned_side_project_and_recently/kgag57p/
- note: Do not buy Pro without approval. Pricing page copyright 2026.

#### Fontshare
- name: Fontshare
- url: https://www.fontshare.com
- category: Fonts, colors & backgrounds
- what it is: Free fonts from the Indian Type Foundry, including Satoshi and Clash Display. Those two are marked closed source on the catalog.
- when to use it: A display or text face with a foundry behind it, when Google Fonts is too familiar.
- directly usable for a web page: yes (Font files)
- install / usage: Download a family from https://www.fontshare.com and follow that family's terms
- license: Free for personal and commercial use. Do not modify or redistribute Satoshi or Clash Display. They are closed source.
- stack: Font files
- source post: https://www.reddit.com/r/typography/comments/12wwfdg/give_me_your_top_3_free_type_foundries_or_free/jhgyge6/
- note: Named on r/typography, 24 Apr 2023.

#### Realtime Colors
- name: Realtime Colors
- url: https://www.realtimecolors.com
- category: Fonts, colors & backgrounds
- what it is: Palette preview on a sample layout, so contrast and roles are visible before you copy the colors.
- when to use it: Choosing a palette and checking it on type, surfaces, and buttons together.
- directly usable for a web page: yes (Palette preview)
- install / usage: Build the palette at https://www.realtimecolors.com and copy the CSS variables
- license: The site says it is 100% free.
- stack: Website
- source post: https://x.com/YassineZaanouni/status/2119700637239894349

#### oklch.com
- name: oklch.com
- url: https://oklch.com
- category: Fonts, colors & backgrounds
- what it is: OKLCH color picker and converter from Evil Martians. Hue, lightness, and chroma move independently. Source is the MIT picker at github.com/evilmartians/oklch-picker.
- when to use it: Picking or converting a color in OKLCH instead of HSL.
- directly usable for a web page: yes (Color picker)
- install / usage: Use https://oklch.com or the source at https://github.com/evilmartians/oklch-picker
- license: MIT
- stack: Website; MIT source
- source post: https://www.reddit.com/r/web_design/comments/1pvk7qz/oklch_obviously_not_a_thing_but_why/nvx2pe6/
- note: Recommended on r/web_design, 25 Dec 2025.

#### Mona Sans
- name: Mona Sans
- url: https://github.com/github/mona-sans
- category: Fonts, colors & backgrounds
- what it is: GitHub's variable grotesque. Axes are weight, width, and slant. Hubot Sans ships beside it.
- when to use it: A variable sans with a license you can read, instead of a closed display face.
- directly usable for a web page: yes (Font files)
- install / usage: Use the OFL files from https://github.com/github/mona-sans
- license: SIL Open Font License
- stack: Variable font
- source post: https://github.com/github/mona-sans
- note: The project page says open source and free to use, licensed under the OFL.

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
