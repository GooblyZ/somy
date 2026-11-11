# Deep dive + adversarial review: (1) filtered shower head with refill cartridges, (2) recurring home consumables (washing-machine cleaner tablets, appliance parts/consumables) — Israel, as of 2026-11-11

Labels: **FACT** = read directly on the primary page/feed/official source in this session (date of reading 2026-11-11 unless stated); **REPORTED** = secondary source or a seller's own unaudited claim; **ESTIMATE** = my inference/calculation; **UNVERIFIED** = could not be checked. In the unit-economics table inputs are labelled VERIFIED / REPORTED / ASSUMPTION as requested.

Method notes (what worked and what did not):
- Worked: Meta Ad Library (country IL, active ads, keyword search, headless Chromium, logged-out view); Shopify `/products.json` feeds of Israeli competitors; Zap.co.il search; Home Center search; AliExpress search pages; Mei Avivim (Tel Aviv water corporation) site; Israeli drinking-water regulations on Hebrew Wikisource; Bank of Israel FX API; WebSearch/WebFetch for US sources.
- **Blocked / could not be read (no guessing):** Google Trends (HTTP 429 on every attempt, 3 separate runs); Shein Israel (captcha challenge); Temu (login wall); KSP (403, geo-blocked from US IP); Shufersal, Super-Pharm, Rami Levy, Yeinot Bitan online (bot walls); ACE (search returned 0 results); gov.il pages (Cloudflare challenge); Alibaba, Made-in-China, Global Sources, CJ Dropshipping search pages (captcha/403/429); newhorizon.co.il (Cloudflare). Hebrew web search engines (Bing/DDG/Google) were also blocked from the headless browser, and the WebSearch tool is US-only and returned almost no Israeli pages — so Israeli forum/press discussion could NOT be surveyed.
- AliExpress pages were served in USD to a US IP; prices shown are therefore **not confirmed as delivered-to-Israel prices**. Many $0.33–$1.09 prices are "new shopper"/"Dollar Express" promos, not regular prices.
- Meta Ad Library counts are the library's own "about N results" for a keyword; my per-advertiser parsing covers only ads that loaded while scrolling. Impressions/spend are not shown for commercial ads. Mid-November is the 11.11/Black-Friday window, so the number of fresh ads is seasonally inflated.

---

## 1. Israeli competition and prices — who already sells this in Israel?

### Takeaway
The "no Israeli evidence" premise of round 1 is wrong for both candidates. Filtered shower heads are already sold by at least **7 Israeli-facing advertisers** (one, SilQ, active since Feb 2024 with ~16 SKUs and a refill range; four more launched or started advertising between June and November 2026), at **189–430 ILS for the head and 65–179 ILS per refill**. Washing-machine cleaner tablets are being pushed hard by at least two Hebrew DTC stores (Relivia since May 2026, Fizz since July 2026) at **140–150 ILS per pack**, while a generic equivalent is listed on Zap at **35 ILS with free shipping** and Durgol liquid at 30–55 ILS. Appliance consumables (Tami4-compatible filters, Roborock kits) are a mature price-comparison category with many specialist sellers.

### Cited Findings — filtered shower heads (Israel)
- FACT: **SilQ** (silqisrael.com, Shopify). 16 products. Oldest products created 2024-02-09 ("Little Q" sink filter, 189 ILS) and 2024-05-16 ("Q head" shower head). Q head 379–395 ILS (compare-at 499); "Black Q" 399; "Qrain" rain head 349; rain-head filter capsule 395; newest "Qhead" sprinkler 379–399 (created 2026-03-26). Refills: vitamin-C scented cartridge 95 ILS (compare-at 190), anti-scale cartridge 79 (compare-at 159), "replacement cartridge" 129, Qrain refill 65, Little Q refill set 189. New scents added Aug–Sep 2026 (lavender, jasmine, peach) — i.e. the range is still being extended — [SilQ products feed](https://silqisrael.com/products.json?limit=250)
- FACT: SilQ Q-head page shows structured-data rating 4.8 with **179 reviews**, and the on-page claim "over 5,000 satisfied Israeli women" (REPORTED, seller claim). Recommends replacing filters every 3 months; **no subscription** (no selling plan; `requires_selling_plan:false`, empty allocations) — instead an automatic 50% discount on a refill when bought with the head. Free shipping nationwide. — [SilQ Q head](https://silqisrael.com/products/q-head)
- FACT: SilQ's on-page claims: "removes chlorine, heavy metals, rust and chemicals", "turns hard water into soft water", "prevents ... hair loss and dandruff", "doubles water pressure and saves 25%", and a reference to a strict "NSF" standard for removing 99% of chlorine — [SilQ Q head](https://silqisrael.com/products/q-head). These are the same claim types being litigated against Jolie in the US (section 7).
- FACT: SilQ Meta ad "SilQ Qhead ראש מקלחת מסנן #1 בישראל" active since 13 Jul 2026 — [Meta Ad Library IL, "ראש מקלחת מסנן"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A8%D7%90%D7%A9%20%D7%9E%D7%A7%D7%9C%D7%97%D7%AA%20%D7%9E%D7%A1%D7%A0%D7%9F&search_type=keyword_unordered)
- FACT: **Care Filter** (carefiltershop.com, Shopify). Oldest product created 2024-07-18 ("Pure" filtered shower head, 369.90 ILS, compare-at 499.90); refill for shower head 99.90; filtering rain head 379.90 (created May 2025), its refill 69.90–89.90; "PureSink" basin filter 349.90 (Jul 2026). — [Care Filter products feed](https://carefiltershop.com/products.json?limit=250). 17 active Meta ads parsed, all started 31 Oct–11 Nov 2026 (old-pipes/rust angle) — [Meta Ad Library IL, "ראש מקלחת פילטר"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A8%D7%90%D7%A9%20%D7%9E%D7%A7%D7%9C%D7%97%D7%AA%20%D7%A4%D7%99%D7%9C%D7%98%D7%A8&search_type=keyword_unordered)
- FACT: **Vedya** (vedya.co.il / vedyashop.com, Shopify, 36 bathroom products; oldest product Oct 2024). Filtered shower head "Ved-O" created 2026-06-13 at 329.90–339.90 ILS (compare-at 549.90); refills 79.90 (anti-scale) and 89.90 (vitamin C, rose scent), created 2026-06-29; earlier rain-head filter cartridge 79.90 (Nov 2025). — [Vedya products feed](https://vedya.co.il/products.json?limit=250). Active ads from 8 Oct 2026 claiming the filter "helps reduce chlorine, limescale and sediment" and "+200% pressure" — [Meta Ad Library IL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A8%D7%90%D7%A9%20%D7%9E%D7%A7%D7%9C%D7%97%D7%AA%20%D7%A4%D7%99%D7%9C%D7%98%D7%A8&search_type=keyword_unordered)
- FACT: **RIVO** (rivo.co.il, Shopify, 7 products). "RIVO shower kit" (head, hose, holder, 5 filters) 249 ILS, created 2026-08-26, feed weight 800 g; "RIVO DUAL" double-sided filtered head 189 ILS (239 with 6 filters), created 2026-10-12; refills: 5 filters 69 / 10 filters 99 (FLOW), 5 for 89 / 10 for 119 (DUAL). Free shipping. No subscription visible. — [RIVO products feed](https://rivo.co.il/products.json?limit=250). Ads started 8 Nov 2026 — [Meta Ad Library IL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A8%D7%90%D7%A9%20%D7%9E%D7%A7%D7%9C%D7%97%D7%AA%20%D7%9E%D7%A1%D7%A0%D7%9F&search_type=keyword_unordered). Note: RIVO also sells a **toothbrush hygiene/steriliser unit at 199 ILS** ("RIVO PURE", created 2026-10-19) — the same category as the partners' current product, at a 54% higher price.
- FACT: **Beau Clean** (beau-clean.com, Shopify, 3 products all created 2026-11-01). Head 379 ILS one-time; **subscription offer: 329 ILS today (feed variant 240), then a filter delivered every 2 months at 89 ILS, pause/cancel after 2 shipments**; standalone filter 119. Product handles are French ("pommeau-filtrant", "filtre-rechange"), suggesting a foreign operator localising into Hebrew. Page claims "234+ satisfied customers" (REPORTED; implausible to verify for a store 10 days old). Positioning is deliberately narrow: "stops rust and sediment in apartments with old pipes", cites Mei Avivim on Tel Aviv water being "hard to very hard", and its ad states "a shower filter lasts about two months ... not three". — [Beau Clean](https://beau-clean.com/), [feed](https://beau-clean.com/products.json)
- FACT: **NewHorizon / אופק חדש** — official importer of Korean **BIOCERA** shower filters: Zero Shower Filter 205 ILS incl. 40 shipping; ATOZERO Premium 430 ILS; replacement filter 179 ILS; seller has 422 Zap ratings — [Zap search "ראש מקלחת מסנן"](https://www.zap.co.il/search.aspx?keyword=%D7%A8%D7%90%D7%A9+%D7%9E%D7%A7%D7%9C%D7%97%D7%AA+%D7%9E%D7%A1%D7%A0%D7%9F). Its ad (started 4 Nov 2026) says "Israeli tap water contains chlorine and rust particles", claims NSF compliance and "one filter lasts 2–4 months for a family" — [Meta Ad Library IL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%A1%D7%A0%D7%9F%20%D7%9C%D7%9E%D7%A7%D7%9C%D7%97%D7%AA&search_type=keyword_unordered)
- FACT: **Tipa Tech (טיפה טק)**, an Israeli water-purifier company, has 3 active ads for a shower filter started 28 Jun, 9 Jul and 13 Jul 2026 (the longest-running active ads found in the category) — [Meta Ad Library IL, "מסנן למקלחת"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%A1%D7%A0%D7%9F%20%D7%9C%D7%9E%D7%A7%D7%9C%D7%97%D7%AA&search_type=keyword_unordered); company site markets itself on NSF-42 — [Tipa Tech](https://www.tipatech.co.il/)
- FACT (Zap, other sellers): "shower filter" 110 ILS incl. shipping at Filter Outlet (5.0, 45 ratings); cross-border "Black Magic 5-mode shower head with water filter" 159 ILS free shipping, up to 14 business days, seller rated 1.0 (236); Amiad whole-home anti-scale filters 690–790 ILS — [Zap search "פילטר למקלחת"](https://www.zap.co.il/search.aspx?keyword=%D7%A4%D7%99%D7%9C%D7%98%D7%A8%20%D7%9C%D7%9E%D7%A7%D7%9C%D7%97%D7%AA)
- FACT: Home Center's search for "ראש טוש מסנן" returns ordinary shower heads (49.90–219.90 ILS) and no filtered head — [Home Center](https://www.homecenter.co.il/search?q=%D7%A8%D7%90%D7%A9+%D7%98%D7%95%D7%A9+%D7%9E%D7%A1%D7%A0%D7%9F); ACE search returned no results — [ACE](https://www.ace.co.il/catalogsearch/result/?q=%D7%A8%D7%90%D7%A9%20%D7%98%D7%95%D7%A9%20%D7%A4%D7%99%D7%9C%D7%98%D7%A8)

Summary table (FACT from feeds/pages above):

| Seller | Since (earliest evidence) | Head price ILS | Refill price ILS | Stated refill interval | Subscription? |
|---|---|---|---|---|---|
| SilQ | Feb–May 2024 | 349–399 | 65–129 (set 189) | 3 months | No (50% refill discount with head) |
| Care Filter | Jul 2024 | 369.90–379.90 | 69.90–99.90 | not read | none found on homepage |
| Biocera via NewHorizon | UNVERIFIED (established Zap seller) | 205–430 | 179 | 2–4 months | not seen |
| Tipa Tech | ads since Jun 2026 | not read | not read | — | not seen |
| Vedya | filtered head Jun 2026 | 329.90–339.90 | 79.90–89.90 | not read | No |
| RIVO | Aug 2026 | 189–249 | 69–119 (packs of 5–10) | not read | No |
| Beau Clean | 1 Nov 2026 | 379 (329 with sub) | 89 sub / 119 one-off | 2 months | **Yes** |

### Cited Findings — washing-machine cleaner tablets (Israel)
- FACT: **Relivia** (reliviails.com, Shopify, 8 cleaning SKUs). "Washing-machine cleaning tablets" created 2026-05-31: 1 pack 139.90 ILS (compare-at 199.90), 2 packs 199.90, "3+1 gift" 299.90 (marked best-seller). Page shows per-treatment price 5.8 / 4.1 / 3.1 ILS, i.e. **24 tablets per pack** (page text: "Relivia Pro – 24 professional cleaning tablets"). Free shipping only above 309 ILS; 30-day money-back promise. Seller claims "9,000+ customers recommend", "+9,652 Facebook users bought recently", "+821 orders in the last 24 hours" (all REPORTED seller widgets, unverifiable). No subscription. — [Relivia product page](https://reliviails.com/products/washing-tablets-relivia), [feed](https://reliviails.com/products.json?limit=250)
- FACT: Relivia has expanded since launch into dishwasher tablets (Jul 2026), mould gel (Aug), toilet-brush kit + refill heads (Aug), laundry sheets (Sep), stain pen (Oct) — a "cleaning consumables brand" build-out rather than a single product — [Relivia feed](https://reliviails.com/products.json?limit=250)
- FACT: **Fizz IL** (fizz.co.il, Shopify, 14 SKUs, earliest 2026-06-30): washing-machine tablets 149 ILS (compare-at 179, created 2026-07-12), dishwasher tablets 149, toilet tablets 99, gasket mould gel 99, etc. — [Fizz feed](https://fizz.co.il/products.json?limit=250)
- FACT: Meta Ad Library IL: keyword "טבליות ניקוי מכונת כביסה" ≈120 active ads; "טבליות לניקוי מכונת כביסה" ≈150; "ניקוי מכונת כביסה" ≈450 (broader, includes other products). Parsed advertisers: Relivia (15 of 28 parsed ads; start dates from 4 Aug 2026 through 1 Nov 2026), Fizz IL plus Fizz-linked pages ("נקיון וסדר הבית", "הבית הנקי שלי", "חולי נקיון וסדר") with ads from 4 Aug 2026, and several advertorial-style pages pointing to reliviails.com ("הסודות לניקיון הבית", "חדשות ישראל אונליין", "נשים ללא פילטר"). Relivia ads offer "50% off two packs + free shipping" and a 30-day refund — [Meta Ad Library IL, tablets](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%98%D7%91%D7%9C%D7%99%D7%95%D7%AA%20%D7%A0%D7%99%D7%A7%D7%95%D7%99%20%D7%9E%D7%9B%D7%95%D7%A0%D7%AA%20%D7%9B%D7%91%D7%99%D7%A1%D7%94&search_type=keyword_unordered)
- FACT (cheap local alternatives on Zap): "BASTION washing-machine cleaning tablets" **35 ILS, free shipping, up to 5 business days** at Walla Shops (seller rating 2.2, 3,231 ratings); cross-border "4-pack tablets" 69 ILS free shipping (14 business days); another 50 ILS + 10 shipping — [Zap "טבליות לניקוי מכונת כביסה"](https://www.zap.co.il/search.aspx?keyword=%D7%98%D7%91%D7%9C%D7%99%D7%95%D7%AA%20%D7%9C%D7%A0%D7%99%D7%A7%D7%95%D7%99%20%D7%9E%D7%9B%D7%95%D7%A0%D7%AA%20%D7%9B%D7%91%D7%99%D7%A1%D7%94). Durgol washing-machine cleaner 30–55 ILS (some with free shipping) — [Zap "ניקוי מכונת כביסה אבנית"](https://www.zap.co.il/search.aspx?keyword=%D7%A0%D7%99%D7%A7%D7%95%D7%99%20%D7%9E%D7%9B%D7%95%D7%A0%D7%AA%20%D7%9B%D7%91%D7%99%D7%A1%D7%94%20%D7%90%D7%91%D7%A0%D7%99%D7%AA)
- REPORTED (search snippets, not opened): TNX 900 ml washer/dishwasher cleaner 49.90 ILS at Home Center — [Home Center](https://www.homecenter.co.il/products/1718026246111); Sano Maxima 500 ml liquid at ≈2.40 ILS/100 ml (≈12 ILS) and a "Nyga" 6-tablet cleaner on KSP — [KSP](https://ksp.co.il/mob/item/177091) (KSP itself could not be opened from here)

### Cited Findings — appliance parts/consumables (Israel)
- FACT: Tami4-compatible filters: Zap lists 26 products; compatible internal filter 142 ILS free shipping (Pure), 2-pack 205, 3-pack 290, 4-pack 372, annual kit 339, original Primo filter 285, filter+UV lamp original 475; sellers include Pure, Aquatec, Mei Gal (86 ratings), "הבית שלך" (4.9, 1,130 ratings) — [Zap "פילטר תמי 4"](https://www.zap.co.il/search.aspx?keyword=%D7%A4%D7%99%D7%9C%D7%98%D7%A8%20%D7%AA%D7%9E%D7%99%204)
- FACT: Roborock accessory/maintenance kits: 18 listings; 99–328 ILS from established electronics sellers (Bug, Daily Sale 2,836 ratings, Speed Computers, G-Tech), and a cross-border kit at 59 ILS incl. shipping — [Zap "ערכת מברשות רובורוק"](https://www.zap.co.il/search.aspx?keyword=%D7%A2%D7%A8%D7%9B%D7%AA%20%D7%9E%D7%91%D7%A8%D7%A9%D7%95%D7%AA%20%D7%A8%D7%95%D7%91%D7%95%D7%A8%D7%95%D7%A7)
- FACT: No active Meta ads in Israel for "פילטר תמי 4 תואם", "אביזרים לנינג'ה", "נייר אפייה לאייר פרייר", "חלקי חילוף לשואב רובוטי" (library returned "no ads match") — [Meta Ad Library IL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A4%D7%99%D7%9C%D7%98%D7%A8%20%D7%AA%D7%9E%D7%99%204%20%D7%AA%D7%95%D7%90%D7%9D&search_type=keyword_unordered)
- FACT: Zap returned no results for "נייר אפייה לנינג'ה" (air-fryer paper liners are not a price-comparison category) — [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%A0%D7%99%D7%99%D7%A8%20%D7%90%D7%A4%D7%99%D7%99%D7%94%20%D7%9C%D7%A0%D7%99%D7%A0%D7%92'%D7%94)

### Inferences
- ESTIMATE: Shower filter is no longer a "first-mover" play in Israel. SilQ has ~2.5 years of continuous operation, a growing SKU range and 179 on-site reviews on its hero product — evidence it sells, but 179 reviews in ~30 months is a modest, not a breakout, volume signal (review-to-order ratios are unknown).
- ESTIMATE: Five advertisers entering/pushing within ~5 months (Tipa Tech Jun, Vedya Jun/Oct, RIVO Aug/Nov, Care Filter Oct–Nov burst, Beau Clean Nov) means auction competition for the same Hebrew audience is rising right now; a newcomer's CPA should be expected to be worse than the incumbents', not better.
- ESTIMATE: The market price anchor for a branded Hebrew DTC filtered head is 329–399 ILS with free shipping, and 65–129 ILS per refill. RIVO is testing the low end (189–249). The partners would not be able to be the cheapest (Shein/AliExpress) nor the most established (SilQ/Biocera).
- ESTIMATE: Relivia and Fizz running dozens of ads continuously for 3+ months and extending their ranges is consistent with the tablets being profitable for them at 140–300 ILS baskets; it is also a sign the Hebrew ad space for this exact product is already occupied by two operators with evident ad budgets and advertorial infrastructure.
- ESTIMATE: Appliance consumables in Israel are won on search/price-comparison and marketplace presence (Zap, KSP, AliExpress), not on paid social. A 3-person Shopify store with paid-social skills has no visible edge there.

### Gaps
- Could not read KSP, Shufersal, Super-Pharm, Rami Levy shelf prices for Sano/Dr. Beckmann/Calgon/Finish machine cleaners (all blocked). The one supermarket-type data point is a search snippet (Sano Maxima ≈12 ILS/500 ml on KSP) — treat as REPORTED.
- Review counts with dates were obtainable only for SilQ (179, undated aggregate). Other stores expose no review schema.
- Actual sales volumes of any Israeli competitor: unknown. Seller counters ("5,000+", "9,000+", "234+", "+821 in 24h") are unaudited marketing.
- Total historical (inactive) Meta ads per advertiser could not be loaded (library returned an error for `active_status=all` queries), so "how long have they advertised in total" is only bounded by product creation dates.

---

## 2. Cheap alternatives accessible to Israelis (AliExpress / Temu / Shein)

### Takeaway
On AliExpress, filtered handheld shower heads with 10,000+ units sold are listed at about $5–8 (≈16–27 ILS at the 11 Nov 2026 rate) and generic PP-cotton replacement cartridges at ≈$0.21–0.28 each; 12 washing-machine tablets at ≈$4 (5,000+ sold). Shein and Temu could not be read in this session, so the "Shein from ~₪10" red flag from round 1 stands unrefuted but not re-verified.

### Cited Findings
- FACT: USD/ILS representative rate 3.172 (last update 2026-11-11) — [Bank of Israel API](https://boi.org.il/PublicApi/GetExchangeRates?asXml=false). So $75 ≈ 238 ILS; $32 ≈ 101.5 ILS.
- FACT (AliExpress, sorted by orders, USD, served to a US IP on 2026-11-11 during the 11.11 sale): "5 Spray ... Filtered Shower Heads with Stop Button" $5.19, 4.9★, 10,000+ sold; similar $7.59 (list $22.35), 10,000+ sold; "2025 new ion drop shower head with handheld filter" $8.19, 4.6★, 10,000+ sold; "12cm Large Panel Shower Head with Filter" $8.39, 5,000+ sold; several items at $0.33–$1.09 are new-shopper/"Dollar Express" promo prices — [AliExpress "filter shower head"](https://he.aliexpress.com/w/wholesale-filter-shower-head.html?SortType=total_tranpro_desc)
- FACT (AliExpress refills): "4 Modes Shower Head ... With Filter Element" $5.59, 20K+ sold; "20/30pcs Replacement PP Cotton Filter Cartridges" $6.39 ($0.21/pc for 30), 2K+ sold; "10pcs ... PP Cotton Filter Cartridge" $2.79 (≈$0.28/pc), 1K+ sold; "Shower Head Water Filter Replacement Cartridge 24x115mm" $1.19, 1K+ sold; branded "ALTHY Vitamin C Revitalizing Shower Water Filter" $46.58, 2K+ sold (shows a premium tier exists even on AliExpress) — [AliExpress "shower head filter replacement cartridge"](https://he.aliexpress.com/w/wholesale-shower-head-filter-replacement-cartridge.html?SortType=total_tranpro_desc)
- FACT (AliExpress tablets): "12PCS Washing Machine Cleaning Effervescent Tablets" $4.05 ($0.34/pc), 4.9★, 5,000+ sold; another 12-pack $4.33, 900+ sold; most other listings under 700 sold — [AliExpress "washing machine cleaner tablets"](https://he.aliexpress.com/w/wholesale-washing-machine-cleaner-tablets.html?SortType=total_tranpro_desc)
- FACT (AliExpress air-fryer liners): 50/100-piece paper liners with 10,000+ sold at $3.79–$4.33 regular (promo $0.33); Ninja-specific square liners 5,000+ sold — [AliExpress "air fryer paper liners ninja"](https://www.aliexpress.com/w/wholesale-air-fryer-paper-liners-ninja.html?SortType=total_tranpro_desc)
- FACT: Cross-border resellers already list these look-alikes on Zap at 3–10x AliExpress: filtered head 159 ILS, tablets 4-pack 69 ILS, Roborock kit 59 ILS — [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%A4%D7%99%D7%9C%D7%98%D7%A8%20%D7%9C%D7%9E%D7%A7%D7%9C%D7%97%D7%AA)

### Inferences
- ESTIMATE: An Israeli consumer can get a functionally similar handheld filter head for ~16–27 ILS and a year of PP-cotton cartridges for ~10–20 ILS, tax-free (far under the $75 threshold). Against a 329–379 ILS Hebrew brand this is a 12–20x price gap; the brand sells trust, Hebrew service, speed and "premium media" claims — exactly the claims that are hardest to substantiate (sections 4, 7).
- ESTIMATE: Refill lock-in is weak. Handheld heads using standard 24×115 mm PP-cotton sticks can be refilled from AliExpress at ~1 ILS each; any refill annuity priced at 14–18 ILS per filter (RIVO: 69/5) or 89 per cartridge (Beau Clean) depends on the customer not checking AliExpress, or on a proprietary cartridge format.
- ESTIMATE: Tablets: 24 tablets ≈ $8 on AliExpress (≈26 ILS) vs 139.90 at Relivia vs 35 ILS for Bastion with free local shipping. The product is not defensible on price; it is sold on fear-based copy and bundles.

### Gaps
- Shein Israel and Temu prices and sold counts: **not readable** (captcha / login wall). Not re-verified.
- AliExpress ship-to-Israel pricing and delivery promise not confirmed (page rendered for US/USD).

---

## 3. Demand in Israel — Trends, ads, water facts, discussion

### Takeaway
Paid-social supply is clearly present and growing (7 shower-filter advertisers; ≈120–150 tablet ads), which is indirect evidence of demand, but search-trend data could not be obtained at all. The factual water story is mixed: Tel Aviv's own water corporation says its water is generally above 150 ppm ("hard to very hard"), yet the same page says hardness is falling because of desalination, and Israeli regulations cap free chlorine in the distribution network at 0.5 mg/L — a quarter or less of the 2–2.7 ppm levels in the US lab tests that the category's marketing borrows from. Shower filters do not soften water.

### Cited Findings
- FACT: Meta Ad Library IL active ads (2026-11-11): "ראש מקלחת מסנן" ≈4 ads / 3 advertisers (RIVO, SilQ, NewHorizon); "פילטר למקלחת" ≈4 ads (Vedya, Beau Clean, plus an unrelated soap brand); "מסנן למקלחת" ≈8 ads (NewHorizon 5, Tipa Tech 3); "ראש מקלחת פילטר" ≈26 ads (Care Filter 17, Vedya 5, Beau Clean 4). Distinct relevant advertisers: 7. Oldest active ads: Tipa Tech 28 Jun 2026, SilQ 13 Jul 2026; most others started within the last 2 weeks. "ראש מקלחת כלור" returned no ads. — [Meta Ad Library IL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A8%D7%90%D7%A9%20%D7%9E%D7%A7%D7%9C%D7%97%D7%AA%20%D7%A4%D7%99%D7%9C%D7%98%D7%A8&search_type=keyword_unordered)
- FACT: Mei Avivim (Tel Aviv-Yafo water corporation): hardness classes are soft 0–60, medium 60–120, hard 120–180, very hard >180 mg/L as CaCO3; "as a rule, water in Tel Aviv-Yafo is above 150 ppm and therefore defined as hard to very hard"; hard water comes from wells in limestone/dolomite aquifers; "in recent years, due to the change in water sources and reliance on desalinated water, hardness is lower", because desalination removes minerals and only calcium is added back; Israel has no standard for hardness of supplied water — [Mei Avivim, קשיות המים](https://www.mei-avivim.co.il/%d7%90%d7%99%d7%9b%d7%95%d7%aa-%d7%94%d7%9e%d7%99%d7%9d2/%d7%a7%d7%a9%d7%99%d7%95%d7%aa-%d7%94%d7%9e%d7%99%d7%9d/)
- FACT (regulations text): Public Health Regulations (Sanitary Quality of Drinking Water and Drinking Water Facilities), 2013, Fifth Schedule, Table A — in the water supply system: chlorine minimum residual 0.1 mg/L, **maximum 0.5 mg/L** (up to 0.8 in main lines before delivery to consumers); chloramine 0.3–3 mg/L; at the disinfection facility outlet chlorine 0.2–1 mg/L; trihalomethanes max 0.1 mg/L. Desalinated water post-treatment: dissolved calcium 80–120 mg/L as CaCO3, alkalinity ≥80 — [Wikisource, drinking-water regulations](https://he.wikisource.org/wiki/%D7%AA%D7%A7%D7%A0%D7%95%D7%AA_%D7%91%D7%A8%D7%99%D7%90%D7%95%D7%AA_%D7%94%D7%A2%D7%9D_(%D7%90%D7%99%D7%9B%D7%95%D7%AA%D7%9D_%D7%94%D7%AA%D7%91%D7%A8%D7%95%D7%90%D7%AA%D7%99%D7%AA_%D7%A9%D7%9C_%D7%9E%D7%99_%D7%A9%D7%AA%D7%99%D7%94)) (Wikisource carries a disclaimer; amendments since 2013 not checked)
- REPORTED: over 50% of Israel's distribution system is desalinated water, some areas 80%; post-treated desalinated water has much less magnesium than recommended — [chemRxiv preprint 2023](https://chemrxiv.org/engage/chemrxiv/article-details/64c6068c9ed5166e93b7bc24); Israeli desalination post-treatment targets total hardness around 120 mg/L as CaCO3 — [Hebrew University publication page](https://cris.huji.ac.il/en/publications/new-desalinated-drinking-water-regulations-are-met-by-an-innovati/)
- REPORTED: Mei Avivim's CEO has warned of severe pipe problems in a large share of Tel Aviv's old buildings — [Maariv](https://www.maariv.co.il/business/Article-720158) (search summary; article not opened)
- REPORTED (US test, context for chlorine levels): Water Filter Guru's Jolie test started from 2.70 ppm chlorine and 128 ppm hardness; the filter cut chlorine 54% to 1.23 ppm and did not reduce hardness — [Water Filter Guru](https://waterfilterguru.com/jolie-shower-filter-review)

### Inferences
- ESTIMATE: The most intuitive Israeli pain — limescale ("אבנית") — is real (Tel Aviv >150 ppm per the utility) but is the one thing a shower filter does not fix. Competitors' copy ("turns hard water into soft", "anti-scale component", "showered in limescale today?") is the weakest point legally and the strongest point commercially; an honest seller gives up the best hook.
- ESTIMATE: The chlorine hook is weaker in Israel than in the US: the legal network maximum is 0.5 mg/L, so a filter that removes ~50–66% of chlorine (section 7) would change e.g. 0.3 → ~0.1–0.15 mg/L. Whether a consumer can feel that is unproven.
- ESTIMATE: The "old pipes / rust / sediment" angle (Beau Clean, Care Filter, NewHorizon) is the most defensible locally: sediment capture is visible (filter changes colour) and does not require a health claim. It is also the angle on which a ~1 ILS PP-cotton filter performs as well as an 89 ILS one.
- ESTIMATE: Two professional water companies (Tipa Tech, Biocera's importer) and a 2.5-year-old DTC brand already own the credibility positions ("NSF", "official importer", "#1 in Israel").

### Gaps
- **Google Trends (geo=IL, 5 years) for all Hebrew terms: not obtained** (HTTP 429 on all attempts). No statement about rising/falling Israeli search interest can be made from this session.
- Israeli Facebook groups / Reddit / forums / Hebrew press on shower filters, chlorine and hair loss: **not surveyed** (search engines blocked; US-only search tool returned no Israeli pages). No evidence either way on organic consumer conversation.
- National hardness by city (Mekorot / Ministry of Health tables) and actual measured chlorine residuals at the tap: not retrieved (gov.il blocked). Only Tel Aviv's qualitative statement and the regulatory limits were read.
- Whether any Israeli incumbent failed/closed: no evidence found either way. The only "failure-type" signal seen is heavy permanent discounting (compare-at prices 40–50% above selling price at SilQ, Vedya, Care Filter, Relivia, Fizz), which is standard DTC theatre, not proof of weak demand.

---

## 4. Claims & regulation

### Takeaway
Nothing found prohibits selling a filtered shower head in Israel, but three things are unresolved and need a professional answer before importing stock: (a) whether a shower head/filter falls under the tapware standards that reference SI 5452 (products in contact with drinking water) at import; (b) what may be claimed — Israeli consumer law lets the regulator demand proof for any factual claim about a product's properties or results; (c) for cleaner tablets, hazardous-substance classification, Hebrew labelling and SDS under SI 2302, plus air-freight restrictions if the formula is percarbonate-based. Dropshipped single parcels sidestep import-standards checks in practice but not the consumer-protection exposure for claims.

### Cited Findings
- REPORTED: SI 5452 ("testing of products in contact with drinking water") is not itself an official standard but is made binding because the drinking-water regulations and several official standards refer to it; tapware standards SI 1317 and SI 1347 contain official clauses referring to SI 5452, so taps within their scope must comply. Current edition published 28 Aug 2022, adopting NSF/ANSI 61 (2021) or AS/NZS 4020 (2018); lead content limit 0.25% for plumbing products stays in force — [Federation of Israeli Chambers of Commerce](https://www.chamber.org.il/foreigntrade/1109/1112/126602/), [chamber webinar page](https://www.chamber.org.il/foreigntrade/1109/1112/136282/), [SII standard page](https://www.sii.org.il/he/lobby/standardization/standard-page?id=6622) (search summaries; pages not opened individually)
- REPORTED: Consumer Protection Law — the ban on misleading consumers applies to advertising, by act or omission; where an ad states facts about a product's properties or the results of using it, the Consumer Protection and Fair Trade Authority commissioner may demand the ad and evidence proving those facts — [Protocol legal guide](https://protocol.co.il/consumer-misleading-advertisement/). A Ministry of Health advisory "Committee for examining misleading of the public" exists for health-related publications — [gov.il](https://www.gov.il/he/Departments/publicbodies/committee-deception). Enforcement is patchy: the State Comptroller (2026) found the Authority imposed only 61 financial sanctions in 2025 in one area examined; one sanction of 1.1m ILS was cut to ~62k on appeal — [State Comptroller 2026 summary](https://library.mevaker.gov.il/sites/DigitalLibrary/Documents/2026/Economic-Report/2026-Economic-Report-108-Taktzir.pdf), [ICE](https://www.ice.co.il/law/news/article/1096416) (search summaries)
- REPORTED: NSF/ANSI 177 is the shower-filter-specific standard (free chlorine reduction under shower conditions) and is often confused with NSF/ANSI 42 (drinking water); it is voluntary — [Alibaba seller blog](https://seller.alibaba.com/blogs/2026/southeast-asia/water-treatment/shower-filter-specifications-guide-alibaba-b2b) (low-reliability source; the "mandatory for US" statement in it is doubtful). Jolie, the category leader, is reported as **not** NSF/ANSI 177 certified despite marketing references to NSF — [Water Filter Guru](https://waterfilterguru.com/jolie-shower-filter-review)
- FACT: The Standards Institution of Israel's cleaning-products testing page: verifies product marking against the current edition of **SI 2302 (hazardous substances — classification, labelling, marking, packaging)**, notes that because it adopts European rules the marking must still meet Israeli legal requirements, and that manufacturers change formulas so the SDS must be current — [SII, cleaning products](https://www.sii.org.il/he/nivdak-cleaning/)
- REPORTED: From 9 Aug 2022 all hazardous substances manufactured in, imported into or sold in Israel must comply with SI 2302 part 1 (2019 edition); SII also approves the SDS and verifies CLP classification; specific cleaners have their own standards (SI 139 dish liquid, SI 261 bleach, SI 4272 oven/grease cleaners) — [SII](https://www.sii.org.il/lobby/importers/nivdak/nivdak-cleaning/), [chamber.org.il webinar](https://www.chamber.org.il/foreigntrade/1109/1112/114198/) (search summary)
- REPORTED: Sodium carbonate peroxyhydrate (sodium percarbonate, the usual active in "effervescent" washer-cleaner tablets) is UN3378, Class 5.1 oxidizer, Packing Group II; decomposes above 50 °C — [NOAA CAMEO](https://cameochemicals.noaa.gov/unna/3378), [ChemicalBook SDS](https://chemicalbook.com/msds/sodium-percarbonate.htm). Whether finished consumer tablets ship as limited-quantity or regulated air cargo was not established.
- FACT: Competitors' own compatibility claims: Vedya advertises "universal thread, no special tools"; Beau Clean "screw on by hand, also in rentals" — [Meta Ad Library IL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A4%D7%99%D7%9C%D7%98%D7%A8%20%D7%9C%D7%9E%D7%A7%D7%9C%D7%97%D7%AA&search_type=keyword_unordered), [Beau Clean](https://beau-clean.com/)

### Inferences
- ESTIMATE — what can truthfully be claimed: "contains a sediment/rust filter you can see getting dirty"; "reduces free chlorine" only with a test report for the specific cartridge at shower flow and temperature (ideally NSF/ANSI 177 or an SGS report naming the SKU); scent/vitamin-C as a sensory feature. **Should not be claimed:** "removes chlorine/heavy metals" (the exact wording sued over in Rusow v. Jolie), "softens water / anti-limescale" (contradicted by independent testing), "prevents hair loss/acne/eczema" (Clifft v. Jolie; no supporting evidence), "NSF certified" without a certificate in NSF's database.
- ESTIMATE: Several Israeli incumbents currently make the risky claims (SilQ, Vedya, NewHorizon). That shows enforcement has not stopped them so far; it does not make the claims safe — Israel has an active consumer class-action culture (even Zap's own footer lists two class-action settlements).
- ESTIMATE: Cleaner tablets carry more regulatory work than the shower head: classification, Hebrew hazard label, SDS, possibly dangerous-goods freight. Relivia/Fizz evidently manage it (or ignore it); a compliant bulk import adds cost and time that a cross-border drop-ship competitor does not bear.

### Gaps
- **Does SI 5452 / SI 1347 legally apply to a hand shower with a filter at import?** Not determined. Needs a query to the Standards Institution / Ministry of Economy import-standards unit or a customs broker with the HS code. UNVERIFIED.
- Thread standard in Israeli showers (G1/2" BSP for hose/handset) — widely assumed and consistent with sellers' "universal thread" copy, but **no primary source was read**. UNVERIFIED.
- Ministry of Health / Ministry of Environmental Protection licensing for importing household cleaning preparations (poisons permit thresholds, registration): not found. Hebrew-label requirements under the Consumer Protection (marking of goods) order: not read.
- No Israeli regulator action or Israeli lawsuit specifically about shower-filter claims was found (search coverage of Israeli sources was poor, so absence is weak evidence).

---

## 5. Sourcing

### Takeaway
I could not open Alibaba/1688/Global Sources/CJ pages, so factory pricing rests on search snippets and on AliExpress retail as an upper bound. The indications: a "15-stage"/vitamin-C class head is quoted around $10.5–12 FOB at low MOQ; simple handheld PP-cotton heads retail delivered on AliExpress at $5–8 (factory lower); cartridges range from ≈$0.2 (PP cotton stick) to a few dollars (multi-media). No supplier with a verifiable NSF/ANSI 177 certificate was identified.

### Cited Findings
- REPORTED (search snippet of listings, not opened): Shenzhen Calux Purification — 15-stage vitamin shower filter $10.50–12.00, MOQ 2 pieces, "custom manufacturer, 11 yrs"; a Ningbo seller — 15-stage filter shower head, MOQ 100 pcs, OEM/ODM, lead time 15 days; a generic vitamin-C shower head at $10.50 for 500–999 pcs (5-stage carbon) — [Alibaba listing](https://www.alibaba.com/product-detail/15-Stage-NSF-Certified-KDF55-Inline_60783785485.html), [nbfyd on Alibaba](https://nbfyd.en.alibaba.com/product/1600797931257-925704472/15_Stage_Shower_Filter_Shower_Head_Water_Softener_Filter_High_Output_Universal_with_Replacement_Filter.html), [Alibaba vitamin-C head](https://www.alibaba.com/product-introduction/Shower-Head-with-Vitamin-c-and_1601137382414.html)
- FACT: AliExpress retail (upper bound on small-quantity cost incl. shipping): handheld filtered heads $5.19–8.39 with 5,000–10,000+ sold; PP-cotton cartridges $0.21–0.28/pc — [AliExpress](https://he.aliexpress.com/w/wholesale-filter-shower-head.html?SortType=total_tranpro_desc), [AliExpress refills](https://he.aliexpress.com/w/wholesale-shower-head-filter-replacement-cartridge.html?SortType=total_tranpro_desc)
- FACT: Seller-entered shipping weights in competitor feeds: RIVO full kit (head, hose, holder, 5 filters) 800 g; SilQ Little Q 500 g — [RIVO feed](https://rivo.co.il/products.json?limit=250), [SilQ feed](https://silqisrael.com/products.json?limit=250)
- REPORTED (from round-1 notes, forwarder marketing): China→Israel air freight ≈$5.31/kg, express ≈$13.25/kg, LCL sea ≈$79.73/CBM — [DTFU Logistics](https://www.dtfulogistics.com/news/shipping-cost-from-china-to-israel/)
- REPORTED (quality failures seen in independent testing of the category leader): only 54% chlorine reduction; zinc rose from 0.009 to 0.42 ppm (likely leached from KDF media); fluoride and some THMs higher after filtering; no hardness reduction — [Water Filter Guru](https://waterfilterguru.com/jolie-shower-filter-review). Flow-rate dependence: one competitor's filter removed 100% chlorine at 0.6 GPM but only 50% at 3.6 GPM — [Water Filter Guru, Canopy](https://waterfilterguru.com/canopy-shower-head-filter-review/) (search summary)
- FACT: Washing-machine tablets retail on AliExpress at ≈$0.34 per tablet in 12-packs — [AliExpress](https://he.aliexpress.com/w/wholesale-washing-machine-cleaner-tablets.html?SortType=total_tranpro_desc)

### Inferences
- ESTIMATE: Landed cost for a mid-quality head + 1–2 cartridges in a branded box, air-freighted in a few hundred units: roughly 35–60 ILS (≈$11–19: $10.5–12 FOB or less for simpler designs, + ~0.5–0.8 kg × $5–13/kg freight, + inspection/packaging). A simple PP-cotton handheld kit could land nearer 20–35 ILS. These are assumptions, not quotes.
- ESTIMATE: Volumetric weight matters: a boxed head with hose is light but bulky; express couriers bill volumetric weight, so the per-unit freight could be 2x the actual-weight figure.
- ESTIMATE: The cheapest way to de-risk quality is to buy the same OEM item retail (AliExpress) and test chlorine reduction with a pool colorimeter before any MOQ.

### Gaps
- No verified factory quote, MOQ, carton dimensions or certification documents were obtained (Alibaba/1688/Global Sources/CJ all blocked). All sourcing numbers above are REPORTED snippets or retail proxies.
- 1688 prices: not accessed.
- Customs duty rate for shower heads / filter cartridges / cleaning preparations by HS code: not checked.
- No factory price found for washing-machine tablets (round 1 also found none).

---

## 6. Retention reality

### Takeaway
The category leader's published retention numbers are inconsistent and self-reported, and nothing was found for small no-name brands. Platform-level data says replenishment subscriptions lose roughly a quarter of subscribers at the first renewal and a majority of churn happens by cycle 2–3. In Israel, only one of seven shower-filter sellers (the 10-day-old Beau Clean) even offers a subscription — the established local player sells refills à la carte with discounts, which suggests subscriptions are not what makes the model work here.

### Cited Findings
- REPORTED: Jolie, Jan 2023: "over $4m" first-year sales; close to 80% of customers were subscribers; churn "3% so far" (period not stated); head $148 with subscription / $165 without; filter $33 every 3 months; CAC not disclosed; claims profitability — [Modern Retail, 17 Jan 2023](https://www.modernretail.co/marketing/dtc-briefing-how-jolie-reached-4-2m-in-sales-its-first-year-while-staying-profitable/)
- REPORTED (vendor case studies, mutually inconsistent): Jolie "over 100,000 active subscribers, <1% monthly churn, >$10m subscription revenue" vs. another page "over 3,500 subscribers, subscriptions >15% of revenue" — [Smartrr case study](https://smartrr.com/case-studies/intentional-about-subscriptions-from-0-to-100k-subscribers), [Smartrr second page](https://smartrr.com/case-studies/step-0-jolie-skin-co). $28m revenue in 2023 and $10m ARR — [Fast Company](https://www.fastcompany.com/91034328/jolie-skin-co-most-innovative-companies-2024); aiming above $100m by 2027 with wholesale (Ulta) — [Beauty Independent](https://beautyindependent.com/filtered-showerhead-brand-jolie-ulta-beauty) (search summaries)
- REPORTED (Recharge platform data, trailing 12 months Jul 2025–Jun 2026, 20,000+ subscription brands): commodity/consumable segment — 73.1% of scheduled renewals processed, 4.0% skipped, 16.8% "active-churn rate"; functional/ritual segment 69.5% / 6.9% / 17.5%; merchant-level median process rate 75.8% (commodity) — [Recharge blog](https://getrecharge.com/blog/wellness-ification-playbook-subscription-retention/) (definitions of "active-churn" not given)
- REPORTED (secondary summaries of Recharge data): ~61% of voluntary churn occurs at cycles 2–3; first-renewal churn ≈26.5–28.2% for health/pets/food; vendor claim that 60–70% of subscribers drop between order 1 and 3 — [Recharge](https://getrecharge.com/?p=27190), [Eightx](https://www.eightx.co/blog/average-subscription-churn-rate-by-category) (low-reliability vendor blog; figures do not fully reconcile)
- FACT: Israeli practice: SilQ — no subscription, 50% off a refill with the head, permanent ~50% "sale" on cartridges (95 vs 190); RIVO — multi-filter packs (5/10); Beau Clean — subscription with a minimum of 2 shipments before pause/cancel — [SilQ](https://silqisrael.com/products/q-head), [RIVO feed](https://rivo.co.il/products.json?limit=250), [Beau Clean](https://beau-clean.com/)
- FACT: Relivia's best-selling tablet bundle is "3+1" = 4 packs × 24 = **96 treatments** for 299.90 ILS — [Relivia](https://reliviails.com/products/washing-tablets-relivia)

### Inferences
- ESTIMATE: For a no-name Israeli store without subscriptions, a plausible planning range is 0.3–1.0 refill orders per customer in year one. This is an assumption; no data exists for small brands. Jolie's "80% subscribers / 3% churn" is from a brand that forced subscription at checkout with a US audience and is not transferable.
- ESTIMATE: Washing-machine tablets as sold in Israel are **not a recurring-revenue product**: the winning offer front-loads 2–4 years of supply (at one treatment every 1–2 weeks to a month) into the first order. The "recurring consumable" thesis from round 1 does not match how the product is actually monetised locally; LTV ≈ first-order margin + cross-sell of other cleaning SKUs (which is exactly what Relivia and Fizz built).
- ESTIMATE: Israeli consumers' subscription tolerance for physical goods is unproven here; a mandatory-commitment subscription (Beau Clean) also raises consumer-law cancellation obligations.

### Gaps
- No reorder-rate data for small/no-name shower-filter brands anywhere.
- No Israeli data on subscription uptake for household products.
- Hello Klean, AquaBliss, Canopy retention: nothing found.

---

## 7. Adversarial review — evidence against the opportunity

### Takeaway
The strongest contrary evidence: (1) two US class actions filed in March 2026 against the category leader over exactly the chlorine-removal and hair-growth claims; (2) independent lab testing showing ~54% chlorine reduction, no softening, and leaching of zinc; (3) Israeli chlorine limits that make the benefit small; (4) a crowded and rapidly crowding Hebrew ad auction; (5) 12–20x cheaper look-alikes with five-figure sales counts. No evidence was found that the global trend is fading, and no evidence that Israeli incumbents failed — SilQ's 2.5-year survival points the other way.

### Cited Findings
- FACT: *Rusow et al. v. Jolie Skin Company, Inc.*, filed 19 Mar 2026, No. 3:26-cv-02411 — alleges the showerheads/filters "only reduce the presence of chlorine by roughly 66 percent" rather than "remove chlorine, heavy metals & other contaminants" as advertised; claims under NY GBL and California UCL/CLRA/FAL; proposed nationwide class — [ClassAction.org](https://www.classaction.org/news/class-action-lawsuit-claims-jolie-filtered-showerheads-leave-substantial-amount-of-chlorine-in-water)
- REPORTED: *Clifft v. Jolie Skin Co.*, filed 18 Mar 2026, C.D. Cal. No. 2:26-cv-02942 — alleges false marketing that the products promote hair growth and reduce shedding without scientific support — [Truth in Advertising](https://truthinadvertising.org/class-action/jolie-filtered-showerhead/), [complaint PDF](https://truthinadvertising.org/wp-content/uploads/2026/06/Clifft-v-Jolie-Skn-complaint.pdf). No ruling or settlement found; allegations are unproven.
- REPORTED: Independent test (article updated 20 Aug 2026): Jolie reduced chlorine 2.70 → 1.23 ppm (54%); did not reduce hardness; did not reduce disinfection by-products (some THMs rose); zinc and fluoride increased after filtration; reviewer says Jolie's NSF-certification references are untrue; cartridge rated 3,000 gallons ≈ 3 months — [Water Filter Guru](https://waterfilterguru.com/jolie-shower-filter-review). (Single publisher that runs its own tests and ranks products.)
- REPORTED: Dermatology commentary: no strong evidence that shower filters treat acne, eczema or hair loss; strongest support is for chlorine reduction possibly helping sensitive skin — [AEDIT](https://aedit.com/aedition/can-a-shower-filter-really-improve-your-skin-and-hair) (search summary)
- REPORTED: No sign of trend decline in 2026 coverage; Jolie expanding into Ulta and targeting >$100m — [Beauty Independent](https://beautyindependent.com/filtered-showerhead-brand-jolie-ulta-beauty). Most 2026 coverage is seller/affiliate content.
- FACT: Israel's regulatory chlorine ceiling in the network is 0.5 mg/L (section 3) — [regulations](https://he.wikisource.org/wiki/%D7%AA%D7%A7%D7%A0%D7%95%D7%AA_%D7%91%D7%A8%D7%99%D7%90%D7%95%D7%AA_%D7%94%D7%A2%D7%9D_(%D7%90%D7%99%D7%9B%D7%95%D7%AA%D7%9D_%D7%94%D7%AA%D7%91%D7%A8%D7%95%D7%90%D7%AA%D7%99%D7%AA_%D7%A9%D7%9C_%D7%9E%D7%99_%D7%A9%D7%AA%D7%99%D7%94))
- FACT: A competitor's own ad admits filter life is "about two months, not three" depending on water — [Meta Ad Library IL / Beau Clean](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A4%D7%99%D7%9C%D7%98%D7%A8%20%D7%9C%D7%9E%D7%A7%D7%9C%D7%97%D7%AA&search_type=keyword_unordered)
- FACT: Tablets — a generic pack is 35 ILS delivered locally (Zap/Walla Shops) and Durgol 30–55 ILS, vs 140–150 ILS DTC; Relivia offers a 30-day full refund (a cost line) — [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%98%D7%91%D7%9C%D7%99%D7%95%D7%AA%20%D7%9C%D7%A0%D7%99%D7%A7%D7%95%D7%99%20%D7%9E%D7%9B%D7%95%D7%A0%D7%AA%20%D7%9B%D7%91%D7%99%D7%A1%D7%94), [Relivia](https://reliviails.com/products/washing-tablets-relivia)
- REPORTED: Samsung markets a built-in drum-clean programme as needing no strong or expensive cleaning agent — [Samsung Israel](https://www.samsung.com/il/washers-and-dryers/washing-machines/ww4000t-front-loading-hygiene-steam-digital-inverter-technology-drum-clean-7kg-white-ww7st4040ce-kj) (search summary)

### Inferences — reasons Israeli consumers may not care / the plan may fail
- Limescale is the felt problem; the product does not solve it; honest copy loses the hook, dishonest copy carries legal risk.
- Chlorine is capped low; desalination is making water softer over time (per Mei Avivim), eroding the "hard water" narrative.
- The audience most likely to buy (women 25–45, hair/skin-conscious) is already being hit by 7 advertisers; SilQ owns "#1 in Israel"; Biocera/Tipa Tech own "certified/professional".
- Price transparency: the same audience orders from Shein/AliExpress weekly; a 20-ILS look-alike is one search away, and refill sticks cost ~1 ILS.
- For tablets: the product is a one-off "deep clean" impulse buy; the two incumbents have a 3–5 month head start, advertorial pages and broader ranges for cross-sell; margins rely on aggressive bundle upsells and fear copy ("bacteria... onto your children's skin"), plus refund guarantees.
- For appliance consumables: no ad-driven demand, entrenched specialist sellers with thousands of Zap ratings, model-specific SKU sprawl (inventory risk), and AliExpress at a fraction of the price.

### Gaps
- No UK ASA rulings or other regulator actions on shower filters were found (search returned nothing; not exhaustive).
- Status of the two Jolie cases after filing: not found.
- No direct evidence of Israeli consumer complaints/returns for local shower-filter brands (review pages not scraped; Zap seller ratings are store-level, not product-level).

---

## 8. Unit economics (ILS) — scenarios, break-even CPA and break-even landed cost

### Takeaway
On paper the shower head works at the benchmark CPA **only at premium pricing (≈349 ILS) or with a full kit at ≈249 ILS at break-even**; a 189 ILS head loses ≈24 ILS on the first order at a $32 CPA and needs ≈0.7 refill orders per customer just to break even. Washing-machine tablets lose money as a single pack (break-even CPA ≈$17) and only clear the benchmark CPA as a 4-pack bundle — which is why incumbents push "3+1". All of this is before overheads, creative costs, apps and the partners' time, and it assumes a newcomer gets the same CPA as the market median, in an auction that already has 7 (showers) or 2 heavy (tablets) advertisers.

### Inputs

| Input | Value | Label | Source / basis |
|---|---|---|---|
| USD/ILS | 3.172 | VERIFIED | [Bank of Israel API, 11 Nov 2026](https://boi.org.il/PublicApi/GetExchangeRates?asXml=false) |
| VAT | 18% (net = price / 1.18) | REPORTED | round-1 notes (01_israel_cost_framework.md) |
| Meta cost per purchase, Israel | median ≈ $32; test range $25–40 → 79 / 101.5 / 127 ILS | REPORTED (single source, from brief) | brief / round-1 notes; not product-specific |
| Market retail anchors | head 189–399; kit 249; refill 65–129; tablets 139.90 / 199.90 / 299.90 | VERIFIED | competitor feeds (section 1) |
| Landed cost, simple head + 1 filter | 35 ILS | ASSUMPTION | AliExpress retail $5–8 delivered as upper bound; + branding/box |
| Landed cost, kit (head, hose, holder, 5 filters; ~0.8 kg) | 55 ILS | ASSUMPTION | Alibaba snippet $10.5–12; air freight ≈$5.31/kg; weight from RIVO feed |
| Landed cost, premium multi-stage/vitamin-C head + 2 cartridges | 60 ILS | ASSUMPTION | Alibaba snippet $10.5–12 FOB + freight + QC |
| Landed cost, refill pack | 6 ILS (5 PP sticks) / 12 ILS (multi-media cartridge) | ASSUMPTION | AliExpress $0.21–0.28/pc; premium cartridges unquoted |
| Landed cost, 24 tablets | 20 ILS per pack | ASSUMPTION | AliExpress retail ≈$8 per 24 as upper bound; no factory quote; excludes compliance costs |
| Domestic delivery to customer (seller pays; "free shipping" is the market norm) | 30 ILS kit / 15 ILS small refill envelope / 35 ILS 4-pack | ASSUMPTION | D2D list price from NIS 38 (round-1 notes); negotiated/locker rates assumed |
| Payment processing | 2.5% of gross | ASSUMPTION | — |
| Pick/pack/packaging | 2–6 ILS | ASSUMPTION | — |
| Returns/refunds/breakage reserve | 5% of net (2% on refills) | ASSUMPTION | competitors offer 30–60-day refunds |
| Refill orders per customer, year 1 | 0.3–1.0 | ASSUMPTION | no data for small brands (section 6) |

### Shower filter — per-order contribution before advertising (ESTIMATE, calculated)

| | A: head 189 | B: kit 249 | C: premium 349 | Refill 69 (5 sticks) | Refill 89 (cartridge) |
|---|---|---|---|---|---|
| Net of VAT | 160.2 | 211.0 | 295.8 | 58.5 | 75.4 |
| Landed cost | 35 | 55 | 60 | 6 | 12 |
| Delivery | 30 | 30 | 30 | 15 | 15 |
| Payment fee | 4.7 | 6.2 | 8.7 | 1.7 | 2.2 |
| Pick/pack | 5 | 5 | 6 | 2 | 2 |
| Returns reserve | 8.0 | 10.6 | 14.8 | 1.2 | 1.5 |
| **Contribution before ads** | **77.4** | **104.2** | **176.2** | **32.6** | **42.7** |
| **Break-even CPA** | **77 ILS ≈ $24.4** | **104 ILS ≈ $32.8** | **176 ILS ≈ $55.5** | — | — |

Result at each CPA (first-order profit; refill orders needed per customer to break even; break-even landed cost with zero refills):

| CPA | A: 189 | B: 249 | C: 349 |
|---|---|---|---|
| $25 (79.3 ILS) | −1.9; 0.06 refills; BE landed 33 | +24.9; 0; BE landed 80 | +96.9; 0; BE landed 157 |
| $32 (101.5 ILS) | −24.1; **0.74 refills**; BE landed 11 | +2.7; 0; BE landed 58 | +74.7; 0; BE landed 135 |
| $40 (126.9 ILS) | −49.5; **1.52 refills**; BE landed −15 (impossible) | −22.7; **0.70 refills**; BE landed 32 | +49.3; 0; BE landed 109 |

Reading: if the average customer buys 0.5 refill orders (≈+16–21 ILS contribution), scenario A is still negative at $32 and B at $40. Scenario C is the only one with real headroom — and it is the price point at which the store competes head-on with SilQ, Vedya, Care Filter and Beau Clean, with no proof that a newcomer converts at a 349 ILS price at the median CPA.

### Washing-machine tablets — per-order contribution before advertising (ESTIMATE, calculated; prices = Relivia's)

| | 1 pack 139.90 | 2 packs 199.90 | 4 packs 299.90 |
|---|---|---|---|
| Net of VAT | 118.6 | 169.4 | 254.2 |
| Landed cost | 20 | 40 | 80 |
| Delivery | 30 | 30 | 35 |
| Payment fee | 3.5 | 5.0 | 7.5 |
| Pick/pack | 4 | 5 | 6 |
| Returns reserve | 5.9 | 8.5 | 12.7 |
| **Contribution before ads** | **55.1** | **80.9** | **112.9** |
| **Break-even CPA** | **$17.4** | **$25.5** | **$35.6** |
| Profit at $32 CPA | −46.4 | −20.6 | +11.4 |
| Break-even landed cost at $32 CPA | impossible (<0) | 19 ILS for 2 packs | 91 ILS for 4 packs |

Reading: profitable only if most buyers take the 4-pack (and landed cost per 24 tablets stays ≤ ~23 ILS), or if cross-sells lift the basket. Relivia charges shipping below 309 ILS, which improves the 1–2 pack rows by the shipping fee if customers accept it.

### Inferences
- The round-1 concern ("orders of 100–150 ILS are unprofitable") is confirmed by the arithmetic; the local market has already responded by pricing heads at 329–399 and tablets as 200–300 ILS bundles.
- Sensitivity: every +10 ILS of landed cost or delivery cuts break-even CPA by ≈$3.2; every +$5 of CPA costs ≈16 ILS per order.
- Excluded costs (all would lower the numbers): creative production/UGC, Shopify apps and plan, customer-service time, unsold inventory, standards testing/labelling, duty, and any refund above the 5% reserve.

### Gaps
- No verified landed cost (no supplier quote, no freight quote, no duty rate).
- CPA is a single-source national median, not a measured figure for these products or price points; real CPA must come from a test.
- Refill rate is an assumption with no small-brand data behind it.

---

## 9. Verdict per candidate

### Takeaway
**Candidate 1 (filtered shower head + refills): CONDITIONAL — proven local demand at 329–399 ILS, but a crowded, claim-sensitive market where the partners would be a late, undifferentiated 8th entrant; test cheaply before any stock.** **Candidate 2a (washing-machine cleaner tablets): CONDITIONAL-leaning-REJECT as a hero product — demand is proven but it is a one-shot bundle business already worked by two aggressive incumbents, with chemical-compliance overhead; viable only as part of a multi-SKU cleaning range.** **Candidate 2b (appliance parts/consumables — Tami4-type filters, robot-vacuum kits, air-fryer liners): REJECT for this team — no paid-social demand, entrenched specialists, AliExpress pricing.**

### Cited Findings (evidence the verdicts rest on; all cited above)
- 7 Israeli shower-filter advertisers; SilQ active since 2024 with 179 reviews on its hero SKU; heads 189–430 ILS, refills 65–179 ILS — [SilQ feed](https://silqisrael.com/products.json?limit=250), [Meta Ad Library IL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A8%D7%90%D7%A9%20%D7%9E%D7%A7%D7%9C%D7%97%D7%AA%20%D7%A4%D7%99%D7%9C%D7%98%D7%A8&search_type=keyword_unordered)
- Class actions over "removes chlorine" and hair claims; independent test 54% chlorine reduction, no softening — [ClassAction.org](https://www.classaction.org/news/class-action-lawsuit-claims-jolie-filtered-showerheads-leave-substantial-amount-of-chlorine-in-water), [Water Filter Guru](https://waterfilterguru.com/jolie-shower-filter-review)
- Tel Aviv water >150 ppm but softening with desalination; chlorine max 0.5 mg/L in the network — [Mei Avivim](https://www.mei-avivim.co.il/%d7%90%d7%99%d7%9b%d7%95%d7%aa-%d7%94%d7%9e%d7%99%d7%9d2/%d7%a7%d7%a9%d7%99%d7%95%d7%aa-%d7%94%d7%9e%d7%99%d7%9d/), [regulations](https://he.wikisource.org/wiki/%D7%AA%D7%A7%D7%A0%D7%95%D7%AA_%D7%91%D7%A8%D7%99%D7%90%D7%95%D7%AA_%D7%94%D7%A2%D7%9D_(%D7%90%D7%99%D7%9B%D7%95%D7%AA%D7%9D_%D7%94%D7%AA%D7%91%D7%A8%D7%95%D7%90%D7%AA%D7%99%D7%AA_%D7%A9%D7%9C_%D7%9E%D7%99_%D7%A9%D7%AA%D7%99%D7%94))
- Tablets: ≈120–150 active Hebrew ads, Relivia 139.90–299.90, Fizz 149, generic 35 ILS delivered — [Meta Ad Library IL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%98%D7%91%D7%9C%D7%99%D7%95%D7%AA%20%D7%A0%D7%99%D7%A7%D7%95%D7%99%20%D7%9E%D7%9B%D7%95%D7%A0%D7%AA%20%D7%9B%D7%91%D7%99%D7%A1%D7%94&search_type=keyword_unordered), [Relivia](https://reliviails.com/products/washing-tablets-relivia), [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%98%D7%91%D7%9C%D7%99%D7%95%D7%AA%20%D7%9C%D7%A0%D7%99%D7%A7%D7%95%D7%99%20%D7%9E%D7%9B%D7%95%D7%A0%D7%AA%20%D7%9B%D7%91%D7%99%D7%A1%D7%94)
- Appliance consumables: zero active Meta ads; Zap dominated by specialists — [Zap Tami4](https://www.zap.co.il/search.aspx?keyword=%D7%A4%D7%99%D7%9C%D7%98%D7%A8%20%D7%AA%D7%9E%D7%99%204)

### Inferences — conditions, failure modes, cheapest tests

**Candidate 1 — shower filter: CONDITIONAL**
- Conditions to proceed: (1) a measured CPA ≤ ~100 ILS at a ≥249 ILS kit price or ≤ ~170 ILS at ≥349 ILS, from a real test; (2) a differentiated, honest angle not already owned — e.g. "old-building rust/sediment you can see" with a transparent, cheap refill, or a design/bundle angle — rather than chlorine/hair/limescale claims; (3) a cartridge with a test report (SGS or NSF/ANSI 177 for the specific SKU) if any chlorine claim is made; (4) a written answer on SI 5452/SI 1347 applicability before importing stock; (5) landed kit cost ≤ ~55 ILS.
- What could make it fail: CPA 1.5–2x the median because of 7 competing advertisers and a 349 ILS price; refill revenue leaking to 1-ILS AliExpress sticks; a consumer-protection complaint or class action over copied competitor claims; returns from customers who expected limescale to disappear; SilQ/RIVO discounting.
- Cheapest pre-investment tests (in order): (a) 0 ILS — watch the Ad Library weekly for 4 weeks: which of Care Filter / Beau Clean / RIVO / Vedya ads are still running after the 11.11–Black Friday window (survivors = profitable creatives); retry Google Trends from an Israeli IP. (b) ≈100–200 ILS — order 2–3 candidate heads + cartridges retail from AliExpress and one SilQ/RIVO unit; measure chlorine before/after with a pool DPD kit, check thread fit, pressure, build quality. (c) ≈1,500–3,000 ILS — a landing page on the existing Shopify store with 2 price points (249 kit vs 349 premium) and pre-order/drop-ship fulfilment of the first 20–30 orders; read CPA, conversion rate, and the share who add a refill pack. (d) Email the Standards Institution/customs broker with the HS code. Stop if CPA > 130 ILS at 249 or > 180 ILS at 349 after ~40–50 purchases' worth of spend.

**Candidate 2a — washing-machine cleaner tablets: CONDITIONAL (weak) as an add-on; REJECT as the single hero**
- Conditions: bundle AOV ≥ ~250–300 ILS (4-pack or mixed cleaning bundle); landed ≤ ~20–23 ILS per 24 tablets including Hebrew hazard labelling/SDS compliance; a freight route that accepts the formula; willingness to build a 5–8 SKU cleaning range for cross-sell (this is what makes Relivia/Fizz work). Not a recurring product — do not model repeat purchase within 12–24 months.
- Failure modes: CPA above $35 against two incumbents with advertorial funnels; refunds under a money-back guarantee; shipment held for labelling/dangerous-goods reasons; consumers discovering the 35 ILS local or $4 AliExpress equivalent; unprovable "bacteria/mould onto your children's skin" claims.
- Cheapest tests: buy Relivia, Fizz and a 35 ILS Bastion pack and compare tablets/packaging/label (are they the same OEM product? is there a Hebrew hazard label?); ask a customs broker about SI 2302 and import licensing for the SDS; only then a small creative test with drop-shipped units.

**Candidate 2b — appliance parts/consumables: REJECT (for this team, now)**
- Why: no evidence of paid-social demand (0 active ads on four Hebrew queries); established specialist sellers with large rating counts on Zap; compatible Tami4 filters already at 142 ILS delivered with multi-pack discounts; AliExpress liners/kits at $1–5; high SKU/model fragmentation; possible standards issues for drinking-water filters (SI 5452 clearly relevant there).
- What would change the verdict: an SEO/Zap/marketplace-led strategy with real stock breadth — a different business from the partners' current paid-social store.

### Gaps (what this research could not establish and should not be assumed)
- Israeli search-trend direction (Google Trends blocked) and organic consumer discussion in Hebrew (forums/Facebook/press not reachable).
- Shein/Temu current prices; supermarket/pharmacy shelf prices; KSP.
- Verified factory quotes, MOQs, certifications, duty rates, real freight cost.
- Legal applicability of SI 5452/SI 1347 to filtered shower heads; chemical import licensing for tablets; thread standard primary source.
- Any competitor's actual sales, CPA or reorder rate.
