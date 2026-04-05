# IntelliToggle Homepage

Recreated from Figma design as part of the VenturSeed Frontend Developer Assignment.

## Live URL

<!-- Add your Netlify URL here after deploying -->
https://intellitoggle-homepage.netlify.app

## Tech Stack

- Nuxt 3
- Vue 3 (Composition API)
- TailwindCSS v3 via @nuxtjs/tailwindcss

## Getting Started

```bash
npm install
npm run dev
```

Open http://localhost:3000

## Build for production

```bash
npm run build
npm run preview
```

## Project Structure

```
app/
  app.vue                  # root layout
  components/
    AppNav.vue             # navbar with mobile toggle
    HeroSection.vue        # hero with dashboard mockup
    TrustedBy.vue          # trusted logos strip
    WhatIsSection.vue      # what is intellitoggle + chart
    OpenFeatureSection.vue # openfeature integration section
    ControlSection.vue     # control & power focused (3 steps)
    DartCodeAI.vue         # dark AI section with cards
    PricingSection.vue     # 3 pricing cards + comparison table
    WhyTeams.vue           # why teams use intellitoggle
    CTABanner.vue          # bottom cta banner
    AppFooter.vue          # footer with newsletter
```

## Interactive Elements

- Mobile hamburger menu toggle (AppNav.vue) — opens/closes on click
- Pricing comparison table accordion — toggle full feature comparison
- Newsletter subscribe form with success feedback (AppFooter.vue)

## Tradeoffs & Notes

- Dashboard mockup in hero is built in code (no image asset available from Figma export)
- Logo SVG is hand-coded to match the Figma logo as closely as possible
- Company trust logos are SVG placeholders since no image assets were exported
- With more time I would: add smooth scroll animations, improve the dashboard mockup with real screenshots, add page transitions

## Pixelay Screenshots

See /pixelay folder for desktop and mobile overlay screenshots.