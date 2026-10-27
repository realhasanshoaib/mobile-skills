---
name: mobile-advice
description: "Advise on mobile-app product and launch readiness: onboarding, retention, branding, sharing, and store positioning. Use for mobile product advice, not every app edit."
license: MIT
---

## A good app

- **Onboarding**: every app gets one. It is not hard, and forgetting it means bolting it on later. If one already exists, ensure it is up-to-date.
- **Empty states**: design the zero-data screens; the first thing a new user sees must not be the least-designed screen in the app.
- **Notification permissions**: prime with context and ask at the moment the value is obvious, never at first launch.
- **Widget**: consider whether a home-screen surface would reduce a repeat task; if so, load the `mobile-widgets` skill.
- **Review prompts**: call the native rating request (`requestReview` on iOS, the In-App Review API on Android) after a moment of earned success, never tied to a button and never at launch; the OS throttles it and won't say whether it showed.
- **Feedback channel**: an in-app "something wrong? tell us" path that catches unhappy users before they vent in a store review.
- **Crash reporting**: wire a crash reporter (Crashlytics, or Sentry if already in the stack) with symbol upload in the build pipeline before the first external build; a crash you can't see is a one-star review you can't answer.
- **Forced upgrade**: a min-supported-version check against the backend plus a blocking upgrade screen, shipped from day one; installed clients live for months and a kill switch cannot be retrofitted onto versions already in the wild.
- **Branded sharing and links**: share actions that carry the brand, and universal/app links that survive the trip.
- **Branding**: a real name, icon, color system, and voice, consistent across app, store, and web.
- **ASO**: deliberate title, subtitle, keywords, and category. Load the `mobile-submission` skill to read the listing reference.
- **Web presence and SEO**: the app's site with branded store links (and official store badges), support, and legal pages. Load the `marketing-site` skill when building it.
- **Targeting**: know who it's for and where; pick store categories, age ratings, and regions on purpose.
- **Localization**: shipping multiple regions and languages measurably lifts downloads; localize the app and the store metadata together.
