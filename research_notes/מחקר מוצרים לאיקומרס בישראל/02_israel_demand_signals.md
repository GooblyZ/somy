# Israel demand signals: what small DTC / dropshipping-style stores actually sell online in Israel (2025-2026), and how to judge real volume

Research date: 2026-11-11. Labels used on every claim: **FACT** (I observed it directly on a primary page/API today), **REPORTED** (a named publication or company said it; not independently verified), **ESTIMATE** (modelled/third-party estimate), **UNVERIFIED** (plausible but I could not confirm).
Excluded by brief and not researched: scented body cream, pheromone cream.

**Tool access disclosure (important for the report writer):**
- Meta Ad Library (facebook.com/ads/library, country IL): **NOT ACCESSIBLE** from this environment (HTTP 403). No ad-count / ad-longevity data in this file comes from the Ad Library. Nothing below should be read as Ad Library evidence.
- Google Trends (geo IL): **NOT ACCESSIBLE** (HTTP 429 on both the explore page and the API). No Trends data in this file.
- TikTok Creative Center, Similarweb, Trustpilot, KSP, Super-Pharm, LastPrice, Payngo, Groo, CityDeal, Walla Shops: blocked (403/empty). Not used.
- General web search was US-indexed and returned very little Hebrew small-store content; Bing/DuckDuckGo direct scraping was challenge-blocked.
- What DID work: Zap.co.il search pages (direct), WooCommerce Store API on some Israeli stores, Shopify `products.json` / `sort_by=best-selling` on some Israeli stores, StoreLeads public report, Israeli/English press.
- Consequence: the "Israeli DTC hero-product store" scan is thin. I could not build a verified list of single-product Hebrew stores with ad longevity. This is the biggest gap and is flagged again below.

---

## Key Question 1: Evidence framework - tiers of evidence for "this product sells in meaningful volume"

### Takeaway
Only store-internal sales rankings, marketplace sold-counters and retailer-reported unit numbers come close to proving sales; reviews, ads and attention prove progressively less, and every signal must be date-stamped to the last 60-90 days. A product should be called a "serious candidate" only when at least one dated sales-type signal and two independent supporting signals agree, and the unit economics work at the local market price actually observed.

### Cited Findings
- Meta Ad Library shows a "Started running on [date]" label for active ads; there is no days-running metric, so duration must be calculated per ad. **REPORTED** (marketing blog, low-medium reliability) - [AdNabu](https://blog.adnabu.com/facebook/meta-ads-library/)
- Inactive commercial ads disappear from the library within days of being paused, so the library cannot show what a brand ran six months ago (survivorship bias: you only see what is live now). **REPORTED** - [Mida](https://www.mida.so/blog/meta-ads-library)
- Rules of thumb in the ad-spy community treat 30/60/90+ days of continuous running as a sign the advertiser is getting a return, but one vendor concedes a single 90-day ad "can be a vanity campaign" and that multiple long-runners at once is the stronger signal. **REPORTED** (vendor opinion, not data) - [Brandsearch](https://brandsearch.co/blog/how-long-to-run-facebook-ads)
- Spend and impressions are shown only for political/social-issue ads; for commercial ads the library exposes no spend or results, so profitability cannot be verified from it. **REPORTED** - [Creatify guide](https://creatify.ai/blog/meta-ad-library-how-to-use-it-to-search-for-competitor-ads-in-2026-(complete-guide))
- Meta added a "low impression count" label for very new/low-delivery ads, useful for discounting ads that exist but barely deliver. **REPORTED** - [PPC Land](https://ppc.land/meta-ads-library-adds-whatsapp-filter-and-low-impression-labels/)
- 72% of Israeli online shoppers say they check reviews before every purchase; the top fears are "product won't arrive / low quality" (69%) and delivery delays (56%) (Wolt/Kantar, n=2,006, published 31 Dec 2025). This is why review widgets are heavily gamed and also why they matter. **REPORTED** - [ICE](https://www.ice.co.il/consumerism/news/article/1098033)
- Judge.me (1,926 stores) and Loox (1,245 stores) are the most-installed review apps among Israeli Shopify stores; Sense RTL (Hebrew) is on 1,942 stores (StoreLeads, updated 6 Nov 2026). These are the widgets whose dates/photos need checking. **ESTIMATE** (third-party crawl) - [StoreLeads](https://storeleads.app/reports/shopify/IL/top-stores)
- Methods verified working today on Israeli stores (**FACT**, tested 2026-11-11):
  - Shopify: `https://<store>/collections/all?sort_by=best-selling` returns the store's own best-seller order; `https://<store>/products.json?limit=250` returns every product with `created_at`, `updated_at`, price, compare-at price and availability. Example: [silkn.co.il best-selling](https://www.silkn.co.il/collections/all?sort_by=best-selling), [silkn.co.il products.json](https://www.silkn.co.il/products.json?limit=250).
  - WooCommerce: `https://<store>/wp-json/wc/store/v1/products?orderby=popularity&order=desc&per_page=25` returns products ordered by the store's internal sales count, with `review_count` and stock status. Example: [nextstock.co.il](https://nextstock.co.il/wp-json/wc/store/v1/products?orderby=popularity&order=desc&per_page=25).
  - Zap: `https://www.zap.co.il/search.aspx?keyword=<Hebrew term>` returns number of listings, sellers, prices and each seller's Zap review count. Example: [Zap "מסנן מקלחת"](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%A1%D7%A0%D7%9F%20%D7%9E%D7%A7%D7%9C%D7%97%D7%AA).

### Inferences
(The tiering below is my analytical framework, built on the sourced limitations above; treat it as methodology, not as cited fact.)

**Tier 1 - Hard sales data (strongest)**
| Signal | Proves | Does NOT prove | How it is faked / misread | Recency check |
|---|---|---|---|---|
| Public company / retailer-reported units ("2,500 power banks in a week") | Real units through one seller in a stated window | That demand persists; that a small store can capture it; margin | PR cherry-picking of the best week; percentages off a tiny base ("+150%") | Article date + the window it states |
| Marketplace sold counters (AliExpress "sold", Temu "sold", TikTok Shop sold) | Cumulative global units for that listing | Israeli demand (counters are global); current velocity (cumulative since listing creation); profit | Brushing/self-orders, merged listings, counters inherited by re-used listings | Compare the counter on two dates 7-14 days apart; read newest review dates and filter reviews by country (IL) |
| Amazon BSR / "X bought in past month" | Relative rank / rolling 30-day volume in that country's Amazon | Anything about Israel (Amazon ~6% of Israeli online orders, see KQ3) | BSR spikes from a one-day deal; variation-level pooling | The 30-day badge is inherently recent; BSR needs a history tool (Keepa) |
| Store-internal best-seller order (Shopify best-selling sort, Woo popularity) | Which SKUs sell most *within that store* | Absolute volume (a #1 seller can be 3 units/month); Shopify sort is all-time weighted, so old winners linger | Store can manually order a collection; cheap add-ons outrank the hero product by units | Cross-check with `created_at` in products.json and with newest review dates |

**Tier 2 - Purchase indications**
| Signal | Proves | Does NOT prove | Faked / misread | Recency check |
|---|---|---|---|---|
| Review count + review dates (velocity) | A floor on orders (typically only a small share of buyers review) | Volume if reviews are imported | Loox/Judge.me AliExpress-import features; identical text across stores; reviews in translated Hebrew with foreign names; all dates clustered in one week | Sort newest-first; count reviews in last 30/90 days; look for Hebrew-native text and customer photos shot in Israeli homes |
| Stock-outs / "back in stock" notices | Either demand > supply or thin inventory | Which of the two | Fake scarcity timers; a dropshipper with zero stock shows "in stock" forever | Re-check availability weekly; `available` flag in products.json |
| Zap seller-review counts, number of sellers listing an item | Supply-side breadth: many merchants think it sells; local price level | Demand per seller; many listings can mean saturation, not opportunity | Same importer feeding many shops | Zap reviews are dated on the seller card |

**Tier 3 - Advertising activity (Meta Ad Library, TikTok Creative Center)**
- Proves: someone is paying to reach Israelis for this product right now; long-running + many creative variants + several independent advertisers suggests money is being recovered.
- Does not prove: profit, volume, or that the advertiser is rational (new dropshippers burn money for weeks; agencies leave ads on).
- Misreads: ads targeted at IL by foreign scam stores; one advertiser with 40 creatives launched yesterday (testing, not scaling); the same ad duplicated across placements counted as many ads; library only shows live ads so you never see the failures.
- Recency: use the "started running" date; ignore ads with the low-impression label; re-check after 14 and 30 days - survival is the signal.
- Suggested reading rule: a product counts as "actively scaled" only if >=2 independent Israeli advertisers each have at least one creative running >=30 days AND fresh creatives added in the last 14 days.

**Tier 4 - Attention signals (views, likes, Google Trends, Zap "trending")**
- Proves interest/curiosity. Does not prove purchase or willingness to pay a local price. Viral views are often entertainment, and Hebrew search terms split across spellings. Google Trends is relative (0-100), noisy at Israel's small volume, and must be compared against a stable anchor term over 5 years to separate seasonality from growth.

**Tier 5 - Brand claims ("50,000 happy customers", "sold out 3 times")**
- Proves nothing by itself. Use only as a hypothesis to test against Tiers 1-3.

**Proposed minimum bar for a "serious candidate" (all five required):**
1. At least one Tier-1 signal dated within the last 90 days that is specific to Israel (retailer-reported units, store-internal best-seller position in an Israeli store, or an Israeli-seller marketplace counter that moved between two observations).
2. At least two independent Tier-2/3 signals from different Israeli sellers (e.g. dated Hebrew reviews in the last 60 days on two stores; or two advertisers with >=30-day ads).
3. Not solely event-driven: the signal appears in at least two separate months, or the seasonality is understood and planned for.
4. A local price point observed in the market (Zap median or competitor price) at which landed cost + delivery + VAT + payment fees + realistic ad cost still leaves the target margin. If the observed Israeli market price is below that, reject regardless of demand.
5. A stated reason an Israeli buyer would not simply order it from AliExpress/Temu (see KQ5).
Anything meeting 1-2 of these is a "lead to verify", not a candidate.

### Gaps
- I could not test the Ad Library rules on real Israeli advertisers (403). The thresholds (30 days, >=2 advertisers) are heuristics drawn from marketing blogs, not validated benchmarks.
- No independent source quantifies what share of Israeli buyers leave reviews; the "reviews are a floor" logic is standard practice but the multiplier is unknown.

---

## Key Question 2: Israeli DTC landscape - actual stores/brands selling hero products, with evidence of volume

### Takeaway
I could verify only a handful of Israeli stores at product level, and none of them through ad data; the verified picture is that best-seller lists inside Israeli stores are dominated by either (a) sub-100 ILS accessories and consumables or (b) branded high-ticket beauty devices, while generic mid-priced gadgets are listed by dozens of interchangeable resellers. A proper census of single-product Hebrew Shopify stores still has to be done manually in the Ad Library.

### Cited Findings
- There are 12,324 live Shopify stores in Israel (updated 6 Nov 2026), up 18% year-over-year in Q3 2026 and up from 6,200 in Q4 2023; 245 are Shopify Plus; 97.2% have "unknown" employee count (i.e. tiny). **ESTIMATE** (third-party crawl) - [StoreLeads](https://storeleads.app/reports/shopify/IL/top-stores)
- Shopify itself judged Israeli online revenue "higher than expected" for the market size and opened a Shopify Plus agency route in Israel. **REPORTED** - [Globes](https://en.globes.co.il/en/article-1001466601)
- **Silk'n Israel** (silkn.co.il, Shopify, official brand site; Israeli-origin beauty-device brand). 9 products. Prices today (sale / compare-at, ILS): LED Face Mask 483/690; LED Face Mask PRO 1,032/1,290; LED Face Mask EMS 1,272/1,590; LED Chest Mask PRO 903/1,290; LumiLips 273/390; LumiGlow 203/290; FaceTite 1,592/1,990; Silk'n 7 hair removal 2,650.50/2,790. All product records were created 24 Jun - 13 Oct 2026, i.e. this storefront is new or re-platformed in mid-2026, so on-site history is short. **FACT** - [products.json](https://www.silkn.co.il/products.json?limit=250)
  - Store-internal best-selling order today: 1) LED Face Mask PRO, 2) LED Face Mask, 3) LumiLips, 4) LED Face Mask EMS, 5) LED Chest Mask PRO, 6) FaceTite, 7) Slider Gel, 8) LumiGlow, 9) Silk'n 7 hair removal (last). **FACT** (ranking only; no absolute units; store is ~5 months old) - [best-selling sort](https://www.silkn.co.il/collections/all?sort_by=best-selling)
- **Home IPL hair removal in Israel is brand/importer territory**: Braun Silk-expert Pro 5 listed at 2,190 ILS with a 5-year official-importer warranty; Ulike sold with 2-year "Ulike Israel" warranty; Sensica (Israeli brand, own site sensica.co.il on WooCommerce) and Philips also present. **FACT** (listings) - [Bug Braun](https://www.bug.co.il/brand/braun/pl7432/ipl/5), [Bug Ulike](https://www.bug.co.il/brand/ulike/me/ipl/hair/removal/device), [CWC Braun](https://www.cwc.co.il/?p=22858)
- **NextStock** (nextstock.co.il, WooCommerce, general gadget catalogue, appears as a seller in almost every Zap category I searched; only 16 Zap reviews). Top 25 by store-internal popularity are almost all 19-89 ILS: Lenovo LP40 earbuds 64 (7 reviews), lint/pet-hair brush 39 (6), USB-C cables 19-49, Apple Watch straps/cases 28-50, T9 hair clipper 69, "wonder" shower head 89, ear-wax cleaner 38, balloons 59, LCD drawing board 59; the only item above 100 ILS is a LIGE smartwatch at 179. Review counts are 5-8 per product. **FACT** - [NextStock popularity API](https://nextstock.co.il/wp-json/wc/store/v1/products?orderby=popularity&order=desc&per_page=25)
- **Nuni** (nuni.co.il, WooCommerce, BBQ/grill specialist). Top 25 by popularity are replacement parts and consumables, not grills: Coleman heat diffusers/burners 80 ILS, cast grates 150-180, Ninja Woodfire pellets 22 ILS/kg (three flavours in the top 15), charcoal 89, Ooni pizza stone 319. **FACT** - [Nuni popularity API](https://www.nuni.co.il/wp-json/wc/store/v1/products?orderby=popularity&order=desc&per_page=25)
- **Pet Planet** (petplanet.co.il, WooCommerce pet shop). Top 25 by popularity are entirely consumables: cat treats 4-15 ILS, crystal/soy litter multipacks 120-336 ILS, puppy pads 69 ILS. No gadget in the top 25. **FACT** - [Pet Planet popularity API](https://petplanet.co.il/wp-json/wc/store/v1/products?orderby=popularity&order=desc&per_page=25)
- **WhiteScent Home** (scent.co.il, WooCommerce, home fragrance - not body cream). Top by popularity: closet scent tags 13.90 ILS, room sprays 29-40 ILS, scented candles 125-189 ILS; 12 of the top 25 were out of stock today. Review counts 0-3. **FACT** (stock-outs may be thin inventory rather than demand) - [WhiteScent popularity API](https://www.scent.co.il/wp-json/wc/store/v1/products?orderby=popularity&order=desc&per_page=25)
- **Kravitz** (kravitz.co.il, Shopify, office/stationery chain). Best-selling sort is stationery, but a "robotic litter box for cats" appears at position 3. **FACT** (single observation; could be a promotion artefact) - [Kravitz best-selling](https://www.kravitz.co.il/collections/all?sort_by=best-selling)
- **Ricochet** (tactical/outdoor retailer): reported +113% purchases and ~+115% revenue in tactical shoes ahead of the August 2026 draft; its top pre-enlistment sellers are commando socks, boxers, shirts, tactical pants, belts, pouches (30 Jul 2026). **REPORTED** (company PR, no base numbers) - [Maariv](https://www.maariv.co.il/economy/consumerism/article-1350373)
- **Agilite** (agilitegear.com, Shopify) is an Israeli tactical-gear DTC brand, but its storefront is English/export-oriented. **FACT** (site observed) - [Agilite](https://agilitegear.com/)
- Zap seller-review counts for small generalist resellers that list the gadget categories below: Diofix 2,942; ShipShop 676; Gadget Team 389; BrandsOnSale 397; Kama Zol 236; Gamby Israel 56; SaleCity 17; NextStock 16 (vs. LastPrice 5,912, HaMeir 3,389, Bug 670). **FACT** (counts shown on Zap today) - [Zap search example](https://www.zap.co.il/search.aspx?keyword=%D7%A9%D7%9E%D7%99%D7%9B%D7%AA%20%D7%9B%D7%95%D7%91%D7%93)

### Inferences
- Across three unrelated Israeli WooCommerce stores, the internal best-seller lists are led by consumables, refills and replacement parts, not by the "wow" gadget. Repeat-purchase items tied to an installed base (grill pellets, litter, treats) are what actually accumulate sales counts.
- The generic-gadget reseller layer (NextStock, Kama Zol, Gamby, ShipShop etc.) lists the same AliExpress-type items across many categories with single-digit reviews per product. That is evidence of supply saturation and low per-product volume, not of a winning product.
- Where a brand owns the product and warranty (Silk'n LED masks ~480-1,270 ILS, Braun/Ulike IPL ~2,000+ ILS), Israeli buyers demonstrably pay high prices locally; LED masks out-ranking the IPL flagship inside Silk'n's own store suggests the 500-1,000 ILS beauty-device band is where current pull is, at least for that brand.
- Do not infer that Silk'n's brand strength means each product sells: the IPL device ranks last in its own store.

### Gaps
- **No verified list of single-product Hebrew DTC stores with Meta ad longevity.** Ad Library was inaccessible; search engines did not surface these stores. This must be done manually: Ad Library, country IL, keywords such as "משלוח חינם", "אחריות", "מבצע", then apply the KQ1 rules.
- No operating-age data for the small stores except Silk'n's storefront dates; WHOIS/first-review dates not collected.
- No Trustpilot/Google-review, Facebook-group or Similarweb data (blocked).
- Sensica's own best-seller ranking could not be read (API returned non-JSON).

---

## Key Question 3: Israeli demand data (marketplaces, retailers, press 2025-2026)

### Takeaway
The hard numbers available are at channel and category level: Chinese platforms take about three-quarters of Israeli online orders, local sites win on electronics/home and in crisis periods, and the only product-level unit figures published are for emergency-power items during the 2025 and 2026 Iran escalations. Product-level "best-seller" articles in the Israeli press are mostly unsourced.

### Cited Findings
- AliExpress, Temu and Shein together accounted for about 75% of Israelis' online orders in June 2026; Amazon ~6%. KSP was the top local site with 18% of orders among the top-20 local sites; in May 2026 the top three local sites were KSP, Super-Pharm, Shufersal (Shop Analytics, published 23 Aug 2026). **REPORTED** - [Globes](https://en.globes.co.il/en/article-1001553175)
- First half of March 2026 vs first half of February 2026 (Iran war): orders on selected Israeli sites +23% on average, on major international sites -52% (Shein -79%, Amazon -75%, Temu -68%, AliExpress -38%, iHerb -23%). Israeli winners: ACE +75% (computer chairs, inflatable mattresses, bed bases, table football), Delta +54% (pyjamas/underwear), Terminal X +49%, Fox +30%, KSP +30% (chargers, batteries, flashlights, board game), Wolt +22%, Shufersal +14%. Methodology/sample not disclosed. **REPORTED** - [Globes, 23 Mar 2026](https://en.globes.co.il/en/article-1001538233)
- 52.8 million parcels arrived in Israel from overseas sites in 2025. **REPORTED** (via coverage of the VAT debate; primary source not opened) - [Ynetnews](https://www.ynetnews.com/business/article/r1iu3almwe)
- Wolt/Kantar 2025 report (n=2,006 online buyers, published 31 Dec 2025): 78% bought online in the year, 61% at least monthly; categories bought online - fashion 90%, restaurant food 90%, electronics 75%, supermarket 69%, toys 66%, pharmacy 47%; 26% bought a product after an influencer recommendation (70% among those who follow influencers); 42% are in coupon/Telegram deal groups; 40% ordered a gift online and 70% of them spent over 200 ILS; 40% say they increased purchases from local businesses since 7 Oct 2023. **REPORTED** - [ICE](https://www.ice.co.il/consumerism/news/article/1098033)
- Emergency power, week to 16 Jun 2025 (Mahsanei Hashmal chain): about 800 generators, about 2,500 high-capacity power banks and about 1,000 battery radios sold in one week; generators sold out. Kravitz: portable power stations demand up >150% and out of stock; water bottles +~60%; DIY/hobby nearly doubled. **REPORTED** (retailer PR, single week) - [ICE, 16 Jun 2025](https://www.ice.co.il/consumerism/news/article/1069846)
- March 2026 (Mahsanei Hashmal, 73 branches): online sales +~70% vs the same period a year earlier; freezers +80-90%, laptops/tablets ~+100%, robot vacuums/moppers +~15%, air conditioners -30%. **REPORTED** - [ICE, 18 Mar 2026](https://www.ice.co.il/consumerism/news/article/1106702)
- Air-conditioner market weak: Tadiran AC sales in Q3 2025 were 266m ILS, down 16.5% y/y; Electra Consumer Products' AC revenue fell to 154m from 167m ILS in Q1 2026; importers discounting by tens of percent. **REPORTED** - [Calcalist](https://www.calcalist.co.il/article/r1t0mzpnmg)
- ICE "best-selling products in Israel 2026" (26 Oct 2026) lists robot/cordless vacuum-mops (Dreame, Roborock, Dyson), multi-basket Ninja air fryers, home ice-cream makers, multi-stylers (Dyson Airwrap, Shark FlexStyle), mini projectors, R36S handheld consoles, GaN chargers/power banks (Anker, Baseus), running shoes, compact car jump starters, rechargeable tyre inflators, vacuum-compression backpacks. It cites "sales data" but names no source and gives no numbers. **UNVERIFIED** (reads like affiliate/advertorial content) - [ICE](https://www.ice.co.il/consumerism/news/article/1135127)
- Zap homepage "popular/trending" today is dominated by iPhone 17, Galaxy S26, PS5, AirPods Pro 3, Ninja electric grills (AG653, Woodfire, DG553, EG203), Makita garden tools, dehumidifiers, garden furniture. **FACT** (attention signal, big-ticket bias) - [Zap](https://www.zap.co.il/)
- Zap supply/price scan, 2026-11-11 (number of listings; min / median / max price in ILS of first page; **FACT** as observed, supply-side only - URL pattern `https://www.zap.co.il/search.aspx?keyword=<term>`):

| Hebrew term | Listings | Min / median / max ILS | Note |
|---|---|---|---|
| קומקום שבת (Shabbat kettle/urn) | 635 | 53 / 178 / 699 | 24 catalogued models - mature category |
| כרית ישיבה (seat cushion) | 461 | 160 / 286 / 5,059 | includes medical cushions |
| מפיץ ריח (scent diffuser) | 371 | 35 / 75 / 199 | low price point |
| מתקן ייבוש כביסה חשמלי (heated drying rack) | 338 | 158 / 279 / 549 | bulky |
| רעש לבן (white noise) | 229 | 98 / 178 / 1,769 | baby sleep |
| מנורת שבת (Shabbat lamp) | 153 | 54 / 160 / 208 | |
| כרית אורטופדית (orthopedic pillow) | 148 | 108 / 233 / 499 | |
| פנס חירום נטען (rechargeable emergency light) | 121 | 25 / 111 / 351 | |
| משאבת אוויר נטענת (cordless inflator) | 75 | 188 / 239 / 699 | 18 sellers on page 1 |
| רדיו חירום (emergency radio) | 55 | 149 / 279 / 528 | |
| שמיכת כובד (weighted blanket) | 51 | 74 / 118 / 530 | price floor very low |
| מאוורר צוואר (neck fan) | 28 | 65 / 98 / 239 | JisuLife branded at 225-239 |
| מסכת לד (LED mask) | 27 | 45 / 1,244 / 1,706 | branded devices dominate |
| מסרק מחליק (straightening brush) | 22 | 25 / 112 / 400 | |
| מסיר שיער לחיות (pet hair remover) | 20 | 20 / 69 / 148 | |
| מסנן מקלחת (shower filter) | 18 | 110 / 205 / 430 | few sellers; Biocera, KDF; water-filter specialists |
| מאכיל אוטומטי (auto feeder) | 15 | 69 / 239 / 799 | |
| מעסה צוואר (neck massager) | 9 | 59 / 108 / 1,259 | |
| מתנע חירום (jump starter) | 2 | 349 / 698 | term mismatch likely |

- Israeli pet-supplies e-commerce estimated at about US$257m in 2025 with 10-15% growth; Euromonitor describes "pet humanisation" and a growing cat population; Statista is more pessimistic on pet food. **ESTIMATE** (gated reports; sources disagree) - [ECDB](https://ecdb.com/resources/sample-data/market/il/pet-supplies), [Euromonitor](https://www.euromonitor.com/pet-care-in-israel/report)
- Israel Post expected parcel deliveries to rise 30-40% in November; AliExpress expected more than 20 million packages in the Singles' Day month (date of article not confirmed). **REPORTED** - [Ynetnews](https://www.ynetnews.com/business/article/bkkoyemnml)

### Inferences
- With ~75% of orders going to Chinese platforms, any product whose only selling point is "cheap gadget" is already bought there; the local opportunity is in what those platforms do badly (KQ5).
- Zap listings counts are supply, not demand. Hundreds of listings at a low median price (scent diffusers 75 ILS, weighted blankets 118 ILS) signal commoditisation. Few listings at a high median (shower filters 205 ILS from specialist sellers; LED masks 1,244 ILS) signal either an unproven niche or a brand-protected one.
- The only product family with published unit sales in Israel in 2025-2026 is emergency power/communication, and those numbers are single-week spikes at a 70+-branch chain.

### Gaps
- No Zap year-end summary, no KSP/Ivory/Super-Pharm bestseller lists (blocked or not found). No AliExpress/Temu Israel bestseller reporting for 2025-2026 beyond the unsourced ICE piece.
- No Google Trends Israel data at all (429).
- Several Zap terms returned zero because Zap redirected to a category page my parser did not read (mosquito killer, bidet, air mattress, dehumidifier, air purifier, dash cam, baby carrier, baby monitor, posture corrector, massage gun, cat fountain). Absence here is NOT evidence of no supply.
- Shop Analytics does not publish (free) category or product breakdowns.

---

## Key Question 4: Israel-specific demand drivers and the product types they create

### Takeaway
The best-evidenced Israel-specific driver in 2025-2026 is security/emergency preparedness (documented unit sales and stock-outs, twice), followed by military service (retailer-reported surges) and a clear crisis-time shift to local sites; climate, religious-calendar and hard-water drivers are plausible but I found supply evidence rather than demand evidence for them.

### Cited Findings
- Emergency preparedness: unit sales and stock-outs of generators, power banks, radios and power stations in June 2025; chargers, batteries and flashlights among KSP's growth items in March 2026; ACE sold inflatable mattresses and computer chairs for shelter/home stays. **REPORTED** - [ICE Jun 2025](https://www.ice.co.il/consumerism/news/article/1069846), [Globes Mar 2026](https://en.globes.co.il/en/article-1001538233)
- 3.2 million Israelis (33.6%) live without adequate shelter protection per a State Comptroller report of January 2026, as cited by a real-estate site (secondary source). **REPORTED** (secondary) - [Klikatnadlan](https://klikatnadlan.co.il/mamadapartmentsisrael2026/)
- Military service: Ricochet +113% tactical shoes before the August 2026 draft (see KQ2). Kourt reported a fourfold weekly rise in soldier care-package orders with an average package value above 200 ILS after leave was cut. Tactical shops reported the "Mashiach" patch selling out in October 2026; one manager said a normal month is ~10 online and ~20 in-store units of that patch. **REPORTED** (company statements) - [Maariv](https://www.maariv.co.il/economy/consumerism/article-1350373), [Walla](https://finance.walla.co.il/item/3629762), [Bhol](https://www.bhol.co.il/news/1728207)
- Gifts: 40% ordered a gift online; 61% of those chose a gift card; 70% spent over 200 ILS on gifts (Wolt/Kantar 2025). **REPORTED** - [ICE](https://www.ice.co.il/consumerism/news/article/1098033)
- Heat: the AC market shrank in 2025-early 2026 (Tadiran -16.5% in Q3 2025; Mahsanei Hashmal AC -30% in March 2026) - household saturation and construction slowdown cited. **REPORTED** - [Calcalist](https://www.calcalist.co.il/article/r1t0mzpnmg), [ICE](https://www.ice.co.il/consumerism/news/article/1106702)
- Hard water: desalinated water now supplies over 50% of Israeli tap consumption; desalinated water is stabilised to about 80-120 mg/L as CaCO3, i.e. moderately soft; National Water Carrier water carries 20-25 mg/L magnesium vs virtually none in desalinated water. So "Israel has hard water" is regionally true but not uniformly. **REPORTED** (academic) - [Rosen et al. abstract](https://ui.adsabs.harvard.edu/abs/2018Desal.426...88R), [HUJI](https://cris.huji.ac.il/en/publications/new-desalinated-drinking-water-regulations-are-met-by-an-innovati/)
- Shabbat/kosher: 635 Zap listings for Shabbat kettles and 153 for Shabbat lamps; Bug lists a Shabbat hot plate at 99 ILS with Tzomet approval; a Haredi news site promotes an urn with automatic boil-to-Shabbat mode. **FACT** (listings) / **REPORTED** (product PR) - [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%A7%D7%95%D7%9E%D7%A7%D7%95%D7%9D%20%D7%A9%D7%91%D7%AA), [Bug](https://www.bug.co.il/פלטה-חשמלית-לשבת-novo-90615455), [Bhol](https://www.bhol.co.il/news/1133687)
- High local prices: the Finance Ministry justified raising the import VAT exemption by citing consumer prices higher than most of Europe; 92% of Israelis reported a cross-border purchase in a 2022 RetailX survey vs 71% globally. **REPORTED** (2022 data is old) - [Times of Israel](https://www.timesofisrael.com/vat-exemption-on-personal-imports-to-rise-from-75-to-150/), [FedEx](https://www.fedex.com/en-nl/small-business-hub/market-insights/spotlight-on-israel.html)
- Pets: see KQ3 (ECDB ~US$257m online, growth 10-15%, estimate). A cited but unverified population figure is ~1.5m dogs and ~2.5m cats. **ESTIMATE / UNVERIFIED** - [Ken Research](https://www.kenresearch.com/israel-animal-health-and-veterinary-services-market)

### Inferences
- Persistent (not just spike) demand most plausibly sits in: backup power and lighting for the home/safe room; soldier and reservist basics and gift packs; Shabbat-compliant small appliances; pet consumables; baby/sleep items for a young population; winter laundry drying and damp control in small apartments.
- Emergency demand is real but arrives in spikes during which big chains sell out and imports are disrupted - a small seller holding local stock benefits, one relying on air shipments from China does not (international orders fell 38-79% in March 2026).
- Cooling products are a weak bet on the evidence found: the AC category is declining and neck fans are a 65-240 ILS commodity.
- The hard-water/limescale pitch needs city-level targeting; in desalination-fed areas the claim is weaker.

### Gaps
- No sales data found for Pesach/Rosh Hashana/Hanukkah product categories, Shabbat appliances, baby products or summer items - only listings.
- No data on apartment-size-driven products (storage, folding furniture).
- Pet ownership figures are not from an official source.

---

## Key Question 5: Where Israeli sellers have a genuine advantage over AliExpress/Temu

### Takeaway
The documented advantages are delivery certainty and trust (the top two shopper fears), anything priced above the US$75 VAT-free import threshold, products needing warranty/standards/Hebrew support, bulky items, and crisis periods when cross-border logistics fail; but AliExpress is closing the gap with local warehouses, 7-10 day delivery, free returns and a "Ship from Israel" seller programme.

### Cited Findings
- Top fears of Israeli online shoppers: product not arriving or low quality 69%, delivery delays 56%; 72% check reviews before every purchase. **REPORTED** - [ICE / Wolt-Kantar](https://www.ice.co.il/consumerism/news/article/1098033)
- Shop Analytics CEO: Israelis "prefer to buy locally and safely, even if the price is slightly higher" during uncertainty; local orders +23% while international -52% in March 2026. **REPORTED** - [Globes](https://en.globes.co.il/en/article-1001538233)
- VAT threshold history: raised from $75 to $150 on 24 Dec 2025; Knesset revoked it 59-25 on 24 Feb 2026, back to $75; a later ministerial order for $130 was also cancelled, returning to $75, with 18% VAT charged on the full value of parcels above $75. The Oct 2026 ICE article also refers to a $75 threshold. Status has flipped several times - re-check before relying on it. **REPORTED** - [Times of Israel, 24 Feb 2026](https://www.timesofisrael.com/knesset-revokes-measure-that-made-more-online-purchases-tax-exempt/), [Ynetnews](https://www.ynetnews.com/business/article/b1excwnxmg), [ICE](https://www.ice.co.il/consumerism/news/article/1135127)
- AliExpress in Israel: about 45 distribution points (April 2026), delivery cut to 7-10 days in some cases; "Elite" club with free returns within 15 days; free doorstep shipping over $45. **REPORTED** - [Globes](https://en.globes.co.il/en/article-1001553175), [Ynetnews](https://www.ynetnews.com/business/article/hjqsvialkx)
- AliExpress opened its marketplace to Israel-registered businesses with a "Ship from Israel" label; initial categories: home appliances, consumer electronics, automotive electronics, office supplies, mother-and-baby, FMCG. Commission and seller numbers not disclosed; article date not shown. **REPORTED** - [Ynetnews](https://www.ynetnews.com/business/article/ryqj93xtze)
- Amazon has struggled in Israel (~6% of orders); KSP's appeal is multi-brand parallel import at low prices; price comparison is quick in a small market. **REPORTED** - [Globes](https://en.globes.co.il/en/article-1001553175)
- Standards: since 1 Jan 2025 a "European route" lets importers rely on EU compliance for many products, but high-risk products (certain electrical appliances, toys, PPE) still need Israeli lab testing/model approval; sources disagree on scope. **REPORTED** - [Herzog law](https://herzoglaw.co.il/en/news-and-insights/what-is-good-for-europe-is-good-for-israel-reform/), [US ITA](https://www.trade.gov/country-commercial-guides/israel-trade-standards), [Kohelet](https://www.kohelet.org.il/en/?p=9632)
- Warranty as a selling point in practice: Braun IPL sold with "5 years official importer warranty", Ulike with 2-year local warranty, Ring doorbell at 299 ILS with 1-year warranty and free shipping. **FACT** (listings) - [Bug](https://www.bug.co.il/brand/braun/pl7432/ipl/5), [Bug Ring](https://www.bug.co.il/brand/ring/battery/doorbell)
- Local prices of generic items are far above AliExpress-type prices yet still listed by many sellers, e.g. neck fans 65-239 ILS, emergency radios 149-528 ILS, cordless inflators 188-699 ILS. **FACT** (Zap listings; AliExpress comparison prices not collected) - [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%A8%D7%93%D7%99%D7%95%20%D7%97%D7%99%D7%A8%D7%95%D7%9D)

### Inferences
- Categories where buying locally despite a higher price is best supported: mains-powered or battery products where safety/warranty matters; items above the $75 import threshold (import adds 18% VAT on the whole value plus handling); bulky/heavy goods; urgent-need items (emergency, pre-enlistment, gifts with a date); consumables and compatible spare parts needed quickly; items where a Hebrew explanation or kashrut/Shabbat approval is part of the value.
- Categories where a local reseller has no defensible edge: sub-100 ILS small accessories and generic gadgets with no urgency - exactly what tops NextStock's list at 19-89 ILS, where a paid-ads model cannot cover acquisition cost.
- The current UV toothbrush steriliser at 129 ILS sits in the weak zone: below the VAT threshold, small, non-urgent, easily found on Chinese platforms.
- "Ship from Israel" on AliExpress is both a threat (local-speed competitors inside the dominant app) and a possible extra sales channel.

### Gaps
- No survey directly asking Israelis which categories they prefer to buy locally and why.
- Scope of the standards reform for specific small appliances and the plug requirement was not confirmed.
- AliExpress Israeli-seller commission/terms unconfirmed (an unofficial-looking page claims 0% commission and ILS settlement - **UNVERIFIED**: [il-ecom-v2.pages.dev](https://il-ecom-v2.pages.dev/en/sell/faq)).

---

## Key Question 6: Cautionary tales - scandals, enforcement, saturation

### Takeaway
Israeli regulators have fined online stores hundreds of thousands to about 2 million ILS for late delivery and refused cancellations - the exact failure mode of long-shipping dropshipping - while the press and the Israel Internet Association actively teach consumers to reverse-image-search products against AliExpress/Temu. The seller base has roughly doubled in three years, and fad products rise and die within months.

### Cited Findings
- Consumer Protection Authority cases against online stores (search-level summaries; I did not open each article, and dates were not shown): intended fine of about 1.82m ILS for undelivered orders and ignored cancellations; about 413,000 ILS against Walla Shops for missed delivery dates; about 2m ILS against "Get It" over refunds not paid and late shipping; a case against homestyle.co.il for misleading delivery times. **REPORTED** (article-to-case mapping not verified) - [ICE law 1029435](https://www.ice.co.il/law/news/article/1029435), [ICE law 1031496](https://www.ice.co.il/law/news/article/1031496), [Walla 3553916](https://finance.walla.co.il/item/3553916), [Walla 3690268](https://finance.walla.co.il/item/3690268), [Walla 3708488](https://finance.walla.co.il/item/3708488)
- Consumers may be owed compensation for late delivery under section 18A of the Consumer Protection Law (conditions apply). **REPORTED** - [Walla 3835289](https://finance.walla.co.il/item/3835289)
- Israel Hayom describes Israeli sites that sell cheap products and then order them from AliExpress for the customer ("dropshipping"), framing it as paying more for cheap goods. **REPORTED** (from search summary; page returned 403 on direct fetch) - [Israel Hayom](https://www.israelhayom.co.il/lifestyle/shopping/article/18147166)
- Israel Internet Association / Bizportal: scams start from sponsored ads on Instagram, Facebook and Google; advice to reverse-image-search - "if the product is on AliExpress or Temu far cheaper, it is probably a scam"; fake stores use Israeli phone numbers and names. **REPORTED** - [Bizportal](https://www.bizportal.co.il/general/news/article/20013928), [Ynet](https://www.ynet.co.il/economy/article/sjdgrtykyl)
- "Abazol", a site linking Israelis to AliExpress sellers, was exposed for falsely presenting a well-known businessman as CEO; it denied delivery problems. Date not confirmed. **REPORTED** - [Mako](https://www.mako.co.il/finances-consumer/Article-e846842a08bd571027.htm)
- Large players failed too: Azrieli, Melisron and Shufersal shut their marketplace operations in December 2023; Azrieli reportedly lost about 300m ILS and Melisron about 100m ILS. **REPORTED** - [Globes](https://en.globes.co.il/en/article-1001553175)
- The former deal site domain baligam.co.il today serves a coupon aggregator ("המרכז הישראלי לקופונים"). **FACT** (observed 2026-11-11) - [baligam.co.il](https://www.baligam.co.il/)
- Fads: the "clicker" digital counter became a school craze in early 2025 and then vanished, per an Israel Hayom piece on five trends that peaked and disappeared. **REPORTED** (search summary only; page 403) - [Israel Hayom](https://www.israelhayom.co.il/tech/gadget-review/article/20729620)
- Seller-side saturation: Israeli Shopify stores grew from 6,200 (Q4 2023) to 12,324 (Nov 2026). **ESTIMATE** - [StoreLeads](https://storeleads.app/reports/shopify/IL/top-stores)
- A Hebrew product-research vendor blog itself quotes Reddit sentiment that copying an already "winning" product is no longer profitable. **REPORTED** (vendor content, low reliability) - [Thunderbit](https://thunderbit.com/he/blog/how-to-find-winning-dropshipping-products-early)

### Inferences
- Shipping from China to the customer after the order is both a legal exposure (delivery-date and cancellation rules are enforced with six- and seven-figure fines) and a trust problem (consumers are told to image-search). Holding stock in Israel is close to a prerequisite.
- Product types that look saturated on the evidence gathered: phone/watch accessories, generic neck fans, weighted blankets, scent diffusers, generic massagers - many sellers, low medians, single-digit reviews.
- Novelty items without a lasting problem to solve follow the clicker pattern.

### Gaps
- No documented case naming a specific Israeli dropshipping store fined or exposed in 2025-2026; the enforcement cases found concern larger online retailers and dates were not confirmed.
- No access to Facebook-group complaints or consumer forums.

---

## Key Question 7: Shortlist of product candidates with Israeli demand signals, and rejections

### Takeaway
No product reaches the proposed "serious candidate" bar on the evidence I could access (mainly because ad-longevity and dated-review checks were not possible); the list below is a ranked set of leads to verify, graded by the evidence actually found. The strongest leads combine an Israel-specific driver, a local price above ~200 ILS, and a reason not to buy from China.

Evidence grades: **A** = Israel-specific unit sales reported; **B** = retailer-reported surge or store-internal best-seller rank; **C** = supply/price evidence only; **D** = unsourced mention.

### Cited Findings
Leads (all need the KQ1 checks before any commitment):

1. **Home/safe-room backup power and light kit** (high-capacity power bank, rechargeable emergency lights, battery/crank radio, possibly bundled). Grade **A** for spike demand, unproven between spikes. ~2,500 power banks and ~1,000 radios in one week at one chain (Jun 2025); chargers/batteries/flashlights drove KSP growth (Mar 2026). Local prices: radios 149-528 ILS (median 279), emergency lights median 111 ILS. Risk: event-driven, big chains and KSP dominate, stock must be local before the spike. - [ICE](https://www.ice.co.il/consumerism/news/article/1069846), [Globes](https://en.globes.co.il/en/article-1001538233), [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%A8%D7%93%D7%99%D7%95%20%D7%97%D7%99%D7%A8%D7%95%D7%9D)
2. **Soldier / reservist essentials and gift packs** (commando socks, belts, pouches, patches, care packages). Grade **B**. Ricochet +113% tactical shoes; Kourt 4x care packages at >200 ILS average; patch sell-outs Oct 2026 (but baseline only ~10 online units/month for one patch at one shop). Risk: established specialists, IDF-approval/quality expectations, sensitivity of the theme. - [Maariv](https://www.maariv.co.il/economy/consumerism/article-1350373), [Walla](https://finance.walla.co.il/item/3629762), [Bhol](https://www.bhol.co.il/news/1728207)
3. **LED light-therapy face mask (beauty device, 400-1,000 ILS band)**. Grade **B**. #1 and #2 best-sellers in Silk'n Israel's store at 1,032 and 483 ILS; Zap median 1,244 ILS across 27 listings. Risk: single-store ranking of a 5-month-old storefront; brand and warranty carry the price; health/efficacy claims and device regulation not checked. - [Silk'n](https://www.silkn.co.il/collections/all?sort_by=best-selling), [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%A1%D7%9B%D7%AA%20%D7%9C%D7%93)
4. **Consumables and compatible parts for appliances Israelis already own** (Ninja Woodfire pellets, grill parts; by extension robot-vacuum filters/pads, air-fryer accessories). Grade **B**. Parts and pellets fill Nuni's popularity top-25; Ninja grills trend on Zap; robot vacuums +15% at Mahsanei Hashmal. Repeat purchase, compatibility knowledge and speed are a local edge. - [Nuni](https://www.nuni.co.il/wp-json/wc/store/v1/products?orderby=popularity&order=desc&per_page=25), [Zap](https://www.zap.co.il/), [ICE](https://www.ice.co.il/consumerism/news/article/1106702)
5. **Pet repeat-purchase items and higher-ticket pet devices** (litter, pads; automatic litter box, feeder). Grade **B/C**. Consumables fill Pet Planet's top-25; robotic litter box is #3 in Kravitz's best-selling sort; feeders 69-799 ILS (median 239). Risk: consumables are heavy and low-margin; specialist chains compete. - [Pet Planet](https://petplanet.co.il/wp-json/wc/store/v1/products?orderby=popularity&order=desc&per_page=25), [Kravitz](https://www.kravitz.co.il/collections/all?sort_by=best-selling), [ECDB](https://ecdb.com/resources/sample-data/market/il/pet-supplies)
6. **Shower filter with replaceable cartridge**. Grade **C**. Only 18 Zap listings, sold by water-filter specialists at 110-430 ILS (median ~205), with cartridges at 179 ILS - a recurring-revenue structure and few generalist competitors. Risk: no demand evidence found; hard-water claim is regional; health/hair claims invite scrutiny. - [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%A1%D7%A0%D7%9F%20%D7%9E%D7%A7%D7%9C%D7%97%D7%AA)
7. **Shabbat-compliant small appliances / lighting** (Shabbat lamp, kettle/urn with Shabbat mode, hot plate). Grade **C**. 635 and 153 Zap listings; median 160-178 ILS; approvals (Tzomet) are a trust asset AliExpress lacks. Risk: mature, price-compared category; electrical standards. - [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%A0%D7%95%D7%A8%D7%AA%20%D7%A9%D7%91%D7%AA), [Bug](https://www.bug.co.il/פלטה-חשמלית-לשבת-novo-90615455)
8. **Heated / electric clothes-drying rack**. Grade **C**. 338 listings, median 279 ILS; bulky and mains-powered, so local delivery and warranty matter; seasonal (winter). - [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%AA%D7%A7%D7%9F%20%D7%99%D7%99%D7%91%D7%95%D7%A9%20%D7%9B%D7%91%D7%99%D7%A1%D7%94%20%D7%97%D7%A9%D7%9E%D7%9C%D7%99)
9. **Orthopedic pillow / seat cushion**. Grade **C**. 148 and 461 listings; medians 233 and 286 ILS; bulky; specialist retailers exist. - [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9B%D7%A8%D7%99%D7%AA%20%D7%90%D7%95%D7%A8%D7%98%D7%95%D7%A4%D7%93%D7%99%D7%AA)
10. **Baby sleep aid / white-noise device**. Grade **C**. 229 listings, median 178 ILS; toys are bought online by 66% of online shoppers (category-level only). - [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%A8%D7%A2%D7%A9%20%D7%9C%D7%91%D7%9F), [ICE](https://www.ice.co.il/consumerism/news/article/1098033)
11. **Car emergency: cordless tyre inflator / jump starter**. Grade **C/D**. Inflators: 75 listings, 18 sellers, median 239 ILS; named in the unsourced ICE list. Risk: already crowded with tool brands (Stanley, Makita). - [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%A9%D7%90%D7%91%D7%AA%20%D7%90%D7%95%D7%95%D7%99%D7%A8%20%D7%A0%D7%98%D7%A2%D7%A0%D7%AA), [ICE](https://www.ice.co.il/consumerism/news/article/1135127)

Rejected, with reasons:
- **Phone/watch accessories, cables, small generic gadgets** - they top NextStock's list but at 19-89 ILS with 5-8 reviews; no margin for paid acquisition, fully available on Chinese platforms. - [NextStock](https://nextstock.co.il/wp-json/wc/store/v1/products?orderby=popularity&order=desc&per_page=25)
- **Neck fans / personal cooling** - 65-239 ILS commodity, seasonal, and the wider cooling market is declining. - [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%90%D7%95%D7%95%D7%A8%D7%A8%20%D7%A6%D7%95%D7%95%D7%90%D7%A8), [Calcalist](https://www.calcalist.co.il/article/r1t0mzpnmg)
- **Weighted blankets** - price floor 74 ILS, median 118 ILS, heavy to ship. - [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%A9%D7%9E%D7%99%D7%9B%D7%AA%20%D7%9B%D7%95%D7%91%D7%93)
- **Generic scent diffusers** - 371 listings at a 75 ILS median. (Premium home-fragrance brands are a different, brand-led business.) - [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%A4%D7%99%D7%A5%20%D7%A8%D7%99%D7%97)
- **Home IPL hair removal** - 2,000+ ILS, owned by Braun/Philips/Ulike/Sensica with multi-year importer warranties; ranks last in Silk'n's own store. - [Bug](https://www.bug.co.il/brand/braun/pl7432/ipl/5), [Silk'n](https://www.silkn.co.il/collections/all?sort_by=best-selling)
- **Robot vacuums, air fryers, multi-stylers, projectors, handheld consoles** - demand is real but belongs to KSP/chains/parallel importers competing on price. - [Globes](https://en.globes.co.il/en/article-1001553175), [ICE](https://www.ice.co.il/consumerism/news/article/1135127)
- **Generators / large power stations** - bulky, regulated, spike-only, chains sell out first. - [ICE](https://www.ice.co.il/consumerism/news/article/1069846)
- **Air conditioners / portable AC** - declining market, deep discounting. - [Calcalist](https://www.calcalist.co.il/article/r1t0mzpnmg)
- **Novelty fads (clicker-type)** - peak and vanish within months. - [Israel Hayom](https://www.israelhayom.co.il/tech/gadget-review/article/20729620)
- Not researched by instruction: scented body cream, pheromone cream.

### Inferences
- The common thread in the stronger leads: local median price well above 200 ILS (or a repeat-purchase stream), a trust/urgency/compatibility reason to buy locally, and an Israel-specific driver. The current 129 ILS UV steriliser has none of the three.
- Leads 1-5 have at least one Tier-1/2-type Israeli signal; leads 6-11 rest on supply and price observation only and should be treated as hypotheses.
- The cheapest validation path is the three free checks that worked today (Shopify best-selling sort, Woo popularity API, Zap price/seller scan) applied to 10-20 named competitor stores per lead, followed by a manual Ad Library pass.

### Gaps
- None of the leads has verified ad-longevity, dated Hebrew review velocity, or AliExpress landed-cost comparison - so margin after all costs is untested for every one.
- No evidence gathered for several niches named in the brief: kitchen gadgets, cleaning tools, kids' toys, fitness, posture/pain devices, holiday items, security cameras. Their absence from the shortlist reflects lack of data, not a negative finding.
- Seasonality could not be measured without Google Trends.
