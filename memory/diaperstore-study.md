# How diaperstore.ca works (studied 2026-11-22 from its public pages)

Looked at: home page, /products.json (public Shopify feed), /collections.json, /pages.json, shipping, refund and FAQ pages.

- **Platform:** full Shopify online store (Horizon theme, v4.1), not Buy Buttons on another site. Separate US store **diaperstoreusa.com** (USD, US stock); each site ships only in its own country. Currency picker shows CAD and USD.
- **Catalogue:** very large (about says "over 7,000 products"; sitemap has 9+ product files). Third-party brands (TENA, Attends, Fancy Feast, INABA, Catit...). Grouped by tags `group:baby/pet/family/home/seasonal`, `type:...`, `brand:...`; many SEO-written collection pages ("Adult Barrier Creams", "Pacifiers", "Winter essentials").
- **Sourcing:** every product in the first 250 of the feed is tagged `ships-via-amazon` and `amazon-x1000`, has item code `DS-<Amazon ASIN>`, a single Amazon-style image (e.g. `81-9MDALPoL.jpg`) and a short template description ("The size, count and colour are as named in the title"). So most items are Amazon.ca listings resold on Shopify and fulfilled through Amazon ("fulfillment carrier partner", arrives in the carrier's box). Adult/medical items ship from a separate supplier in plain boxes (Purolator/FedEx/Intelcom/Canada Post). Prices ~$9–$200, median ~$32, no compare-at prices.
- **Offer:** free shipping over $100, else $7; express $20. US: free over $49. 30-day returns (unopened), full refund for wrong/damaged. Phone line, FAQ, guides/blog, About video.
- **Apps seen:** Judge.me (reviews), Recharge (subscriptions), Shopify Markets (CAD/USD).

## What Health Camper should copy vs. not
Copy: full Shopify storefront with clear collections ("shelves"), free-shipping threshold banner, simple plain-language policies, FAQ, guides that link to products (our blog), reviews app later, CAD + USD markets, separate shipping rules per country.
Don't copy as-is: reselling Amazon listings with Amazon's photos and text. Risks: Amazon images/text are copyrighted by sellers/Amazon (our rule: never copy Amazon images); customers get Amazon-branded boxes and Amazon prices are visible for comparison; thin margins; returns go through us. For Health Camper the safer equivalent is: own-brand print-on-demand (Printful) + digital downloads sold in Shopify, and Amazon gear shown as an affiliate shelf (links out, no resale).
