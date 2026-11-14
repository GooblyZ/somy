# "Universal everyday pain" products for Israel (excluding travel and flying), researched 2026-11-14

Labels: **FACT** means I saw it directly today on the page or tool output linked. **REPORTED** means a secondary source (press or an aggregator) said it. **ESTIMATE** means my own model or assumption. **UNVERIFIED** means plausible but not confirmed.
Scope: travel and flying products are excluded because another agent covers them. Products already rejected in earlier rounds (shower filters, pet-hair rollers alone, lash and nail kits, name necklaces, book nooks, Shabbat lamps, soldier gifts, scented and pheromone creams) were not re-researched.

**Methods and access (read this first):**
- **Meta Ad Library**: worked through headless Chromium, with a new browser context for each query. The URL pattern was `https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=<term>&search_type=keyword_unordered`. The page shows a count such as "~N תוצאות" plus advertiser names and "התחילה לפעול ב-" dates.
  - **Caveat 1**: many queries rendered a page with no count. That page was byte-identical (604 characters) to the page for the nonsense control term "zzqxqzz". I therefore read "no count" as **"0 active ads, or the page did not render"**.
  - **Caveat 2**: one term ("מגן שמש לרכב") showed 4 results in the first run and no count in two later runs. Single-term zeros are therefore **UNVERIFIED**.
  - **Caveat 3**: counts are fuzzy keyword matches. For example "אבנית" (limescale) returns 730 ads, mostly water-treatment services and clinics, so a count is not a product-competitor count. I list advertiser names where they matter.
- **AliExpress**: headless Chromium, with the cookie set to the IL region and ILS currency, `shipCountry=IL`, sorted by orders. Search URL pattern: `https://www.aliexpress.com/w/wholesale-<term>.html?shipCountry=IL`. No captcha appeared.
  - **Caveat**: the result lists mix in "new shopper" welcome-deal prices of ₪1.3–₪3.59. These are **not** real unit costs. I quote the mid-list prices of products with a real title and, where shown, a sold count.
- **Zap.co.il**: plain curl was blocked (244-byte response), but headless Chromium worked. Pattern: `https://www.zap.co.il/search.aspx?keyword=<term>`. Prices are Israeli retail and marketplace listing prices.
- **Shopify products.json**: worked on bagly.co.il. **WooCommerce Store API**: worked on namelabels.co.il.
- **Not used / blocked**: Google Trends, KSP, Super-Pharm, gov.il (blocked in the earlier round, so not retried). WebSearch is US-indexed, so Hebrew press coverage is thin.
- Shipping costs come from the previous round's FACT table (KakoBuy EUB line to Israel, queried 2026-11-11): about $8.55 / $11.98 / $15.41 / $23.98 for 100 g / 300 g / 500 g / 1 kg, which fits $6.84 + $17.15 per kg. See `../מחקר מוצרים לאיקומרס בישראל/10_unit_economics_verification.md`. Bulk air freight is REPORTED at about $5.3/kg (DTFU, cited in the same file).

---

## Q1. Life-situation pain map: who has the pain, how big the segment is, current solutions and prices in Israel, AliExpress cost, Hebrew DTC advertisers

### Takeaway
The strongest Israeli-specific recurring pains with a light, demo-able fix are:
- dirty windows and shutters in apartment buildings (dust and khamsin);
- mosquitoes at home, sharpened by the 2024 West Nile outbreak;
- summer heat in cars, strollers and in bed under the AC;
- parents' home safety, usually bought as a gift by adult children.

In several of these, Israeli shelf prices are 3–6× the AliExpress price and almost no Hebrew DTC brand advertises on Meta (magnetic window cleaner, AC deflector, car umbrella shade, stroller fan). The binding constraint is **shipping weight, not product cost**. At 0.5–1 kg, postal dropshipping pushes landed cost to 45–60% of a 199 ILS price, so nearly every idea only works with bulk air import and a price of 229–279 ILS.

### Cited Findings

**Population and segment base**
- REPORTED: about 182,000 births in 2025 ([INN](https://www.israelnationalnews.com/flashes/673467)). Another report gives 183,678 for 2025 against 181,614 in 2024 ([Algemeiner](https://www.algemeiner.com/?p=779321)).
- REPORTED: population was 10,178,000 at end-2025 ([Yeshiva World](https://www.theyeshivaworld.com/?p=2493233)).
- REPORTED: just over 3 million private households, averaging 3.17 people each ([JPost](https://www.jpost.com/israel-news/article-908103)).
- REPORTED: the vehicle fleet is about 4.2 million, of which about 3.67 million are private cars. The reference year is not stated ([Ynet](https://www.ynetnews.com/culture/article/bjxp11urkee)). The CBS "Motor Vehicles 2024" PDF exists but was not read ([CBS](https://www.cbs.gov.il/he/publications/DocLib/2025/1978/e_print.pdf)).
- REPORTED (Statista citing CBS, 2020): 94.3% of households own an air conditioner and 47.5% own a clothes dryer, so about half of households air-dry their laundry ([Statista AC](https://statista.com/statistics/1399539/share-of-households-in-israel-with-an-air-conditioner-by-sub-district), [Statista dryer](https://statista.com/statistics/1402213/share-of-households-in-israel-with-a-clothes-dryer-by-sub-district)). The CBS 2023 durable-goods release was not read ([CBS](https://www.cbs.gov.il/he/mediarelease/DocLib/2026/001/15_26_001b.pdf)).

**Heat**
- REPORTED: summer 2025 was well above average. The 8–14 Aug 2025 heatwave reached 45–49.7 °C in the valleys and set a record for the hottest night ([WMO summary](https://public.wmo.int/sites/default/files/2025-09/Heat%20Wave%20Summary%20Israel.pdf), [IMS 2025 review](https://ims.gov.il/sites/default/files/2026-02/Initial%20Review%20of%202025.pdf)).
- REPORTED: heat deaths of children left in parked cars recur. Five such deaths occurred in summer 2016 alone ([Forward](https://forward.com/news/breaking-news/345801/fifth-israeli-child-of-summer-dies-of-heat-in-parked-car/)).

**Mosquitoes**
- REPORTED: the 2024 West Nile outbreak was the largest in decades, with 710 cases and 46 deaths by late July 2024. The Health Ministry urged repellents and fans ([Lokmat/IANS](https://www.lokmattimes.com/international/israeli-west-nile-virus-cases-rise-to-710), [Ynet](https://www.ynetnews.com/health_science/article/sj003nn1ya)).

**Regulation of child-in-car alert devices**
- REPORTED: since 2021, Traffic Regulation 83D requires a child-presence alert for children under 4 in cars, with a 250 ILS fine. Devices need Transport Ministry approval ([JPost](https://m.jpost.com/israel-news/new-system-approved-to-prevent-forgetting-children-in-cars-674278)). Whether the rule is still in force in 2026 is UNVERIFIED.

**Pain table.** Ad Library counts, Zap prices and AliExpress prices are all FACT from tool output on 2026-11-14 unless marked.

| Situation / pain | Who and how many | Israeli retail (Zap etc.) | AliExpress (ILS, delivered to IL) | Hebrew Meta ads (active, IL) |
|---|---|---|---|---|
| Dirty outside of windows in apartments; you cannot reach the outer glass | Most of the ~3M households (apartment share UNVERIFIED) | Magnetic window cleaner ₪99–379. Tyroler models 2–10 mm ₪197, 2–18 mm ₪247, 2–28 mm ₪319, up to 42 mm ₪379; Glider D-3 ₪301–360 ([Zap](https://www.zap.co.il/search.aspx?keyword=מנקה%20חלונות%20כפול)) | ₪32–49 (5,000+ sold); premium about ₪83 ([Ali](https://www.aliexpress.com/w/wholesale-double-glazed-magnetic-window-cleaner.html?shipCountry=IL)) | "מנקה חלונות מגנטי": no count (≈0). "טירולר": ≈0. "מנקה חלונות": 51 (Karcher, Izzy, GadgetElectro, Olivier, cleaning services) |
| Shutter (תריס) and track dust | Same households | Shutter/track brushes ₪35–50; telescopic duster ₪69–80 ([Zap](https://www.zap.co.il/search.aspx?keyword=מברשת%20לניקוי%20תריסים)) | ₪2–4 (10,000+ sold) ([Ali](https://www.aliexpress.com/w/wholesale-blind-cleaner-brush.html?shipCountry=IL)) | "ניקוי תריסים": 13, all cleaning services plus Karcher |
| Mosquitoes through windows at night | Most households, May–Oct | DIY magnetic mosquito screen kits ₪151–229 per window (130×150); plain net ₪48–84; DIY aluminium roller screen ₪249–399 ([Zap](https://www.zap.co.il/search.aspx?keyword=רשת%20נגד%20יתושים%20לחלון)) | Magnetic door screen ₪73; window mesh price per piece unclear ([Ali](https://www.aliexpress.com/w/wholesale-magnetic-mosquito-net-window-diy.html?shipCountry=IL)) | "רשת מגנטית": 5 (Ecouaer Home, אטומקס, one individual). "יתושים" query failed. "מלכודת יתושים", "כילה", "רשת נגד יתושים": ≈0 |
| Mosquito UV lamps | Same | not checked | ₪57–117 ([Ali](https://www.aliexpress.com/w/wholesale-mosquito-trap-uv.html?shipCountry=IL)) | ≈0 |
| Cockroaches | Most households | not checked | bait-station search returned 0 products | "ג'וקים": 310, mostly pest-control (Bugo.il, Kim) |
| Sleeping under an AC draft (wall-split ACs are near-universal: 94% of households own an AC) | ~2.8M households (ESTIMATE from 94% of 3M) | AC wind deflector ₪96–205 ([Zap](https://www.zap.co.il/search.aspx?keyword=מסיט%20רוח%20למזגן)) | ₪17.5–52 ([Ali](https://www.aliexpress.com/w/wholesale-air-conditioner-wind-deflector.html?shipCountry=IL)) | "מסיט רוח למזגן" / "מסיט רוח": ≈0. "מגן מזגן": 3 (car services) |
| Sleeping hot | Everyone, Jun–Sep | "מזרן קירור" on Zap is mostly dog mats ₪90–250; human cooling pad 65×50 ₪148 ([Zap](https://www.zap.co.il/search.aspx?keyword=מזרן%20קירור)) | Cooling mattress pad ₪58–101; water-cooled pad ₪182 ([Ali](https://www.aliexpress.com/w/wholesale-cooling-mattress-pad.html?shipCountry=IL)) | "מזרן קירור": 8 (mattress makers: מזרני קיבוץ השלושה, European Comfort, Migvan Alaska). "שמיכה מקררת": ≈0 |
| Personal heat outdoors | Everyone, summer | Neck fan ₪65–239 ([Zap](https://www.zap.co.il/search.aspx?keyword=מאוורר%20צוואר)) | ₪17–47 ([Ali](https://www.aliexpress.com/w/wholesale-neck-fan-bladeless.html?shipCountry=IL)) | "מאוורר צוואר": ≈0. "מאוורר נטען": 5 (SKIL, SmartCase) |
| Parked car at 60 °C+, hot steering wheel and seats | ~3.67M private cars (REPORTED) | Umbrella windshield shade ₪125–179; classic foldable shade ₪22–89 ([Zap umbrella](https://www.zap.co.il/search.aspx?keyword=מטריית%20שמש%20לרכב), [Zap shade](https://www.zap.co.il/search.aspx?keyword=מגן%20שמש%20לשמשה)) | Umbrella shade ₪25–39 ([Ali](https://www.aliexpress.com/w/wholesale-car-sun-shade-umbrella.html?shipCountry=IL)) | "מגן שמש לרכב": 4 in one run (Morag service centre, Johnson Clean, המרכז למטייל), ≈0 in reruns. "שמשיה לרכב" / "מגן שמש מטריה": ≈0 |
| Things falling into the seat gap | Car owners | Zap search irrelevant (no listings) | Seat gap filler 2-pack ₪5–11 (50,000+ sold) ([Ali](https://www.aliexpress.com/w/wholesale-car-seat-gap-filler.html?shipCountry=IL)) | ≈0 |
| Door dings and wall scrapes in tight underground parking | Car owners in apartment buildings (number UNVERIFIED) | Zap has no car-specific results; generic foam corner guards ₪49–101 ([Zap](https://www.zap.co.il/search.aspx?keyword=מגן%20קיר%20לחניה)) | Garage wall foam bumper 4-pack ₪11.5–18.5 (4K+ sold); door edge guards ₪1.3–9 ([Ali](https://www.aliexpress.com/w/wholesale-garage-wall-bumper-foam-car-door.html?shipCountry=IL)) | "מגן דלת לרכב": 5, one advertiser (רונן שיווק אביזרים לרכב, running since Dec 2025). "מגן קיר": 25, mostly irrelevant |
| Car trash, car organiser | Car owners | not checked | ₪5–37 ([Ali](https://www.aliexpress.com/w/wholesale-car-trash-can.html?shipCountry=IL)) | "פח לרכב": 8 (garages, leasing). "מארגן לרכב": 3 (Ecouaer, from Sep–Oct 2026) |
| Phone mount | Car owners | Mounts ₪58–119 ([Zap](https://www.zap.co.il/search.aspx?keyword=מארגן%20למושב%20רכב)) | ₪1–32 ([Ali](https://www.aliexpress.com/w/wholesale-car-phone-holder-magnetic.html?shipCountry=IL)) | "מחזיק טלפון לרכב": 4 (עולם הדילים, Everwell Living, Ybaou) |
| Baby overheating in stroller or car seat | ~182K births a year, so ~550K children aged 0–3 (ESTIMATE) | Stroller clip fan ₪98–148; rear-view mirror with fan ₪179 ([Zap](https://www.zap.co.il/search.aspx?keyword=מאוורר%20לעגלה)) | Clip fan ₪7–33 (3,000+ sold); car-seat cooling fan/pad ₪32–52 ([Ali](https://www.aliexpress.com/w/wholesale-stroller-fan-clip-rechargeable.html?shipCountry=IL)) | "מאוורר לעגלה": 5 (mommy.mor, SmartCase) |
| Baby in rear-facing seat | Parents of babies | not checked | Mirror ₪5–23 ([Ali](https://www.aliexpress.com/w/wholesale-baby-car-mirror.html?shipCountry=IL)) | "מראה לתינוק": 45, mostly gift and therapy pages |
| Baby sleep | Parents | not checked | White-noise machine ₪17–50 (1,000+ sold) ([Ali](https://www.aliexpress.com/w/wholesale-white-noise-machine-baby.html?shipCountry=IL)) | "רעש לבן": 270, mixed (AudioFeel, therapists). "תינוק שינה": 120 (Agalis chain, sleep consultants, Lullaby) |
| Baby feeding and bath | Parents | Bath seats ₪103–119 (Zap, same search as above) | Silicone bib ₪3–4; bath support ₪4–15 ([Ali](https://www.aliexpress.com/w/wholesale-silicone-bib.html?shipCountry=IL)) | "ביב סיליקון": ≈0. "מנשא תינוק": 8 (Lamer, BABITO) |
| School: lunch box, bottle, labelling | ~2.4M pupils (UNVERIFIED, not looked up) | Kids lunch boxes ₪50–112 ([Zap](https://www.zap.co.il/search.aspx?keyword=קופסת%20אוכל%20לילדים)). Hebrew name labels ₪20–60 per sheet or set (FACT, [NameLabels Woo API](https://www.namelabels.co.il/wp-json/wc/store/v1/products?per_page=30)) | Bento ₪23–44; iron-on name labels about ₪3.3 ([Ali](https://www.aliexpress.com/w/wholesale-name-labels-clothes.html?shipCountry=IL)) | "מדבקות שם": 250 (NameLabels, וואווי, U name it, Tiny Tag). "קופסת אוכל": 160 (Yoopi, BoxIL, YOOZ). "בקבוק לילדים": 140 (Dana's Personal Design, Savory Bottle) |
| Back and neck pain at a desk | Office workers | not checked | Posture corrector ₪7–31 (10,000+ sold); laptop stand ₪12–15 (10,000+ sold); cervical pillow ₪29–86 (50,000+ sold) ([Ali](https://www.aliexpress.com/w/wholesale-posture-corrector.html?shipCountry=IL)) | "כרית גב": 290. "כרית אורתופדית": 180 (Orthopedali, URIEL, Papus; one ad running since Mar 2024). "מעמד למחשב": 13 |
| Sleep: light | Everyone | Sleep mask ₪35–98 ([Zap](https://www.zap.co.il/search.aspx?keyword=מסכת%20שינה)) | ₪1.3–19 (10,000+ sold) ([Ali](https://www.aliexpress.com/w/wholesale-sleep-mask-3d.html?shipCountry=IL)) | "מסכת שינה": 36 (Holyzzz, Bandzzz, Soleva, FlyHugz) |
| Limescale in kettles and bathroom; mould in coastal flats | Most households | not checked | Descaler tablets and mould gel ₪3.6–24 ([Ali](https://www.aliexpress.com/w/wholesale-mold-remover-gel.html?shipCountry=IL)) | "אבנית": 730 (water-treatment firms). "עובש": 450 (AC cleaning, painters, cleaning services). "קומקום": 130 (Quooker, Wilfa, מינרל בר) |
| Balcony and window laundry drying | ~52% of households have no dryer (REPORTED, 2020) | Drying racks ₪190–549 (Homapex ₪190–310, Leifheit ₪299–549); installed "רב חבל" outside-window rack ₪750–920 ([Zap](https://www.zap.co.il/search.aspx?keyword=מתקן%20לייבוש%20כביסה), [Zap](https://www.zap.co.il/search.aspx?keyword=מתלה%20כביסה%20לחלון)) | Wall-mounted folding rack ₪87–107 ([Ali](https://www.aliexpress.com/w/wholesale-balcony-clothes-drying-rack.html?shipCountry=IL)) | "מתלה כביסה": 85, including Hebrew DTC brands "מתלה גאוני לכביסה", "ברקת – לתלות כביסה ולהתאהב", "מתלה כביסה רב-חבל", Sheroolik |
| Elderly parents: pills, reaching, falls at night | ~1.3M aged 65+ (UNVERIFIED, not looked up) | Weekly pill boxes ₪14–65 ([Zap](https://www.zap.co.il/search.aspx?keyword=קופסת%20תרופות%20שבועית)) | Pill box ₪9–31; reacher ₪14–26 (5,000+ sold); rechargeable motion night light ₪2–3 each, likely promo-distorted ([Ali](https://www.aliexpress.com/w/wholesale-grab-reacher-tool.html?shipCountry=IL)) | "קופסת תרופות": 71, mostly health advertorials. "לחצן מצוקה": 97 (services). "מושב בטיחות": 82, including a senior-accessibility shop "כל הנוחות שבעולם" |
| Home security | Households | not checked | not checked | "מצלמת אבטחה": 85 (Anker Israel, dashcam brands) |
| Beach: sand, shade | Coastal population, summer | not checked | Pop-up beach tent ₪133–168; umbrella sand anchor ₪36 ([Ali](https://www.aliexpress.com/w/wholesale-beach-tent-pop-up.html?shipCountry=IL)) | "צל לים": 5. "אוהל חוף": about 1 |
| Holidays (Pesach cleaning, Sukkah, Hanukkah) | Jewish households | not checked | not checked | "ניקיון לפסח": about 1 (shower renovation). "סוכה" / "מתנה לחנוכה": query failed or no count |

**The BAGLY reference store itself**
- FACT: [bagly.co.il/products.json](https://bagly.co.il/products.json?limit=250) returned 250 products. Most are bags at ₪199–389, usually shown against "compare-at" prices of ₪300–600.
- FACT, same file: they include kids' school sets (Pokémon, Fortnite, Roblox, Sakura) at ₪309–359, all created May–July 2026, so school-age kids are already a Bagly segment.
- FACT, same file: small accessories priced ₪35–149 (lunch boxes, a bottle, a medicine organiser, a power bank). The pattern is a hero product plus accessory upsells.

### Inferences
- ESTIMATE: the clearest arbitrage, where Israeli shelf price is at least 4× the AliExpress price and Hebrew Meta advertisers are few, is:
  - magnetic window cleaners (₪197–379 vs ₪32–49);
  - AC wind deflectors (₪96–205 vs ₪17–52);
  - car umbrella shades (₪125–179 vs ₪25–39);
  - stroller fans (₪98–148 vs ₪7–33).
- Note on those gaps: these are generic AliExpress items, so the gap partly reflects Israeli importer margins on the same goods. A shopper who searches AliExpress will find them, which is why each needs a bundle, Hebrew instructions and branding.
- Mosquito DIY magnetic screens are already a ₪151–229 local category on Zap. Meta competition is thin (5 ads), and the urgency is real since 2024.
- Saturated or service-dominated categories (many Hebrew advertisers): name labels, lunch boxes and bottles, orthopedic pillows and back cushions, laundry racks, limescale, mould, cockroaches.

### Gaps
- No Israeli search-volume data (Google Trends blocked), so pain intensity rests on climate, health and penetration proxies, not demand data.
- Share of Israelis living in apartments, underground-parking prevalence, number of pupils and number aged 65+ were not looked up (marked UNVERIFIED).
- Zap prices are listing prices and say nothing about sold volume.
- Ad Library zeros are UNVERIFIED (see the method caveats).
- Weights in the next section are ESTIMATES from product type, not read from listings.

---

## Q2. Ranked shortlist of 8–10 BAGLY-like opportunities, with unit economics

### Takeaway
With the planning model below, no idea is profitable at CPA ₪86 if it is postal-dropshipped at ₪199: landed cost is 45–60% of price. Ideas become viable when **all three** hold: price ₪249–279 as a bundle, bulk air import (landed ≤ ~30%), and CPA ≤ ~₪90.

The top three are:
1. Magnetic window-care kit.
2. Magnetic DIY mosquito-screen kit.
3. Safe-home kit for parents (a gift).

**Unit-economics model (ESTIMATE; all inputs are assumptions, not data):**
- profit per order = P/1.18 (VAT 18%) − 7% of P (payments and apps 4%, returns and defects allowance 3%) − ₪8 (packing and local delivery subsidy) − landed cost − CPA. This simplifies to 0.7775·P − 8 − L − CPA.
- Postal landed cost = goods + ($6.84 + $17.15·kg) × 3.17. This uses the KakoBuy EUB fit from file 10, which is an agent retail rate and so an upper bound.
- Bulk landed cost = goods + ₪25/kg air freight + ₪6/unit share of broker and duty. This is an ESTIMATE; brokerage is ₪250–450 per release per file 10, amortised over about 100+ units.
- Goods costs are AliExpress mid-list prices, rounded up. Script: `/tmp/claude-0/-home-user-somy/56050f0a-2de7-5734-b72d-e7d3e8ae6cb9/scratchpad/pains/ue.py`.
- "Break-even CPA" means the CPA at which profit is zero.

| # | Bundle idea and price | Goods (ESTIMATE) / weight (ESTIMATE) | Landed: postal / bulk | Profit at CPA 50 / 86 / 120 (bulk) | Break-even CPA (bulk) |
|---|---|---|---|---|---|
| 1 | **"חלון נקי" window-care kit**: adjustable magnetic double-glazing cleaner (2–28 mm), shutter-slat brush, track brush, 2 spare pads. ₪249, or ₪279 | ₪48 / 1.0 kg | ₪124 (50%) / ₪79 (32%) | ₪249: +57 / +21 / −13. ₪279: +80 / +44 / +10 | ₪107 at ₪249; ₪130 at ₪279 |
| 2 | **Magnetic DIY mosquito screen**, 2-window kit (cut-to-size, Hebrew video guide). ₪199; 3-window ₪279 | ₪40 / 0.5 kg (2-window); ₪55 / 0.7 kg (3-window) | ₪89 (45%) / ₪58 (29%) | ₪199: +38 / +2 / −32. ₪279: +80 / +44 / +10 | ₪88 at ₪199; ₪130 at ₪279 |
| 3 | **"הבית הבטוח של אבא ואמא" gift kit**: 3 rechargeable motion-sensor night lights (hallway to toilet), reacher grabber, weekly AM/PM pill box, non-slip pads. ₪199–249 | ₪45 / 0.8 kg | ₪110 (55%) / ₪71 (36%) | ₪199: +26 / −10 / −44. ₪249: +65 / +29 / −5 | ₪76 at ₪199; ₪115 at ₪249 |
| 4 | **AC anti-draft deflector**, 2-pack (bedroom plus living room). ₪199; 3-pack ₪249 | ₪45 / 0.9 kg; long box, volumetric risk | ₪116 (58%) / ₪74 (37%) | ₪199: +23 / −13 / −47. ₪249 (3-pack, ₪65 goods / 1.3 kg): about +32 / −4 / −38 | ₪73 at ₪199; ₪82 at ₪249 |
| 5 | **Summer car kit**: umbrella windshield shade, 2 seat-gap fillers, 4 door-edge guards. ₪199–229 | ₪50 / 0.7 kg | ₪110 (55%) / ₪74 (37%) | ₪199: +23 / −13 / −47. ₪229: +46 / +10 / −24 | ₪73 at ₪199; ₪96 at ₪229 |
| 6 | **Stroller and car-seat summer kit**: clip-on rechargeable fan, breathable cooling seat liner, UV/mesh stroller cover. ₪199–229 | ₪55 / 0.6 kg | ₪109 (55%) / ₪76 (38%) | ₪199: +21 / −15 / −49. ₪229: +44 / +8 / −26 | ₪71 at ₪199; ₪94 at ₪229 |
| 7 | **Underground-parking kit**: 4 foam wall bumpers plus door-edge guards. ₪149, or as a cross-sell with #5 | ₪30 / 0.8 kg, bulky | ₪95 (64%) / ₪56 (38%) | ₪149: +2 / −34 / −68 | ₪52 |
| 8 | **Ice-silk cooling sheet and pillowcase set**. ₪229 | ₪70 / 1.2 kg | ₪157 (69%) / ₪106 (46%) | ₪229: +14 / −22 / −56 | ₪64 |
| 9 | **Back-to-school Hebrew kit**: lunch box, bottle, iron-on Hebrew name labels. ₪199 | ₪60 / 0.8 kg | ₪125 (63%) / ₪86 (43%) | ₪199: +11 / −25 / −59 | ₪61 |

Profit figures are ESTIMATES computed with the model above; none are sales or margin data.

**Per-idea detail.** All ad counts are FACT from Ad Library runs on 2026-11-14 (caveats in the method section).

**1. Window-care kit (rank 1)**
- **Pain**: every apartment household has outer glass that cannot be reached, plus shutter dust. It recurs monthly, worse after khamsin and dust storms.
- **Demo**: wiping the outside of a closed window from inside is a perfect 10-second video.
- **Israel price anchor**: Tyroler ₪197–379 and Glider ₪211–360 on [Zap](https://www.zap.co.il/search.aspx?keyword=מנקה%20חלונות%20כפול) (FACT). Even ₪279 for a bundle looks cheap against them.
- **Competition**: an established local brand (Tyroler) but ≈0 active Meta ads for "מנקה חלונות מגנטי" (FACT, caveat). The 51 ads for "מנקה חלונות" are mostly services and Karcher.
- **Seasonality**: year-round, with peaks before Pesach (Mar–Apr) and Rosh Hashana.
- **Repeat and bundle**: spare pads are a consumable; the shutter brush is a cross-sell.
- **Risks**: magnet strength must match glass thickness (Israeli double glazing varies), so a wrong fit causes returns and a dropped outer half. Needs a safety cord and clear "measure your glass" sizing. Quality on AliExpress varies. No electrical or regulatory issue. IP: avoid copying Glider/Tyroler branding and photos.
- **Cheapest validation**: buy 3 AliExpress units at different thickness ranges for about ₪150, film a Hebrew demo, then run a ₪1,000–1,500 Meta test to a pre-order or landing page at ₪249/₪279 and measure CTR, add-to-cart and cost per checkout-initiated.

**2. Magnetic mosquito screen (rank 2)**
- **Pain**: mosquitoes from May to October in most homes. The 2024 West Nile outbreak (710 cases and 46 deaths by late July 2024, REPORTED) adds health fear.
- **Demo**: stick on the frame, then walk through or open the window.
- **Israel price anchor**: ₪151–229 per window for DIY magnetic kits on [Zap](https://www.zap.co.il/search.aspx?keyword=רשת%20נגד%20יתושים%20לחלון) (FACT). Installed screens cost more (not checked).
- **Competition**: Ecouaer Home and אטומקס advertise "רשת מגנטית" (5 ads, FACT).
- **Seasonality**: strong. Sell from March to September; dead in winter, so launch in March 2027.
- **Repeat and bundle**: buyers return for more windows; cross-sell a door screen (AliExpress ₪73).
- **Risks**: Israeli windows (sliding aluminium "חלון ויטרינה", "דריי-קיפ") vary, so a wrong-size kit means returns. Offer cut-to-size with a Hebrew measuring guide. Low regulatory risk.
- **Cheapest validation**: lead-capture ad in March ("כמה חלונות יש לך?"), then pre-order.

**3. Safe-home kit for parents (rank 3)**
- **Pain**: falls on the way to the toilet at night, pill confusion, and items out of reach. Buyers are adult children aged 35–60 (a gift, low price sensitivity).
- **Demo**: a hallway lights up when someone walks.
- **Israel price anchor**: pill boxes ₪14–65 (FACT, Zap). There is no bundled equivalent in my checks (UNVERIFIED).
- **Competition**: "קופסת תרופות" has 71 ads, mostly health advertorials. "כל הנוחות שבעולם" is a senior-products advertiser (FACT).
- **Seasonality**: gift peaks at Rosh Hashana, Pesach and Mother's Day (Feb).
- **Risks**: lithium rechargeable lights need a battery shipping line (+8–45% per file 10), and USB chargers may trigger standards requirements (SI 900 note in file 10, UNVERIFIED for this item). Using AAA battery-powered lights avoids part of this. Do not make medical claims.
- **Cheapest validation**: a gift-angle ad test before Pesach 2027, plus a WhatsApp poll of 30 people aged 40+.

**4. AC deflector**
- **Pain**: about 94% of households have an AC (REPORTED, 2020). The cold draft on the bed or a baby's cot is a near-universal complaint.
- **Israel price anchor**: ₪96–205 on [Zap](https://www.zap.co.il/search.aspx?keyword=מסיט%20רוח%20למזגן) (FACT).
- **Competition**: ≈0 Meta ads (FACT, caveat).
- **Main problem**: long, bulky packaging (60–100 cm), so shipping is volumetric. Margins only work with sea or air bulk freight.
- **Seasonality**: Jun–Sep and the winter heating months.
- **Risks**: fit with Israeli split-AC models (Tadiran, Electra) and adhesive failing in heat. Electra/Tadiran-compatible sizing must be verified.

**5. Car kit**
- **Segment**: about 3.67M private cars (REPORTED).
- **Israel price anchor**: umbrella shade ₪125–179 (FACT, Zap), but basic shades cost only ₪22–89, so anchoring is weaker.
- **Competition**: ≈0–4 ads.
- **Main problem**: umbrella shades are a known AliExpress commodity (₪25–39), so this must be a branded kit with size-by-car-model fit.
- **Seasonality**: Apr–Oct.

**6. Stroller summer kit**
- **Segment**: about 182K births a year (REPORTED).
- **Israel price anchor**: fans ₪98–148 (FACT, Zap).
- **Competition**: 5 ads.
- **Risks**: highest regulatory exposure on the list. Products for babies plus lithium batteries mean battery shipping, possible standards needs and child-safety (finger-guard) liability. Do not sell any child-in-car alert device without Transport Ministry approval (Reg. 83D, REPORTED).

**7. Parking kit**
- Low basket value and bulky foam; only works as an add-on to #5.

**8. Cooling sheets**
- Too heavy; mattress makers already advertise; texture quality is hard to judge from photos.

**9. School kit**
- Crowded: 140–250 ads per term. BAGLY itself sells ₪309–359 school sets (FACT).
- Seasonal (Jul–Aug only). Personalisation would need local printing.

### Inferences
- ESTIMATE: three consistent rules emerge.
  1. Validate with postal dropship at break-even.
  2. Switch to a 100–300-unit air shipment once a test shows CPA ≤ about ₪90.
  3. Price at ₪249–279 with a visible Israeli anchor (Zap/Tyroler ₪197–379 makes ₪279 feel cheap).
- ESTIMATE: the window kit is the most BAGLY-like. It has a large, universal, non-seasonal segment, an obvious demo, a high local price anchor, no regulatory issue and almost no Meta competition. The mosquito kit comes second but is seasonal; launch it in March.
- If the partners want one store theme, "Israeli home, summer-proof" covers #1, #2, #4 and #8 as a cross-sell family that raises AOV.

### Gaps
- No real CJ or agent quotes, product weights, or dimensional weights. Bulk freight per kg is REPORTED forwarder marketing, not a quote.
- Customs duty per HS code for each item was not checked.
- Return rates for magnetic cleaners and screens are unknown.
- Tyroler's sales volume is unknown; Zap review counts (e.g. "5,912 חוות דעת" on one listing) may be shop-level, not product-level (UNVERIFIED).
- Whether Reg. 83D (child alert) is still enforced in 2026 is UNVERIFIED.

---

## Q3. Ideas rejected, and why

### Takeaway
Rejections fall into four groups:
- **Commodity**: the AliExpress price is under ₪15 and Israelis can easily find it.
- **Crowded**: 100+ Hebrew advertisers or established local brands.
- **Heavy or bulky**: landed cost over 40% even in bulk.
- **Regulated**: electrical, wireless, child-safety, chemicals or liquids.

### Cited Findings
- **Hebrew name labels and stickers**: crowded and low-ticket. 250 active ads for "מדבקות שם", including NameLabels, וואווי and U name it ([Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=מדבקות%20שם&search_type=keyword_unordered), FACT). Prices are ₪20–60 ([NameLabels API](https://www.namelabels.co.il/wp-json/wc/store/v1/products?per_page=30), FACT). They only make sense as a free add-in to a school kit.
- **Lunch boxes and kids' bottles alone**: 160 and 140 ads (FACT). Local prices are ₪50–112 (FACT, Zap). BAGLY already sells these.
- **Laundry drying racks**: a huge pain (about half of households have no dryer, REPORTED 2020), but heavy (2–5 kg, ESTIMATE). Hebrew DTC brands already advertise ("מתלה גאוני לכביסה", "ברקת", "רב חבל"; 85 ads, FACT). Leifheit and Homapex sell ₪190–549 (FACT).
- **Child-left-in-car alert devices**: require Transport Ministry approval under Reg. 83D (REPORTED, [JPost](https://m.jpost.com/israel-news/new-system-approved-to-prevent-forgetting-children-in-cars-674278)). The approved-device list is outside our ability to source.
- **Car phone mounts, seat-gap fillers alone, door-edge guards alone, car trash cans**: commodities at ₪1–37 on AliExpress with 10,000–50,000+ sold (FACT). Usable only inside a kit.
- **Posture correctors, laptop stands, 3D sleep masks**: AliExpress ₪1.3–31 with 10,000+ sold (FACT). Sleep masks have 36 Hebrew ads (Holyzzz, Bandzzz, FACT).
- **Orthopedic and cervical pillows, back cushions**: 180–290 ads (Orthopedali, URIEL; one ad running since Mar 2024, FACT). Bulky.
- **Kettle descalers, limescale and mould gels**: chemicals and liquids. They are prohibited on postal lines (KakoBuy note in file 10), likely need chemical or cosmetics-type registration (UNVERIFIED), and cheap citric acid is in every supermarket. The "אבנית" (730) and "עובש" (450) ad spaces are dominated by services.
- **Mosquito UV zappers, white-noise machines, neck fans**: electrical, battery or charger items. Commercial import needs a standards release (SI 900 route, FACT in file 10, for mains/charger-bundled appliances). Neck fans are a commodity at ₪17–47.
- **Security cameras and doorbell cams**: wireless equipment, which likely needs Ministry of Communications approval (UNVERIFIED). Anker Israel and dashcam brands advertise (85 ads, FACT).
- **Beach tents and shade**: ₪133–168 on AliExpress plus 1.5 kg+ (ESTIMATE). Very short season.
- **Cockroach products**: no AliExpress bait products found (FACT). Pesticides are regulated, and pest-control services dominate the 310 ads.
- **Baby silicone bibs, bath supports, baby mirrors**: AliExpress ₪3–23 (FACT). Low ticket; food-contact or child-safety items.
- **Pesach cleaning, Sukkah, Hanukkah items**: very short windows and local supply. No useful Ad Library signal (queries returned almost nothing).

### Inferences
- ESTIMATE: most "universal pain" ideas fail on basket value or weight, not on demand. The survivors pass because a bundle lifts the price to ₪249–279 while staying at or under about 1 kg.

### Gaps
- Regulatory status was not checked item by item: Standards Institute, Ministry of Communications and Ministry of Environmental Protection requirements for pesticides and chemicals. gov.il was blocked in the earlier round. Confirm with a customs broker before ordering any electrical, battery, wireless or chemical item.
