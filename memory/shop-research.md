# Selling camping gear from healthcamper.com: options for a solo owner in Toronto (researched Nov 2026)

**Context:** static GitHub Pages site (plain HTML), solo non-developer owner, small budget, low effort. Tagline: "gear for calmer nights outdoors."

**Method note:** In this session, shopify.com and stripe.com could not be fetched directly (blocked by the network allowlist). All figures come from web-search snippets of official pages where possible, otherwise from third-party sources. Before relying on any price, check it on the vendor's live pricing page. Unverified or conflicting items are marked ⚠️.

## TL;DR recommendation

1. **Start with affiliate links (Amazon.ca Associates and MEC through AvantLink).** You hold no stock, have no shipping or returns, and carry no product-safety duties as a seller. It works on plain HTML today. Add a clear affiliate disclosure.
2. **If you want branded items (blanket, mug, eye mask, tee), add print-on-demand.** Use a Canadian fulfilment partner (Printful in Mississauga, or a Printify Canadian provider), sold through **Shopify Starter (~$7 CAD/mo) Buy Buttons** or **Stripe Payment Links (no monthly fee)**.
3. **Avoid holding stock of tents and sleeping bags at first.** Shipping bulky items, handling returns, and meeting tent flammability rules and bilingual textile labelling are the costly parts. Skip AliExpress dropshipping for safety-regulated categories such as tents, lanterns and fuel.

## Comparison table

| Option | Setup cost | Monthly | Per-sale fees (CAD unless noted) | Effort | Handles tax? | Works on static GH Pages? |
|---|---|---|---|---|---|---|
| **Affiliate (Amazon.ca / MEC)** | $0 | $0 | You *earn* ~3–4.5% (Amazon), ~6% (MEC) ⚠️ | Very low | N/A (not a sale of goods) | ✅ plain links |
| **Shopify Starter** | $0 (3-day trial; $1/mo promo for 3 months) | ~$7 CAD (≈$5 USD) | **5% + 30¢** online card rate | Low | ✅ Shopify Tax computes GST/HST/PST/QST (you still register yourself); possible 0.25% Shopify Tax fee, capped at $0.99/order on Starter ⚠️ | ✅ Buy Button embed or checkout links |
| **Shopify Basic** | $0 | $38/mo (annual) or ~$51/mo (monthly) | 2.8%–2.9% + 30¢ ⚠️ (+~1–1.5% international card, +1.5% currency conversion) | Low–medium | ✅ same as above | ✅ Buy Button, or use a Shopify-hosted store |
| **Stripe Payment Links** | $0 | $0 | 2.9% + C$0.30; +0.8% international cards; +2% FX | Low | Optional Stripe Tax: +0.5% per transaction where registered | ✅ paste a link or button |
| **Snipcart** | $0 (test mode free) | Min ~$20 USD/mo if sales < $1k USD ⚠️ | 2% + gateway (e.g. Stripe 2.9% + 30¢) | Medium (HTML attributes, some JS) | Partial (tax rules config/integration) | ✅ designed for static sites |
| **Gumroad** | $0 | $0 | 10% + $0.50 USD (+ processing); 30% via Discover | Low | MoR "where obligated" (digital-centric) | ✅ link/overlay |
| **Lemon Squeezy** | $0 | $0 | 5% + 50¢ USD | Low | MoR for digital | ❌ for physical goods (see below) |
| **POD (Printful/Printify)** | $0 | $0 (optional paid tiers) | Base product cost + shipping; you set margin | Low | Via the store you connect | Needs Shopify/Stripe/etc. in front |
| **Own stock** | Inventory $$$ | $0 shipping account | Postage + packaging + returns | High | Via checkout tool | ✅ with any of the above |

## 1. Shopify

- **Starter:** $5 USD/mo ([shopify.com/starter](https://www.shopify.com/starter)). The Canadian pricing page snippet shows **$7 CAD/mo** with "$1/month for first 3 months" ([shopify.com/ca/pricing](https://www.shopify.com/ca/pricing)). Starter is designed for selling "through social media, email, SMS, WhatsApp, and anywhere else you might want to share a link." Its transaction rate is **5% when using Shopify Payments** ([shopify.com/starter](https://www.shopify.com/starter)). Starter has no full online-store theme.
- **Buy Button:** the Shopify Help Center says the Buy Button sales channel is included in all plans and can be placed on a non-Shopify website or blog using generated HTML/JS embed code ([help.shopify.com/manual/sell-online/buy-button](https://help.shopify.com/manual/sell-online/buy-button)). This works on a plain-HTML GitHub Pages site because it is client-side JS. Styling options are limited ([community thread](https://community.shopify.com/t/shopify-starter-plan-buy-buttons-and-collaborators/280200)).
- **Basic:** $38 CAD/mo billed yearly, about $51 CAD month-to-month. Online card rate is "starting at 2.8% + 30¢ CAD" per the shopify.ca pricing snippet; some third-party sites still say 2.9% ⚠️ ([shopify.ca/pricing](https://shopify.ca/pricing), [salaccounting.ca](https://salaccounting.ca/blog/shopify-pricing-canada/)). Using a third-party gateway adds about 2% ([bsscommerce](https://bsscommerce.com/shopify/shopify-pricing-canada/)). International-card and FX surcharges are reported at about 1–1.5% each (third-party sources, conflicting ⚠️) ([easysellapp](https://easysellapp.com/blogs/wiki/shopify-currency-conversion-fees-changed-april-2026)).
- **Payouts (Canada):** paid out on a 3-day pay period ([help.shopify.com](https://help.shopify.com/en/manual/payments/shopify-payments/supported-countries/canada/accepting-payments)).
- **Tax:** Shopify Tax calculates GST/HST/PST/QST/RST by destination province ([changelog](https://changelog.shopify.com/posts/shopify-tax-has-expanded-to-canada), [help: Shopify Tax Canada](https://help.shopify.com/en/manual/taxes/shopify-tax/shopify-tax-canada)). **It does not register or file for you** ([taxcloud](https://taxcloud.com/blog/shopify-canada-sales-tax-setup/)). Help Center snippet: a 0.25% fee on Canadian orders calculated with Shopify Tax, capped at $0.99 CAD/order for Starter ⚠️ (check whether a free threshold applies).

## 2. Stripe Payment Links

- **Fees:** 2.9% + C$0.30 for domestic cards; +0.8% for international cards; +2% if currency conversion is needed. No setup or monthly fee ([stripe.com/en-ca/pricing](https://www.stripe.com/en-ca/pricing), [Stripe Oct 2023 update](https://support.stripe.com/questions/October-2023-pricing-updates-for-global-sticker-pricing-users)).
- **Stripe Tax:** 0.5% of volume for no-code integrations (Payment Links/Checkout), charged only in jurisdictions where you are registered ([support.stripe.com](https://support.stripe.com/questions/understanding-stripe-tax-pay-as-you-go-pricing)). A reported $2.50 per-transaction cap is unverified ⚠️.
- **Shipping:** Payment Links can require a billing+shipping address, restrict allowed countries (e.g. Canada only), and offer one or more fixed shipping rates ([docs.stripe.com/payment-links/customize](https://docs.stripe.com/payment-links/customize)). There is no cart: each link is one product, or a fixed bundle. Inventory tracking is minimal.

## 3. Snipcart

2% per transaction plus gateway fees, with a minimum monthly fee when sales are low. Recent sources say **$20 USD/mo if under $1,000 USD sales/mo**; older sources say $10 ⚠️ ([toolradar](https://toolradar.com/tools/snipcart/pricing), [Snipcart blog](https://snipcart.com/blog/stripe-checkout-form-integration-vs-snipcart)). Snipcart was built for static sites, but you configure it by adding HTML attributes and a script, which is more fiddly than Buy Buttons.

## 4. Gumroad / Lemon Squeezy

- **Gumroad:** 10% + $0.50 USD on direct sales, 30% on Discover sales. It acts as merchant of record "where it has tax obligations" since Jan 1 2025 ([gumroad.com/pricing](https://gumroad.com/pricing), [checkoutpage](https://checkoutpage.com/blog/gumroad-fees)). Sources conflict on physical-goods support ⚠️. It was built for digital goods: expensive and awkward for tents.
- **Lemon Squeezy:** 5% + 50¢ USD. It is digital-focused, and a competitor states physical products are not allowed; conflicting third-party claims exist ⚠️ ([payhip](https://payhip.com/blog/?p=5070), [flaviocopes](https://flaviocopes.com/payment-providers/lemon-squeezy-vs-gumroad/)). **Neither is a good fit for physical camping gear.**

## 5. Affiliate programs

- **Amazon.ca Associates:** the official Canadian fee table snippet lists "Furniture, Home, Home Improvement, Lawn & Garden, Outdoors, Pets" at **4.50%** ([associates.amazon.ca](https://associates.amazon.ca/help/node/topic/G4ARBJC7Z2NK48CA)). 2026 third-party guides cite **3%** for Home/Sports/Outdoors ⚠️, so check Associates Central ([getlasso](https://getlasso.co/amazon-affiliate-commission-rate/)).
- **3-sales rule:** you have **180 days to refer 3 qualifying sales** or the application is withdrawn, and rejected IDs can't be reinstated ([associates.amazon.ca – dormancy/application](https://associates.amazon.ca/help/node/topic/G7MJTPEP9NC3YKMG)). Your own purchases don't count.
- **Cookie:** 24 hours. Items added to the cart in that window still count if bought within ~89–90 days ⚠️ (secondary sources).
- **MEC:** runs an affiliate program through **AvantLink** ([mec.ca affiliate page](https://www.mec.ca/fr/explore/mec-affiliate-program)). Third parties list **~6% commission, 14-day cookie** ⚠️ ([getlasso](https://getlasso.co/affiliate/mec/), [affi.io](https://affi.io/m/mec-mountain-equipment-company-ltd)). I did not verify Sail, Sporting Life, or Canadian Tire programs.
- **Disclosure:** the Competition Act's deceptive-marketing provisions (ss. 52, 74.01) apply. The Bureau treats any compensation as a "material connection" that must be disclosed clearly ([McMillan](https://mcmillan.ca/insights/under-the-influence-the-canadian-competition-bureaus-stand-on-misleading-product-endorsements/)). Ad Standards' guidelines (updated Oct 2025) state that affiliate links trigger disclosure ([Ad Standards PDF](https://adstandards.ca/wp-content/uploads/Ad-Standards-Influencer-Marketing-Disclosure-Guidelines-2025-10-08.pdf)). Put a plain-language note next to the links, e.g. "We earn a commission if you buy through these links," and not only in the footer. Amazon also requires its own "As an Amazon Associate I earn from qualifying purchases" statement.

## 6. Dropshipping and print-on-demand

- **Printful** has a facility at **3500 Laird Rd, Mississauga, ON**. Most apparel ships from it in 2–5 business days, with no cross-border duties for Canadian orders ([help.printful.com](https://help.printful.com/hc/en-us/articles/360014067239), [printful.com/ca/print-on-demand-canada](https://www.printful.com/ca/print-on-demand-canada)). Mugs and blankets may route from US or other facilities. Printful's own marketing claims Canadian sublimation for mugs and blankets, which I did not independently confirm ⚠️.
- **Printify:** you can manually choose Canadian print providers. Catalogue includes mugs and blankets ([printify.com/print-on-demand/canada](https://printify.com/print-on-demand/canada)).
- **POD connects natively to Shopify.** With Stripe Payment Links you would forward orders to Printful/Printify manually.
- **AliExpress downsides:** delivery takes 7–45 days, quality is inconsistent, and photos can be misleading ([Shopify community](https://community.shopify.com/t/is-dropshipping-with-aliexpress-still-profitable-despite-long-shipping-times/190892)). Canada's low-value import threshold for postal and non-US courier parcels is about **CAD $20**. Above that, GST/HST and duties can surprise your customer. US/Mexico courier parcels get $150 duty / $40 tax thresholds under CUSMA ([CBSA CN20-18](https://cbsa-asfc.gc.ca/publications/cn-ad/cn20-18-eng.html)). As the Canadian seller, you take on CCPSA and labelling duties for goods you never inspected.

## 7. Holding your own stock

- **Canada Post Solutions for Small Business** is a free membership. **Through Dec 31 2026, all members get the program's top-tier discounts**, normally for high-volume shippers ([Canada Post](https://www.canadapost-postescanada.ca/cpc/en/small-business/marketing/campaign/unified-pricing.page), [discounts page](https://www.canadapost-postescanada.ca/cpc/en/small-business/shipping-discounts.page)). Domestic Expedited Parcel discounts run up to ~31–38% ⚠️; the tier and lane mapping is unclear.
- **Stallion Express:** a Toronto-area discount shipper whose domestic service starts at ~$6 for a 1 lb local parcel (marketing figure) ([stallionexpress.ca](https://stallionexpress.ca/blog/stallion-domestic-shipping/)). I could not verify whether it charges a monthly fee.

## Shipping reality for bulky items

Canada Post bills the greater of actual weight and volumetric weight: L×W×H cm ÷ **6,000** for Regular Parcel, **÷5,000** for Xpresspost/Expedited ([Canada Post cubing](https://www.canadapost-postescanada.ca/blogs/business/ecommerce/understanding-cubing-how-to-avoid-unexpected-shipping-fees/)). A boxed sleeping bag of 40×30×30 cm bills as about 6 kg at Regular rates even if it weighs 1.5 kg. Parcels are "oversized" if any side is over 1 m or the second-longest side is over 76 cm, which adds a $21–30 surcharge. A fuel surcharge also applies. My rough estimate, not verified ⚠️: shipping a tent or sleeping bag from Toronto would cost about $15–25 within Ontario and $30–50+ to BC or the Maritimes. That is a large share of the margin on a $100 item. Get real quotes from the Canada Post calculator before pricing.

## Tax (GST/HST/QST)

- **Small supplier:** you don't have to register until worldwide taxable sales **exceed $30,000 in a single calendar quarter or over four consecutive quarters**. In the single-quarter case, you charge tax on the sale that crosses the line and register within 29 days ([CRA](https://www.canada.ca/en/revenue-agency/services/tax/businesses/topics/gst-hst-businesses/when-register-charge)). Voluntary registration lets you claim input tax credits.
- **Once registered,** you charge tax based on the **destination province**: 13% HST in Ontario; 15% in NS, NB, NL and PEI; 5% GST elsewhere. The 13% Ontario rate is from general knowledge, as no CRA page appeared in results. BC, SK and MB PST registration may be needed for out-of-province sellers once their own thresholds are hit, which I did not verify ⚠️.
- **Quebec:** sellers outside Quebec must register for QST under the **specified system** once taxable sales to Quebec consumers exceed **$30,000**. The measurement period is described inconsistently ([Baker Tilly](https://www.bakertilly.ca/insights/new-qst-registration-requirements-for-non-resident-suppliers)). You can avoid Quebec early by shipping only to selected provinces. French-language requirements under Bill 96 also apply to selling into Quebec (not researched in depth ⚠️).
- **Affiliate income** is a commission for a referral service, not a sale of goods. You don't charge HST to customers, but the commissions are business income on form T2125. Commissions from a non-resident payer may be zero-rated, and those still count toward the $30k threshold. Confirm with an accountant ⚠️.
- **Business Number (BN):** you get one automatically when registering for GST/HST, or if you need an import/export (RM) account to import inventory commercially. A sole proprietor otherwise files under their SIN.

## Returns (Ontario Consumer Protection Act, 2002)

There is **no general legal right to return** an online purchase in Ontario; returns follow your stated policy. For internet agreements over $50, though, you must:

- **Disclose clearly before purchase:** your business name, address and contact details; a description of the goods; the itemized price, shipping, taxes and total in CAD; delivery date; and your cancellation, return, exchange and refund policies.
- Give an **express opportunity to accept or decline and to correct errors** before the purchase is placed.
- **Send a copy of the agreement within 15 days**; an email order confirmation with all the above qualifies.

If disclosure is missing, the consumer can cancel **up to 7 days after receiving the copy**. If no copy is delivered, they can cancel **within 30 days** ([Mann Lawyers](https://www.mannlawyers.com/resources/internet-agreements-with-ontario-consumers-consumer-protection-act-considerations-for-businesses/), [CLEO](https://www.cleo.on.ca/en/publications/otmshop/all), [ontario.ca CPA](https://www.ontario.ca/laws/statute/02c30)). ⚠️ Ontario's **Consumer Protection Act, 2023** received assent in Dec 2023 but awaited proclamation as of the latest source found (Dec 2024). I could not confirm whether it is in force in Nov 2026.

## Privacy (PIPEDA)

Collecting names, addresses and emails is commercial activity, so PIPEDA applies even to a sole proprietor ([OPC for businesses](https://priv.gc.ca/en/for-businesses), [OPC small-business notes](https://www.priv.gc.ca/en/privacy-topics/privacy-laws-in-canada/the-personal-information-protection-and-electronic-documents-act-pipeda/pipeda-compliance-help/pipeda-compliance-and-training-tools/bus_notes/)). The site's privacy policy should add:

- **What is collected:** name, shipping and billing address, email, phone, and order history.
- **Why** it is collected: fulfilment, receipts, support, and tax records.
- **Who processes it:** Shopify/Stripe/Printful, possibly outside Canada (e.g. the US).
- **Retention:** e.g. 6 years for CRA records.
- **Marketing:** only with separate opt-in consent; CASL also applies to marketing emails.
- **Rights:** how to request access or correction (respond within ~30 days).
- **Contact:** the name of a privacy contact.
- **Affiliate tracking:** affiliate links set third-party cookies (Amazon, AvantLink).
- **Breaches:** keep a breach log and report breaches posing a "real risk of significant harm" to the OPC and affected people.

## Product safety and liability

- **CCPSA:** applies to manufacturers, importers, sellers and advertisers, including online. Sellers must **report a serious incident to Health Canada and to their supplier within 2 days** of becoming aware. Manufacturers and **importers** must also file a written report within **10 days**. Sellers must keep records of their supplier and of where and when they sold each product ([Health Canada s.14 overview](https://www.canada.ca/en/health-canada/services/consumer-product-safety/legislation-guidelines/acts-regulations/canada-consumer-product-safety-act/industry/overview-mandatory-reporting-section-14.html), [Bennett Jones](https://www.bennettjones.com/Insights/Updates/The-Canada-Consumer-Product-Safety-Act-New-Obligations-for-Manufacturers-Importers-and-Sellers-of-Consumer-Products)). If you import or dropship from abroad, **you are the importer**.
- **Tents:** the **Tents Regulations (SOR/2024-217)** incorporate **CAN/CGSB-182.1-2020**, *Flammability and Labelling Requirements for Tents* (the standard is 182.1, not 82.1). Tents need **mandatory bilingual labelling** ([SGS](https://sgs.com/news/2024/12/safeguards-16724-health-canada-publishes-new-tents-regulations-under-the-ccpsa), [Health Canada tents guide](https://www.canada.ca/en/health-canada/services/consumer-product-safety/reports-publications/industry-professionals/industry-guide-canadian-requirements-tents.html)). Buy only from suppliers who can show compliance.
- **Textiles** (blankets, sleeping bags, pillows, eye masks): the Textile Labelling Act requires fibre content in **English and French**. Filled articles must disclose shell and filling fibres separately. Labels also need the dealer identity, as a CA number or name and address ([Competition Bureau](https://competition-bureau.canada.ca/en/labelling/textile-labelling/labelling-textile-requirements-nutshell), [stuffed articles guide](https://competition-bureau.canada.ca/en/node/469)). Quebec's stuffing permit regime was **repealed in 2021** ([Quebec economy ministry](https://www.economie.gouv.qc.ca/en/outside-quebec/quebec-statute-on-stuffing-and-upholstered-and-stuffed-articles)).
- **Bilingual packaging:** the Consumer Packaging and Labelling Act generally requires product identity and net quantity in both official languages on prepackaged consumer goods (from general knowledge; not re-verified ⚠️).
- **Candles, fuel and lanterns:** candles are covered by the **Candles Regulations (SOR/2016-168)**, which set rules on flame height, self-extinguishing and bilingual warnings (not re-verified ⚠️). Fuel canisters, fuel tablets and matches are **dangerous goods**: Canada Post restricts them, and couriers require DG training ([Canada Post DG](https://www.canadapost-postescanada.ca/cpc/en/support/articles/non-mailable-matter/transportation-of-dangerous-goods-classes-and-index.page)). **Sell battery/LED lanterns only, not fuel or candles.** Lithium batteries also carry shipping rules.
- **Insurance:** product liability insurance isn't legally required. Brokers quote small online sellers about **$350–$900/yr for $1M general liability**, with ranges up to $500–$5,000 depending on products and US sales ([Zensurance](https://www.zensurance.com/blog/what-online-sellers-and-retailers-should-know-about-product-liability-insurance), [HelloSafe](https://hellosafe.ca/en/business-insurance/e-commerce)). Tents, stoves and heat sources push premiums up.

## Business basics

- **Sole proprietorship:** no incorporation is needed.
- **Registering "Health Camper" in Ontario:** this is required if trading under a name other than your own legal name. It costs **$60 online** through the Ontario Business Registry and is valid 5 years; renewal costs the same ([ontario.ca fees](https://ontario.ca/page/cost-time-required-to-register-change-search-for-business-name-corporation-not-for-profit)). An optional name search costs about $8–26. Name registration is not trademark protection.
- **Business Number:** obtained with GST/HST registration, or when you need an import account. Income goes on your personal return via form T2125.

## Could not verify / flagged

- **Vendor pages:** live Shopify and Stripe pricing pages could not be fetched (network allowlist), so numbers come from search snippets.
- **Shopify:** whether Basic's online rate is 2.8% or 2.9%; Shopify Tax fee details in Canada; exact international and FX surcharges.
- **Amazon.ca:** the current Outdoors/Home commission (4.5% official snippet vs 3% in 2026 blogs).
- **Affiliates:** MEC's commission and cookie window; Sail and other Canadian retailer programs.
- **Snipcart:** the current minimum fee.
- **Gumroad and Lemon Squeezy:** whether they support physical products.
- **Ontario CPA 2023:** whether it is in force.
- **Provincial PST:** registration thresholds for BC, SK and MB.
- **Shipping:** actual parcel rates for bulky items (the estimate above is mine) and whether Stallion has a monthly fee.
- **Regulations:** current text of the Candles Regulations and CPLA details.
