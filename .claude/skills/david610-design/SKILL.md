---
name: david610-design
description: Recreate and extend the visual language of David610/david610.github.io. Use this skill whenever the user asks to match David's portfolio style, reuse the david610.github.io design, build a clean technical/editorial portfolio, or apply this restrained resume-like design system to another website, dashboard, landing page, or app. Preserve the source site's narrow content column, sans + monospace typography contrast, neutral borders, compact cards, small badges, sparse blue accents, print-aware layout, and command-palette feel. Do not turn it into generic SaaS styling.
---

# David610 Design

Use the visual system of `David610/david610.github.io` as a design language, not as a page template.

The source is a compact technical portfolio/resume. Its identity comes from restraint, information density, typography, borders, and small utility interactions. When applying the skill to a different product, preserve that DNA while adapting the information architecture to the product.

## Core aesthetic

Aim for:

- editorial rather than promotional
- technical rather than decorative
- compact rather than oversized
- white-space disciplined rather than empty
- monochrome first, blue only as an accent
- structured information rather than visual spectacle
- visibly designed, but almost no ornament

The result should feel like a strong personal technical document that became an interface.

Do not introduce visual ideas simply because they are common in modern frontend work.

Avoid:

- gradient backgrounds
- glassmorphism
- huge marketing heroes
- oversized display typography
- glowing effects
- floating decorative blobs
- heavy drop shadows
- excessive card nesting
- large-radius pill-shaped containers everywhere
- purple or multicolor AI-style palettes
- generic dashboard chrome unless the product actually needs it
- gratuitous animation

## Design tokens

Use these as the default palette unless the target product has a required brand color.

### Light theme

- background: `#ffffff`
- primary text: `#333333`
- muted text: `#666666`
- border: `#eaeaea`
- subtle surface: `#f1f1f1`
- accent blue: `#0070f3`
- accent hover: `#0056b3`
- input border: `#e2e8f0`

### Dark theme

- background: `#111827`
- elevated surface: `#1f2937`
- muted surface: `#374151`
- primary text: `#f3f4f6`
- muted text: `#9ca3af`
- accent blue: `#60a5fa`
- border: `#374151`

Dark mode should remain restrained. Do not add neon effects or change the character of the design.

## Typography

Typography is the main visual device.

Use two voices:

1. Sans-serif for hierarchy, names, headings, labels, controls, and important facts.
2. Monospace for descriptions, metadata, technical content, supporting copy, tags, and dense factual text.

For web implementations, prefer the platform/system sans stack used by the source:

`-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif`

For monospace, use the framework's native monospace stack or:

`ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace`

Do not replace this with fashionable display fonts unless the user explicitly asks for a reinterpretation. The plainness is part of the identity.

### Type hierarchy

Use approximately:

- page name / primary heading: 24px, bold
- section heading: 20px, bold
- card title: 16px, semibold
- main descriptive text: 14px
- supporting metadata: 12–14px
- badge text: 12px

Keep headings compact. Avoid 48–72px landing-page headlines.

Section headings may use a thin bottom border. This is one of the source site's strongest structural cues.

## Layout

The source uses a centered, narrow reading column.

Default rules:

- outer content width: no more than about 800px
- primary reading width: about 672px / `max-w-2xl`
- desktop outer padding: about 64px where space allows
- mobile padding: about 16px
- major section rhythm: roughly 32px
- internal section rhythm: roughly 12px
- card-to-card rhythm: 12–16px

Prefer one strong vertical reading flow.

Do not stretch normal content edge-to-edge just because the target viewport is wide. If the product needs a wider layout, keep individual reading blocks narrow and preserve the compact typography and border system.

## Header pattern

A typical top block should contain:

- identity/title at left
- short monospace descriptor below
- small metadata such as location below that
- compact icon controls
- optional square/rounded-square portrait or identifying visual at right

Controls should be small and functional, not large call-to-action buttons.

For icon-only controls:

- about 32 × 32px
- thin 1px border
- radius around 6px
- no shadow
- simple line or monochrome icons
- visible keyboard focus state

Use Lucide-style line icons or similarly restrained iconography.

## Sections

Each major section should read like a document section.

Default structure:

1. short bold heading
2. thin divider where useful
3. one or more compact content blocks
4. monospace supporting text

Do not wrap every section in a large card.

Let whitespace, headings, and thin borders create structure.

## Cards

Cards are quiet containers, not visual features.

Default card:

- white/light surface
- 1px neutral border
- 8px radius
- 16px padding
- no shadow
- compact internal spacing

In dark mode, use the elevated dark surface and dark border.

A card header often contains:

- title/company/entity on the left
- small date/status on the right
- optional location below
- one small badge inline with the title

On small screens, allow the right-side metadata to wrap or stack rather than compressing the title.

## Badges

Badges should be small and informational.

Default:

- 12px monospace text
- semibold
- 2px vertical / 8px horizontal padding
- about 6px radius
- no shadow

Use two primary treatments:

- neutral badge: gray background with white text
- accent badge: blue background with white text

Do not make every taxonomy item colorful. Color should communicate a real distinction.

## Lists and dense content

This design works well for structured factual content.

For bullet lists:

- use compact vertical spacing
- keep line length controlled
- use muted monospace text
- use standard discs unless there is a strong semantic reason for icons

Avoid replacing useful bullets with decorative feature cards.

## Interaction style

Interactions should feel like utilities.

The source includes a command menu opened with `Cmd/Ctrl + J`. When a command palette or quick-action menu is useful, preserve this feel:

- centered modal
- neutral overlay
- white/dark rectangular panel
- modest 8px radius
- compact search field
- simple rows
- clear keyboard access
- no dramatic animation

Other useful interaction patterns from the source:

- language switch
- print action
- dark-mode toggle
- contact action
- compact loading state for media

Do not add interactions just to imitate the source. Use them when they fit the product.

## Motion

Use very little autonomous motion.

Good:

- short loading spinner
- immediate hover/focus feedback
- subtle menu open/close transition
- smooth scrolling when it helps navigation

Avoid:

- section-by-section entrance animations
- bouncing icons
- parallax
- looping decorative motion
- animated gradients

The design should still feel complete with motion disabled.

## Responsive behavior

Preserve information density on mobile.

- reduce outer padding to about 16px
- keep the single-column flow
- stack title/date rows when they no longer fit
- allow badge rows to wrap
- keep controls compact
- never shrink text until it becomes difficult to read
- do not convert the page into a carousel

For richer applications, responsive changes should simplify the shell while keeping the same typography, borders, surfaces, and spacing discipline.

## Print behavior

Print quality is part of this design language.

When the target page contains document-like information:

- hide purely interactive controls
- remove fixed UI that does not belong on paper
- preserve the content hierarchy
- avoid clipped cards
- use sensible page breaks
- keep links readable
- maintain compact spacing

A page built with this skill should be able to look credible as a printed technical document when that use case is relevant.

## Accessibility

Keep the restrained visual language without sacrificing usability.

Always provide:

- visible focus states
- adequate text contrast
- semantic headings
- labels or accessible names for icon-only controls
- keyboard support for command menus and dialogs
- reduced-motion support when motion exists
- sufficient hit areas even when controls look visually compact

## Adapting the style to other products

Do not copy the resume page literally.

Instead map the source design language to the product.

Examples:

### Dashboard

Use:

- narrow or moderately wide content frame
- compact sans headings
- monospace metrics and metadata
- thin bordered panels
- small status badges
- no decorative chart cards

Charts should remain visually quiet with neutral axes and one accent color.

### SaaS settings page

Use:

- document-like sections
- small section headings with dividers
- compact form controls
- bordered groups only where grouping is useful
- monospace help text where technical detail matters

### Landing page

Use:

- a compact header rather than a huge hero
- strong factual headline
- short technical descriptor
- evidence or project blocks in quiet bordered cards
- one restrained primary action

Do not force the style into a conventional startup landing-page template.

### Portfolio or CV

Stay closest to the source:

- narrow reading column
- identity + metadata header
- card-based education/experience entries
- monospace descriptions
- compact badges
- print-friendly output

## Implementation guidance

Respect the project's existing framework.

If the project already uses Tailwind, map the tokens and spacing into Tailwind utilities or theme variables.

If it uses CSS modules, styled components, vanilla CSS, or another system, reproduce the visual rules there instead of adding Tailwind only for this skill.

Prefer reusable tokens for:

- colors
- spacing
- radius
- border
- type scale
- muted text

Avoid introducing a large component library solely to recreate simple bordered cards and buttons.

## Validation checklist

Before considering the design finished, inspect the actual rendered result.

Check:

- Is the content width disciplined?
- Does the page feel compact rather than oversized?
- Is monospace used for secondary/technical information?
- Are borders doing more work than shadows?
- Is blue used sparingly?
- Are cards quiet and compact?
- Are section headings clear without being huge?
- Are controls small but usable?
- Does mobile preserve the hierarchy?
- Does dark mode keep the same character?
- If relevant, does print still look intentional?
- Did any generic SaaS or AI-design patterns slip in?

If the result looks more like a template gallery than a technical document, simplify it.

## Source fidelity

The design was derived from:

- `index.html`
- `index_en.html`
- `styles.css`
- `script.js`
- `README.md`

in `David610/david610.github.io`.

When those source files are available and the user asks for exact fidelity, inspect them before changing the design rather than relying only on this summary.
