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
- 2026-11-02: Rujal is starting a **Shopify trial** (Rujal signs up themselves). Plan: Starter + Buy Button sales channel, store in CAD, Canada-only shipping, GST/HST collection OFF until registered, first products = print-on-demand via Printful. **Keep healthcamper.com on GitHub Pages — do not connect the domain to Shopify.** Next for Claude: when Rujal sends the myshopify address and Buy Button embed codes, build the shop pages from the approved mock (Buy Button code and its storefront token are public by design, safe to commit).
- 2026-11-05: New goal from Rujal — launch the store in all **G7 countries** (US, Canada, UK, France, Germany, Italy, Japan), selling camping + calm/mental-wellbeing products **and digital content**, using Shopify-app dropshippers with local fulfilment per country. Rujal asked Claude to create the Shopify account ($1 offer) with the Health Camper email — Claude can't (no browser access to shopify.com, and signup needs Rujal's ID, card and email verification); Rujal signs up themselves. Research done (Nov 5; prices/locations from search summaries — recheck on vendor pages):
  - **Suppliers (Shopify apps, free, pay per order):** Printful has local production in Canada (Toronto), US (Charlotte, Dallas), UK, EU (Spain, Latvia) and a Japan partner. Gelato prints in the customer's own country in ~32 countries incl. Japan, France, Germany (Italy unconfirmed). Digital: Shopify's free Digital Downloads app (Sky Pilot for big audio files).
  - **Avoid:** AliExpress/DSers, tents/sleeping bags, fuel/candles, Japanese domestic dropship (no working Shopify app; Shopkyo removed 2024).
  - **Phased plan:** 1) Canada + US now — Printful + Digital Downloads (digital to Canada/US only) + affiliate shelf for gear. 2) UK + Japan — add Gelato; use Shopify Managed Markets (open to Canadian merchants since Jul 15 2026, fees unclear) for UK VAT / Japan tax; Japanese translation human-checked. 3) France, Germany, Italy last — needs EU GPSR responsible person, local-language safety info, VAT setup (OSS or Managed Markets).
  - **Rules that bite:** US $800 duty-free suspended → fulfil US orders from US; UK VAT from first sale for overseas sellers; EU €150 duty exemption ended Jul 1 2026; digital sales owe EU/UK VAT from first sale; no health claims (FTC, UK ASA).
- ⏳ Waiting for Rujal: approve the mock; send Shopify details once set up.
- Rules for the shop: never imply buying gear unlocks anything in the app; no "helps you sleep" health claims for products; every product pairs with an app sound (soft cross-promotion); privacy policy + terms of sale + shipping/returns pages must be added before the shop goes live, without changing the app privacy policy's promise that the **app** collects nothing.

### Shop recommendation (researched Nov 2026 — recheck prices on vendor pages before signing up)
- **Phase 1 — affiliate shelf ($0/month).** Bulky, regulated gear (tents, sleeping bags, pads, hammocks, headlamps, lanterns) links out to retailers: MEC affiliate program (via AvantLink, ~6%, unverified) and Amazon.ca Associates (~3–4.5%; must make 3 qualifying sales within 180 days). No stock, shipping, returns, HST or product-safety duties. Must show a clear disclosure next to the links ("We earn a small commission if you buy through these links") plus Amazon's required line.
- **Phase 2 — branded print-on-demand items** (mug, blanket, trail journal, tee) via **Printful** (Mississauga facility) or Printify Canadian providers, sold with **Shopify Starter (~$7 CAD/mo, 5% + 30¢ per sale)** Buy Buttons embedded in the static site. Stripe Payment Links ($0/mo, 2.9% + 30¢) are the cheaper but more manual alternative (no cart, orders forwarded to Printful by hand).
- **Not yet:** holding stock of tents/sleeping bags (bulky shipping $15–50+, Canada's Tents Regulations CAN/CGSB-182.1 flammability + bilingual labels, Textile Labelling Act, CCPSA incident reporting), AliExpress dropshipping, fuel/candles (dangerous goods), Gumroad/Lemon Squeezy (digital-only fit), Snipcart (fiddly, monthly minimum).
- **Tax:** no GST/HST registration needed until sales pass $30,000 (single quarter or four consecutive quarters). Affiliate commissions are business income (form T2125), not sales.
- **Before selling own products:** register "Health Camper" business name in Ontario ($60 / 5 years); add Terms of Sale + Shipping & Returns pages meeting Ontario Consumer Protection Act internet-agreement rules (full price/taxes/shipping/policies shown before purchase, order confirmation email); add a shop section to the privacy policy (PIPEDA: what's collected, Shopify/Stripe/Printful as processors, retention, contact); consider product liability insurance (~$350–900/yr) once selling own-brand goods.
- **Shop structure (in the mock):** five shelves — Sleep under the stars, Light the camp, Around the fire, Rest & hang, Kits & keepsakes; 15 products + "Quiet Night Kit" bundle; every product card shows the app sound it pairs with ("♪ Rain on Tent"). Prices in CAD, rounded, mid-range; bundles ~10–15% off.
