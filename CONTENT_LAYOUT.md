# Serenity Sketch Funnel - Content Layout

## Page Structure Overview

Single-page newsletter signup funnel optimized for mobile loading. Content loads progressively with lazy-loading for below-the-fold sections. Optimized for high-intent lead capture with a single primary CTA in the hero section.

---

## 1. Hero Section (Above the Fold)
**Purpose:** Instant value proposition and high-intent CTA

- **H1:** "Melt Away Stress Through Artistic Play"
- **Hero Image:** Gameplay preview (responsive WebP) - replaces video suggestion
- **Value Statement (2 lines):** "The guided creative experience that blends the focus of meditation with the joy of art. Start your journey to inner quiet today."
- **CTA Button (ONE PRIMARY):** "Get the Private Demo Link" → scrolls to form section
- **Note:** Removed "Learn More" button to eliminate choice paralysis - users either convert or scroll down to self-qualify

---

## 2. Newsletter Signup Form Section
**Purpose:** Capture email and platform preference with clear value exchange

- **Heading:** "Step 1: Get the Demo & Exclusive Invites"
- **Description:** "Enter your email below to receive the private playable demo link instantly. You'll also get:"
  - **Bullet List:**
    - First Access: Be the first to receive new demo updates.
    - Community Invites: Join exclusive playtest sessions.
    - The Vision: Receive behind-the-scenes insights on blending creativity and mindfulness.
- **Form Fields:**
  - Email (required)
  - Platform selection checkboxes (PC, iPad, iPhone, Android, Nintendo Switch)
  - Hidden tracking fields (UTM params, click IDs)
- **Privacy Policy:** Link to data privacy policy
- **Subscription Checkbox:** Pre-checked, required for demo access
- **Submit Button:** "Email Me My Demo Link"
- **Trust Copy:** "We hate spam. We only use your email to send the demo link and project updates. [Privacy Policy Link]"

---

## 3. About Serenity Sketch Section (Lazy-Loaded)
**Purpose:** Address complexity and educate users who need more information before signing up

**Loading Behavior:** Hidden initially, loads via IntersectionObserver when user approaches (300px before viewport)

**Content Structure:**
- **H2:** "What is Serenity Sketch?"
- **Intro Paragraph:** "A Guided Path to Inner Quiet. Serenity Sketch is a digital experience you can play on your phone, tablet, or PC—designed for those who seek the quiet focus of meditation but are drawn to the process of creation."

- **H3:** "The Hybrid Experience: Mindfulness Meets Art"

- **Feature Block 1: Let Go with Water Painting**
  - **Paragraph:** "Discover the ancient practice of painting with water. There are no mistakes, no permanent marks—just a simple, soothing canvas that evaporates as you create, focusing you purely on the present moment."
  - **Image 1:** about1 (painting with water concept)

- **Feature Block 2: Guided Prompts, Not Goals**
  - **Paragraph:** "Gentle voice prompts and self-reflection questions guide you through your session. These are invitations to explore, not tasks to complete, helping you connect with your creativity and feel more grounded."
  - **Image 2:** about2 (guided prompts concept)

- **Feature Block 3: Explore Inviting Environments**
  - **Bullet List:** 4 natural environments (forest, ocean bay, cliffs, wood)
  - **Paragraph:** "Immerse yourself in calming soundscapes designed to isolate your focus. Choose from four natural environments, each with unique sound profiles to deepen your relaxation."
  - **Image 3:** about3 (natural environments)

- **Final CTA Button:** "Join the Waitlist (Get the Demo Now)" → scrolls back to form section

---

## 4. Footer
**Purpose:** Minimal footer with site link

- Text: "Built for fast loading."
- Link: "Full Website & Company Info" (to main Squarespace site)

---

## Technical Features

- **Lazy Loading:** Educational section loads only when scrolled near
- **Responsive Images:** All images use `<picture>` with multiple sizes (WebP format)
- **Smooth Scrolling:** Navigation buttons use smooth scroll behavior
- **Analytics:** GTM tracking for button clicks and form submissions
- **Mobile Optimized:** Fast initial load, progressive content loading

---

## Navigation Flow

1. User lands → sees hero with value statement + single primary CTA
2. User clicks "Get the Private Demo Link" → scrolls to form
3. User scrolls down → About section loads automatically (lazy load)
4. User reads About section → clicks "Join the Waitlist (Get the Demo Now)" → scrolls back to form
5. User submits form → redirects to success page

---

## Key Changes from Original

- **Simplified Hero:** Removed dual CTA choice, single focused call-to-action
- **Enhanced Value Proposition:** Clearer benefit statement in hero
- **Improved Form Description:** Bullet list format for better scanability
- **Restructured About Section:** Focus on "Hybrid Experience" with three clear feature blocks
- **Streamlined Footer:** Simplified text
