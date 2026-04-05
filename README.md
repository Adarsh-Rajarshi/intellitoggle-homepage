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

## Tradeoffs & Notes

- Went with Nuxt 3 static generation over SSR since this is a 
  marketing homepage — no need for server-side rendering, 
  and static gives better performance on Netlify CDN.

- Used @nuxtjs/tailwindcss module instead of the new 
  @tailwindcss/vite approach — more stable with Nuxt 3's 
  module system and avoids ESM conflicts during build.

- Dashboard mockup in the hero is hand-coded in Vue — 
  Figma assets weren't exportable so I rebuilt the layout 
  in code to match as closely as possible. Given more time 
  I'd swap this with a real screenshot using Nuxt Image 
  with lazy loading.

- Trust logos are SVG placeholders — no image assets were 
  available in the Figma file. In production I'd replace 
  these with optimized WebP assets.

- Chose component-per-section architecture deliberately — 
  makes it easy to drop individual sections into a Craft CMS 
  or Ghost template later without refactoring.

- Skipped page transitions for now to stay within the 
  timebox — would add Vue's built-in Transition component 
  for smooth section reveals on scroll.

- With more time: add ARIA labels throughout, implement 
  Nuxt Image for performance, add scroll-triggered animations 
  using Vue's Intersection Observer.
## Pixelay Screenshots

See /pixelay folder for desktop and mobile overlay screenshots.