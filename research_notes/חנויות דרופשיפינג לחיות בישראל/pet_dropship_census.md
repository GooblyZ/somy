# Census: Israeli-facing online stores selling pet toys/gadgets, and which ones dropship (data collected 2026-11-13)

Scope note. Builds on `research_notes/מחקר מוצרים לאיקומרס בישראל/09_deepdive_pets_israel_specific.md` (Catopia, Pet Planet, Anipet, Kama Zol, A10/Dison) and does not redo that work. All observations below were made on **2026-11-13** unless another date is given. Labels: **FACT** = observed directly in a page, feed or Ad Library card; **REPORTED** = the seller's own claim; **ESTIMATE** = my calculation; **UNVERIFIED** = plausible but not checked.

**How the data was collected**
- Meta Ad Library, country=IL, active ads, keyword search, headless Chromium, a new browser context for each query. 41 queries in total. The page loads even though the HTTP status is 403. Each query renders only the first ~25–30 ad cards, so **ad counts below are lower bounds** ("ads seen"), not totals. The total-results figure Meta shows ("כ-N תוצאות") is quoted where it appeared.
- Shopify `/products.json` (up to 3 pages of 250), `/policies/*`, and the homepage HTML scanned for app signatures. WooCommerce Store API.
- Scripts and raw dumps: `/tmp/claude-0/-home-user-somy/56050f0a-2de7-5734-b72d-e7d3e8ae6cb9/scratchpad/petcensus/` (`adlib.js`, `probe.py`, `deep.py`, `bydom.py`, `out*/`).

**Blocked or failed (no data from these):**
- **Zap.co.il**: every search returned a ~126-character bot-check page. A retry was refused by this environment's permission policy as bot-check circumvention, so **no Zap "רכישה מחו"ל" data was collected in this pass**. The Zap facts in file 09 still stand.
- **Ad Library**: these queries came back as a 604-character empty shell, which can be a false zero or rate limiting: לייזר לחתול, משגר כדורים, האכלה אוטומטית, מאכיל אוטומטי, מזרקת מים, איירטאג, מתגלגל, מקל לייזר, חתולים. The store-name queries (Catopia, קטופיה, Petrix, Patent Prime, Meow Li) also failed this way, all late in the session. So **whether Catopia advertises is still unknown**.
- **StoreLeads** IL Pets category page: HTTP 404.
- **WebSearch** (US-only index) returned no Israeli pet-gadget stores.
- **Also not reached**: meowmouth-il.com, kamazol.co.il, interpet.co.il and www.cresomall.com (connection errors); speedog.co.il, petnet.co.il, gag-lachayot.co.il, pets-il.printandsell.shop and mhaim1.com (HTTP 403); zylarx.com returned HTTP 429 on a later request.
- **AliExpress image/title matching** was not done. Dropship evidence rests on SKUs, vendor fields, policies and catalog structure.

**Dropship indicators applied (one point each):**
- (D1) stated delivery of 5+ business days, or "abroad / warehouse abroad"
- (D2) customs, "מכס" or the $75 exemption in the policy
- (D3) AliExpress-ID SKUs (`1005xxxxxxxxxx…`, the DSers/AliExpress pattern) or CJ SKUs
- (D4) vendor fields with Chinese-seller or "us"-mall style names (e.g. `lovelifeC`, `firstroost-us`) or random codes (`c1`, `2b`)
- (D5) a general store: many unrelated products with emoji and "50% off" titles
- (D6) no business ID or address, Gmail-only contact
- (D7) Ali Reviews, or the Trustoo/Ryviu/Loox stack used to import marketplace reviews

**Classes:**
- **Confirmed**: the seller states it, or the shop's own data shows it (D1 with abroad wording, or D3).
- **Likely**: 2 or more indicators.
- **Unclear**: fewer than 2.
- **Local stock**: chains and shops with stated same-day or 1–4-day delivery, a physical store, or FMCG catalogs.

---

## 1. Which Israeli-facing stores sell pet toys/gadgets online, and which dropship?

### Takeaway
I found **one confirmed and four likely dropshippers that actually sell pet toys/gadgets**, plus **one hybrid** (Catopia):
- **Confirmed**: PetSolutions.
- **Likely**: Zylarx, Kaufroom and Nexapest (general stores that carry pet gadgets as a minority), and Patent Prime (cat accessories).
- **Hybrid**: Catopia, a cat specialist with dropship origins that now claims a Holon warehouse.

Five more likely-dropship or single-product **pet** stores sell **supplements or care products, not toys** (Meow Li, Bloomi, Rovex, Woof, Pups, VetCalm). All of them were launched in 2026 and are advertised hard with Meta "advertorial" ads.

The dedicated *pet-toy/gadget* dropship segment in Israel is **thin: no store dominates it, and the live ads are recent**. The visible competition is the local chains, which sell toys alongside food.

### Table A: dropshippers and hybrids that sell pet items (FACT unless labelled)

| # | Store + URL | Platform | Niche | Age (earliest product `created_at`) | Pet products / total | Price range ₪ (pet items) | Sample hero products | Stated delivery / origin | Dropship evidence | Activity evidence | Class / confidence |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | **PetSolutions** — [petsolutions.co.il](https://petsolutions.co.il/products.json?limit=250) | Shopify | dogs + cats, toys/enrichment/grooming | 2025-01-05; newest 2026-11-07 | 21 pet-related of 46 (the rest are pet-adjacent: car seat cover, memorial kits) | 39.9–329.9 | "Tago" spring hunting toy for dogs ₪159.9; snuffle/enrichment game ₪109.9; lick/enrichment bowl ₪139.9; treat puzzle ₪109.9; cat hunting game ₪79.9; de-shedding glove ₪39.9–79.9 | Shipping policy lists **7–14** and **8–18 business days**, plus "additional delays of 1–9 business days". Refund policy: "in exceptional cases... return to a **warehouse abroad** address" — [shipping](https://petsolutions.co.il/policies/shipping-policy), [refund](https://petsolutions.co.il/policies/refund-policy) | D1 (abroad + 7–18 days), **D3: SKU `1005009178562974_202594829` = AliExpress product-ID pattern**, D6 (contact `petssolutionsofficial@gmail.com`, ToS lists no address/ID) — [ToS](https://petsolutions.co.il/policies/terms-of-service) | Active Meta ads seen with start dates **22 Jul 2026** and **10 Nov 2026** ("Tago" creative) on the queries צעצוע לכלב, צעצוע אינטראקטיבי, משועמם. Products still being added (Sept–Nov 2026) | **CONFIRMED dropshipper. High confidence** |
| 2 | **Zylarx** — [zylarx.com](https://zylarx.com/products.json?limit=250) | Shopify (Ryviu reviews) | general store; pet gadgets are a minority | 2024-04-27 (earliest pet item); feed has ≥631 products; newest 2026-11-12 | 17 pet-related of 631 | ~38–147 | "Automatic rechargeable rolling ball for cats and dogs" ₪65 and "smart bouncing ball with LED" ₪65 (both created 2026-11-12); robot puppy ₪76.99; electric spray comb ₪70; pet toilet water dispenser ₪79.99 | `/policies/shipping-policy` returns 404 and the contact page is empty. **No stated delivery time** | D4 (vendors `lovelifeC` 162, `mysite` 67, `Carkur`, `manchestore`, `se.aurora009`), D5 (sells a hand-crank generator, Celtic necklaces, tactical keychains and women's clothing alongside the pet items), SKU pattern `CW251205045-…`, D6 | **4 active ads seen, all started 12 Nov 2026** (rolling/smart ball for bored dogs) on צעצוע לכלב, צעצוע חכם, משועמם | **LIKELY dropshipper** (probably a cross-border general store translated into Hebrew). **Medium-high** |
| 3 | **Kaufroom** — [kaufroom.com](https://kaufroom.com/products.json?limit=250) | Shopify (Vitals, Trustoo, Ryviu) | general store | earliest pet item 2026-05-11; ≥750 products; newest 2026-11-13 | 41 pet-related of 750 | ~49–99 (one cat bed is priced at a placeholder ₪1,999,999.99) | interactive electronic smart dog ball ₪59.99; anti-bark device ₪89.99; detangling comb ₪59.99; reusable pet-hair laundry balls ₪59.99; pet tooth spray ₪59.99 | none found | D4 (vendors `2b`, `1`, `c1`), D5 (power stabilisers, socks, grease paste, emoji "50% off" titles), placeholder prices, mixed English/Hebrew titles | **4 active ads seen, started 29 Oct and 6 Nov 2026** (page "Kaufroom Home", query משועמם) | **LIKELY**. **Medium-high** |
| 4 | **Nexapest** — [nexapest.com](https://nexapest.com/products.json?limit=250) | Shopify (Vitals, Trustoo, Ryviu) | general store | **2026-10-29** (store ~2 weeks old) | 7 pet-related of 71 | 44–119 | automatic pet water fountain ₪119; rechargeable pet clipper ₪109; slicker brush ₪59.99; anti-static cat fur spray ₪44 | none found | D4 (vendors `firstroost-us` 38, `solitudemalls`, `houstonget`), D5 (eyeliner, scratch-repair pen, plumber's wrench, night-vision monocular) | **2 active ads seen, started 12 Nov 2026** (query צעצוע חכם) | **LIKELY**. **Medium** |
| 5 | **Patent Prime** — [patent-prime.com](https://patent-prime.com/products.json?limit=250) | Shopify (Judge.me, Trustoo) | cats (fountain accessories, litter, dental) | 2024-10-13; newest 2026-10-28 | 12 total, all cat-related (3 caught by my keyword filter: litter-trap mat ₪89, cat play bed ₪149.9, e-book) | 59.9–279.9 | "MeowMouth" dental powder; fountain cleaning kit; extra filter packs ("8 filters at half price") | "should arrive within **5–12 business days**" after processing — [shipping](https://patent-prime.com/policies/shipping-policy) | D1 (5–12 days), D7 (Trustoo + Judge.me), SKU strings such as `14:29#Transparent double` (AliExpress variant-property format) | Ads seen on בעלי חתולים and מברשת לחתול pointing to patent-prime.com. A separate page, "Meow Mouth", with 4 ads started 8 and 10 Nov 2026, lands on **meowmouth-il.com** (unreachable). It is UNVERIFIED that this belongs to Patent Prime | **LIKELY**. **Medium** |
| 6 | **Catopia** — [catopiaa.com](https://catopiaa.com/products.json?limit=250) | Shopify (**Ali Reviews**, Vitals) | cats, broad (food, litter, toys, gadgets) | **2023-08-07**; newest 2026-06-26 | 131 pet-related of 151 | 9.9–1,195 | automatic feeder ₪349; **360 laser toy ₪129.9**; 3 L fountain ₪179; **AirTag collar ₪59.9**; catnip lick toy ₪29.9; reusable hair roller ₪49.9; wand toys ₪39.9–59.9 | **Contradictory, both on the seller's own pages.** The shipping policy says 3–5 business days, ₪29.9 courier, "at most 10 business days" ([shipping](https://catopiaa.com/policies/shipping-policy)). The contact page says "warehouse in Holon", same-day in the centre, 1–4 days elsewhere, free above ₪299, **yet its FAQ says "the delivery will arrive within 7–21 business days"** ([contact](https://catopiaa.com/pages/contact)) | D7 (Ali Reviews app), D1 (leftover 7–21-day FAQ text); vendor names of real brands (WORLD'S BEST, KING CAT, WILDA) show it also stocks branded consumables | No products added since 2026-06-26. Not seen in any keyword ad scrape; the name query failed. 32 reviews on one product (file 09) | **HYBRID: likely began as a dropshipper, now REPORTED to hold local stock in Holon. Medium** |

### Table B: single-product / supplement "pet funnel" brands (likely dropship or 3PL; **not toys**, but they compete for the same Meta audience)

| Store | Platform / age | Products | Delivery (stated) | Indicators | Active ads seen | Class |
|---|---|---|---|---|---|---|
| **Meow Li** — [meowli.co.il](https://meowli.co.il/products.json?limit=250) | Shopify, products created 2026-10-11 to 10-28 | 6: taurine supplement (monthly subscription), "2 balls with bell", cat fur brush, digital guide, "priority & shipping protection" upsell; ₪10–258 | "regular delivery **5–15 business days**... no more than **35 business days**"; mentions customs (מכס) — [shipping](https://meowli.co.il/policies/shipping-policy) | D1, D2 | none matched by domain in this scrape | LIKELY. Medium |
| **Bloomi** — [bloomi.co.il](https://bloomi.co.il/products.json?limit=250) | Shopify, 2026-06-16 | 3: dog dental powder, paw balm, probiotic chews; ₪39–199.9 | 6–14 business days; customs mentioned (homepage) | D1, D2 | **7 ads**, started 19–27 Oct 2026 (pages "Bloomi", "בעלי כלבים בישראל") | LIKELY. Medium |
| **Rovex** — [try-rovex.com](https://try-rovex.com/products.json?limit=250) | Shopify, 2026-06-23 | 9: dog joint/daily supplements, dental spray, "insurance & warranty" upsell; ₪19.9–250 | **7–20 business days** (homepage) | D1, D7 (Loox + Judge.me + Ryviu) | ad seen (query ליקוק): "50% off + free shipping" | LIKELY. Medium |
| **Woof** — [mywoof-il.com](https://mywoof-il.com/products.json?limit=250) | Shopify, 2026-08-03 | 5: calming chews, salmon oil, joint, probiotic, dental powder; ₪139–399 | "5–7" and "1–3" days, "from warehouses" (homepage) | D7 only | **7 ads**, started 2–23 Sep 2026 (page "WOOF - Pet Wellness") | UNCLEAR (may ship from a local 3PL) |
| **Pups** — [trypups.com](https://trypups.com/products.json?limit=250) | Shopify, 2026-05-07 | 7: calming, joints, dental+allergy kit, paw balm, salmon oil; ₪79–249.5 | none found | Ryviu; persona and UGC pages ("בעלי כלבים ממליצים", "mango_the_sausage_ with Pups") | **12 ads**, started 22–30 Oct 2026 | UNCLEAR |
| **VetCalm** — [vetcalm-il.com](https://vetcalm-il.com/products.json?limit=250) | Shopify, 2026-10-09 | 7: calming room diffuser (subscription), e-guides, "mystery gift worth ₪100", shipping insurance; ₪12–374.88 | 3–8 / 3–6 / 1–2 days (homepage) | single-product funnel; **ads run from personal-name pages** ("גיל רוזנברג", "יעל אשכנזי") written as first-person stories | **6 ads**, started 24–25 Oct 2026, appearing on צעצוע לכלב, **שטיח הרחה**, משועמם | UNCLEAR (funnel tactics; origin not stated) |
| **Bazaria** — [bazaria-il.com](https://bazaria-il.com/products.json?limit=250) | Shopify, 2025-09-28 | 138 products, only 1 pet item (CalmiDog™ ₪129); ™-branded generic gadgets | none found | D4 (vendor `Bringwell` 45), D5, ™-renaming | **7 ads**, started 11 Aug and 8 Sep 2026 | LIKELY general dropshipper. Pet share is marginal |

These six funnel brands share one template:
- products: dental powder, calming chews, salmon oil, paw balm
- upsells: a "shipping protection" product and an e-book
- many review apps installed at once
- launched in 2026, all between May and October

INFERENCE: this points to one playbook or course, possibly shared operators. That is UNVERIFIED.

### Table C: other stores that sell pet items online, not dropship or unclear

| Store | Platform | Notes | Class |
|---|---|---|---|
| **Petrix** — [petrix.co.il](https://petrix.co.il/products.json?limit=250) | Shopify (Judge.me, Ryviu) | 154 of 210 products are pet items, created 2025-04-30 to 2026-11-06. Branded leashes, collars, silicone bowls, personalised bowls; ₪24.9–479; vendor "Petrix" only; no shipping policy page (404) | UNCLEAR (own-brand, possibly private-label imports) |
| **petli** — [mypetli.com](https://mypetli.com/products.json?limit=250) | Shopify | 8 products, 2025-07 to 2025-11; natural flea collars, combs, dental kit; ₪19.9–209.9; nothing added after Nov 2025 | UNCLEAR, apparently dormant |
| **DON Pet Style** — [donpetstyle.com](https://donpetstyle.com/) | Wix | "Made in Tel Aviv" premium beds and accessories; ad started 21 Oct 2026 | Local brand |
| **A10** — [a10.co.il](https://a10.co.il/) | Wix | hardware/gadget importer ("from the importer to the consumer"), sells the hair roller (file 09). Homepage mentions 3–8 days and customs | UNCLEAR |
| **Dison** — [dison.co.il](https://dison.co.il/) | unknown (no signature found) | roller "unique patent, up to 5 days" (file 09) | UNCLEAR |
| **Kama Zol** | — | Zap "purchase from abroad" flag on a roller (file 09); site unreachable today | LIKELY (Zap flag = D1), carried over |
| **VetPets** — [shopvetpets.com](https://shopvetpets.com/) | Shopify (Loox) | English, "3–5 business days" | Foreign, not Israel-specific |
| **Print-on-demand**: "Emma Girard" → pets-il.printandsell.shop | — | **5 ads**, started 9 Nov 2026, query צעצועים לחתולים. Site returned 403 | Foreign POD, UNVERIFIED |
| **Cross-border marketplaces advertising pet toys in IL**: AliExpress, Alibaba.com, cresomall.com (pages "Pickelect.y", "Sakesfor.Pro", started 3 and 6 Nov 2026), Ecouaer US (pet-hair/grooming, 3 ads Jul–Sep 2026) | — | English-language ads delivered in IL on "cat toy" / "dog toy" | Direct foreign competition |

### Table D: local-stock pet retailers selling toys online (competition, NOT dropshippers)
All FACT from Ad Library cards and/or feeds; delivery claims are REPORTED.
- **Anipet**: Shopify chain. Active ads started 3 Aug, 2 Sep and 12 Nov 2026 — [anipet.co.il](https://www.anipet.co.il/)
- **Pet Planet**: Woo (file 09)
- **JoyBox**: Woo, 2–4 / 1–2 days. 5 ads (3 Sep to 13 Oct 2026) — [joybox.co.il](https://joybox.co.il/)
- **PetBest**: Woo, "free shipping". 7 ads (Sep 2025 to Aug 2026)
- **Top Dog**: Woo chain. Ads 1 and 4 Nov 2026
- **Pet Expert**: Woo. Ad 26 Aug 2026
- **Pets Online**: Woo. Ads 9 Sep 2026
- **super4pet**: Shopify since 2020-04-27; Monge/KONG/Purina vendors
- Other chains and shops: **CrazyPet** (ads Apr 2026), **Zanzibar4pets**, **Petcall**, **All4pet**, **Keflahayot** (Hod Hasharon, 7 ads), **Megapet**, **Petnet**, **Gag Lachayot**, **Brownfield** (cat-tree ad, 10 Aug 2026), **PetPower** (tofu litter ad, 25 Oct 2026), **Royal Pet**, **Petilux**, **Biopet**, **Shelly Pets**, **Zoolu**, **Dr Food**, **Mitz Petel Pets**, **Hish Hay**
- **Bestec**: electronics importer, 5 cat-fountain ads started 21 Oct 2026 — [bestec.co.il](https://www.bestec.co.il/)
- **Bug** (bug.co.il) and **KSP** (general retailers)

### Ad Library keyword totals (FACT, Meta's own "about N results" for active IL ads, 2026-11-13; most hits are unrelated)
- צעצוע לחתול ≈6
- צעצוע לכלב ≈16
- צעצוע אינטראקטיבי ≈3
- שטיח הרחה ≈3 (all VetCalm persona ads)
- מזרקה לחתול ≈5 (all Bestec)
- צעצועים לחתולים ≈15
- צעצוע חכם ≈19
- משועמם ≈37
- גאדג'טים לחיות ≈15 (no pet stores among them)
- בעלי חתולים ≈46
- כלבים ≈2,100
- dog toy ≈4,000 and cat toy ≈360 (dominated by drama apps, Alibaba and AliExpress)

Source: [Meta Ad Library, IL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A6%D7%A2%D7%A6%D7%95%D7%A2%20%D7%9C%D7%9B%D7%9C%D7%91&search_type=keyword_unordered) (pattern; swap q=).

### Cited Findings (key ones restated)
- PetSolutions carries an AliExpress-ID SKU, states 7–14 / 8–18 business-day delivery and a "warehouse abroad" return address — [products.json](https://petsolutions.co.il/products.json?limit=250), [shipping](https://petsolutions.co.il/policies/shipping-policy), [refund](https://petsolutions.co.il/policies/refund-policy)
- Zylarx launched two rolling/bouncing smart-ball products on 2026-11-12 and started 4 ads the same day — [products.json](https://zylarx.com/products.json?limit=250), [Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A6%D7%A2%D7%A6%D7%95%D7%A2%20%D7%97%D7%9B%D7%9D&search_type=keyword_unordered)
- Catopia says it has a Holon warehouse and 1–4-day delivery, but its own FAQ still says 7–21 business days, and it runs Ali Reviews — [contact](https://catopiaa.com/pages/contact), [shipping](https://catopiaa.com/policies/shipping-policy)
- Meow Li states 5–15 business days (up to 35) and mentions customs — [shipping](https://meowli.co.il/policies/shipping-policy)
- Patent Prime states 5–12 business days — [shipping](https://patent-prime.com/policies/shipping-policy)

### Inferences
- The products dropshippers push in Israeli ads right now are **rolling/auto-moving balls** (Zylarx, Kaufroom), **dog enrichment/hunting toys** (PetSolutions "Tago", snuffle and lick bowls) and **grooming gadgets** (Nexapest, Kaufroom). I saw **no active ads** for laser toys, ball launchers, pet cameras or GPS collars. Those queries returned empty pages, which may be false zeros.
- Most ads in the niche started in the **last 4 weeks** (Oct to Nov 2026). This looks like product testing, not established winners. Ad longevity, the best free proxy for profitability, is short everywhere except PetSolutions (oldest live ad 22 Jul 2026, ~16 weeks) and the funnel brands from Aug–Sep 2026 (Woof, Bazaria).

### Gaps
- Sales, order volumes and conversion for every store: unknown. Revenue was not estimated.
- Review counts and dates (Judge.me/Ryviu widgets) were not read.
- Zap "purchase from abroad" flags were not re-checked (blocked).
- No AliExpress listing-match check was done.
- Catopia's ad activity is unknown.

---

## 2. How many are there, and how complete is this census?

### Takeaway
Counts from this pass, among stores that sell pet **toys/gadgets** to Israelis in Hebrew:
- **Confirmed dropshippers: 1** (PetSolutions).
- **Likely dropshippers: 5**:
  - Zylarx, Kaufroom, Nexapest (general stores where pets are 2–10% of the catalog)
  - Patent Prime (cat accessories)
  - Kama Zol (Zap flag, carried over from file 09)
- **Hybrid: 1** (Catopia).
- **Unclear: 4** (Petrix, petli, A10, Dison).
- **Local-stock competitors: ~30** online pet retailers and chains.
- **Separately, pet supplement/care funnels: 7.** 3 likely dropship (Meow Li, Bloomi, Rovex), 3 unclear (Woof, Pups, VetCalm), and Bazaria, a likely general dropshipper with one pet SKU.

**Hebrew-language stores dedicated to pet toys/gadgets and confirmed or likely dropshipping: 2** (PetSolutions and Patent Prime), plus Catopia if its history counts.

### Cited Findings
- Store-level evidence is in Tables A–D above, with URLs, all observed 2026-11-13.
- Israel has ~12,324 Shopify stores (StoreLeads estimate, Nov 2026, carried over from earlier research). No IL × Pets breakdown could be fetched: the [StoreLeads](https://storeleads.app/reports/shopify/IL/category/Pets%20&%20Animals) page returned 404.

### Inferences (completeness)
- ESTIMATE: this census probably captures **most of the stores *currently advertising* on Meta** with Hebrew pet-toy copy. I used 41 query variants, and the same few domains kept recurring (PetSolutions, Zylarx and VetCalm each showed up on 3+ queries).
- It **under-counts**:
  - (a) stores not running Meta ads right now (organic, TikTok-only or Google-only sellers)
  - (b) stores hidden by the 9+ Ad Library queries that returned empty pages, especially the gadget-specific terms (laser, launcher, feeder, fountain, AirTag)
  - (c) general dropship stores with a few pet SKUs, which are very numerous and hard to find by pet keywords
  - (d) stores selling via Instagram or WhatsApp only
- A reasonable range for *dedicated* Hebrew pet-gadget dropship stores is therefore **low single digits to ~10**. For general stores that carry some pet gadgets, it is **tens**. Both ranges are UNVERIFIED and should not be treated as counts.
- The census does **not** cover TikTok Shop (not operating in Israel to my knowledge, UNVERIFIED), Instagram shops, Facebook Marketplace or AliExpress's own Hebrew storefront, which is the largest "dropship" competitor of all.

### Gaps
- No Shopify-by-category list for Israel was accessible (StoreLeads 404; BuiltWith/MyIP not attempted within the budget).
- TikTok and Instagram were not searched.

---

## 3. What this says about saturation and opportunity

### Takeaway
The niche is **not saturated by specialist dropshippers**. In this pass there was one confirmed Hebrew pet-toy dropshipper (PetSolutions, 46 SKUs, ads since July 2026) and one small cat-accessory store (Patent Prime). It **is crowded on three other fronts**:
- **Local chains** that sell toys next to food and offer 1–4-day delivery (Anipet, JoyBox, PetBest, Top Dog and others)
- **General Hebrew-translated dropship stores** that drop in the same viral gadgets (Zylarx, Kaufroom, Nexapest all launched smart balls or grooming gadgets in Oct–Nov 2026)
- **AliExpress/Alibaba**, which advertise "cat toy" and "dog toy" in Israel directly

### Cited Findings
- Local chains deliver in 1–4 days and advertise continuously (JoyBox 2–4 days; Catopia 1–4 days claimed) — [joybox.co.il](https://joybox.co.il/), [Catopia contact](https://catopiaa.com/pages/contact)
- General dropshippers are testing the same gadgets right now: Zylarx rolling ball, ads from 2026-11-12; Kaufroom smart dog ball, product from 2026-07-09 and ads from 29 Oct 2026; Nexapest fountain and clipper, store from 2026-10-29 — [Zylarx](https://zylarx.com/products.json?limit=250), [Kaufroom](https://kaufroom.com/products.json?limit=250), [Nexapest](https://nexapest.com/products.json?limit=250)
- The advertising style that dominates the pet niche on Meta IL is first-person "advertorial" or persona ads selling calming and dental products, not toys (VetCalm, Pups, Bloomi, Woof) — [Ad Library: שטיח הרחה](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A9%D7%98%D7%99%D7%97%20%D7%94%D7%A8%D7%97%D7%94&search_type=keyword_unordered)

### Inferences
- **Opportunity**: a Hebrew, brand-led **dog-enrichment/interactive toy** store has only one direct dropship rival (PetSolutions) visible on Meta. The search volume behind it is unknown: Google Trends was blocked earlier.
- **Speed is the biggest weakness.** PetSolutions' 7–18-day promise, against the chains' 1–4 days, leaves room for:
  - a hybrid model: hold local stock of the 3–5 winners, as Catopia apparently did, and dropship the long tail
  - a gadget-only store that chains don't carry: auto-moving balls, enrichment puzzles, smart lasers
- **Risks**:
  - The same gadgets appear quickly in general stores at ₪59–65 with "50% off" framing, which caps prices.
  - AliExpress advertises directly.
  - The ad pattern suggests most tests are under 4 weeks old, so there is no evidence yet that any of these products is profitable in Israel.
  - Pet supplements and calming products, the most heavily advertised category, carry regulatory risk (veterinary claims). This was not researched.
- **Next cheap checks**:
  - (1) Re-run the empty Ad Library gadget queries in a few days, one per new context, with pauses.
  - (2) Read the Ryviu/Judge.me review counts and dates for PetSolutions, Zylarx and Patent Prime.
  - (3) Image-search PetSolutions' "Tago" and Zylarx's ball on AliExpress for landed cost.
  - (4) Check Zap manually in a normal browser for "רכישה מחו"ל" flags.

### Gaps
- No sales, traffic or profitability data for any store. Ad counts are lower bounds and show activity, not success.
- The demand side (search volume for Hebrew pet-toy terms) is unmeasured in this pass.
