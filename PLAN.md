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
| 5 | Implement success page (`success.html`) with inbox-confirm message + “Learn more” link to Squarespace site | ✅ Done | Added “Need us to resend?” CTA + learn-more link |
| 6 | Integrate MailerLite form with hidden fields + redirect to success page | ⏳ Pending | Form + success redirect wired; needs live test with MailerLite |
| 7 | Test flow (desktop & mobile), send test submission, verify GTM + MailerLite logging | ⏳ Pending | Document any issues before deploy |
| 8 | Prepare deployment notes for GitHub Pages (assets paths, cache) | ⏳ Pending | Outline steps for user to publish |

## Next Actions
1. Provide/confirm final visual assets or authorize placeholder generation.
2. Implement landing and success HTML/CSS per plan.
3. Hook MailerLite form redirect and validate on staging.

