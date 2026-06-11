# Project Constraints: Benedikt Bauer Portfolio

This document outlines the architectural and design constraints for the Benedikt Bauer developer portfolio.

## Tech Stack
- **Framework**: Astro (Static Site Generation)
- **Styling**: Tailwind CSS v4 (using the new `@theme` variable system)
- **Deployment**: Static hosting

## Design System
- **Style**: Minimalist, high-signal, clean typography (Inter).
- **Color Palette**:
  - Base: `bg-stone-50` (Off-white)
  - Text: `text-stone-900` (Main), `text-stone-600` (Secondary)
  - Accent: `#0077b6` (Deep professional blue), defined as `var(--color-accent)` in Tailwind.
- **Layout**:
  - Container: `max-w-screen-2xl` (targets ~80% width on 1080p).
  - Structure: Two-column grid on desktop (`lg:grid-cols-[1fr_2fr]`) with section labels on the left.
  - Spacing: Responsive padding that balances hero impact with immediate readability.

## Brand Identity (The Cyclist Logo)
- **Asset**: Custom abstract geometric bicycle (derived from `public/bicycle-logo.svg`).
- **Behavior**: "Hero-to-Watermark" transition.
  - Starts centered at full opacity with significant top padding.
  - Fades to **10% opacity** (`minOpacity: 0.1`) on scroll.
  - Remains `fixed` in the background as a subtle watermark after scrolling.

## Content Guidelines
- **Focus**: IT Architecture, security standards, and full-stack development.
- **Tone**: Senior professional, senior engineer, peer-to-peer developer focus.
- **Highlights**: BEYONDER projects (Empto, BlueOak) and selected Open Source work (Trivy, Ambient Toolbox).
- **Personal**: Brief, meaningful inclusions of cycling and photography to humanize the profile.

## Development Workflow
- **Build**: `npm run build` generates a clean `dist/` folder.
- **Validation**: Ensure no regressions in the scroll-based logo transition when adding new content.
- **Responsiveness**: Always verify changes on both mobile (stacked) and wide desktop (grid) views.
