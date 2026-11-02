# Health Camper website — memory for Claude sessions

Owner: Rujal (non-developer). Explain things in plain language and do the work for them.
Ask before signing up for any service or spending money.

## What this repo is
- The marketing website **healthcamper.com** for the Health Camper iOS app.
- Plain static HTML + CSS, no build step. Served by **GitHub Pages from `main`** (root folder) with the `CNAME` file (`healthcamper.com`). Never delete `CNAME`.
- Pushing to `main` deploys in 1–2 minutes. Rujal has authorized pushes to `main` for this repo. After pushing, check that https://healthcamper.com shows the change (there is no `.github/` workflow; Pages builds automatically).
- Anything committed to the repo becomes public on the site, so drafts and previews live outside the repo (or as claude.ai artifacts) until Rujal approves them.

## The app (what the site promotes)
- Free, camping-themed mindfulness app for iPhone. No account, no ads, no subscription, no paywall.
- Confirmed v1.0 features (use only these when describing the app): guided breathing (visual pacer), meditation timer / quiet minutes, sleep sounds synthesized live on the phone (never loop, work offline, keep playing when locked, sleep timer — Deep Sleep Noise, Rain on Tent, Campfire, Mountain Wind, Forest River, Crickets), mood journal, streaks, "Today's climb" (Camp One affirmation, Camp Two one small goal, Camp Three quiet minutes), optional Apple Health (writes Mindful Minutes only).
- Guide character: **Pemba**, a Sherpa trail guide.
- **Not shipped yet — always say "coming soon / in a future update":** First Light (calm 5-minute morning talk; Pemba's 8 AM daily talk), a pure White Noise mode.
- Do not claim: sleep stories, long guided meditation journeys, body scans, SOS sessions, push reminders/nudges, daily journaling prompts — none are confirmed in v1.0.
- Status: v1.0 submitted to App Review (last known "Waiting for Review"). Not on the App Store yet, so the site says "coming soon". There is **no Android app**.
- Future: optional "Camp Pass" subscription ($29.99/yr) planned for v1.2 only. **Do not advertise it.** Keep the "free" promise accurate.
- App repo: `rujal-tuladhar/health-camper` (marketing material in `marketing/` on branch `claude/hello-07hyfa`). Don't edit it from here; reading it needs it added to the session.

## Site map
- `index.html` — home (hero, features, affirmation, AI-character video, blog preview, download/sign-up). Sign-up is only a `mailto:` link for now.
- `blog/` — 18 articles + `index.html`; new posts start from `blog/_post-template.html` (see README). Each post ends with an `.article-cta` box that promotes the app.
- `notes.html` — "Notes from Camp", 12 short kind-reminder cards.
- `privacy-policy.html`, `support.html` — **live and linked from the App Store listing. Never rename or move these URLs.**
- `sitemap.xml`, `robots.txt`, `css/style.css` (all shared styles; colors are variables at the top).

## Look and feel
- The website itself is light: forest green `#1f4d3f`, dark forest `#143528`, sage `#7fb69b`, mist `#eaf4ee`, cream `#fbf9f4`, sun `#f4b860`. Headlines in **Lora** (serif), body in **Nunito**.
- The app and the Notes cards use the darker "campsite at night" look (navy/near-black `#0a0f24`→`#0d211c` with ember orange `#ff9440` / `#c4643a`). Use it for night-themed bands and cards.

## Content rules (from Rujal)
- Every page should promote the app in some way, gently.
- Original content only — never copy other accounts' quotes or art.
- No medical claims, no made-up statistics.
- Public contact email: **healthcamper00@gmail.com**.

## Plan & status
_Last updated: 2026-11-02_

### Known fixes
1. ✅ Removed "Google Play" from the home page (no Android app). Hero now says "Free on iPhone. Coming soon to the App Store."
2. ✅ Pre-launch feature claims cleaned up: home feature cards and meta description now list only confirmed v1.0 features; First Light marked "coming in a future update" (notes.html, be-kind-to-yourself-hard-morning); 10 older blog call-out boxes rewritten to confirmed features only.
3. ⏳ Keep "free, no subscription, no paywall" accurate; don't mention Camp Pass until v1.2 ships. When v1.2 nears, the wording on support.html, posts and the App Store listing must change to something like "free, with an optional supporter pass".
4. ⏳ Replace the mailto sign-up with a real email-list tool — waiting for Rujal to approve one (options: Buttondown, MailerLite, Kit/ConvertKit free tiers; README mentions Formspree).
5. ⏳ When the app is live: add the App Store badge + link everywhere ("Get the App" buttons, every blog CTA, notes.html, hero), and change "coming soon" wording.

### Camp Store (selling camping gear on the site)
- Goal: sell camping products tied to the brand, "gear for calmer nights outdoors".
- ✅ Research done (see "Shop recommendation" below).
- ✅ Design mock of shop section + product page + cart built as a preview (NOT on the live site): https://claude.ai/artifact/7YbZXmfqjjAtest6pSXKo9 (source kept outside the repo).
- ⏳ Waiting for Rujal: approve the approach, choose a platform, approve the mock. Nothing has been signed up for or bought.
- Rules for the shop: never imply buying gear unlocks anything in the app; no "helps you sleep" health claims for products; every product pairs with an app sound (soft cross-promotion); privacy policy + terms of sale + shipping/returns pages must be added before the shop goes live, without changing the app privacy policy's promise that the **app** collects nothing.
