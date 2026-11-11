# Israel e-commerce / dropshipping cost & constraint framework (as of 2026-11-11)

Labels used throughout: **FACT** = primary/official source read in this session; **REPORTED** = secondary source (press, law-firm, trade body, vendor/agency blog); **ESTIMATE** = my inference. Where a number comes from a vendor/affiliate blog it is flagged LOW-RELIABILITY. Nothing here was read directly on gov.il / Tax Authority pages (search did not surface them and several fetches were blocked), so almost everything is REPORTED, not FACT. That is itself a finding: the report writer should not present any figure below as officially verified without a gov.il check.

---

## 1. Import taxes: VAT rate, personal-import exemption, dropship parcel vs. commercial import

### Takeaway
VAT is 18%. The personal-import exemption went $75 -> $150 (late Dec 2025) -> cancelled by Knesset (23-24 Feb 2026) -> interim $130 (25 Feb - 1 Jun 2026, single source) -> back to **$75 since 1-2 June 2026**, and $75 is the reported status in Sept-Oct 2026. A dropshipped parcel under $75 reaches the consumer with zero import tax, exactly like an AliExpress/Temu order, so the seller has no tax advantage and a structural price disadvantage (margin + local VAT on own sale) versus the platforms.

### Cited Findings
- REPORTED: VAT rate 18% (2026 budget kept VAT at 18%) — [VATupdate, 10 Dec 2025](https://www.vatupdate.com/2025/12/10/israel-approves-2026-budget-vat-stays-at-18-expands-exemptions-eases-bank-entry-rules); 18% "as of Oct 2026" on commercial imports — [UnitedXP importer FAQ](https://www.unitedxp.co.il/?p=92398)
- REPORTED: Smotrich signed order raising exemption $75 -> $150, effective 24 Dec 2025 — [Mako](https://www.mako.co.il/finances-news/Article-70757e118574b91026.htm); [Ynet](https://www.ynet.co.il/economy/article/r1env7omze)
- REPORTED: Knesset plenum cancelled the $150 order, 59-25, reported 24 Feb 2026; order cost est. ~NIS 1bn tax revenue — [Globes, 24 Feb 2026](https://en.globes.co.il/en/article-1001535894)
- REPORTED (single LOW-RELIABILITY source, coupon site): interim threshold $130 from 25 Feb 2026 to 1 Jun 2026; back to $75 on 1 Jun 2026; "$75 as of 15 Sept 2026" — [Cuponist](https://cuponist.co.il/vat-customs-parcels-abroad-2026/)
- REPORTED: "since 2 June 2026 the threshold is back to $75 per order" (update note on article) — [Bizportal](https://www.bizportal.co.il/general/news/article/20024799). Note 1-day date discrepancy vs Cuponist (1 Jun vs 2 Jun).
- CONFLICT: a guide "as of March 2026" says $150 excluding shipping — [Netrise/Insignia](https://insignia.netrise.co.il/en/?p=6109); this fits neither the Globes cancellation nor the $130 interim claim; treat as stale.
- REPORTED: Exemption test = goods value only, excluding shipping/insurance if itemised separately; if not separable, the total counts; parcels from same supplier to same customer within 72h are aggregated; once taxable, VAT is computed on goods + shipping + insurance; FX = Bank of Israel representative rate + 0.5% — [Cuponist](https://cuponist.co.il/vat-customs-parcels-abroad-2026/)
- REPORTED bands (personal import): up to $75 fully exempt; $75-$500: 18% VAT, no customs, purchase tax only on goods subject to it; $500-$1,000: VAT + customs and/or purchase tax per product; >$1,000: handled like commercial import; alcohol/tobacco never exempt — [Cuponist](https://cuponist.co.il/vat-customs-parcels-abroad-2026/); $75-$500 = VAT only confirmed by [Protocol](https://protocol.co.il/personal-importation-taxes/); $75 full exemption confirmed by [Kol Zchut personal-import guide](https://www.kolzchut.org.il/he/זכותון_בנושא_יבוא_אישי_(חבילות_מחו"ל))
- REPORTED: False value declaration can lead to confiscation or a fine as condition of release — [Kol Zchut](https://www.kolzchut.org.il/he/זכותון_בנושא_יבוא_אישי_(חבילות_מחו"ל))
- REPORTED (commercial import): customs value is CIF (goods + freight + insurance); import VAT 18% is charged on value incl. customs and purchase tax; a VAT-registered business can generally deduct import VAT as input tax — [UnitedXP importer FAQ](https://www.unitedxp.co.il/?p=92398)
- REPORTED (OLD, 2018-2020 courier fee sheets, personal-import): handling fee NIS 87.75 incl. VAT or 3% of taxes (higher of); customs-broker fee NIS 333.45 incl. VAT for shipments >$1,000; "computer fee" applies above $100 — [ship.co.il fee sheet 2020](https://site.ship.co.il/media/1434/דף_עמלות_משלוחי_יבוא_אישי_מקוצר_כולל_הפניות_ללינקים_-_עברית_-_מהדורה__8_-_01.01.20.pdf). Outdated; use as order-of-magnitude only.
- REPORTED: Unlike the EU, Israel has imposed no special levy on low-value parcels from foreign shopping sites (article ~mid-2026) — [Israel Hayom](https://www.israelhayom.co.il/lifestyle/fashion/article/20883455)
- REPORTED: after the (temporary) exemption increase, NEXT saw larger basket values — [Calcalist](https://www.calcalist.co.il/shopping/article/h1kfkdk4bg)

### Inferences
- ESTIMATE: At $75 the tax-free ceiling is roughly 250-280 ILS of goods value depending on the USD/ILS rate (rate not verified in this session). Any product a small store would sell at ~100-200 ILS retail has a supplier cost far below $75, so dropship parcels (model A) enter tax-free.
- ESTIMATE: Competitiveness. Consumer buying direct from AliExpress/Temu pays: platform price, usually free shipping, 0% import tax under $75. The store's customer pays: same factory cost + store margin + ad cost + (if seller is an osek murshe) 18% VAT embedded in the retail price. A store price of 129 ILS contains ~19.7 ILS VAT (129/1.18 = 109.3 net). So for any item findable on AliExpress/Temu the store must win on something other than price (Hebrew creative, speed, bundle, trust, returns).
- ESTIMATE: Model B (bulk import) pays 18% import VAT on CIF + duty, but that VAT is deductible against output VAT, so VAT is not an extra cost versus Model A if the seller charges VAT anyway; the real extra costs of B are duty (product-specific), broker/clearance fixed fees, standards compliance, and inventory risk.
- ESTIMATE: Order splitting / under-declaring to stay under $75 is risky (72h aggregation rule, confiscation/fine).

### Gaps
- No official Tax Authority / gov.il page was retrieved confirming the current $75 threshold or the $130 interim step; the $130 step rests on one coupon-site source. Must be verified at the Tax Authority's personal-import page/calculator.
- Customs duty rates by category (many consumer goods are 0% but some carry 6-12% and purchase tax) were NOT verified; must be looked up per HS code in the Tax Authority tariff ("taarif ha-meches"). One news snippet claiming 40% on electronics is unverified and looks wrong as a general statement.
- Current (2026) customs broker / clearance fees for a small commercial air shipment: no current source found. Only the 2018-2020 courier sheets above.
- VAT treatment of an Israeli-registered seller whose goods ship direct from China to the consumer (does the seller owe 18% output VAT on the full sale when no import VAT was paid?) was not researched with a tax source; needs an accountant. Also not verified: the 2026 "osek patur" turnover ceiling.
- USD/ILS rate for Nov 2026 not verified.

---

## 2. Shipping: China -> Israel small parcels; domestic delivery; 3PL

### Takeaway
I could not find any published, Israel-specific per-weight rate card for CJ Dropshipping, YunExpress, 4PX or Cainiao; these must be pulled from the CJ in-account calculator per SKU. Reported transit China->Israel is ~7-20 days via CJ and 15-30 days via standard AliExpress lines, while the big platforms are now reported at "within a week" for many parcels. Domestic B2C courier delivery in Israel is reported at roughly NIS 38-48 per parcel list price from one provider.

### Cited Findings
- REPORTED (LOW-RELIABILITY, Israeli dropshipping blogs, 2026): CJ Dropshipping to Israel 7-20 days vs AliExpress 15-30 days; Chinese suppliers generally 2-4 weeks; Israeli local suppliers 2-5 business days — [Aviv Malka guide](https://aviv-malka.com/dropshipping-complete-guide-israel/); [Jonny Studio guide](https://jonnystudio.co.il/dropshipping-israel-guide/)
- REPORTED (third-party tracker): YunExpress to Israel ~16 days average — [Ordertracker](https://www.ordertracker.com/carriers/yunexpress)
- REPORTED: YunExpress bills the higher of actual vs volumetric weight — [YunExpress](https://www.yunexpress.com/our-solutions/b2c/standard-express) (Israel not listed among its published standard-line countries)
- REPORTED (NOT Israel; US reference only): CJPacket Ordinary 500 g China->US quoted at $12.07 in CJ's calculator, 2026 — [Easync review](https://easync.io/articles/cj-dropshipping-review/); CJ processing 1-3 days before dispatch — [Dropshipping Champions](https://dropshippingchampions.com/blog/cj-dropshipping-review)
- REPORTED (freight-forwarder marketing, Oct 2026): China->Israel air freight $5.31/kg, express $13.25/kg, LCL sea $79.73/CBM; air 3-7 days, sea 35-45 days door-to-door — [DTFU Logistics](https://www.dtfulogistics.com/news/shipping-cost-from-china-to-israel/). Relevant to Model B bulk, not per-parcel dropship.
- REPORTED: express (DHL/FedEx) single parcel from AliExpress to Israel $15-40 — [Aviv Malka AliExpress guide](https://aviv-malka.com/aliexpress-shipping-israel-times-prices/)
- REPORTED (benchmark of what the customer is used to): parcels from Shein/Temu/AliExpress-type sites arrive "within a week" per the cargo handler at Ben Gurion — [Ynet, 18 Oct 2026](https://www.ynet.co.il/economy/article/bj8y0qznml); AliExpress local warehouses cut some deliveries to 7-10 days; its logistics arm Parcel Home has ~45 distribution points in Israel (Apr 2026) — [Globes, 23 Aug 2026](https://en.globes.co.il/en/article-1001553175)
- REPORTED: average inbound parcel weight handled by Israel Post ~1.3 kg (vs 1.1 kg Jan-Sep 2025) — [Channel 14](https://www.c14.co.il/article/1763538)
- REPORTED (vendor page, 28 Jul 2026, VAT status not stated): Israeli B2C courier D2D: standard route from NIS 38 (3-5 business days), next-day NIS 45, same-day NIS 48+; a return costs about the same as a delivery; suggests free-shipping threshold ~1.5x average cart — [D2D](https://www.d2d.co.il/blog/ecommerce-delivery-israel)
- REPORTED (LOW-RELIABILITY): per-parcel delivery cost range NIS 25-150 depending on size/speed/volume/home vs pickup point — [e-shop.co.il](https://www.e-shop.co.il/build-ecommerce-website/how-much-does-it-cost-to-build-an-online-store-the-complete-guide); Israel Post single door-to-door next-day NIS 45-86 by weight/zone — [PickPackage](https://pickpackage.com/he/דמי-משלוח-ברשתות-בישראל/)
- REPORTED: Israel Post's own shop charges consumers NIS 20 shipping, free above NIS 99 — [Israel Post shop](https://shop.israelpost.co.il/)
- REPORTED: courier Cargo handles >500k shipments/month for >1,000 businesses, with pickup points and lockers — [Calcalist (sponsored-style guide)](https://www.calcalist.co.il/article/rjombn9ofe); Cheetah has heavy consumer complaints about lost/undelivered parcels in 2026 — [ICE](https://www.ice.co.il/consumerism/news/article/1021727)
- REPORTED: retailers moving away from free shipping (Zara Israel began charging; one retailer shows paid shipping above NIS 199 from 1 Oct 2026) — [Ynet](https://www.ynet.co.il/economy/article/bj8y0qznml); [ICE](https://www.ice.co.il/consumerism/news/article/1133415)

### Inferences
- ESTIMATE: For modelling Model A, use a placeholder of roughly $4-9 for 100-500 g and $9-20 for 1-2 kg China->Israel on economy tracked lines, and REPLACE with the CJ calculator quote per SKU before any decision. This placeholder is my extrapolation from the US CJPacket datapoint and forwarder per-kg rates, not a sourced Israel figure.
- ESTIMATE: Volumetric weight is typically (L x W x H cm)/6000 or /8000 on these lines; bulky-light items (holders, organisers, pillows) are penalised. Divisor per line not verified.
- ESTIMATE: Battery / liquid / magnet / powder / cosmetic items normally need "special" or "sensitive goods" lines that cost more and are slower; not verified with an Israel-specific source.
- ESTIMATE: A 7-20 day dropship promise now competes with platforms delivering in ~7 days with free shipping and free returns (AliExpress Elite). Model B's only speed edge is 1-5 day local delivery.
- ESTIMATE: Domestic delivery for a small store without volume discount: budget NIS 25-40 ex-VAT per home delivery, somewhat less for pickup point/locker; the retail convention of NIS 20-30 charged to the customer or free above a threshold means the seller usually subsidises part of it.

### Gaps
- No Israel-specific rate table for CJPacket / YunExpress / 4PX / Cainiao by weight (100 g-2 kg). Needs manual lookup in the CJ app (rates are per product and per line).
- No published business rate cards found for HFD, Cheetah, Mahir Li, Israel Post e-commerce contracts, lockers/pickup points; these are quote-based.
- No Israeli 3PL fee data (storage per pallet/shelf, pick & pack per order, receiving) found.
- Shipping restrictions for batteries/liquids/magnets/cosmetics on Israel lines not verified.
- No data on parcel loss/damage rates on these lines.

---

## 3. Payment processing fees (Shopify in Israel, local gateways, PayPal, Bit, installments)

### Takeaway
Shopify Payments is not reported as available to Israeli businesses, so a store pays the Israeli gateway's fee (roughly 0.9-1.9% reported for domestic cards plus a monthly fee) plus Shopify's third-party transaction fee (reported 2% / 1% / 0.5% by plan). All-in card cost of roughly 2.5-4% of gross revenue on the Basic plan is a reasonable modelling range.

### Cited Findings
- FACT (Shopify help): Shopify charges third-party transaction fees when a provider other than Shopify Payments is used, varying by plan, in addition to the provider's own processing fee — [Shopify Help](https://help.shopify.com/en/manual/international/pricing/fees)
- REPORTED (community): the tiers are 2% Basic / 1% Grow(Shopify) / 0.5% Advanced — [Shopify Community](https://community.shopify.com/t/why-does-shopify-charge-a-2-transaction-fee-for-third-party-providers/246613/1); Israeli Shopify consultancy says expect "2% to 0.5%" and that Shopify's own processor is not offered to Israeli businesses — [Shopmaster](https://www.shopmaster.co.il/payment) (undated, footer 2004-2024, affiliate links)
- REPORTED (Shopmaster, undated, LOW-RELIABILITY): PayPlus for Shopify: setup NIS 195, NIS 59/month up to 2,000 transactions + 0.6%, plus 1.2% clearing for Israeli cards (or bring your own acquirer agreement), foreign cards 2.8%; Payme via iCount 1.45% + NIS 1.20, setup NIS 85; iCount NIS 19/month; PayPal 3.4% + NIS 1.20, and PayPal-only stores lose Israeli sales — [Shopmaster](https://www.shopmaster.co.il/payment)
- REPORTED (agency comparison dated 11 Sep 2026, "averages as of early 2026"): PayPlus 0.9-1.3% + NIS 0-150/mo (payout usually next business day); Cardcom ~1.2% + ~NIS 49/mo; Tranzila 1.2-1.7% + NIS 90-200/mo; Max 1.2-1.6% + ~NIS 19/mo; Green Invoice 1.5-1.9% + NIS 49-249/mo; foreign/business/Diners/Amex cards cost more — [Sitelink](https://sitelink.co.il/web/ecommerce/payment-solutions-for-businesses-israel-2026/)
- CONFLICT: another 2026 guide puts the realistic Israeli-card range at 1.7-2.5% + ~NIS 0.5-1.5 per transaction — [NisAI guide](https://nisai.dev/guides/stripe-israel-payments/)
- REPORTED (vendor page): Grow (formerly Meshulam) via Green Invoice "Extra" plan: 1.4% for NIS 1-5,000 monthly volume; tourist card 3.5%; Bit adds +0.3% to the clearing fee; Diners +0.5% (min 1.7%) — [Green Invoice / Grow](https://www.greeninvoice.co.il/market/clearing/meshulam)
- REPORTED: Grow supports cards, Bit, Apple Pay, Google Pay, PayBox and bank transfer in one interface — [Calcalist](https://www.calcalist.co.il/article/hykea2z00ze)
- REPORTED: from May 2026 Bit charges recipients 0.8% on transfers above NIS 25k per year (relevant if taking payment to a personal Bit rather than via a gateway) — [Bizportal](https://www.bizportal.co.il/financialconsumerism/news/article/20040168)

### Inferences
- ESTIMATE: On Shopify Basic with PayPlus: ~1.2% clearing + 0.6% PayPlus + 2% Shopify = ~3.8% of gross (VAT-inclusive) revenue, plus ~NIS 59/month fixed. On a 129 ILS order that is ~4.9 ILS. Upgrading plan cuts the Shopify part to 1% or 0.5% once volume justifies the higher subscription.
- ESTIMATE: Fees are charged on the VAT-inclusive amount, so as a % of net revenue they are ~18% higher than the headline rate.

### Gaps
- No primary pricing page retrieved for PayPlus, Cardcom, Tranzila, Grow, Hyp; all figures are third-party and partly conflicting. Request quotes.
- Installments ("tashlumim"): no source found for the merchant-side cost of interest-free regular installments vs "credit" installments, or early-payout (nikayon) discount rates.
- Shopify subscription prices for Israel in 2026 and whether Shopify Payments has since launched in Israel were not verified on Shopify's site.
- Chargeback fees and PayPal's current Israel rate card not verified.

---

## 4. Consumer law: distance-selling cancellation, warranty, labelling, price display, spam; return rates

### Takeaway
A distance-sale buyer can cancel within 14 days of receiving the product (or the disclosure document, whichever is later) for any reason; the seller may keep at most 5% or NIS 100, whichever is lower. Missing disclosure means the clock never starts, and a defect/mismatch cancellation carries no fee and the seller must collect the product. Marketing by email/SMS without prior opt-in exposes the seller to up to NIS 1,000 statutory damages per message.

### Cited Findings
- REPORTED: s.14C Consumer Protection Law: distance sale may be cancelled within 14 days from the later of receipt of goods or receipt of the transaction-details document; s.14I: seller must allow cancellation through the same channel, including a dedicated prominent link on the website — [Bizportal](https://www.bizportal.co.il/financialconsumerism/news/article/20042624); [Kol Zchut](https://www.kolzchut.org.il/he/ביטול_עסקה_שנעשתה_באינטרנט_או_בטלפון)
- REPORTED: cancellation fee capped at 5% of price or NIS 100, the lower of the two; if no full disclosure document was provided the 14 days do not begin; defect/non-conformity cancellation = no fee and the seller collects the product — [Israel Consumer Council template letters](https://www.consumers.org.il/files/guide/mails/longdisproduct3bmismach.docx); [Bizportal](https://www.bizportal.co.il/financialconsumerism/news/article/20042624)
- REPORTED: buyers aged 65+, people with disabilities and new immigrants get 4 months to cancel if the transaction involved a conversation with the business (chat/email counts) — [Kol Zchut](https://www.kolzchut.org.il/he/ביטול_עסקה_ברוכלות_או_עסקת_מכר_מרחוק_על_ידי_אדם_עם_מוגבלות)
- REPORTED: goods excluded from cancellation include perishables, and recordable/copyable goods whose original packaging was opened; underwear and swimwear are excluded under the in-store cancellation regulations; the Consumer Protection Authority has been considering extending the underwear exclusion to distance sales (not confirmed in force) — [Protocol](https://protocol.co.il/consumer-transaction-cancellation-no-right/); [Kol Zchut](https://www.kolzchut.org.il/he/עסקה_צרכנית_שלא_ניתן_לבטל)
- REPORTED: the Consumer Protection Law's online-purchase rules apply to Israeli websites only (i.e. the local store carries duties that AliExpress/Temu purchases do not) — [Kol Zchut](https://www.kolzchut.org.il/he/ביטול_עסקה_צרכנית)
- REPORTED: many businesses refuse or ignore cancellation requests; consumers are advised to document — [Bizportal](https://www.bizportal.co.il/financialconsumerism/news/article/20042624)
- REPORTED: Spam law (s.30A Communications Law): advertising by email/SMS/fax requires prior explicit written consent; statutory damages up to NIS 1,000 per message without proof of harm; recent small-claims awards e.g. NIS 350 per message + NIS 500 costs (Nov 2025); exception for existing customers who gave details during a purchase subject to conditions (s.30A(c)); criminal fine up to NIS 226,000 (2026) — [Kol Zchut](https://www.kolzchut.org.il/he/פיצוי_בגין_משלוח_דברי_פרסומת_ללא_הסכמה_של_הנמען_%28חוק_הספאם%29); [Bizportal](https://www.bizportal.co.il/takdin/news/article/20038595); [Chamber of Commerce](https://www.chamber.org.il/serviceslobby/legal/74023/115485/)
- REPORTED (OLD, 2019, no study cited): Israeli online return rate ~10-15% vs ~30% globally — [Hon.co.il](https://www.hon.co.il/איך-מחזירים-מוצרים-בקנייה-באינטרנט/)
- REPORTED (international, vendor blogs, not Israel): fashion 24-40%, electronics 15-20% (another source 8-10%), overall online ~20% — [Claimlane](https://www.claimlane.com/resources/blog/average-ecommerce-return-rates); [ShipNetwork](https://www.shipnetwork.com/post/return-rates-by-industry)
- REPORTED: AliExpress Elite members (anyone spending >NIS 800/yr) get free returns within 15 days, raising the service bar — [Ynet, 18 Oct 2026](https://www.ynet.co.il/economy/article/bj8y0qznml)

### Inferences
- ESTIMATE: For a 100-150 ILS product the cancellation fee recoverable is only ~5-7.5 ILS, while a regret return costs the seller the outbound shipping already spent, payment fees (often not refunded), and in Model A a product that is uneconomic to send back to China (effectively a write-off). Model a full loss of landed cost + ad cost on every Model A return.
- ESTIMATE: Use 3-8% return/refund rate for non-apparel gadgets/home goods and 15-30% for apparel/footwear as planning assumptions; no current Israeli data supports these, they are scaled from the sources above.
- ESTIMATE: Long dropship delivery raises "item not received" disputes and chargebacks; the 14-day window starts at receipt, so slow shipping lengthens exposure.

### Gaps
- Could not open the statute or the Consumer Protection Authority pages (403). Not verified in-session: who bears return shipping on a regret cancellation; refund deadline (commonly cited as 14 days from cancellation notice); mandatory content of the disclosure document; statutory compensation for violations; exact list of distance-sale exclusions.
- Warranty duties (Consumer Protection (Warranty and After-Sale Service) Regulations: which goods/price levels trigger a mandatory 1-year warranty certificate), Hebrew labelling requirements (Consumer Protection Order on marking of goods: importer name/address, country of origin, Hebrew instructions), and price-display rules (price must be VAT-inclusive total in ILS) were NOT sourced in this session. These are real obligations for Model B and should be verified.
- Whether WhatsApp marketing falls under s.30A: no explicit source.
- No current Israeli return-rate data by category.

---

## 5. Product regulation that kills or complicates categories

### Takeaway
Regulation bites almost entirely on **commercial import (Model B)**: official standards and import groups, importer declarations, cosmetics notification and a registered responsible representative, wireless approvals. Personal-import parcels (Model A, where the consumer is the importer) are largely exempt in practice, e.g. up to 5 units of many wireless products need no Ministry of Communications approval. Since Jan 2025 the "what's good for Europe" reform lets importers rely on EU conformity documents instead of Israeli testing for many products, which lowers but does not remove the Model B burden.

### Cited Findings
- REPORTED: Amendment 19 to the Standards Law (Jan 2025) allows import based on EU regulation instead of the Israeli standard; 69 EU regulations adopted, phased in through 2027; no local testing needed if EU documentation exists; highest-risk Group 1 goods (e.g. baby products) need an importer declaration plus an EU document (DoC or proof of lawful marketing in the EU) — [Goldfarb law firm](https://www.goldfarb.com/he/מהפכת-התקינה-בישראל-הרפורמה-האירופית/); [UnitedXP](https://www.unitedxp.co.il/מהפכת-התקינה-בישראל-הרפורמה-האירופית/)
- REPORTED: Customs procedure: import groups 2 and 3 clear on a standards declaration/approval; code 65 added 1 Jan 2025 for declarations based on an EU regulation; not all standards joined the EU track on day one — [Customs procedure, updated 19 Jan 2025 (via Ruth Cargo)](https://www.ruthcargo.co.il/wp-content/uploads/2025/01/נוהל-שחרור-טובין-הנמצאים-תחת-תקינה-רשמית-במסגרת-רפורמות-לא-עוצרים-בנמל-ומה-שטוב-לאירופה-טוב-לישראל-מעודכן-ליום-19.1.25.pdf)
- REPORTED: phase 6 took effect 1 Jul 2026 (e.g. lifts, tools); phase 7 on 1 Jan 2027 (construction/plumbing equipment); July 2026 amendments to the Standards Law and Import-Export Ordinance and a "what's good for the US" track — [Chamber of Commerce update](https://www.chamber.org.il/foreigntrade/1109/1112/156283/); [Chamber of Commerce, July 2026](https://www.chamber.org.il/foreigntrade/1109/1112/163102/)
- FACT (gov.il service pages listed in search; content summarised by search tool): a cosmetics dealer must be registered in the cosmetics dealers register (valid 5 years) and the "responsible representative" must file a marketing notification through the cosmetics portal before marketing each cosmetic — [gov.il cosmetics notification](https://www.gov.il/he/service/cosmetics-marketing); [gov.il cosmetics business registration](https://www.gov.il/he/service/cosmetics-business)
- REPORTED: cosmetics reform in force 1 Apr 2023: licence-per-product replaced by notification; parallel-import track based on conformity to a reference cosmetic — [Chamber of Commerce](https://www.chamber.org.il/foreigntrade/1109/1110/126354/); [Shibolet law firm](https://www.shibolet.com/אושרה-הרפורמה-ביבוא-של-מוצרי-מזון-ותמר/)
- REPORTED: Ministry of Communications: personal import of up to 5 units per shipment of listed wireless household products is exempt from licence/approval with no CE requirement; a second track exempts both commercial and personal import if the product carries CE marking incl. radio compliance; Feb 2025: wireless cameras and smart doorbells exempted for personal import (these were ~35% of personal-import items needing approval in 2024); listed personal-import exemptions (smart lighting, smart scales, RC toys etc.) still require approval for commercial import — [Gadgety](https://www.gadgety.co.il/?p=371030); [Gadgety](https://www.gadgety.co.il/?p=337539); [Ynet](https://www.ynet.co.il/economy/article/h1f9wcihc)
- REPORTED: MoC published further draft amendments to conformity-approval and exemption regulations (incl. white goods, air conditioners) in 2026 — [Chamber of Commerce](https://www.chamber.org.il/foreigntrade/1109/1110/163305/)

### Inferences
- ESTIMATE, category screen for Model B (commercial stock): HIGH friction = cosmetics/skincare/anything applied to the body (registered representative + notification per SKU), medical or health-claim devices (AMAR registration), food supplements and food-contact items (Ministry of Health food import rules), toys and baby/children's products (Group 1, official standard), mains-powered electricals and chargers (official standards, Israeli plug), lasers, radio/Bluetooth/Wi-Fi devices unless CE-documented. LOW friction = non-electrical, non-child, non-body-contact home/organisation/accessory goods with no official standard.
- ESTIMATE: Under Model A the same categories physically pass as personal import, but the Israeli seller advertising them still carries consumer-law, advertising (health claims) and product-liability exposure; "legal to arrive" is not "safe to sell". The current product (UV sterilizer: mains/USB electrical, UV-C emitter, health claim) sits in a regulated zone for Model B.
- ESTIMATE: Obtaining genuine EU DoC/test reports from small Chinese factories is the practical bottleneck of the EU-track route.

### Gaps
- Not verified in-session: AMAR (medical device) scope and personal-import rule; food supplement and food-contact import rules; toy standard (SI 562) and children's product specifics; laser class limits; lithium battery import/air-transport limits; which exact official standards map to which import group for typical gadget categories (requires the Ministry of Economy standards search engine); personal-import quantity limits for cosmetics.
- Whether customs treats repeated dropship parcels arranged by an Israeli seller as commercial rather than personal import: no source found; legal grey area.
- Status in Nov 2026 of each MoC exemption (several sources are 2024-2025 announcements).

---

## 6. Advertising costs and conversion benchmarks in Israel

### Takeaway
The only Israel-specific Meta data found is from an ad-analytics vendor: median CPC ~$0.31-0.58 and median cost per purchase ~$32 (about 2/3 of global), with November the most expensive month. There is no credible Israel-specific public benchmark for TikTok, ROAS, store conversion rate or COD share; these must be measured, not assumed.

### Cited Findings
- REPORTED (vendor dataset, methodology unclear): Israel median Meta CPC averaged ~$0.58 Jul 2025-Jun 2026 (low $0.35 Aug 2025, high $0.83 Nov 2025) vs ~$1.07 global; another page of the same tool shows $0.59 (Jun 2025) falling to ~$0.31 (Jun 2026) — [Superads CPC Israel](https://www.superads.ai/facebook-ads-costs/cpc-cost-per-click/israel)
- REPORTED (same vendor): Israel median cost per purchase averaged ~$31.8 Jun 2025-May 2026 vs ~$49.8 global — [Superads cost per purchase Israel](https://www.superads.ai/facebook-ads-costs/cost-per-purchase/israel)
- REPORTED (same vendor): global Meta CPM averaged ~$20.59, peak Nov 2025; Israel "consistently priced below" the overall market (no Israel all-industry CPM number given) — [Superads CPM](https://www.superads.ai/facebook-ads-costs/cpm)
- REPORTED (global, vendor blog): Meta CPM rose ~20% across industries during 2025 — [Influee](https://influee.co/ca/blog/facebook-ads-benchmarks)

### Inferences
- ESTIMATE: A ~$32 median cost per purchase is ~105-120 ILS at plausible exchange rates, i.e. about the whole revenue of a 129 ILS order. The median includes high-AOV advertisers, so a cheap impulse product can do better, but the implication is hard: a single-item order at ~100-130 ILS cannot absorb a typical Israeli Meta CPA. Viability requires either CPA far below median (strong creative, ~20-40 ILS), or AOV pushed to ~200-350 ILS via bundles/quantity breaks, or repeat purchase.
- ESTIMATE: Break-even ROAS = 1 / (contribution margin before ads as % of VAT-inclusive revenue). With a 40% pre-ad margin break-even ROAS is 2.5; with 25% it is 4.0.
- ESTIMATE: Q4 (Nov: Singles' Day, Black Friday) is the most expensive auction period; today's date falls in it.

### Gaps
- No credible Israeli source for TikTok CPM/CPC, Meta CPM for Israel, ROAS norms, DTC conversion rates, blended ad cost as % of revenue, or COD usage. Agency posts with such numbers did not surface; treat any figure offered elsewhere as unverified.
- Superads data: sample composition unknown; purchase-objective CPA by price point not available.

---

## 7. Competitive pressure: cross-border platforms and local players

### Takeaway
Chinese platforms dominate: AliExpress, Temu and Shein together took about 75% of Israelis' online orders in June 2026 (Shop Analytics), Amazon only ~6%, and KSP leads local sites. Israel Post expects ~9 million inbound parcels in 2026 (8.2M in 2025), ~80% from Chinese sites. Anything generic that a small store sells is very likely already on AliExpress/Temu at factory price, tax-free under $75, with ~1-week delivery and (AliExpress Elite) free returns.

### Cited Findings
- REPORTED: June 2026 (Shop Analytics): AliExpress + Temu + Shein ~75% of Israelis' online orders; Amazon 6%; KSP = 18% of orders among top-20 local sites; May 2026 top local sites KSP, Super-Pharm, Shufersal — [Globes, 23 Aug 2026](https://en.globes.co.il/en/article-1001553175)
- REPORTED: Azrieli.com, Melisron's Groo and Shufersal's marketplace all closed within a week in Dec 2023 (Azrieli.com lost ~NIS 300M; Groo investment ~NIS 100M) — [Globes, 23 Aug 2026](https://en.globes.co.il/en/article-1001553175). (Azrieli.com therefore is not an active competitor.)
- REPORTED: Israel Post forecast ~9M parcels for 2026 vs 8.2M in 2025; ~80% of orders from Chinese sites (AliExpress, Temu, Shein) — [Channel 14](https://www.c14.co.il/article/1763538)
- REPORTED (Israel Post data, Oct 2025): AliExpress ~50% share, Temu jumped to 18-19%; Shop Analytics for one November: AliExpress orders -24% y/y, Temu +76% — [Ynet/Yedioth](https://www.ynet.co.il/yedioth/article/yokra14559446)
- REPORTED: market estimates of >20M parcels arriving in Israel in Nov 2026; Israel Post expects +30-40% in November; AliExpress launched Israeli "Elite" club on 18 Oct 2026 (auto-enrolled above NIS 800/yr; 5% off labelled items, 8% on the 1st of each month, free returns within 15 days, 24/7 support) — [Ynet, 18 Oct 2026](https://www.ynet.co.il/economy/article/bj8y0qznml)
- REPORTED: Amazon free shipping to Israel on eligible orders above $49 (page quoted in 2026); the $65 figure dates from 2021 — [Morning Star](https://morningstaronline.co.uk/node/165971); [Jewish Press 2021](https://www.jewishpress.com/news/business-economy/amazon-resumes-free-shipping-to-israel-with-caveats/2021/08/12/)
- REPORTED: overseas online purchases fell sharply during the Iran war period as flights were cancelled, shoppers shifted to local sites — [Globes](https://en.globes.co.il/en/article-1001538233)
- REPORTED: total online card spending June 2026 NIS 30.03bn, +22.9% y/y (Shva data) — [Bizportal](https://www.bizportal.co.il/general/news/article/20035420)
- REPORTED: no special low-value parcel levy in Israel, unlike the EU — [Israel Hayom](https://www.israelhayom.co.il/lifestyle/fashion/article/20883455)

### Inferences
- ESTIMATE: The practical test for any candidate product is "search it on AliExpress and Temu in Hebrew/English; what is the delivered price?" The store's sustainable premium over that price is the thing to estimate; generic gadgets rarely sustain more than a modest multiple once shoppers price-check.
- ESTIMATE: Supply disruption (war, flight cancellations) periodically favours sellers holding local stock (Model B); it is an episodic, not structural, advantage.
- ESTIMATE: With the exemption back at $75 (not $150), local sellers of goods costing $75-150 regained some protection, but that band is above this store's price range, so the reversal does not help it.

### Gaps
- Individual 2026 shares for AliExpress vs Temu vs Shein not found (only combined 75%, and Oct 2025 split).
- No CBS / Bank of Israel cross-border e-commerce value series retrieved; no Temu-specific 2026 Israel developments (local warehouse, local sellers) found.
- No data retrieved for Zap, Ivory, Terminal X, Walla Shops traffic or share; KSP/Super-Pharm/Shufersal ranking only.
- The 6% Amazon and 75% figures are share of orders tracked by Shop Analytics; methodology not examined.

---

## 8. Price-point psychology and average order value

### Takeaway
No reliable Israeli data on online average order value or impulse price bands was found. The only hard anchors are regulatory and competitive: the $75 tax-free ceiling, the NIS 99-199 free-shipping thresholds used by local retailers, and the ~$32 median Meta cost per purchase.

### Cited Findings
- REPORTED: Israel Post's shop: NIS 20 shipping, free above NIS 99 — [Israel Post shop](https://shop.israelpost.co.il/)
- REPORTED: a retailer moved from free shipping at NIS 199 to showing paid options above NIS 199 from 1 Oct 2026; Zara Israel began charging for shipping — [ICE](https://www.ice.co.il/consumerism/news/article/1133415); [Ynet](https://www.ynet.co.il/economy/article/bj8y0qznml)
- REPORTED: guidance to set the free-shipping threshold at ~1.5x average cart — [D2D](https://www.d2d.co.il/blog/ecommerce-delivery-israel)
- REPORTED: AliExpress treats NIS 800/year as its loyal-customer bar — [Ynet](https://www.ynet.co.il/economy/article/bj8y0qznml)
- REPORTED: Israel median Meta cost per purchase ~$31.8 — [Superads](https://www.superads.ai/facebook-ads-costs/cost-per-purchase/israel)

### Inferences
- ESTIMATE: A single-unit price of ~100-150 ILS is an awkward zone: too low to cover a ~100+ ILS typical CPA plus ~30-40 ILS delivery, yet high enough that shoppers price-check on AliExpress. Workable structures are (a) low-cost item with bundle/multi-buy pushing AOV to ~200-350 ILS, or (b) a higher-ticket item with real margin, still under the ~$75 supplier-cost ceiling for Model A.
- ESTIMATE: Shoppers trained by Temu/Shein expect free or near-free shipping; a visible NIS 25-30 shipping fee on a NIS 100 item is a conversion drag, so shipping is usually baked into price.

### Gaps
- No Israeli AOV statistic (overall or DTC), no data on impulse price bands from social ads, no COD prevalence data. All of section 8's conclusions are inference.

---

## 9. Profitability model template (cost line items; two operating models)

### Takeaway
Per-order net profit = retail price (VAT-incl.) minus VAT, product, inbound freight, import charges, domestic delivery, payment fees, returns allowance, ad cost, and fixed overhead per order. The two biggest and least-verified lines are ad cost per order and China->Israel freight; both must be measured/quoted per SKU.

### Cited Findings
(Each line: value or range, label, source section above.)

**Common to both models**
- Retail price P (ILS, VAT-inclusive; price display must be the final price) — input.
- Output VAT: P x 18/118 if seller is an osek murshe (VAT 18% REPORTED) — [VATupdate](https://www.vatupdate.com/2025/12/10/israel-approves-2026-budget-vat-stays-at-18-expands-exemptions-eases-bank-entry-rules). Whether/how this applies in pure dropship is an accountant question (Gap, section 1).
- Payment processing: gateway ~0.9-1.9% domestic cards (REPORTED) + PayPlus platform 0.6% if PayPlus (REPORTED, undated) + Shopify third-party fee 2% / 1% / 0.5% by plan (REPORTED) => ~2.5-4% of P; fixed ~NIS 0-150/month gateway; PayPal 3.4% + NIS 1.20 (REPORTED, undated) — [Sitelink](https://sitelink.co.il/web/ecommerce/payment-solutions-for-businesses-israel-2026/); [Shopmaster](https://www.shopmaster.co.il/payment); [Shopify Help](https://help.shopify.com/en/manual/international/pricing/fees)
- Advertising per order (CPA): Israel median Meta cost per purchase ~$31.8 (REPORTED, vendor data) — [Superads](https://www.superads.ai/facebook-ads-costs/cost-per-purchase/israel). Model as scenarios: 25 / 50 / 100 ILS (ESTIMATE). Compute break-even CPA = pre-ad contribution.
- Cancellation recovery: at most min(5% of P, NIS 100) on regret cancellations; nothing on defect cancellations (REPORTED) — [Bizportal](https://www.bizportal.co.il/financialconsumerism/news/article/20042624)
- Returns/refunds allowance: 3-8% of orders for gadgets/home, 15-30% apparel (ESTIMATE; only old/foreign data) — [Hon.co.il 2019](https://www.hon.co.il/איך-מחזירים-מוצרים-בקנייה-באינטרנט/); [Claimlane](https://www.claimlane.com/resources/blog/average-ecommerce-return-rates)
- Spam-law exposure: up to NIS 1,000 per unsolicited message (REPORTED) — [Kol Zchut](https://www.kolzchut.org.il/he/פיצוי_בגין_משלוח_דברי_פרסומת_ללא_הסכמה_של_הנמען_%28חוק_הספאם%29)
- Fixed overhead: Shopify subscription + apps, accountant, gateway monthly (NOT VERIFIED; input).

**Model A: dropship parcel direct from China to consumer**
- Product cost: supplier price (CJ/agent), USD -> ILS (input).
- Supplier processing: 1-3 days (REPORTED) — [Dropshipping Champions](https://dropshippingchampions.com/blog/cj-dropshipping-review)
- International shipping per parcel: NO verified Israel rate. Placeholder $4-9 (100-500 g), $9-20 (1-2 kg) (ESTIMATE; replace with CJ calculator quote); billed on max(actual, volumetric) (REPORTED) — [YunExpress](https://www.yunexpress.com/our-solutions/b2c/standard-express)
- Transit: 7-20 days CJ, 15-30 days AliExpress standard, ~16 days YunExpress (REPORTED, low reliability) — [Aviv Malka](https://aviv-malka.com/dropshipping-complete-guide-israel/); [Ordertracker](https://www.ordertracker.com/carriers/yunexpress)
- Import tax: 0 if goods value <= $75 (shipping excluded when itemised; 72h aggregation); otherwise 18% VAT on goods+shipping+insurance collected from the consumer plus a carrier handling fee (REPORTED) — [Cuponist](https://cuponist.co.il/vat-customs-parcels-abroad-2026/); [Bizportal](https://www.bizportal.co.il/general/news/article/20024799)
- Domestic delivery: included in the international line (last mile by Israel Post/local partner) — ESTIMATE.
- Standards/approvals: generally not triggered for personal-import parcels; MoC exemption up to 5 wireless units per shipment (REPORTED) — [Gadgety](https://www.gadgety.co.il/?p=371030)
- Return handling: assume returned unit is a write-off; refund P minus <= 5% (ESTIMATE).
- Competitive benchmark to record per SKU: AliExpress/Temu delivered price and delivery days (platform delivery often ~1 week, REPORTED) — [Ynet](https://www.ynet.co.il/economy/article/bj8y0qznml)

**Model B: bulk commercial import + local stock**
- Product cost FOB/EXW per unit at MOQ (input).
- International freight: air ~$5.3/kg, express ~$13.3/kg, LCL sea ~$80/CBM, sea 35-45 days door-to-door (REPORTED, forwarder marketing) — [DTFU Logistics](https://www.dtfulogistics.com/news/shipping-cost-from-china-to-israel/)
- Customs duty: by HS code on CIF value; NOT VERIFIED (many consumer goods 0%, some 6-12%, purchase tax on specific goods) — look up in the Tax Authority tariff.
- Import VAT: 18% on CIF + duty + purchase tax; deductible as input VAT for an osek murshe, so a cash-flow item, not a cost (REPORTED) — [UnitedXP](https://www.unitedxp.co.il/?p=92398)
- Customs broker / clearance / port or terminal fees per shipment: NOT VERIFIED for 2026; old personal-import courier sheets show ~NIS 88 handling and ~NIS 333 broker fee (REPORTED, 2020) — [ship.co.il 2020](https://site.ship.co.il/media/1434/דף_עמלות_משלוחי_יבוא_אישי_מקוצר_כולל_הפניות_ללינקים_-_עברית_-_מהדורה__8_-_01.01.20.pdf). ESTIMATE: budget NIS 500-1,500 fixed per small commercial consignment until quoted.
- Compliance: importer declaration / EU DoC for goods under official standards; cosmetics need registered dealer + notification per product; wireless goods need MoC approval or CE-based exemption (REPORTED) — [Goldfarb](https://www.goldfarb.com/he/מהפכת-התקינה-בישראל-הרפורמה-האירופית/); [gov.il cosmetics](https://www.gov.il/he/service/cosmetics-marketing); [Gadgety](https://www.gadgety.co.il/?p=337539). Cost NOT VERIFIED (testing/consultant fees are quote-based).
- Hebrew label / importer details / warranty certificate: required in principle; cost per unit small (ESTIMATE; legal basis not verified in-session).
- Storage + pick & pack (3PL or self): NOT VERIFIED; input.
- Domestic delivery: NIS 38 standard (3-5 days), NIS 45 next-day, NIS 48+ same-day list prices from one courier; return ~ same as a delivery (REPORTED) — [D2D](https://www.d2d.co.il/blog/ecommerce-delivery-israel); broader range NIS 25-150 (REPORTED, low reliability) — [e-shop.co.il](https://www.e-shop.co.il/build-ecommerce-website/how-much-does-it-cost-to-build-an-online-store-the-complete-guide)
- Shipping revenue: what the customer is charged (common: NIS 20-30 or free above NIS 99-199) (REPORTED) — [Israel Post shop](https://shop.israelpost.co.il/); [ICE](https://www.ice.co.il/consumerism/news/article/1133415)
- Returns: product may be resaleable; cost = return courier (~NIS 38) + refund minus <= 5% fee (REPORTED/ESTIMATE).
- Inventory risk: unsold stock write-down and cash tied up (ESTIMATE; input).

### Inferences
- Formula (per order, osek murshe): Net = P/1.18 - product - inbound freight - duty & clearance (B) - domestic delivery net of shipping charged (B) - payment fees (~2.5-4% of P) - CPA - returns allowance - overhead per order.
- Worked illustration for the existing product at P = 129 ILS (all cost inputs other than P are placeholders, not data): net of VAT 109.3; payment ~4.9; leaves ~104 ILS to cover product + freight + ads + returns. With the reported median Meta cost per purchase (~105-120 ILS) the order is loss-making before product cost; even at a CPA of 40 ILS, product + freight must stay under ~55 ILS to leave ~10 ILS.
- Decision rule suggested by the numbers: screen candidates on (1) delivered AliExpress/Temu price vs intended retail, (2) landed cost <= ~25-30% of VAT-inclusive retail, (3) AOV potential >= ~200 ILS via bundles, (4) not in a high-friction regulatory category if Model B is intended, (5) small/dense (low volumetric weight), no batteries/liquids.

### Gaps
- Unverified inputs that dominate the model: China->Israel per-parcel freight by weight; real CPA for this store; customs duty per HS code; broker fees; 3PL fees; domestic courier contract rates; installment costs; USD/ILS rate.
- Every "FACT" claim about tax thresholds should be re-checked on the Tax Authority site before publication; this session produced no directly-read primary tax source.
