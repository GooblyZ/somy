# Israeli single-hero-product DTC brands (BAGLY-style): census, longevity evidence, winning patterns, and gap ideas

Research date: **2026-11-14**. Labels: **FACT** = I observed it directly today in a primary page/feed/Ad Library result; **REPORTED** = the brand's own claim (review widgets, "X happy customers", guarantees) or a third party's statement, not independently verified; **ESTIMATE** = my arithmetic/inference; **UNVERIFIED** = plausible but not confirmed.
Excluded by brief: scented body cream, pheromone products (none were included; one pillow-mist brand, Soleva, is noted but is not a body cream).

**How the data was collected (read this before using any number):**
- Meta Ad Library was reachable today via headless Chromium (unlike on 2026-11-11, when note 02 found it blocked). URL pattern: `https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=<term>&search_type=keyword_unordered`, fresh browser context per query, ~40 queries. Searching a store's **domain** as the keyword (e.g. `q=bagly.co.il`) worked well and returns that store's ads plus "persona" pages that link to it. Scripts: `/tmp/claude-0/-home-user-somy/56050f0a-2de7-5734-b72d-e7d3e8ae6cb9/scratchpad/heroes/adlib.js`, raw JSON per query in `.../heroes/out/`.
- Ad Library caveats: (1) results are sorted by relevance, not date, and I scrolled only about 30 ad cards per query, so the **"oldest active ad" I report is the oldest among the cards I loaded, a lower bound on longevity**; (2) the "N ads" figure is the sum of Meta's "X ads use this creative and text" groupings on the cards loaded, so it is a **lower bound**; (3) the "≈ results" total that Meta prints (e.g. "כ-290 תוצאות") counts active ads matching the keyword, which for a domain query is a reasonable proxy for how many ads the brand runs right now; (4) roughly a third of queries returned nothing (blank result area after 40 s). I cannot tell "zero ads" from "page did not load", so **an empty result is UNVERIFIED, not proof that no advertiser exists**; (5) active ads show activity and probable return on spend, **not sales**.
- Store data: Shopify `/products.json?limit=250` (earliest `created_at` = store-age proxy; the feed caps at 250 products) and `/meta.json` (myshopify domain, registered country, currency), plus product-page HTML scraped for review-widget counts, delivery text and guarantee text. Script: `.../heroes/shop.py`, `.../heroes/hero.py`. WooCommerce stores (izzy.co.il, hamadlik.co.il, dareordare.co.il, cycplusisrael.com) were noted but not parsed.
- AliExpress: headless Chromium search sorted by orders, ILS display (`.../heroes/ali.js`, output in `.../heroes/out/ali_*.txt`). Very low prices like ₪2.3–₪5 are usually "new shopper" welcome deals or accessory variants, so I quote the realistic band.
- Not done: no captcha or bot check was bypassed. TikTok Creative Center, Similarweb and Google Trends were not tried (all blocked per note 02).

---

## Q1. Which Israeli one-product / few-product DTC brands are active in 2025–2026, and what do they sell?

### Takeaway
I found 38 active Hebrew-language DTC stores built around one hero product or a small line, across travel, cleaning, pests, sleep and snoring, pain, pets, beauty tools and seasonal goods. About 30 of them are on Shopify. Most launched in 2026, sell a hero at 139–399 ILS with 2- or 3-unit bundles, and ship from abroad in 5–16 business days.

### Cited Findings

Below, **AL** = Meta Ad Library active-ads search for Israel. "Oldest active" = oldest start date among loaded cards (lower bound). "Results" = Meta's approximate active-ad count for the keyword. All rows are **FACT as observed on 2026-11-14** unless a cell says REPORTED.

**Travel (the BAGLY cluster)**
- **BAGLY**: hero is the BaglyTravel under-seat flight bag at 389.90 ILS (compare-at 500), product created 2026-01-21. The line also has OnlyBag 448.90, MoreSpace expandable 239.90, SafeTravel anti-theft 199.90, and add-ons BaglyPillow 89.90 (2026-07-23) and Liquid Kit 49.90 (2026-08-11). Store: Shopify `bagly-2.myshopify.com`. The feed hits its 250-product cap; the earliest product is 2022-10-26, so this is an older general bag store that pivoted to a hero. The hero page's review widget shows 16 reviews (REPORTED). Delivery is "3–14 business days" to a pickup point, and there is a "14-day trial" (REPORTED). AL `q=bagly.co.il`: about 290 results. Oldest active ad is 2026-04-16, a group of 18 ads with a scarcity hook ("the last stock of our flight bag has almost run out"). Persona and creator pages also run ads (נעמה סוויסה, אליעד ומאיה, "המלצות לפני שטסים"), and an influencer coupon "adva199" takes 90 ILS off. Ad hook: "the flight is cheap, then hundreds of shekels just for a suitcase". Sources: [products.json](https://bagly.co.il/products.json?limit=250), [hero page](https://bagly.co.il/products/תיק-טיסות-baglytravel), [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=bagly.co.il&search_type=keyword_unordered)
- **KitFlow**: flight bags AeroFlow and SkyFlow at 369 (compare-at 550), Apex 399, JetSet/FlyEase "flight kits" 559, packing cubes 119, and a 0-ILS "free" destination-list product (compare-at 79) used as a gift. Shopify, 17 products, earliest 2026-05-12, registered country IL. AL (`q=תיק טיסה`): 5 ads, start 2026-07-12. The domain query returned empty (UNVERIFIED). Sources: [products.json](https://kitflow.co.il/products.json?limit=250), [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%AA%D7%99%D7%A7%20%D7%98%D7%99%D7%A1%D7%94&search_type=keyword_unordered)
- **Protego**: flight bag 349 (compare-at 698), add-on wheels kit 299, plus sleep mask, pillow and earbud upsells. Shopify, 6 products, earliest 2026-10-01. AL: 1 ad from 2026-10-27. Source: [products.json](https://tryprotego.com/products.json?limit=250)
- **FlyHugz**: a US brand (USD prices, 58 products since 2023-11-02) that started running Hebrew ads; 8 ads from 2026-11-12. Travel pillow $39.90. Source: [products.json](https://flyhugz.com/products.json?limit=250)
- **Rosina**: travel pillow at 119 / 2 for 199 / 3 for 249; 6 ads from 2026-11-12. The store has 4 unrelated products since 2026-10-07 (it also sells a ratchet extender), registered country US. Source: [products.json](https://rosinaofficial.com/products.json?limit=250)
- **ZuZu Sandals**: travel and comfort sandals. Shopify since 2020-05-30, 24 products. AL: 8 ads from 2026-02-25. Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=zuzusandals.com&search_type=keyword_unordered)

**Home cleaning and hygiene**
- **Relivia**: hero is washing-machine cleaning tablets: 1 pack 139.90 / 2 packs 199.90 / "3+1 free" 299.90 (compare-at 199.90/399.90/599.90), created 2026-05-31. It then added a new consumable roughly every month: laundry scent beads (2026-06-24, 99.90 / 3 for 219.90 / 6 for 399.90), dishwasher tablets (2026-07-28, same ladder as the hero), mold gel (2026-08-06), toilet kit with 42/84/126 heads (2026-08-20, 199.90/299.90/399.90). Shopify, 9 products. Delivery "7–16 business days" (REPORTED, i.e. from abroad). The FAQ mentions a 30-day full refund; the page claims 9,000 (REPORTED). AL `q=reliviails.com`: about 470 results; oldest active 2026-06-20 (a group of 21 ads). Persona/"news" pages run ads too ("נשים ללא פילטר", "הסודות לניקיון הבית", "חדשות ישראל אונליין", "I've dismantled 6,000 washing machines in 19 years"). Sources: [products.json](https://reliviails.com/products.json?limit=250), [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=reliviails.com&search_type=keyword_unordered)
- **Fizz**: hero is Fizz Air, a plug-in odor purifier for the cat litter box: 1 for 139 / 3 for 271 / 5 for 382 / 7 for 477. Also sells a stain remover 89, a grout pen 54.90 and sponges. Shopify, 14 products, earliest 2026-06-30. Review widget 2,610 (REPORTED); delivery "5–10 business days". AL `q=fizz.co.il`: about 960 results, the highest volume found. Oldest active 2026-08-04 (groups of 12 and 8 ads). Persona pages: "איכות האוויר בבית", "נקיון וסדר הבית", "חולי נקיון וסדר". Hooks cover dog urine, cigarette smell and washing-machine smell. Sources: [products.json](https://fizz.co.il/products.json?limit=250), [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=fizz.co.il&search_type=keyword_unordered)
- **Freshora**: a true single-product store, a fridge odor absorber at 179 (compare-at 358), created 2026-05-18. Review widget 379, plus a "4,127" claim (REPORTED). Delivery "10–20 / 14–17 business days". AL: persona ads ("שרה כהן", "צרכנים בודקים") dated 2026-10-13 and 2026-11-11; the domain query returned empty (UNVERIFIED). Source: [products.json](https://try-freshora.com/products.json?limit=250)
- **SilQ** (already known): Q head filter shower head 379/395 (compare-at 499), refill cartridge 129, Little Q 189. Shopify since 2024-02-09, 16 products. The Q head widget shows 179 reviews (REPORTED). AL `q=silqisrael.com`: about 16 results; oldest active 2026-07-13 (14 ads); plus influencer whitelisting ("libby.chebb עם SilQ"). Sources: [products.json](https://silqisrael.com/products.json?limit=250), [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=silqisrael.com&search_type=keyword_unordered)
- **Vedya**: XL shower head 179.90 (compare-at 224.90) and a filter shower head 149.90, plus bathroom add-ons. Shopify since 2024-10-23, 36 products. Delivery 4–14 business days, 14-day trial (REPORTED). AL `q=vedyashop.com`: about 98 results; oldest active 2026-02-18 (groups of 10, 7, 4 and 3 ads), including a toilet-brush creative. Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=vedyashop.com&search_type=keyword_unordered)
- **YUKA TECH**: smart sensor trash bins Y1 329 (compare-at 599, out of stock) and Y2 579 (compare-at 799), plus consumable refill bag-rings (6-pack 79.90/89.90). Shopify, 4 products since 2024-03-09. Delivery "2–5 business days", which means local stock; "1-year warranty" (REPORTED). AL `q=yuka-tech.co.il`: about 22 results, all in one group of 22 ads starting **2025-04-01**. Sources: [products.json](https://yuka-tech.co.il/products.json?limit=250), [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=yuka-tech.co.il&search_type=keyword_unordered)
- **Urban Home**: no-drill shelves and vacuum hooks (StickyHook 79.90, compare-at 133.90). Shopify since 2024-06-13, 136 products, registered country US. "30-day money-back" (REPORTED). AL `q=urbanhome.co.il`: about 44 results; oldest active **2025-05-26** (18 ads), plus a renter hook from 2025-11-17 ("renting? don't drill a hole in your deposit"). Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=urbanhome.co.il&search_type=keyword_unordered)
- **TORO**: grill-cleaning kits at 389 and GrillClean Pro 449 (compare-at 599), plus replacement heads 79.90 as the consumable. Shopify since 2026-03-10, 7 products. Widget counts 118 and "3,983" (REPORTED). Delivery 6–15 business days; "30-day trial with full refund" (REPORTED). AL `q=toro-israel.com`: about 29 results, all in one group starting 2026-11-06 (a new creative). Source: [products.json](https://toro-israel.com/products.json?limit=250)
- **HOMELY**: a generic gadget line (vegetable chopper 179.99, steam iron 219.99, stain remover 129.99). Shopify since 2026-06-12, 34 products, "7–14 business days". AL: 7 ads from 2026-08-24. Source: [products.json](https://homelyofficial.com/products.json?limit=250)
- **Izzy**: handheld steam cleaner, WooCommerce. AL: 5 ads from 2026-10-16. Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=izzy.co.il&search_type=keyword_unordered)

**Pests**
- **Bugo**: hero is a plug-in "chemical-free" pest repeller at 139 (compare-at 199), created 2026-02-26. It then built a line: outdoor solar repeller (2026-03-23), pet tags 149, indoor mosquito/fly trap at 149 / 269 / 379 / 459 for 1–4 units, refills 59.90–169 (consumable), ant gel, bird repeller 269, outdoor mosquito device 229–669, and a "full home protection" bundle at 499. Shopify, 20 products. The page offers "30-day money back" and claims "10,000" (REPORTED). AL `q=bugo.co.il`: about 710 results; oldest active **2026-03-18** (a group of 28 ads), about 8 months. Sources: [products.json](https://bugo.co.il/products.json?limit=250), [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=bugo.co.il&search_type=keyword_unordered). Note: whether ultrasonic repellers actually work is UNVERIFIED, and claims like this carry consumer-protection risk.

**Sleep and snoring**
- **AudioFeel**: noise-filter earplugs at 179 / 2 pairs 288 / 3 pairs 399, cleaning kit 34.99 as the add-on, and "LIVE + ZEN" combos at 308. Shopify since 2024-11-28, 17 products, "30-day trial" (REPORTED). AL `q=audiofeel.co.il`: about 150 results; oldest active **2025-12-08** (a group of 30 ads), plus a 2026-03-30 group of 13. Persona/partner pages include a "psychodramatist" practitioner page. Sources: [products.json](https://audiofeel.co.il/products.json?limit=250), [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=audiofeel.co.il&search_type=keyword_unordered)
- **Quick Relief**: a 2024 pain and massage store (157 products since 2024-01-27). Its current ads push a snoring night splint at 139 (compare-at 200) with a "30 nights trial", and an ergonomic memory-foam pillow. AL `q=quickreliefil.com`: about 27 results, one group of 27 ads from 2026-05-13. Delivery 5–12 business days. Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=quickreliefil.com&search_type=keyword_unordered)
- **SnoreAway** (snoreaway.store and breezeil.store, same Shopify shop `dy5m68-ua`): universal anti-snoring mouthpiece at 189.90 (compare-at 289.90), with upsells: cleaning spray 69.90, brush 49.90, and "1-year insurance & warranty" 19.90. 6 products since 2026-04-25. AL: ads from 2026-08-14 run under person names and a "ד״ר שלמה וייס" doctor persona. Sources: [products.json](https://snoreaway.store/products.json?limit=250), [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A0%D7%97%D7%99%D7%A8%D7%95%D7%AA&search_type=keyword_unordered)
- **AirStrips**: magnetic nasal strips at 64.90, free shipping over 150. 4 products since 2025-10-27. AL: 2 ads from 2026-08-23. Source: [products.json](https://airstrips.co.il/products.json?limit=250)
- **Bandzzz**: 3D sleep mask 119/139/189, a pair for 239, and sleep add-ons (white-noise machine 199.90, knee pillow 149.90). 14 products since 2026-09-17. AL: 7 ads from 2026-11-13. Source: [products.json](https://bandzzz.co.il/products.json?limit=250)
- **Holyzzz**: Bluetooth sleep mask 149.90 and a flight sleep kit 199.90. 2 products since 2026-10-25; 3 ads from 2026-11-11. Source: [products.json](https://holyzzz.com/products.json?limit=250)
- **Soleva**: pillow mist (a room/pillow spray, not a body cream) plus heated joint wraps 179–249 and pillows. 25 products since 2026-06-18; 7 ads from 2026-11-12. Source: [products.json](https://solevasleep.com/products.json?limit=250)

**Pain, posture and orthopedic**
- **Aloeteva**: herbal knee and back patches. Shopify `knee-champ.myshopify.com` since 2021-01-29, 59 products, registered country US. AL `q=aloeteva.com`: about 200 results; oldest active **2025-10-05**; many testimonial personas ("מגזין בריאות", "משהו טבעי שעושה לי בריא", named individuals). Claims include "immediate relief without surgery". Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=aloeteva.com&search_type=keyword_unordered)
- **Jepeta (ג'פטה)**: home device for back pain and sciatica, plus a blood-pressure monitor. Shopify since 2024-02-24, 59 products, "30-day trial" (REPORTED). AL `q=jepeta.com`: about 89 results; oldest active **2025-09-09** (7 ads), with "עולם הבריאות" persona pages. Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=jepeta.com&search_type=keyword_unordered)
- **Ortofix**: orthopedic cloud sandals 179 (compare-at 358), sneakers 269, knee sleeve 149. Shopify since 2024-01-19, 18 products. Widget shows 87 reviews and a "10,000" claim (REPORTED); delivery 5–15 days. AL (`q=כאב גב תחתון`): groups of 4, 3 and 2 ads from 2026-09-05, under pages such as "דף האורתופדיה של ישראל". Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9B%D7%90%D7%91%20%D7%92%D7%91%20%D7%AA%D7%97%D7%AA%D7%95%D7%9F&search_type=keyword_unordered)
- **Selera**: seat cushion 199.90, lumbar pillow 249.90, gel travel cushion 199.90. 7 products since 2026-05-19. AL: "senior flight attendant" persona ads from 2026-09-29. Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9B%D7%A8%D7%99%D7%AA%20%D7%A6%D7%95%D7%95%D7%90%D7%A8%20%D7%9C%D7%98%D7%99%D7%A1%D7%94&search_type=keyword_unordered)
- **Mova Glow**: a generic store (27 products since 2026-10-22, registered AE, currency AED). Posture corrector "2 for 199 + free shipping". 2 ads from 2026-11-05. Source: [products.json](https://movaglow.com/products.json?limit=250)

**Pets**
- **WOOF**: dog dental powder at 189 / 2 for 279 / 3 for 399, created 2026-08-03, then probiotic, joint, salmon-oil and calming SKUs. 5 products; meta country TH. "90-day guarantee & refund" (REPORTED); widget 29 reviews. AL `q=mywoof-il.com`: about 98 results; oldest active 2026-09-02 (26 ads), plus pet-influencer whitelisting. Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=mywoof-il.com&search_type=keyword_unordered)
- **Pups**: the same concept (dental powder 199, allergy chews 199, dental+allergy bundle 249). 7 products since 2026-05-07. Ads from 2026-10-22. Source: [products.json](https://trypups.com/products.json?limit=250)

**Beauty tools, kids, eyes, supplements**
- **Novela**: hero is a kids' anti-nail-biting product; it also sells gel-nail stickers at 1+1 for 149.90 / 2+2 for 199.90 and beauty tools at 49.90–179.90. Shopify since 2025-06-13, 17 products. Widgets show 508 and 1,491 (REPORTED); delivery 5–14 days. AL `q=novela.co.il`: about 320 results; oldest active **2026-06-02** (28 ads); personas "ישראליות בודקות וממליצות" and "ילדים בלי כסיסה". Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=novela.co.il&search_type=keyword_unordered)
- **LAOR**: hair eraser at 149 / 2 for 229 / 3 for 279. Shopify since 2022-06-10, 10 products. Widget 245 (REPORTED); 5–14 days. AL: only one 2025-06-22 ad was seen (in `q=מקלחת`); the domain query was empty (UNVERIFIED). Source: [products.json](https://laorskin.com/products.json?limit=250)
- **Mistly**: warm-mist dry-eye device at 219 kit / 249 (compare-at 372), plus 89-ILS e-books and a "Hear+" red-light device for tinnitus at 299. 9 products since 2026-05-26; meta country AE. Widget 662 (REPORTED); "30-day trial" (REPORTED). AL `q=mistlycare.com`: about 230 results, oldest active only 2026-10-21; personas include "שקט באוזניים – קהילת טינטון ישראל". Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=mistlycare.com&search_type=keyword_unordered)
- **Mayven**: hair gummies (a supplement) at 2 for 269 / 3 for 319 / 4 for 379. Shopify since 2022-06-29, 148 products. Widget 1,421 (REPORTED). AL `q=mayven.co.il`: about 330 results; oldest active 2026-10-08 (22 ads), with heavy creator whitelisting ("Mayven עם Aline"). Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=mayven.co.il&search_type=keyword_unordered)
- **Head to Toe**: natural oil formulas for kids (runny nose, cough, mosquito bites) at 65.60–147.60. Shopify since 2023-11-30, 25 products. Delivery "1–4 business days", which means local stock. AL `q=headtotoe.co.il`: about 28 results; oldest active **2025-12-07** (24 ads). Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=headtotoe.co.il&search_type=keyword_unordered)
- **Sahara Oodie**: wearable blanket-hoodie, 139 adult / 99 kids (compare-at 249). Shopify since 2025-01-09. Delivery 1–5 days (local). A "40,000" claim (REPORTED). AL (`q=הלהיט`): a 2024-10-21 ad (from the predecessor saharashop.co.il) and a 2026-10-12 ad, so it is a seasonal winter hero now in at least its 2nd–3rd season. Source: [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%94%D7%9C%D7%94%D7%99%D7%98&search_type=keyword_unordered)

**Generalists posing as brands (context, not heroes)**
- `israelwind.com` (meta country HK), `ecouaer.com` (HK) and `ybaou.com` (CN) each hit the 250-product cap and run Hebrew single-product ads (phone holders, organizers, travel pillows). They are foreign-run catalogue dropshippers. Sources: [israelwind](https://israelwind.com/meta.json), [ecouaer](https://ecouaer.com/meta.json), [ybaou](https://ybaou.com/meta.json)

### Inferences
- ESTIMATE: Store age misleads in two ways. A recent `created_at` can hide an older business (BAGLY 2022, Quick Relief 2024 and Urban Home 2024 all reused older stores for new heroes), and an old feed can hide a brand-new hero. The best age signal is **the hero product's own created_at plus the oldest active ad that points to it**.
- ESTIMATE: Several "Israeli" stores have a meta.json country of AE, US, TH, HK or CN (Mistly, Mova Glow, WOOF, Aloeteva, Urban Home, Rosina). Foreign operators or foreign entities are running Hebrew hero stores; the Israeli market is being worked from outside.

### Gaps
- No sales, revenue or conversion data exists for any brand; only activity signals.
- For about a third of domain queries the Ad Library loaded no results (for example kitflow.co.il, movaglow.com, holyzzz.com, flyhugz.com, laorskin.com, try-freshora.com, ortofix.co.il, sahara-oodie.co.il, selera.co.il). Their ad longevity is UNVERIFIED.
- TikTok ad activity was not checked (no accessible public source).

---

## Q2. Which brands show the strongest evidence of sustained profitability?

### Takeaway
Fourteen brands have currently-active ads that started at least about 4 months ago and are paired with product additions or a multi-year store. In order of longevity: YUKA (since 2025-04-01), Urban Home (2025-05-26), Jepeta (2025-09-09), Aloeteva (2025-10-05), Head to Toe (2025-12-07), AudioFeel (2025-12-08), Vedya (2026-02-18), Bugo (2026-03-18), BAGLY (2026-04-16), Quick Relief (2026-05-13), Novela (2026-06-02), Relivia (2026-06-20), SilQ (2026-07-13, store since 2024) and Fizz (2026-08-04). Bugo, Relivia, Fizz, Novela and BAGLY combine longevity with very high current ad volume (about 290–960 active ads) and monthly product additions. That combination is the strongest public signal of a working funnel.

### Cited Findings (evidence grades)
Grading: **A** = an active ad running ≥6 months, or ≥3 months plus a high ad count (≥200 results) plus product additions; **B** = 2–6 months, or a multi-year store with modest ads; **C** = under 2 months or too little data. All observed 2026-11-14; sources as in Q1.

| Brand | Hero & price (ILS) | Bundles | Oldest active ad (lower bound) | Active ads (≈results) | Store / hero age | Delivery | Grade |
|---|---|---|---|---|---|---|---|
| YUKA TECH | smart bin 329 / 579 | refill rings 6-pack 79.90–89.90 | 2025-04-01 (~19 mo) | ~22 | store 2024-03 | 2–5 days (local) | A |
| Urban Home | no-drill shelves/hooks ~80 | multi-buy | 2025-05-26 (~18 mo) | ~44 | 2024-06 | n/a | A |
| Jepeta | back/sciatica device | n/a | 2025-09-09 (~14 mo) | ~89 | 2024-02 | 7–14 days | A (health-claim risk) |
| Aloeteva | knee/back patches | n/a | 2025-10-05 (~13 mo) | ~200 | 2021-01 | n/a | A (health-claim risk) |
| Head to Toe | kids' natural oils 66–148 | n/a | 2025-12-07 (~11 mo) | ~28 | 2023-11 | 1–4 days (local) | A- |
| AudioFeel | earplugs 179 | 2 for 288, 3 for 399 | 2025-12-08 (~11 mo) | ~150 | 2024-11 | n/a | A |
| Vedya | shower head 179.90 | n/a | 2026-02-18 (~9 mo) | ~98 | 2024-10 | 4–14 days | A- |
| Bugo | plug-in repeller 139 | trap 1/2/3/4 = 149/269/379/459; home pack 499; refills | 2026-03-18 (~8 mo) | ~710 | hero 2026-02-26 | n/a | A |
| BAGLY | flight bag 389.90 | add-ons 49.90–89.90 | 2026-04-16 (~7 mo) | ~290 | store 2022, hero 2026-01 | 3–14 days | A |
| Quick Relief | snoring splint 139 / pillow | n/a | 2026-05-13 (~6 mo) | ~27 | store 2024-01 | 5–12 days | B+ |
| Novela | anti-nail-biting (kids); nail stickers | 1+1 149.90, 2+2 199.90 | 2026-06-02 (~5.5 mo) | ~320 | 2025-06 | 5–14 days | A |
| Relivia | washer tablets 139.90 | 2 for 199.90, 3+1 for 299.90 | 2026-06-20 (~5 mo) | ~470 | 2026-05-31 | 7–16 days | A |
| SilQ | filter shower head 379–395 | cartridge 129 | 2026-07-13 (~4 mo) | ~16 | 2024-02 | n/a | A- |
| Fizz | litter-box odor plug-in 139 | 3/5/7 = 271/382/477 | 2026-08-04 (~3.3 mo) | ~960 | 2026-06-30 | 5–10 days | A- |
| WOOF | dog dental powder 189 | 2 for 279, 3 for 399 | 2026-09-02 (~2.5 mo) | ~98 | 2026-08 | n/a | B+ |
| SnoreAway | anti-snore device 189.90 | spray, brush, insurance upsells | 2026-08-14 (~3 mo) | n/a | 2026-04 | n/a | B |
| Ortofix | ortho sandals 179 | n/a | 2026-09-05 | n/a | 2024-01 | 5–15 days | B+ |
| Mayven | hair gummies | 2/3/4 = 269/319/379 | 2026-10-08 | ~330 | 2022-06 | n/a | B+ (supplement) |
| Sahara Oodie | hoodie blanket 139 | n/a | seasonal: 2024-10 & 2026-10 | n/a | 2025-01 | 1–5 days (local) | A- (seasonal) |
| KitFlow | flight bag 369 | kits 559 | 2026-07-12 | ≥5 | 2026-05 | n/a | B- |
| Freshora | fridge odor absorber 179 | n/a | 2026-10-13 | n/a | 2026-05 | 10–20 days | B |
| Mistly | dry-eye device 219–249 | e-book upsell | 2026-10-21 | ~230 | 2026-05 | 6–12 days | B |
| TORO | grill kit 389–449 | replacement heads | 2026-11-06 (new creative) | ~29 | 2026-03 | 6–15 days | B- |
| ZuZu, LAOR, HOMELY, Selera, Pups | (see Q1) | | 2025-06 to 2026-10 | low | | | B-/B |
| Protego, Holyzzz, Bandzzz, Rosina, FlyHugz (IL), AirStrips, Mova Glow, Soleva, Izzy | (see Q1) | | Oct–Nov 2026 | low | | | C |

### Inferences
- ESTIMATE: The repeat-winner mechanic is **"hero, then a monthly sibling SKU aimed at the same customer"**. Relivia went washer tablets, dishwasher tablets, scent beads, mold gel, toilet kit in under 3 months. Bugo went repeller, outdoor, pet, mosquito trap, refills, birds, home bundle. WOOF went dental, probiotic, joints, calming. A store keeps adding SKUs only when the hero's buyers come back, so this is the second-strongest signal after ad longevity.
- ESTIMATE: The longest-running advertisers (YUKA, Urban Home, Head to Toe) run **fewer ads but longer**, and two of them ship locally (2–5 and 1–4 days). The high-volume newcomers (Fizz, Bugo, Relivia) run hundreds of creatives and ship from abroad. Both models appear to work; the local-stock ones show the longest single-creative lifetimes.
- ESTIMATE: Health and pain advertisers (Aloeteva, Jepeta, Mistly, SnoreAway, Ortofix, Selera) are among the longest-running, but they lean on fake-looking "magazine" or "doctor" persona pages. That exposes them to Meta ad-policy enforcement and Israeli consumer-protection risk. It is a pattern to avoid copying, even though it appears to sell.

### Gaps
- Oldest-ad dates are lower bounds; a brand's true first ad may be much older, and paused ads vanish from the library.
- Review counts are widget figures or marketing claims ("10,000 / 25,000 / 70,000 customers") and could not be dated. Review-date distributions were not extracted (no time left within the budget), so "rising reviews" could not be tested.

---

## Q3. What patterns do the winners share (price, bundles, pain, demo-ability, consumables, guarantees)?

### Takeaway
The winners are a **139–189 ILS hero sold mainly in a 2-pack or 3(+1)-pack that lands at 199–399**. They have low-weight, low-cost items with high perceived value (tablets, powders, plug-ins, earplugs, bags); a **hidden or gross, recurring household or sleep pain** shown in a 5-second demo; a **30-day (sometimes 90-day) money-back promise**; and a **consumable or sibling SKU** for repeat orders. Flight bags are the exception: a single 349–449 ILS item whose hook is "saves you a 200–400 ILS baggage fee every flight".

### Cited Findings
- **Price ladders (FACT, store feeds 2026-11-14):**
  - Relivia 139.90 / 199.90 / 299.90 (3+1)
  - Fizz 139 / 271 (3) / 382 (5) / 477 (7)
  - WOOF 189 / 279 / 399
  - AudioFeel 179 / 288 / 399
  - LAOR 149 / 229 / 279
  - Novela 1+1 149.90 / 2+2 199.90
  - Mayven 269 / 319 / 379
  - Bugo trap 149 / 269 / 379 / 459
  - Rosina 119 / 199 / 249
  - Mova Glow 129 / 2 for 199
  - In every ladder the 2-unit tier crosses about 199 ILS, which matches the ≥199 ILS threshold in note 10.
- **Single high-ticket heroes (FACT):** BAGLY 389.90; KitFlow 369; Protego 349; SilQ 379–395; YUKA 329/579; TORO 389–449; Mistly 219–249.
- **Compare-at anchors (FACT):** compare-at prices typically sit 1.3–2× the selling price; Protego and WOOF use exactly 2× ("50% off").
- **Guarantees (REPORTED, product pages):** 30-day money-back at Bugo, Urban Home, TORO, Mistly, AudioFeel (30-day trial), Jepeta and Aloeteva (30-day trial); 90 days at WOOF; "30 nights" at Quick Relief; 14 days at BAGLY and Vedya.
- **Consumables and upsells (FACT):** SilQ cartridge 129; YUKA refill rings 79.90–89.90; Bugo refills 59.90–169; TORO replacement heads 79.90; AudioFeel cleaning kit 34.99; SnoreAway cleaning spray 69.90 plus a 19.90 "insurance" add-on; BAGLY liquid kit 49.90 and pillow 89.90; KitFlow and Protego free-gift products priced at 0 against a shown compare-at.
- **Pain types and hooks (FACT, ad text in Ad Library):**
  - Hidden dirt or germs: Relivia "your washing machine may hide bacteria and mold"; Fizz "you washed twice and it still smells"; Freshora fridge smell; SilQ water.
  - Money wasted: BAGLY "hundreds of shekels just for a suitcase"; KitFlow "paying hundreds of shekels for a trolley every flight?".
  - Sleep: snoring, light, noise.
  - Pests: Bugo "no spray, no stress, just plug it in".
  - Kids' habits: Novela nail-biting; Head to Toe "the kids won't stop getting bitten".
  - Pets: WOOF "if you couldn't brush his teeth, it's not your fault".
- **Ad-format patterns (FACT):** persona or "magazine" pages that link to the store (Relivia, Fizz, Aloeteva, Jepeta, Mistly, SnoreAway, Selera, Freshora, Ortofix, BAGLY); creator whitelisting shown as "<creator> עם <brand>" (Mayven, SilQ, WOOF, Novela); scarcity (BAGLY "the stock has almost run out"); influencer coupons (BAGLY "adva199").
- **Delivery (REPORTED, product pages):** most heroes promise 5–16 business days, meaning they ship from abroad. Exceptions with local stock: YUKA 2–5, Head to Toe 1–4, Sahara Oodie 1–5.

### Inferences
- ESTIMATE: Demo-ability clusters into three formats: (a) before/after dirt (tablets, steam, grill kits); (b) plug-in-and-forget (Bugo, Fizz); (c) a fit or comparison demo (the bag under the seat versus a trolley fee). All three film in 5–15 seconds on a phone. That is the common thread with BAGLY.
- ESTIMATE: Bundle ladders work because unit cost is tiny relative to price. Tablets, powders, plug-in odor units and earplugs probably cost ₪5–30 landed (UNVERIFIED for each brand), so a 3+1 still leaves room for a ~86 ILS CPA. Products whose AliExpress cost is ₪100+ cannot use this mechanic (see Q4).
- ESTIMATE: "Recurring pain" in the winners mostly means **a pain that returns on a schedule** (monthly machine cleaning, every flight, every night of snoring, every summer's mosquitoes). That makes a consumable refill or a seasonal re-buy natural.

### Gaps
- Return rates, real COGS and CPA for these brands are unknown.
- I could not test whether 3+1 outperforms 1+1 in Israel; no public data.

---

## Q4. Product ideas that fit the winning patterns and are not yet served by an Israeli hero brand

### Takeaway
Of 15 ideas checked in the Ad Library and AliExpress, only three clearly or nearly clear the unit-economics bar: a **kettle/coffee-machine descaler tablet line** (the Relivia mechanic applied to Israeli hard water), a **bedwetting alarm for children**, and a **mosquito-bite heat-pen family pack**. Three are borderline (shelter emergency kit, cordless water flosser, magnetic mosquito door screen). Most gadget ideas fail because their AliExpress cost of ₪100–420 is already 40–65% of a plausible Israeli price. The lesson from the winners holds: **low unit cost, high perceived value, a bundle ladder**.

### Method used for the economics (ESTIMATE)
- Contribution ≈ P/1.18 (VAT) − landed − ~3% payment fee − CPA, with the median CPA of 86 ILS from note 10.
- Landed = AliExpress price + ~25–45 ILS freight per small parcel (note 10's freight band for 100–300 g parcels was 27–38 ILS; heavier items are higher).
- Pass rule from note 10: price ≥ ~199, landed ≤ 25–30% of price, CPA ≤ ~20% of price.

### Cited Findings (FACT = observed 2026-11-14 in AL / AliExpress search; economics = ESTIMATE)

1. **Descaler tablets for kettles and coffee machines, as a 1/2/3+1 consumable line.**
   - Pain and moment: limescale flakes in the kettle and a coffee machine that slows or tastes bitter; noticed every morning.
   - Customer: every household.
   - Ad Library: `q=אבנית בקומקום` showed only water-filter installers (מי מזור, KSDD); `q=מסיר אבנית למכונת קפה` returned empty (UNVERIFIED). No hero seen. [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%90%D7%91%D7%A0%D7%99%D7%AA%20%D7%91%D7%A7%D7%95%D7%9E%D7%A7%D7%95%D7%9D&search_type=keyword_unordered)
   - AliExpress: espresso cleaning/descaling tablets ₪7.8–9.4 per pack, 1K–2K+ sold. [Ali](https://www.aliexpress.com/w/wholesale-descaling-tablets-coffee-machine-kettle.html?SortType=total_tranpro_desc)
   - Price idea: 119.90 / 2 for 169.90 / 3+1 for 229.90.
   - Economics: landed for 4 packs ≈ 4×9 + 30 = ~66, which is ~29% of 229.90; contribution at CPA 86 ≈ 195 − 66 − 7 − 86 = ~36 ILS. **Passes at the 3+1 tier**; fails at a single pack.
   - Risks: Israeli import and labelling rules for cleaning chemicals are UNVERIFIED; this is a commodity in supermarkets, so the brand and demo must carry it.
2. **Bedwetting (enuresis) alarm with a Hebrew parent program and a 30-night guarantee.**
   - Pain and moment: the 3 a.m. sheet change and a child's shame; school sleepovers.
   - Customer: parents of children aged 5–10.
   - Ad Library: `q=הרטבת לילה` returned empty (UNVERIFIED). No hero seen in the travel, sleep or kids queries.
   - AliExpress: alarms with sound, light and vibration ₪42.8–47.6, 281–676 sold. [Ali](https://www.aliexpress.com/w/wholesale-bedwetting-alarm.html?SortType=total_tranpro_desc)
   - Price idea: 249, plus a sensor-pad refill or 2-pack for 79.
   - Economics: landed ≈ 48 + 25 = ~73 (~29%); contribution ≈ 211 − 73 − 7 − 86 = ~45 ILS. **Passes.**
   - Risks: it borders on a medical-device claim; check classification (UNVERIFIED). A single purchase per child limits repeat orders.
3. **Mosquito-bite heat pen, sold as a family pack.**
   - Pain and moment: kids' itchy bites at night, April–October.
   - Ad Library: `q=עקיצות יתושים` showed only Head to Toe oils, a todoshop persona and Moraz repellent. No heat-pen brand. [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A2%D7%A7%D7%99%D7%A6%D7%95%D7%AA%20%D7%99%D7%AA%D7%95%D7%A9%D7%99%D7%9D&search_type=keyword_unordered)
   - AliExpress: realistic ₪11–29 per pen (₪2–3 listings are welcome deals or low quality); 1K–2K+ sold. [Ali](https://www.aliexpress.com/w/wholesale-mosquito-bite-relief-heat-pen.html?SortType=total_tranpro_desc)
   - Price idea: 1 for 119, 2 for 179, 3 for 229 (one per bag, car and bedroom).
   - Economics: 3-pack landed at ₪11 per unit ≈ 33 + 35 = ~68 (~30%), which passes; at ₪25 per unit ≈ 110 (~48%), which fails. **Borderline: it depends on the unit cost.** It is seasonal, and it pairs well as an upsell for a mosquito hero.
4. **Shelter (mamad) emergency kit: crank/solar radio with power bank, lantern and essentials.**
   - Pain and moment: a power cut or alert at night; Israel-specific, episodic demand.
   - Ad Library: `q=ערכת חירום` showed only tactical/medical gear, car kits and Jacobi. No consumer hero. [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A2%D7%A8%D7%9B%D7%AA%20%D7%97%D7%99%D7%A8%D7%95%D7%9D&search_type=keyword_unordered)
   - AliExpress: crank radio and power banks ₪29–73 (10K+ sold for the ₪62 model); 10,000 mAh versions ₪137. [Ali](https://www.aliexpress.com/w/wholesale-emergency-hand-crank-radio-power-bank.html?SortType=total_tranpro_desc)
   - Price idea: 279.
   - Economics: landed ≈ ₪90–130 (32–47%). **Borderline.** Demand spikes with security events, and fear-based ads raise ethical and policy risk.
5. **Cordless water flosser.**
   - Ad Library: `q=שיניים מים` returned empty (UNVERIFIED); big retail brands are sold at chains.
   - AliExpress: ₪53 (D52) to ₪115 (MIJIA), 10K+ sold. [Ali](https://www.aliexpress.com/w/wholesale-cordless-water-flosser.html?SortType=total_tranpro_desc)
   - Price idea: 249, plus a 4-pack of tips for 59 as the consumable.
   - Economics: landed ≈ 83 (~33%). **Borderline**, with heavy retail competition.
6. **Magnetic mosquito screen door (balcony or kitchen).**
   - Ad Library: Reshet-IL (reshet-il.co.il) has run "רשת הפלא" window-net ads since 2025-07-21, so the niche is **partly served**. [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A8%D7%A9%D7%AA%20%D7%A0%D7%92%D7%93%20%D7%99%D7%AA%D7%95%D7%A9%D7%99%D7%9D&search_type=keyword_unordered)
   - AliExpress: ₪9.5–89 per piece. [Ali](https://www.aliexpress.com/w/wholesale-magnetic-screen-door.html?SortType=total_tranpro_desc)
   - Price idea: 2 for 229.
   - Economics: landed ≈ ₪88–116 (38–50%). **Borderline to fail**; door sizes also drive returns.
7. **Window-cleaning robot.**
   - Ad Library: only retailers (Payngo, Petcom with Ecovacs Winbot, electro-gal). No DTC hero.
   - AliExpress: ₪179–331, 2K–5K+ sold. [Ali](https://www.aliexpress.com/w/wholesale-window-cleaning-robot.html?SortType=total_tranpro_desc)
   - Price idea: 599–699.
   - Economics: landed ≈ ₪240–390 (40–55%). **Fails.** Warranty and return risk is high.
8. **Ventilated car-seat cooling cushion (summer heat).**
   - Ad Library: `q=מושב מאוורר` showed only office chairs. No hero.
   - AliExpress: ₪57–318 (the popular 8-fan model is ₪105). [Ali](https://www.aliexpress.com/w/wholesale-car-seat-cooling-cushion-fan.html?SortType=total_tranpro_desc)
   - Price idea: 249.
   - Economics: landed ≈ ₪100–150 (40–60%), bulky and seasonal. **Fails.**
9. **Electric heated lunch box (reservists, drivers, workers without a microwave).**
   - Ad Library: `q=קופסת אוכל מחממת` and `q=אוכל חם בעבודה` returned empty (UNVERIFIED).
   - AliExpress: ₪68–161 for real units (1.5 L 60 W ≈ ₪110). [Ali](https://www.aliexpress.com/w/wholesale-electric-heated-lunch-box.html?SortType=total_tranpro_desc)
   - Price idea: 229.
   - Economics: landed ≈ ₪110–150 (48–65%). **Fails.**
10. **Ultrasonic cleaner for glasses and jewelry.**
    - Ad Library: `q=מנקה אולטרסוני` returned empty (UNVERIFIED).
    - AliExpress: real 40 kHz units ₪96–138. [Ali](https://www.aliexpress.com/w/wholesale-ultrasonic-cleaner-glasses-jewelry.html?SortType=total_tranpro_desc)
    - Price idea: 249.
    - Economics: landed ≈ ₪130–170 (~55–65%). **Fails.**
11. **Bladeless neck fan.**
    - Ad Library: `q=מאוורר צוואר` and `q=מאוורר תלייה` returned empty (UNVERIFIED); retail chains sell them.
    - AliExpress: ₪18–47. [Ali](https://www.aliexpress.com/w/wholesale-bladeless-neck-fan.html?SortType=total_tranpro_desc)
    - Price idea: 2 for 199.
    - Economics: landed ≈ ₪75–140 (38–70%). **Fails**, and it is seasonal and commoditised.
12. **Closet / mamad mold and humidity solution.**
    - Ad Library: `q=סופג לחות` and `q=עובש בארון` showed only Jacobi, Freshora and Israelwind vacuum bags. No hero.
    - AliExpress: electric mini dehumidifiers ₪77–160; hanging desiccant bags ~₪2.9 per piece in 10-packs (heavy); silica beads 500 g ₪32. [Ali](https://www.aliexpress.com/w/wholesale-mini-dehumidifier.html?SortType=total_tranpro_desc), [Ali bags](https://www.aliexpress.com/w/wholesale-hanging-moisture-absorber-bag-closet.html?SortType=total_tranpro_desc)
    - Economics: the electric version lands ~₪110–200 against a 199–249 price; the bags are heavy, so freight dominates. **Fails** unless sourced locally in Israel.
13. **Upholstery and mattress spot cleaner.**
    - AliExpress: ₪422–1,352. [Ali](https://www.aliexpress.com/w/wholesale-upholstery-spot-cleaner-machine.html?SortType=total_tranpro_desc)
    - **Fails** (landed above 60% of a 799 price).
14. **UV dust-mite mattress vacuum.**
    - Ad Library: one 2026-06-28 ad from easylifeil.com, so semi-served.
    - AliExpress: ₪102 for a handheld 10 kPa unit; MIJIA ₪388. [Ali](https://www.aliexpress.com/w/wholesale-dust-mite-vacuum-UV-mattress.html?SortType=total_tranpro_desc)
    - Price idea: 349–399.
    - Economics: landed ≈ ₪147 (37–42%). **Fails or borderline.**
15. **Electric lint remover.**
    - AliExpress: ₪4.5–32. [Ali](https://www.aliexpress.com/w/wholesale-electric-lint-remover.html?SortType=total_tranpro_desc)
    - A 79–99 ILS shelf price is too low for paid social. **Fails** except as a 3-pack gift or an add-on.

### Inferences
- ESTIMATE: The ideas that pass share the winners' DNA: a cheap-to-make consumable or small device, a recurring or nightly pain, a demo or story that films easily, and a 2/3+1 ladder that crosses 199–229 ILS. Bulky or premium gadgets (robots, cushions, cleaners) fail the 25–30% landed rule at AliExpress retail prices, and would only work with factory pricing (UNVERIFIED) or local stock bought in volume.
- ESTIMATE: The partners' best path is probably **a Relivia/Fizz-style consumable line in an unclaimed niche** (descaling is the clearest gap found) or **a nightly-pain kids or sleep product with a guarantee** (the bedwetting alarm), rather than another flight bag. Flight bags now have at least four Hebrew advertisers (BAGLY, KitFlow, Protego, Rosina-type pillows), and travel sleep has at least five (Holyzzz, Bandzzz, FlyHugz, Selera, Rosina).

### Gaps
- Empty Ad Library results for idea terms (bedwetting, water flosser, neck fan, lunch box, ultrasonic, magnetic net, coffee descaler) could be load failures. Before committing, re-check each one manually, also with English and brand-like spellings.
- AliExpress prices are retail search-page prices on 2026-11-14 and exclude Israel-specific shipping; real landed cost from a 1688 or agent quote is unknown.
- Regulatory status (medical-device classification for the enuresis alarm; chemical labelling for descaler tablets; Ministry of Communications approval for radio/Bluetooth items) is UNVERIFIED.
- No search-demand data (Google Trends was blocked per note 02) to size any idea.
