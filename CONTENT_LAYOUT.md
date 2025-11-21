# Serenity Sketch Funnel - Content Layout

## Page Structure Overview

Single-page newsletter signup funnel optimized for mobile loading. Content loads progressively with lazy-loading for below-the-fold sections.

---

## 1. Hero Section (Above the Fold)
**Purpose:** Primary value proposition and immediate call-to-action

- **H1:** "Sign up to our newsletter, to receive a playable demo"
- **Hero Image:** Gameplay preview (responsive WebP)
- **Benefits List:** 3-item list with numbered badges
  - Demo link delivered to your inbox
  - Development updates and art drops
  - Invites to exclusive playtest sessions
- **CTA Buttons:** 
  - "Sign up" (primary) → scrolls to form
  - "Learn More" (secondary) → scrolls to About section

---

## 2. Newsletter Signup Form Section
**Purpose:** Capture email and platform preference, convert to subscriber

- **Heading:** "Step 1 · Tell us where to send the demo"
- **Description:** Newsletter benefits and value proposition
- **Form Fields:**
  - Email (required)
  - Platform selection checkboxes (PC, iPad, iPhone, Android, Nintendo Switch)
  - Hidden tracking fields (UTM params, click IDs)
- **Privacy Policy:** Link to data privacy policy
- **Subscription Checkbox:** Pre-checked, required for demo access
- **Submit Button:** "Email me the demo"
- **Trust Copy:** Helper text for existing subscribers + link to main site

---

## 3. About Serenity Sketch Section (Lazy-Loaded)
**Purpose:** Educational content about the game, loads only when user scrolls near it

**Loading Behavior:** Hidden initially, loads via IntersectionObserver when user approaches (300px before viewport)

**Content Structure:**
- **H2:** "About Serenity Sketch"
- **Intro Paragraph:** Game description (digital experience, guided painting journey)
- **Image 1:** about1 (painting with water concept)

- **H3:** "You're Not the First to Walk This Path"
- **H4:** "Painting with Water—Simple, Timeless"
- **Paragraph:** Ancient practice of evaporating water painting
- **Image 2:** about2 (guided prompts concept)

- **H4:** "Be Guided Along the Path of Letting Go"
- **Paragraph:** Daily prompts with gentle voice, self-reflection questions

- **H4:** "Explore Natural, Inviting Settings"
- **Bullet List:** 4 natural environments (forest, ocean bay, cliffs, wood)
- **Paragraph:** Calming soundscapes
- **Image 3:** about3 (natural environments)

- **CTA Button:** "Sign Up" → scrolls back to form section

---

## 4. Footer
**Purpose:** Minimal footer with site link

- Text: "Built for fast loading on GitHub Pages"
- Link: "See the full site" (to main Squarespace site)

---

## Technical Features

- **Lazy Loading:** Educational section loads only when scrolled near
- **Responsive Images:** All images use `<picture>` with multiple sizes (WebP format)
- **Smooth Scrolling:** Navigation buttons use smooth scroll behavior
- **Analytics:** GTM tracking for button clicks and form submissions
- **Mobile Optimized:** Fast initial load, progressive content loading

---

## Navigation Flow

1. User lands → sees hero + benefits
2. User clicks "Sign up" → scrolls to form
3. User clicks "Learn More" → scrolls to About section (triggers lazy load)
4. User reads About section → clicks "Sign Up" → scrolls back to form
5. User submits form → redirects to success page

