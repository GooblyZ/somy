# Unit-economics verification for a small Israeli Shopify store (research date 2026-11-11)

Labels: **FACT** = read directly in this session on a primary system/page (URL given). **REPORTED** = secondary source (press, vendor, accountant blog). **ESTIMATE / ASSUMPTION** = my inference or a planning value, not data. **UNVERIFIED** = could not be confirmed.

Access disclosure (what could and could not be read):
- gov.il and kolzchut.org.il: blocked by a Cloudflare bot check, also with headless Chromium. taxes.gov.il returned 502. **No gov.il page was read.**
- The Israel Tax Authority's online customs tariff ("shaarolami", customs.mof.gov.il) **was readable** and is the primary source for the $75 item and for all duty rates below.
- Bank of Israel public API: readable (primary).
- CJ Dropshipping shipping calculator: blocked (Cloudflare "are you a robot" page; the developer API requires an account token). **No CJ rate was obtained.** YunExpress, 4PX, Cainiao, SF: no public Israel rate card found.
- PayPlus, Tranzila, Cardcom: their sites publish no price list (pricing pages 404 / quote-only). Grow, PayPal Israel and Shopify price pages were read.
- Israeli courier and 3PL rate cards: not published; only "from" prices on vendor pages.

---

## 1. China -> Israel shipping by weight; air freight and brokerage for a small commercial shipment

### Takeaway
The only live calculator I could query (KakoBuy, a China shopping-agent, 12 Nov 2026 Beijing time) prices the cheapest tracked postal line to Israel at about $8.6 / $12.0 / $15.4 / $24.0 / $41.1 for 100 g / 300 g / 500 g / 1 kg / 2 kg (27 / 38 / 49 / 76 / 130 ILS), 15-20 days, with battery lines 8-45% dearer. These are agent retail prices and should be read as an upper bound; CJ's own rates remain unverified and must be pulled from a logged-in CJ account per SKU.

### Cited Findings
- **FACT** (calculator output, queried 2026-11-11 UTC, destination "IL - Israel", no dimensions entered) - [KakoBuy shipping fee estimation](https://www.kakobuy.com/) (menu: Estimate):

| Line (as named by the calculator) | 100 g | 300 g | 500 g | 1 kg | 2 kg | Transit |
|---|---|---|---|---|---|---|
| EUB / ePacket, China Post (no batteries, no perfume) | $8.55 | $11.98 | $15.41 | $23.98 | $41.13 | 15-20 days |
| EUB with built-in battery | $9.23 | $14.69 | $20.14 | $33.78 | $61.07 | 15-20 days |
| Israel self-pickup locker line (no batteries) | $16.08 | $16.08 | $16.08 | $26.80 | $48.24 | 10-25 days |
| Israel Line-F | $17.06 | $17.06 | $17.06 | $27.78 | $49.21 | 10-25 days |
| Israel dedicated line (batteries and perfume permitted) | $19.01 | $19.01 | $19.01 | $32.65 | $59.93 | 10-25 days |
| E-EMS | $29.87 | $33.69 | $37.51 | $47.06 | $66.15 | 5-20 days |
| FedEx | $34.82 | $34.82 | $34.82 | $48.47 | $75.75 | 8-15 days |
| GD-EMS | $51.32 | $51.32 | $51.32 | $78.61 | $133.17 | 4-13 days |

- **FACT** (same calculator): volumetric rules shown - FedEx line "volume/5000", billable weight = greater of actual and volumetric; E-EMS: if any side <= 60 cm charged on actual weight, otherwise greater of actual and L x W x H / 6000; postal EUB lines state prohibited: flammable, explosive, liquids - [KakoBuy](https://www.kakobuy.com/)
- **REPORTED**: a tracking site lists a fixed-band China->Israel service at CNY 99 (~$14.5) up to 500 g and CNY 149 (~$21.8) up to 1 kg, ~8 days average; carrier not named - [Ship24](https://ship24.com/ship-from-china/israel) (page returned 404 when I opened it directly; figure is from the search snippet only)
- **REPORTED** (from round 1, not re-verified): YunExpress bills the greater of actual and volumetric weight - [YunExpress](https://www.yunexpress.com/our-solutions/b2c/standard-express); CJ to Israel 7-20 days per Israeli blogs - [Aviv Malka](https://aviv-malka.com/dropshipping-complete-guide-israel/)
- **REPORTED** (forwarder marketing, Oct 2026, from round 1): air freight China->Israel ~$5.3/kg, express ~$13.3/kg, LCL ~$80/CBM - [DTFU Logistics](https://www.dtfulogistics.com/news/shipping-cost-from-china-to-israel/). A second forwarder-type source gives express $9-12/kg for 0.5-20 kg parcels (search summary; page not opened) - [Basenton](https://www.basenton.com/how-much-does-it-cost-to-ship-from-china-to-israel/)
- **FACT** (courier price list page; commercial section dated 27.10.2021, so old): commercial import release fee by shipment value: $35-100: 90 ILS; $101-499: 150 ILS; $500-999: 250 ILS; $1,000+: 399 ILS (ex VAT); physical inspection 150 ILS; handling of legality documents 350 ILS; computer fee 20.5 ILS ($100-1,000) or 42 ILS ($1,000+); security fee 48.5 ILS above $500. Personal import (dated 24.12.2025): release 99.90 ILS for $75-500, 199.90 ILS for $501-1,000 - [GCX price list](https://gcx.co.il/he/מחירון/)
- **REPORTED** (forwarder blog, 2026): customs-broker fee 250-450 ILS regular release, ~550 ILS fast, ~850 ILS urgent; small commercial cargo up to 5 kg 250-400 ILS; customs paperwork 60-90 ILS; for LCL/FCL brokers often charge a % of goods value with a minimum per declaration (550-1,500 ILS for a container) - [Gindi customs brokerage fees](https://www.gindi-smart.com/customs-brokerage-fees/)
- **FACT** (Tax Authority tariff, legal-requirements table for heading 85.09): mains-powered or charger-bundled household electro-mechanical appliances require a standards release for commercial import under the Free Import Order (Israeli standard SI 900: test-lab conditional release, Ministry of Economy declaration route, or Standards Institute approval); the same rows are marked "does not apply to personal import" - [Customs tariff item 8509809000](https://shaarolami-query.customs.mof.gov.il/CustomspilotWeb/he/CustomsBook/Import/ImportCustomsItemDetails?customsItemId=3188)

### Inferences
- ESTIMATE: the KakoBuy EUB price fits "$6.84 + $17.15 per kg" exactly at 100 g, 300 g, 1 kg and 2 kg. Agent lines include a retail markup, so a dropship agent (CJ etc.) is likely cheaper, but by how much is UNVERIFIED. Planning range for Model A international freight, in ILS at 3.17: 100 g 20-30; 300 g 28-40; 500 g 35-50; 1 kg 55-80; 2 kg 95-135; add ~10-45% for battery items. The lower ends are assumptions, the upper ends are the calculator values.
- ESTIMATE: for small light items the "dedicated Israel lines" have a 500 g minimum charge (~$16-19), so sub-300 g products should go by postal ePacket-type lines; above ~1 kg freight alone (76-130 ILS) makes Model A unworkable under ~299 ILS retail.
- ESTIMATE, small commercial air shipment of 50-100 kg (2-5 cartons): freight $5-13/kg => roughly $250-1,300 (800-4,100 ILS); broker + computer/security + terminal/handling roughly 600-1,500 ILS per consignment; standards approval only if the product is under an official standard. Per unit for a 300 g item (about 165-330 units in the consignment): roughly 5-17 ILS per unit freight plus 2-9 ILS per unit clearance. All of this must be replaced by one written door-to-door quote.

### Gaps
- No CJPacket, YunExpress, 4PX, Cainiao or SF rate for Israel. Partners must open the CJ product page for each candidate SKU and record the Israel line options (price, days, battery allowed).
- No 2026 Israeli air-terminal (Maman/Swissport) handling tariff, no Standards Institute test fee, no door-to-door LCL quote. Ask a forwarder for an all-in DAP/DDP quote for a named carton count and weight.
- No loss/damage rate data for any line.

---

## 2. Israeli domestic delivery, 3PL, return shipping liability, return rates

### Takeaway
No carrier publishes a business rate card; public "from" prices put home delivery at 22-38 ILS per parcel depending on monthly volume and a point-to-point locker parcel at 22 ILS. On a change-of-mind cancellation the statute makes the consumer return the goods to the seller's place of business and caps the seller's deduction at 5% or 100 ILS (the lower), and that cap explicitly covers shipping and packaging costs, so the seller cannot charge back the original delivery beyond that cap.

### Cited Findings
- **REPORTED** (courier-broker marketing page, undated, VAT status not stated): business delivery "from" prices by monthly volume: up to 100 parcels from 35 ILS; up to 200 from 30 ILS; up to 500 from 25 ILS; over 500 from 22 ILS - [Outside the Box](https://outside-the-box.co.il/משלוחים-לעסקים-קטנים/)
- **REPORTED** (vendor blog, 28 Jul 2026, VAT status not stated): standard route delivery from 38 ILS (3-5 business days), next-day 45 ILS, same-day 48 ILS+; a return costs about the same as a delivery; cash on delivery is offered; no COD fee or share given - [D2D](https://www.d2d.co.il/blog/ecommerce-delivery-israel)
- **REPORTED** (search summary of Boxit's own page; date unknown): Box2Box locker-to-locker parcel 22 ILS, no minimum volume or commitment, marketed to small e-commerce stores - [Boxit Box2Box](https://boxit.co.il/box2box/)
- **REPORTED** (third-party tariff blog; page body could not be loaded, figures from search summary): Israel Post 2026: door-to-door courier for a casual customer 69.50 ILS, counter-to-counter parcel from 29 ILS, next-day from 45 ILS; business subscribers pay less with volume - [PickPackage](https://pickpackage.com/he/תעריפי-דואר-ישראל-חבילות-ומשלוחים-2026/)
- **REPORTED**: consumer-facing pickup-point/locker charges on merchant sites are typically ~20 ILS, often free above 199-300 ILS (older listings) - [Boxit search results incl. merchant pages](https://boxit.co.il/box2box/)
- **REPORTED** (3PL vendor guide): Israeli fulfilment pricing is built from monthly storage (per volume, pallet or bin), a per-order pick-and-pack fee and last-mile delivery; some providers require 100-200 orders per month minimum; no prices published - [HSP](http://h-s-p.co.il/ecommerce-shipping-deliveries/fulfillment-services-israel/)
- **FACT** (statute text read on Hebrew Wikisource, not on an official site): Consumer Protection Law s.14E(b): on a cancellation that is not due to defect/non-conformity/late supply, the seller refunds within 14 days of the cancellation notice and may keep cancellation fees of no more than 5% of the price or 100 ILS, whichever is lower; if the consumer received the goods "he shall return them to the dealer at the dealer's place of business". s.14E(a): on cancellation for defect, non-conformity, late or non-supply, no fee at all, and the consumer "shall place the goods at the dealer's disposal at the place where they were delivered to him" (i.e. the seller collects). s.14E(d): "cancellation fees" include expenses or commitments for shipping and packaging - [Consumer Protection Law, Wikisource](https://he.wikisource.org/wiki/חוק_הגנת_הצרכן)
- **FACT** (same source): distance-sale exclusions in s.14C(d): perishables; lodging/travel/leisure services within 7 days of the service date; information (software/data); goods made specially for the consumer; recordable/copyable goods whose original packaging was opened - [Wikisource](https://he.wikisource.org/wiki/חוק_הגנת_הצרכן)
- **REPORTED** (from round 1; no newer data found): Israeli online return rate ~10-15% (2019, unsourced) - [Hon.co.il](https://www.hon.co.il/איך-מחזירים-מוצרים-בקנייה-באינטרנט/)

### Inferences
- ESTIMATE: under s.14E(b)+(d) a regret return leaves the seller with: refund of the full price minus at most min(5%, 100 ILS); the outbound delivery cost is sunk (it is inside the 5% cap); the customer bears the cost of getting the item back to the seller. For Model A the "place of business" cannot practically be China, so the seller needs an Israeli return address and the unit is usually unsellable or uneconomic to restock. This is my reading of the text, not a legal opinion.
- ESTIMATE: for the model use D = 30 ILS ex VAT per home delivery at under 200 parcels/month (range 22-38), ~20-22 ILS for locker/pickup point, and the same again for a seller-paid return leg.
- ASSUMPTION: return/refund rate 5% (range 3-8%) for non-apparel gadgets; 15-30% apparel. No current Israeli data supports these.

### Gaps
- No rate card from Israel Post (business e-commerce contract), HFD, Cheetah, Mahir Li, Yango Delivery, Lionwheel, Baldar or GetPackage. All are quote-based; partners must request quotes stating monthly volume, weight band, home vs pickup point, COD fee and return fee.
- No Israeli 3PL price (storage per pallet/bin, pick & pack per order, receiving). Must be quoted.
- COD share of Israeli online orders: no data found.
- The statute was read on Wikisource, not on Nevo/gov.il; confirm wording with a lawyer before writing the store's cancellation policy.

---

## 3. Payment costs (gateways, PayPal, Shopify third-party fee, installments)

### Takeaway
On Shopify Basic the verified all-in card cost with Grow is 2.75-3.6% of the VAT-inclusive order value plus 29-69 ILS per month: Shopify's 2% third-party fee is the largest part. PayPal Israel costs 3.4% + 1.20 ILS. Paying the merchant upfront for a 3-instalment sale costs a further ~0.9%, and 12 instalments ~4.8%.

### Cited Findings
- **FACT** (Shopify Israel pricing page, read 2026-11-11): Basic US$39/month (US$29 if paid yearly), third-party payment provider fee 2%; Grow US$105 (US$79 yearly), 1%; Advanced US$399 (US$299 yearly), 0.6%. The page does not say Shopify Payments is available in Israel - [Shopify IL pricing](https://www.shopify.com/il/pricing)
- **FACT** (Grow price page, prices exclude VAT): "Grow" plan 0.75% per transaction, 59 ILS/month on annual billing or 69 ILS monthly, 100 transactions and documents included, 0.5 ILS per extra; "Grow Light" plan 1% per transaction (0.5 ILS minimum), 29 ILS/month, 20 transactions included, 1 ILS per extra, plus surcharges: Shopify +0.6%, Wix +0.4%, 3DS +2.5 ILS per action, refund 6.90 ILS per action; tourist cards 3.5%; Diners 1.5%; incoming bank transfer 1 ILS. Bit, Apple Pay and Google Pay appear under the same per-transaction fee (no separate rate shown). Payout: funds available from the 1st of the following month - [Grow pricing](https://grow.business/pricing/)
- **FACT** (same page): instalment advance ("hakdama") fee = prime + 5.5% annualised, prime stated as 5% as of 9 Jul 2026; fee by number of instalments: 2: 0.438%; 3: 0.875%; 4: 1.313%; 6: 2.188%; 10: 3.938%; 12: 4.813%; plus a 29 ILS monthly management fee for the advance service - [Grow pricing](https://grow.business/pricing/)
- **FACT** (PayPal Israel merchant fees, page last updated 13 Oct 2026): commercial transactions 3.40% + 1.20 ILS (4.01% + 1.42 ILS including 18% VAT); international surcharge +1.0% (US/Canada/Europe) or +2.0%; currency conversion 2.5%; dispute fee 30 ILS (60 ILS high-volume) - [PayPal IL merchant fees](https://www.paypal.com/il/webapps/mpp/merchant-fees)
- **FACT** (iCount price page, ex VAT): invoicing plans from 32 ILS/month (up to 10 documents), 59 ILS (up to 100), 85 ILS (up to 200); credit-card clearing module 30 ILS/month with an iCount terminal or 20 ILS/month with another terminal; card-token storage 20 ILS/month; per-transaction clearing % is not on the page - [iCount pricing](https://www.icount.co.il/pricing/)
- **REPORTED** (from round 1, agency comparison Sep 2026): PayPlus 0.9-1.3% + 0-150 ILS/month; Cardcom ~1.2% + ~49 ILS/month; Tranzila 1.2-1.7% + 90-200 ILS/month - [Sitelink](https://sitelink.co.il/web/ecommerce/payment-solutions-for-businesses-israel-2026/)
- **REPORTED**: instalment "discount" fees are charged on the instalment spread and often do not appear explicitly in the acquiring agreement; foreign, premium and instalment transactions carry different rates - [Maariv](https://www.maariv.co.il/economy/consumerism/article-1334675)
- **REPORTED** (from round 1): from 1 May 2026 Bit charges recipients 0.8% above 25k ILS/year on person-to-person receipts - [Bizportal](https://www.bizportal.co.il/financialconsumerism/news/article/20040168)

### Inferences
- ESTIMATE: fee on a Shopify Basic order, as % of VAT-inclusive price P: Grow Light 1% + 0.6% + Shopify 2% = 3.6%; Grow 0.75% + Shopify 2% = 2.75% (the page lists the Shopify surcharge only for Grow Light). The model below uses 3.6%. Gateway fees carry 18% VAT that an osek murshe can deduct, so they are modelled ex VAT.
- ESTIMATE: regular interest-free instalments cost the merchant nothing extra if it waits for each instalment; the ~0.9-4.8% applies only if it wants the money upfront. With month-following payout (Grow) and ad spend paid daily, working capital of roughly one month of ad spend is needed.
- ESTIMATE: on Basic, moving to the Grow Shopify plan (extra ~US$66/month, about 209 ILS) saves 1% of sales, which pays off above roughly 21,000 ILS of monthly sales.

### Gaps
- PayPlus, Tranzila, Cardcom: no public prices. Get written quotes including Shopify plug-in fee, Bit surcharge, 3DS fee, refund fee, chargeback fee and payout timing.
- Whether Shopify's 2% is also charged on orders paid by Bit/PayPal through an external gateway was not checked beyond the pricing page.
- Chargeback fees for Israeli gateways not found.

---

## 4. Tax verification: VAT rate, $75 exemption, duty rates, VAT treatment of dropship sales, osek patur ceiling

### Takeaway
The $75 personal-import exemption is confirmed in the Tax Authority's live customs tariff (item 98.02, validity date 12/11/2026), and every consumer-goods tariff line I checked (307 lines across 29 headings) carries a 0% general customs duty and almost all carry no purchase tax; so for Model B the real import costs are freight, clearance and compliance, with 18% import VAT recoverable. The VAT treatment of a registered Israeli seller whose goods ship from China straight to an Israeli consumer is genuinely disputed among accountants and no Tax Authority ruling was found; the prudent base case is 18% output VAT on the full price.

### Cited Findings
- **FACT** (Tax Authority customs tariff, "discount codes / tariff" view, validity date shown 12/11/2026): item 98.02: "goods, including gift parcels and excluding tobacco products, alcohol and intoxicating beverages, packed in one or more packages and intended for personal use as defined in s.129 of the Customs Ordinance, provided that their transaction price does not exceed 75 US dollars". Item 98.03: same type of goods where the transaction price does not exceed 500 US dollars, excluding goods under 98.02. Item 98.04: parcels up to 30 kg gross / up to 1,000 dollars, not for trade - [Customs tariff, discount codes](https://shaarolami-query.customs.mof.gov.il/CustomspilotWeb/he/CustomsBook/Import/DiscountCodes)
- **FACT** (same system, framework order): "dollar" is the US dollar converted under the Customs Rules (calculation of a price stated in foreign currency), 1989; the "representative rate" is the one published by the Bank of Israel - [Customs tariff, framework order](https://shaarolami-query.customs.mof.gov.il/CustomspilotWeb/he/CustomsBook/Import/OrderFrame)
- **REPORTED**, history: raised to $150 on 24 Dec 2025; Knesset cancelled it 24 Feb 2026; sources conflict on an interim $130 step (Kol Zchut is reported to list $130 for 25 Feb-1 Jun 2026, while other reports say the Knesset also cancelled the $130 order and the threshold returned to $75) - [Kol Zchut](https://www.kolzchut.org.il/he/זכותון_בנושא_יבוא_אישי_(חבילות_מחו"ל)) (search summary only; page blocked); [Bizportal](https://www.bizportal.co.il/general/news/article/20024799); [Times of Israel](https://www.timesofisrael.com/knesset-revokes-measure-that-made-more-online-purchases-tax-exempt/). Whatever the path, the tariff in force today says $75.
- **REPORTED**: the exemption is tested on the value of the goods; shipping and insurance are not counted toward eligibility; two or more parcels from the same supplier to the same customer within 72 hours are treated as one; between $75 and ~$500 only 18% VAT applies - [Kol Zchut](https://www.kolzchut.org.il/he/זכותון_בנושא_יבוא_אישי_(חבילות_מחו"ל)) (search summary); [Protocol](https://protocol.co.il/personal-importation-taxes/). The tariff text itself says "transaction price" and does not spell out the treatment of shipping, so the shipping exclusion stays REPORTED.
- **REPORTED** (indirect corroboration of the VAT rate): PayPal's Israeli fee page, updated 13 Oct 2026, computes its fees "including 18% VAT" - [PayPal IL](https://www.paypal.com/il/webapps/mpp/merchant-fees). No gov.il VAT page could be opened.
- **FACT** (Tax Authority customs tariff, first schedule, queried 2026-11-11 with validity date 12/11/2026; "general" customs rate and purchase tax per 10-digit line; control check: passenger cars 87.03 correctly returned 7% customs and purchase tax, so the extraction does detect non-zero rates) - [Customs tariff search](https://shaarolami-query.customs.mof.gov.il/CustomspilotWeb/he/CustomsBook/Import/CustomsTaarifEntry):

| Category | Headings checked (number of lines) | General customs | Purchase tax |
|---|---|---|---|
| Small electrical appliances | 85.09 (5), 85.16 hair dryers, stylers, irons, kettles, heaters (24), 85.10 shavers/clippers (5), 84.14 fans/pumps (43) | Exempt on all lines | Exempt, except motor-vehicle-type lines in 84.14 (12%) |
| Beauty / cosmetic devices, massagers | 85.43 other electrical apparatus (28), 90.19 massage apparatus (5) | Exempt | Exempt, except e-cigarette lines (270%+), one vehicle-type "others" line 8543.7039 (12%) and underwater massage units over 100 cm (12%) |
| Cosmetics, perfume, manicure tools, brushes, combs | 33.04 (6), 33.03 (1), 82.14 (3), 96.03 (14), 96.15 (6) | Exempt | Exempt |
| Toys and games | 95.03 (1), 95.04 (5) | Exempt | Exempt |
| Textiles and apparel | 63.02 bed/bath linen (17), 61.09 T-shirts (4), 61.04 (22), 63.07 other made-ups incl. baby carriers (10), 94.04 pillows/duvets (6) | Exempt | Exempt |
| Footwear, bags, leather accessories | 64.02 (5), 64.04 (3), 42.02 (12), 42.03 (7) | Exempt | Exempt |
| Pet supplies | 42.01 collars, leashes, harnesses, pet coats (1) | Exempt | Exempt |
| Plastic and metal housewares | 39.24 (6), 39.26 (18), 73.23 (6), 96.17 vacuum flasks (1) | Exempt | Exempt, except vehicle-type lines in 39.26 (12%) |
| Lighting, flashlights, batteries/power banks | 94.05 (22), 85.13 (2), 85.07 (15) | Exempt | Exempt, except vehicle lamps (12%) and vehicle batteries (80 ILS each) |
| Imitation jewellery, sports goods | 71.17 (7), 95.06 (20) | Exempt | Exempt |

- **REPORTED**, VAT on dropship sales, the two positions:
  - Position 1 (out of scope): under s.14 of the VAT Law an asset is deemed sold in Israel only if it was in Israel when delivered to the buyer; where goods never enter Israel the sale is outside the VAT Law, no VAT file is needed and related input VAT is not deductible (s.41). The article's framing is goods that never pass through Israel - [CPA Amnon Ben-Shushan, 21 Jun 2024](https://www.bshcpa.co.il/דרופשיפינג/)
  - Position 2 (taxable): "a sale to a customer in Israel is subject to VAT even if the product is shipped from abroad"; sales to customers abroad are not - [Dray & Dray CPAs, 28 Dec 2024](https://cpa-dray.com/he/blog/דרופשיפינג/)
  - Older statement of the authorities' stance: when the store owner and the customer are both Israeli, "the position of the VAT authorities is that the transaction takes place in Israel and is therefore subject to VAT", yet at the time VAT offices were not opening files for dropshippers or were refusing input-VAT deduction; a published Tax Authority position was said to be pending - [The Bookkeepers CPAs, 28 Feb 2018](https://www.thebookkeepers.co.il/single-post/2018/02/28/סוגיות-מעמ-בעסקאות-דרופשיפינג-כשהלקוח-תושב-ישראל)
  - A Globes article in cooperation with the tax advisers' chamber says VAT offices check whether all transactions are dropshipping and if so do not allow a VAT file, so input VAT cannot be offset (search summary; article about eBay/Amazon export-type dropshipping) - [Globes](https://www.globes.co.il/news/article.aspx?did=1001171667)
- **REPORTED**: osek patur turnover ceiling for 2026 is 122,833 ILS per year (2025: 120,000 ILS); above it registration as osek murshe is mandatory - [Bizportal](https://www.bizportal.co.il/guides/news/article/20045314); [Green Invoice](https://www.greeninvoice.co.il/magazine/תקרת-עוסק-פטור/)
- **REPORTED** (from round 1): import VAT of 18% is charged on CIF value plus duty and purchase tax and is deductible as input tax by a registered business - [UnitedXP](https://www.unitedxp.co.il/?p=92398)

### Inferences
- ESTIMATE: at today's representative rate (3.172) $75 = 238 ILS of goods value (about 239 ILS with the +0.5% conversion margin reported in round 1). Any single dropshipped parcel with a supplier invoice above that triggers 18% VAT plus a ~100 ILS courier release fee charged to the customer - a deal-breaker. Bundles and multi-buys must be checked against the 72-hour aggregation rule.
- ESTIMATE, VAT base case for the model: the store is an Israeli business selling to Israeli consumers from an Israeli-facing site and issuing Israeli invoices. The goods ARE in Israel when handed to the buyer (they are delivered at the buyer's door), which is why the s.14 "never enters Israel" argument, written for eBay/Amazon sales to foreign buyers, is weak here. Model 18% output VAT on the full sale price (P x 18/118). In Model A there is no import VAT to reclaim (the consumer is the importer and the parcel is exempt), and input VAT on the foreign supplier's invoice does not exist; input VAT on Israeli costs (gateway, courier, accountant, Meta if invoiced with VAT) is deductible only if the Tax Authority accepts the sales as taxable transactions. Uncertainty: HIGH; this needs a written opinion from the partners' accountant, ideally a pre-ruling.
- ESTIMATE: an additional exposure in Model A that no source addressed: the personal-import exemption requires "personal use", while the parcels are in substance the store's commercial supply chain. Whether customs could treat a pattern of such parcels as commercial import is UNVERIFIED.
- ESTIMATE: the osek patur route (no VAT on sales, 122,833 ILS/year ceiling, about 10,200 ILS/month) is only a test-phase option and usually not available to a company or to a business that will clearly exceed the ceiling; three partners trading through one entity would cross it at ~70-100 orders/month.
- ESTIMATE: since duty and purchase tax are zero on the checked lines, Model B landed cost = FOB + freight + clearance + compliance; import VAT is a cash-flow item only.

### Gaps
- No gov.il / Tax Authority guidance page, VAT order or Knesset record was opened (blocked). The legal instrument that grants the VAT exemption alongside tariff item 98.02, and the official wording on shipping costs and the 72-hour rule, are therefore not primary-verified.
- No Tax Authority circular, ruling or court decision on VAT for an Israeli seller dropshipping to Israeli consumers was found. Treat every statement on this as accountant opinion.
- The exact 10-digit classification of any specific product must be confirmed by a customs broker; "others" lines at 12% purchase tax exist next to exempt lines (vehicle-type goods).
- Osek patur ceiling not confirmed on a Tax Authority page.

---

## 5. USD/ILS exchange rate

### Takeaway
The Bank of Israel representative rate was 3.172 ILS per USD on 11 Nov 2026; October 2026 averaged 3.088 (range 3.053-3.128) and 2-11 November averaged 3.164, so the shekel has weakened about 4% since early October.

### Cited Findings
- **FACT**: representative USD rate 3.172, last update 2026-11-11 - [Bank of Israel public API](https://boi.org.il/PublicApi/GetExchangeRates?asXml=false)
- **FACT**: daily series Oct-Nov 2026: 1 Oct 3.080; low 6 Oct 3.053; 15 Oct 3.103; 30 Oct 3.118; 2 Nov 3.136; 3-4 Nov 3.157; 6 Nov 3.194 (high); 9 Nov 3.171; 10 Nov 3.161; 11 Nov 3.172 - [Bank of Israel SDMX series RER_USD_ILS](https://edge.boi.gov.il/FusionEdgeServer/sdmx/v2/data/dataflow/BOI.STATISTICS/EXR/1.0/RER_USD_ILS?startperiod=2026-10-01&endperiod=2026-11-11&format=csv)
- **REPORTED**: a third-party index listed 2.811 on 29 May 2026 and 2.907 on 7 May 2026 - [Cbonds](https://cbonds.com.ua/indexes/183631/)

### Inferences
- ESTIMATE: use 3.17 in the model and stress at 3.0 and 3.4. If the May figure is right the dollar has risen ~13% in under six months, which raises every USD-denominated cost (product, freight, Shopify plan) while shekel revenue stays the same; margin plans need an FX buffer of at least 5-10%.
- ESTIMATE: $75 threshold = 238 ILS today; it was ~211 ILS at a 2.81 rate.

### Gaps
- None material. The May 2026 values come from an aggregator and were not checked against the BOI series.

---

## 6. Advertising benchmarks for Israel 2025-2026

### Takeaway
Two independent datasets now agree on the order of magnitude: Israeli Meta CPM is roughly 20-27 ILS ($6-10) in normal months and about 60-65% higher in November; the median cost per Meta-reported purchase for Israeli online stores is about 86 ILS (range 35-175 ILS) or about $32, and it equals about 21% of average order value in the median store. Nothing found supports a CPA below ~35 ILS as a planning assumption, and no credible Israel-specific TikTok, conversion-rate, AOV or COD data exists publicly.

### Cited Findings
- **REPORTED** (Israeli agency's client data, 1 Jan-28 Sep 2026, 2.1M ILS spend, 94M impressions, 2.3M clicks, number of stores not stated, media cost before VAT and fees, purchases as reported by Meta; published 29 Sep 2026; MEDIUM reliability, the best local source found): median store CPM 24.1 ILS (range 17.7-27.2); CPC 0.88 ILS (0.53-1.90); CTR range 1.3-3.8%; cost per purchase median 86 ILS (range 35-175); cost per purchase as a share of AOV median 21% (range 12-43%); Meta spend as a share of revenue 14.2%; median monthly Meta budget 10,900 ILS (about 5,100-79,800); pooled CPM lowest in April 19.5 ILS and highest in September 26.6 ILS; window ends before November - [Preneuriat](https://preneuriat.com/blog/facebook-ads-cost-israel)
- **REPORTED** (ad-analytics vendor, medians across campaigns from accounts using the tool, all industries, Israel sample size not given; LOW-MEDIUM reliability): Israel median Meta CPM ~$9.15 over Jul 2025-Jun 2026; Sep 2025 $6.19 (low), Oct 2025 $8.13, Nov 2025 $15.18 (high), Dec 2025 $10.71, Mar 2026 $6.34, Apr 2026 $10.33, Jun 2026 ~$9.79; global median ~$20.9 - [Superads CPM Israel](https://www.superads.ai/facebook-ads-costs/cpm-cost-per-mille/israel)
- **REPORTED** (same vendor): Israel median cost per purchase: Jul 2025 $39.62, Oct 2025 $47.41 (peak), Nov 2025 $26.18, May 2026 $16.49 (low), Jun 2026 $30.59; 12-month average ~$32.2 vs ~$49.9 global - [Superads cost per purchase Israel](https://www.superads.ai/facebook-ads-costs/cost-per-purchase/israel)
- **REPORTED** (search summaries, pages not opened): ecommerce-only Meta CPM for Israel $7.48 - [Lebesgue](https://lebesgue.io/facebook-ads/facebook-cpm-by-country); Israel CPM $6.80-11.20, +4% y/y - [Stackmatix](https://www.stackmatix.com/blog/facebook-ads-cpm-by-country-2026); Israeli agency blog ranges 15-60 ILS CPM - [Simple-web](https://www.simple-web.co.il/en/blog/facebook-instagram-ads-cost)
- **REPORTED** (global, not Israel): Triple Whale median Meta ROAS 1.86 across ~35,000 brands in 2025; Varos 2.19 (Apr 2025) - [Consequential](https://consequential.io/blog/what-is-a-good-roas-for-a-dtc-brand); Triple Whale average Meta CPM rose from $11.82 (2024) to $14.19 (2025), +20% - [Clouted](https://clouted.com/blog/meta-advertising-CPM-inflation-statistics); Triple Whale BFCM 2025: Meta ROAS 2.26, median AOV $77.79 - [Triple Whale](https://www.triplewhale.com/blog/facebook-ads-bfcm)
- **REPORTED** (global vendor data): against a September baseline the median brand paid 84% more per 1,000 impressions on Black Friday and 59% more across Black Friday week, while cost per purchase fell 20% and Meta-reported ROAS rose 19% - [Lebesgue](https://lebesgue.io/facebook-ads/are-meta-ads-worth-it-black-friday)
- **REPORTED** (global, no Israel data): TikTok CPM about $6.2 average, typical band $4-13; CPC ~$0.99 - [Mega Digital](https://megadigital.ai/en/blog/how-much-do-tiktok-ads-cost/); [Adcore](https://www.adcore.com/blog/?p=44197)
- **REPORTED** (Hebrew agency blogs, unsourced rules of thumb): ecommerce conversion rate "commonly 1-3%", leading stores 4-5% - [SFB](https://www.sfb.co.il/blog-post/what-is-a-good-conversion-rate); one store-platform vendor claims an average basket of 338 ILS - [iStores](https://www.istores.co.il/z/)
- **REPORTED** (Wolt/Kantar 2025, n=2,006, from round 1): 26% bought after an influencer recommendation; 42% are members of coupon/Telegram deal groups - [ICE](https://www.ice.co.il/consumerism/news/article/1098033)

### Inferences
- ESTIMATE: the two CPM sources reconcile: 24.1 ILS / 3.1 = ~$7.8, inside Superads' $6-10 normal-month band. November 2025 at $15.18 was 87% above October and 66% above the 12-month median; expect the same now (Singles' Day, Black Friday). But in both the Israeli vendor series (Oct $47 -> Nov $26) and the global Lebesgue data, cost per purchase fell in the peak weeks because conversion rates rise; high CPM in November is not by itself a reason to pause, if the offer is promotional.
- ESTIMATE: the single most useful number is "cost per purchase = 21% of AOV (12-43%)". With a median CPA of 86 ILS that implies a median AOV near 400 ILS in the sample. A 99-149 ILS single-item order would need a CPA of 12-43% x price = 12-64 ILS, i.e. at or below the bottom of the observed 35-175 ILS range. That is the core reason paid-social single low-priced products do not work in Israel.
- ESTIMATE: implied arithmetic from the medians: 1,000 ILS buys ~41,500 impressions and ~1,135 clicks; at 86 ILS per purchase that is ~11.6 purchases, a click-to-purchase rate of about 1.0%.
- ESTIMATE: the model scenarios are CPA low 35 / medium 86 / high 175 ILS, taken straight from the Preneuriat range.

### Gaps
- No Israel TikTok Ads CPM/CPA; TikTok Ads Manager is available for Israel targeting as far as known, but I found no 2026 source confirming terms or costs.
- No independent Israeli conversion-rate, AOV or COD-share statistics; no Israeli e-commerce association dataset found.
- Triple Whale / Varos dashboards do not publish an Israel cut. Preneuriat's store count and category mix are undisclosed, and Meta-reported purchases overstate incremental sales.
- Whether Meta invoices Israeli advertisers with 18% VAT (recoverable by an osek murshe, a real cost for an osek patur) was not verified.

---

## 7. Reality check: do Israeli dropshippers and small DTC stores make money, and how do survivors operate

### Takeaway
I found no credible, numbers-disclosing first-hand account from an Israeli dropshipper or small DTC founder for 2024-2026; the Hebrew material is dominated by course sellers, and the frequently quoted "90% of stores fail" has no traceable source. The only hard evidence is indirect: the ad benchmarks above, the 75% order share of Chinese platforms, and best-seller lists of real Israeli stores (round 1), all of which point to survivors selling higher-AOV or repeat-purchase goods from local stock rather than single cheap gadgets shipped from China.

### Cited Findings
- **REPORTED** (Hebrew vendor/blog content, LOW reliability, search summaries): "traditional dropshipping is no longer profitable for most people", citing ad costs and negative ROI on most campaigns; typical dropshipping margin 10-30% vs 40-70% for private label; minimum workable ROAS quoted as 2-2.5 - [Profitzon](https://profitzon.co.il/dropshipping-vs-amazon-wholesale-comparison/) (page returned 403; summary only); [Clickmor](https://www.clickmor.com/single-post/דרופשיפינג-מול-מותג-פרטי-מהי-השיטה-הרווחית-ביותר); [Banku](https://banku.co.il/כמה-אפשר-להרוויח-מדרופשיפינג-והסוד-שאיש-לא-מגלה/)
- **REPORTED** (global vendor blogs, not Israel): realistic dropshipping net margins 5-15%; "successful" stores 15-25% - [Syncost](https://www.syncost.com/blogs/is-dropshipping-profitable); [LetsTalkShop](https://www.letstalkshop.com/blog/is-shopify-dropshipping-still-profitable)
- **REPORTED**: Shopify has never published a store success/failure rate and no independent body has; the "90-95% fail within 120 days" figure circulates between blogs without a named study; the best-sourced comparison is the US Bureau of Labor Statistics figure that ~22% of new businesses close in year one - [GroPulse](https://gropulse.com/shopify-success-rate/)
- **REPORTED** (from round 1): live Israeli Shopify stores grew from 6,200 (Q4 2023) to 12,324 (Nov 2026) - [StoreLeads](https://storeleads.app/reports/shopify/IL/top-stores); Israeli media describe local sites that resell AliExpress goods and advise reverse image search - [Bizportal](https://www.bizportal.co.il/general/news/article/20013928)
- **REPORTED**, influencer pricing in Israel 2026 (press and agency blogs; no official price list exists): nano collaborations in the hundreds of ILS, micro in the hundreds to low thousands, sometimes product-only - [ICE](https://www.ice.co.il/advertising-marketing/news/article/1133279); [YouHoo](https://www.youhoo.co.il/influencer-marketing-guide-2026/); average ~1,300 ILS per post, micro (10k-100k followers) ~1,800-18,000 ILS - [Dipy](https://dipy.io/ugc-advertising-costs-2026/); top names 20,000-25,000 ILS per story frame and 40,000-60,000 per Reel - [i24NEWS](https://www.i24news.tv/he/news/economic/consumption/artc-46bc42d1)
- **REPORTED**: Zap price comparison charges stores per click plus a fixed monthly fee, no upfront payment or term commitment; Zap's marketplace charges a category-dependent sales commission (percentages not published) - [Zap join page](https://www.zap.co.il/joinzap.aspx)
- **REPORTED** (affiliate-course sites, LOW reliability): KSP runs an affiliate programme with commissions "up to 35%" depending on product - [avodamehabait](https://www.avodamehabait.net/ksp-affiliate-program). No source for KSP marketplace seller commission.
- **REPORTED** (from round 1): AliExpress opened to Israel-registered sellers with a "Ship from Israel" label - [Ynetnews](https://www.ynetnews.com/business/article/ryqj93xtze)

### Inferences
- ESTIMATE: an influencer story at 500-1,500 ILS must produce roughly 6-17 orders to match the 86 ILS median Meta CPA; that is plausible only with a well-matched micro-creator and should be tested on a pay-per-sale (coupon code, 10-20% commission) basis first. Commission-only deals convert the CPA into a fixed % of revenue, which is what a low-priced product needs.
- ESTIMATE: survivor patterns consistent with the evidence gathered in rounds 1-2 (store best-seller lists, Zap prices, ad benchmarks): local stock with 1-3 day delivery; AOV of 250-450 ILS via bundles or higher-ticket items; repeat-purchase consumables or refills; a brand/warranty reason not to buy on AliExpress; presence on Zap/marketplaces for price-comparison traffic; owned audiences (WhatsApp/Telegram lists, with opt-in because of the spam law). None of these is proven by disclosed Israeli P&L data.
- ESTIMATE: the answer to "can paid-social single-product stores be profitable in Israel at all": yes only inside a narrow window - price of roughly 199 ILS or more, landed cost at or below ~25-30% of price, CPA held under ~20-25% of price, local stock. Below 149 ILS the arithmetic in section 8 fails at any CPA observed in the Israeli data.

### Gaps
- No Israeli founder interview, forum thread or podcast with real margins, ROAS, refund rates or failure reasons was found (Hebrew Facebook groups are not indexable; Reddit returned nothing Israel-specific; Geektime/Calcalist searches surfaced nothing relevant). This is a real absence of public evidence, not a negative finding.
- No failure-rate statistic for Israeli stores; no Telegram deal-channel pricing or affiliate commission norms; no WhatsApp funnel performance data; no KSP/Walla Shops seller commission.
- Suggested primary research: ask 3-5 Israeli store owners directly (Facebook groups such as Israeli Shopify/e-commerce communities) for CPA, AOV and return rate; pull StoreLeads' historical list to count how many Israeli stores live in 2024 are dead today.

---

## 8. Sensitivity table: contribution per order and maximum landed cost, Model A (direct from China) vs Model B (local stock)

### Takeaway
At 99 ILS neither model works at any observed CPA; at 149 ILS only a low CPA (35 ILS) with a landed cost under ~48 ILS (A) or ~17 ILS (B) reaches 25%; from 199 ILS upward the business becomes workable at a low CPA, and only at 299-449 ILS does it survive the median Israeli CPA of 86 ILS. Model B needs a cheaper product than Model A by roughly the domestic delivery cost (about 30 ILS), which it has to win back through higher conversion, lower returns and the ability to charge more.

### Cited Findings
Inputs and their status (sources in the sections above):

| Input | Value used | Status |
|---|---|---|
| VAT on sale | 18%, net revenue R = P / 1.18 | Rate REPORTED (not read on gov.il; corroborated by PayPal page). Applying it to the full price in Model A is an ASSUMPTION (disputed, section 4) |
| Customs duty, purchase tax | 0 | VERIFIED for the tariff lines listed in section 4 |
| Import tax on Model A parcel | 0 if supplier price <= $75 (238 ILS at 3.172) | VERIFIED (tariff item 98.02; FX from Bank of Israel) |
| Payment + Shopify fee f | 3.6% of P (Grow Light 1% + 0.6% Shopify surcharge + Shopify Basic 2%) | VERIFIED from price pages; fixed monthly fees excluded |
| CPA scenarios | Low 35 / Medium 86 / High 175 ILS | REPORTED (Preneuriat range and median, Israeli stores, Jan-Sep 2026) |
| Return/refund rate r | 5% | ASSUMPTION (no Israeli data) |
| Domestic delivery D (Model B) | 30 ILS ex VAT, seller pays, free shipping to customer | ASSUMPTION inside the REPORTED 22-38 ILS "from" range |
| Seller-paid return leg D_ret (Model B) | 30 ILS on returned orders | ASSUMPTION (conservative; the statute puts regret-return shipping on the customer) |
| USD/ILS | 3.17 | VERIFIED |
| Fixed costs (Shopify plan, gateway monthly, accountant, apps), creative costs, agency fees, stock write-offs, 3PL fees, cancellation-fee income | not included | Must be added by the partners |

Formulae (all ILS per order; P = price incl. VAT; R = P/1.18; t = target net contribution as a share of R; L = landed cost per unit):
- Model A: landed cost L_A = supplier product price + international shipping (last mile included). A refunded order loses the whole net revenue and the unit.
  Contribution_A = R x (1 - r) - L_A - f x P - CPA
  Max L_A = R x (1 - r - t) - f x P - CPA
- Model B: landed cost L_B = FOB + freight + clearance + compliance + storage per unit. A returned unit goes back to stock.
  Contribution_B = (1 - r) x (R - L_B) - D - r x D_ret - f x P - CPA
  Max L_B = R - (t x R + D + r x D_ret + f x P + CPA) / (1 - r)
- Break-even ROAS on VAT-inclusive revenue = P / break-even CPA.

Table 1. Model A (direct from China). "Before landed" = R x (1 - r) - f x P - CPA, i.e. what is left to pay for product + international freight.

| Price P | Net revenue R | Fee f x P | CPA 35: before landed | max L at 15% | max L at 25% | CPA 86: before landed | max L at 15% | max L at 25% | CPA 175: before landed | max L at 15% | max L at 25% |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 99 | 83.9 | 3.6 | 41 | 29 | 20 | -10 | none | none | -99 | none | none |
| 149 | 126.3 | 5.4 | 80 | 61 | 48 | 29 | 10 | none | -60 | none | none |
| 199 | 168.6 | 7.2 | 118 | 93 | 76 | 67 | 42 | 25 | -22 | none | none |
| 299 | 253.4 | 10.8 | 195 | 157 | 132 | 144 | 106 | 81 | 55 | 17 | none |
| 449 | 380.5 | 16.2 | 310 | 253 | 215 | 259 | 202 | 164 | 170 | 113 | 75 |

Table 2. Model B (local stock, seller pays 30 ILS delivery). "Max L at 0%" = landed cost at which the order just breaks even.

| Price P | CPA 35: max L at 0% | max L at 15% | max L at 25% | CPA 86: max L at 0% | max L at 15% | max L at 25% | CPA 175: max L at 0% | max L at 15% | max L at 25% |
|---|---|---|---|---|---|---|---|---|---|
| 99 | 10 | none | none | none | none | none | none | none | none |
| 149 | 51 | 31 | 17 | none | none | none | none | none | none |
| 199 | 91 | 64 | 47 | 37 | 11 | none | none | none | none |
| 299 | 172 | 132 | 105 | 118 | 78 | 52 | 25 | none | none |
| 449 | 293 | 233 | 193 | 240 | 180 | 140 | 146 | 86 | 46 |

"none" = the maximum landed cost is negative: no product cost makes the target reachable.

Table 3. Break-even CPA if landed cost is 30% of price (a common sourcing target):

| Price P | Landed cost (30%) | Break-even CPA, Model A | Break-even CPA, Model B | Break-even ROAS A / B |
|---|---|---|---|---|
| 99 | 30 | 46 | 16 | 2.2 / 6.2 |
| 149 | 45 | 70 | 41 | 2.1 / 3.6 |
| 199 | 60 | 93 | 65 | 2.1 / 3.1 |
| 299 | 90 | 140 | 113 | 2.1 / 2.6 |
| 449 | 135 | 211 | 186 | 2.1 / 2.4 |

Table 4. What the Model A freight (section 1, agent-calculator upper bound at 3.17) leaves for the product itself at a 25% target and CPA 35:

| Price P | Max landed (Table 1) | 100 g freight 27 | 300 g freight 38 | 500 g freight 49 | 1 kg freight 76 | 2 kg freight 130 |
|---|---|---|---|---|---|---|
| 99 | 20 | none | none | none | none | none |
| 149 | 48 | 21 | 10 | none | none | none |
| 199 | 76 | 49 | 38 | 27 | 0 | none |
| 299 | 132 | 105 | 94 | 83 | 56 | 2 |
| 449 | 215 | 188 | 177 | 166 | 139 | 85 |

Sources for the inputs: [Preneuriat](https://preneuriat.com/blog/facebook-ads-cost-israel); [Grow pricing](https://grow.business/pricing/); [Shopify IL pricing](https://www.shopify.com/il/pricing); [Customs tariff](https://shaarolami-query.customs.mof.gov.il/CustomspilotWeb/he/CustomsBook/Import/DiscountCodes); [Bank of Israel](https://boi.org.il/PublicApi/GetExchangeRates?asXml=false); [KakoBuy calculator](https://www.kakobuy.com/); [Outside the Box](https://outside-the-box.co.il/משלוחים-לעסקים-קטנים/); [Consumer Protection Law](https://he.wikisource.org/wiki/חוק_הגנת_הצרכן)

### Inferences
- The current product (129 ILS, Model A): R = 109.3; fee 4.6; at CPA 35 the amount left for product + freight is ~64 ILS at break-even and ~37 ILS for a 25% contribution; at the median CPA of 86 ILS it is ~13 ILS at break-even. With freight alone at 27-38 ILS for a 100-300 g parcel, the product cannot work on paid social. (Computed with the Table 1 formula.)
- Sensitivities worth knowing: each 10 ILS of CPA moves contribution by 10 ILS (A) / 10.5 ILS of allowable landed cost (B); each 1 point of return rate costs R x 1% in A (1.3-3.8 ILS) but only ~0.3 ILS + lost margin in B; charging the customer 20-25 ILS for shipping in Model B (about 17-21 ILS net of VAT) closes most of the 30 ILS gap between the models; if the accountant confirms that Model A sales are outside VAT, R rises to P and every "max L" in Table 1 rises by about 15% of P (e.g. +22 ILS at 149) - but do not plan on that.
- Model B's lower maximum landed cost is offset in practice by cheaper inbound freight per unit (bulk air ~5-17 ILS per 300 g unit versus 28-40 ILS per parcel), so for a 300 g item the product-cost budget is similar in both models; B wins on delivery speed, returns handling and legal exposure, A wins on zero inventory risk.
- Rule of thumb from the tables: target P >= 199 ILS, landed cost <= 25-30% of P, and a tested CPA <= 20% of P; stop any test where CPA stays above 35% of P.

### Gaps
- Every row depends on three unmeasured store-specific numbers: real CPA, real return rate, real per-parcel freight from CJ. Replace the assumptions with: a CJ quote per SKU; two courier quotes; one gateway quote; and a 7-14 day ad test with a spend cap.
- Fixed monthly costs (about US$39 Shopify + 29-69 ILS gateway + accountant + apps) and the partners' time are excluded; at 100 orders/month they add roughly 5-10 ILS per order (ESTIMATE).
- The VAT treatment of Model A and the personal-import status of store-arranged parcels remain open legal questions that could change Table 1 in either direction.
