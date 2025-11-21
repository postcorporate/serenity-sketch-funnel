# Serenity Sketch Funnel Plan

## Context
- Goal: migrate Squarespace homepage content/branding into a fast two-step GitHub-hosted funnel that captures newsletter signups via MailerLite and delivers the Serenity Sketch demo.
- Conversion: MailerLite subscription → send demo link + keep audience engaged with development updates.
- Tracking: retain GTM snippet and ensure success events fire for analytics.

## Task Tracker
| Step | Description | Status | Notes |
| --- | --- | --- | --- |
| 1 | Review existing `index.html` and embedded MailerLite/GTM setup | ✅ Done | Confirmed GTM (`GTM-PSX9CFD6`) and MailerLite form `mlb2-32107971` already wired |
| 2 | Define stripped-down two-stage funnel structure & content outline | ✅ Done | Stage 1 landing + Stage 2 success page, CTA = demo-for-newsletter |
| 3 | Collect or request optimized assets (logo + 1–2 gameplay WebPs) | ✅ Done | Assets delivered in `images/` (Hero1/2 desktop+mobile, logo SVG + fallback) |
| 4 | Draft lightweight landing page (`index.html`) layout & copy | ✅ Done | Rebuilt hero + CTA copy, trimmed CSS, integrated benefits + form |
| 5 | Implement success page (`success.html`) with inbox-confirm message + "Learn more" link to Squarespace site | ✅ Done | Updated with "Step 2: Check Your Inbox!" heading and simplified body copy mentioning demo link + newsletter opt-in |
| 6 | Integrate MailerLite form with hidden fields + redirect to success page | ⏳ Pending | Form + success redirect wired; needs live test with MailerLite |
| 6a | Update form with GDPR-compliant checkboxes (legal consent + optional marketing) | ✅ Done | Replaced pre-checked subscription with mandatory legal checkbox (unchecked) + optional marketing checkbox (unchecked). Note: Terms of Service & EULA link currently points to placeholder URL - update if needed |
| 7 | Implement lazy-loading educational content section (below-the-fold) | ✅ Done | Added IntersectionObserver-based lazy loading system for mobile-optimized content loading |
| 8 | Populate educational content section with Serenity Sketch information | ⏳ Pending | Add game details, features, screenshots, or other educational content to `lazy-content-inner` div |
| 9 | Test flow (desktop & mobile), send test submission, verify GTM + MailerLite logging | ⏳ Pending | Document any issues before deploy |
| 10 | Prepare deployment notes for GitHub Pages (assets paths, cache) | ⏳ Pending | Outline steps for user to publish |

## Next Actions
1. Populate educational content section with Serenity Sketch information (features, gameplay details, screenshots, etc.)
2. Provide/confirm final visual assets or authorize placeholder generation.
3. Implement landing and success HTML/CSS per plan.
4. Hook MailerLite form redirect and validate on staging.

## Lazy-Loading Educational Content Section

### Implementation Details
- **Location**: Below the form section, before footer
- **Element ID**: `educational-content` (container), `lazy-content-inner` (content area)
- **Loading Strategy**: 
  - Content is hidden in HTML but not rendered until user scrolls near it
  - Uses `IntersectionObserver` with 300px rootMargin for early loading
  - Uses `requestIdleCallback` to load during browser idle time
  - Smooth fade-in animation when content appears
- **Mobile Optimization**: 
  - No additional HTTP requests (content in HTML)
  - Minimal impact on initial page load
  - Works on older browsers with scroll-based fallback

### Content to Add
The educational section currently has placeholder content. To populate it, edit the `#lazy-content-inner` div in `index.html` and add:
- Game description and features
- Screenshots or gameplay images (use `loading="lazy"` attribute)
- Development updates or behind-the-scenes content
- Any other educational content about Serenity Sketch

### Analytics
- Event `educational_content_loaded` fires when content is loaded (tracked in GTM)

