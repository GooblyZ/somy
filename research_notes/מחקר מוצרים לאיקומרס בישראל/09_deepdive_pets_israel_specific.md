# Deep dive + adversarial review: PETS (hair-removal kit, cat fountain + filters, small repeat items) and ISRAEL-SPECIFIC (safe-room power/light kits, soldier/reservist gifts, Shabbat products, heat/hard-water)

Research date: 2026-11-11. Labels: **FACT** = I observed it today on a primary page/API; **REPORTED** = a named publication/company said it; **ESTIMATE** = modelled/third-party; **UNVERIFIED** = could not confirm; **ASSUMPTION** = my modelling input, not data.

**Access disclosure (read first).**
- Worked: Israeli WooCommerce Store APIs (Pet Planet, Bpower, Miluimnik, Tactit, Y-not), Shopify `products.json` / best-selling sort (Catopia, Anipet), Zap search (via headless Chromium), AliExpress search with region=IL / currency=ILS cookie (headless Chromium), Brave Search (partly, rate-limited), Israeli press, Patsnap litigation record.
- **Did NOT work — no data from these sources anywhere in this file:** Google Trends geo=IL (HTTP 429 on explore, embed and API, 3 attempts); Meta Ad Library country IL (HTTP 403, 3 attempts); Temu (forced login wall); Shein il.shein.com (captcha challenge); Alibaba search and product pages (slider captcha / empty page); Made-in-China (403); KSP (403); oref.org.il (403); Google Patents (503); bhol.co.il, israelhayom.co.il (403). 1688 and CJ were not attempted after Alibaba failed.
- Consequences: (a) no search-trend evidence on spike-vs-sustained demand; (b) no Israeli advertiser count / ad longevity; (c) no Temu/Shein prices; (d) no fresh factory quotes — sourcing costs below are AliExpress single-unit delivered prices (an upper bound for cost, a lower bound for what consumers can pay) plus the listing prices already in file 04. Every unit-economics cost line is therefore labelled ASSUMPTION unless stated.
- AliExpress caveat: observed during the 11.11 sale; many ₪1.3–₪3.57 prices are new-user "welcome deal" prices and understate the normal price. Sold counters are global and cumulative.

---

## 1. Israeli market size and facts (pets, reservists, Shabbat observance, safe rooms, official emergency list)

### Takeaway
Hard official numbers exist for safe rooms, reservist policy and Shabbat observance; pet numbers are weak (dog registry figures are old or unsourced, there is no official cat count). The facts cut against two candidates: reservist call-ups were deliberately cut to a 40,000-per-day cap for 2026, and only about 27% of Jewish Israelis fully keep Shabbat.

### Cited Findings
**Pets**
- REPORTED (1 Mar 2020): national dog registry held 496,538 living registered dogs (943,140 ever registered) — [INN/Arutz 7](https://www.inn.co.il/news/428890). Old.
- REPORTED (26 Aug 2026, no source named in the article): "more than 636 thousand dogs are registered in Israel"; same article shows a 3 kg Bonzo bag at ₪44.90 in discount supermarkets vs ₪65 at Anipet — [Maariv](https://www.maariv.co.il/economy/consumerism/article-1359874). UNVERIFIED as to origin of the 636K figure.
- FACT (document read; data from May 2011, i.e. 15 years old): the only government household survey of pet ownership and spending found is a Ministry of Industry/Trade research paper dated November 2011 (about 1,000 phone interviews); digits in the PDF text layer are garbled, so I do not quote its numbers — [gov.il PDF](https://www.gov.il/BlobFolder/reports/the-pet-market-and-household-expenses-for-pet-maintenance/he/X11389.pdf).
- REPORTED (13 Mar 2022): "unfortunately there are no exact numbers for the quantity of cats" (official quoted in a fact-check on the "3 million street cats" claim) — [Globes](https://www.globes.co.il/news/article.aspx?did=1001405070). No official owned-cat count was found.
- ESTIMATE (already in file 02, repeated only for context): Israeli pet-supplies e-commerce about US$257m in 2025 — [ECDB](https://ecdb.com/resources/sample-data/market/il/pet-supplies).

**Reservists**
- REPORTED (9 Feb 2026): Defense and Finance ministers agreed to cap reservists serving on any given day in 2026 at 40,000; routine duty cut from 72 to 55 days; about 300,000 were activated at the war's peak; combat reservists averaged about 136 days in the first war year — [Times of Israel](https://www.timesofisrael.com/idf-says-cutting-back-superfluous-reservists-will-reduce-duty-time/).
- REPORTED (search-result summaries of Hebrew press, pages themselves returned 403 or empty — treat as UNVERIFIED detail): government extended the emergency call-up ceiling to 240,000 until end-September 2026 (down from 360–450K earlier); actual 2026 daily average estimated near 80,000, double the 40,000 budget frame — [Israel Hayom](https://www.israelhayom.co.il/news/geopolitics/article/21059095), [Maariv](https://www.maariv.co.il/news/politics/article-1327358).
- REPORTED (5 Aug 2026): more than a third of reservists are parents; many serve more than 100 days a year; Israel "is now cutting back the number of reservists" — [NPR](https://www.npr.org/2026/08/05/nx-s1-5902952/israel-is-facing-a-shortage-of-army-reservists).
- Gift-giving patterns: only the items already in file 02 (Kourt 4x care packages above ₪200; Wolt/Kantar: 40% ordered a gift online, 61% of them a gift card). New FACT: BuyMe (gift-card platform) has a dedicated "gifts for reservists" category — [BuyMe](https://buyme.co.il/categories/מתנות-למילואים).

**Shabbat observance**
- REPORTED (9 Jun 2025; N12 / Rushinek institute survey; sample size not shown on the page): 27% fully keep Shabbat, 9% partially, 20% only make kiddush, 44% not at all; 43% keep kashrut fully — [Kipa](https://www.kipa.co.il/חדשות/1205433-0/). Search snippets of the same survey say 53% of ages 18–29 report keeping Shabbat — [Makor Rishon](https://www.makorrishon.co.il/) (snippet only, UNVERIFIED).

**Safe rooms**
- REPORTED (16 Jul 2026, CBS household self-report data): about 50% of households have no mamad; 15% have no mamad, no protected room and no accessible shelter; Jewish households 53% with mamad (91% some protection), Arab households 36% (54%); under 40% of households in Jerusalem, Tel Aviv and Haifa have a mamad — [N12/Mako](https://www.mako.co.il/news-money/real_estate/Article-42de33d495a6f91027.htm).
- REPORTED: State Comptroller (Jan 2026): about 3.2 million residents (33.6%) lack standard protection — [Maariv](https://www.maariv.co.il/economy/realestate/article-1292477).

**Official Home Front Command list (secondary source; oref.org.il itself was blocked)**
- REPORTED (17 Jun 2025): long-stay kit = water and dry food for at least three days; flashlight, emergency lighting and spare batteries; first-aid kit and regular medicines with printed prescriptions; battery-powered portable radio and a portable phone charger (power bank); recommended extras: cash, document copies, small fire extinguisher and smoke detector, children's games, pet food/water/leash; test batteries and electronics every six months — [Srugim](https://www.srugim.co.il/1139084-פיקוד-העורף-לארגן-תיק-לשהייה-ארוכה-במק).

### Inferences
- Roughly half of households (those with a mamad) are the natural buyers of a "mamad kit"; the other half shelter in stairwells/public shelters and need a carry bag rather than a room kit. The official list is short and made of commodity items (flashlight, radio, power bank) that every electronics chain stocks.
- The reservist population being "gifted" is shrinking by policy in 2026 compared with 2023–2025, although actual numbers ran above budget.
- A Shabbat-specific product addresses roughly a quarter to a third of Jewish households at most, a population already served by dedicated Haredi/religious retail.

### Gaps
- No current official figure for registered dogs, owned cats, pet-owning households or household pet spending (Ministry of Agriculture year-end summary not found; CBS expenditure survey not retrieved).
- No cumulative count of reservists called up 2024–2026; no data on how often/what civilians gift reservists.
- CBS's own page for the mamad survey and the Home Front Command's own equipment page were not read directly.

---

## 2. Israeli competition and ILS prices per candidate

### Takeaway
Every candidate already has Israeli sellers at prices that leave little room: the ChomChom-type roller sells locally at ₪49.90–₪89 (pair ₪79.90), fountains at ₪125–₪400 with filter packs at ₪29–₪100, mamad kits at ₪199–₪528, Shabbat lamps at ₪84–₪208 including the original KosherLamp, and soldier gifts are dominated by personalised/printed items at ₪20–₪250. The single most important new fact: an Israeli Shopify cat store (Catopia, products dated from August 2023) ranks a fountain #1 and the reusable hair roller #2 in its own best-selling order — the first Israeli sales-rank evidence for candidates 1 and 2, and simultaneously proof that the niche is already occupied.

### Cited Findings
**(1) Pet-hair removal — FACT, all observed 2026-11-11**
- Catopia (Shopify, Holon address, products created from 2023-08-07): "reusable pet-hair roller" ₪49.90 single / ₪79.90 pair (compare-at ₪99.90), marketed as "electrostatic patent", "no glue"; it is **#2 in the store's best-selling sort** — [product feed](https://catopiaa.com/products.json?limit=250), [best-selling sort](https://catopiaa.com/collections/all?sort_by=best-selling). Also sells a "reusable hair remover for clothes/surfaces" at ₪34.90.
- Pet Planet (WooCommerce): reusable roller ₪59; adhesive rollers ₪20–35; refill ₪20; telescopic giant roller ₪79 (out of stock); "pet hair remover" ₪50 (out of stock); all show 0 on-site reviews — [Pet Planet search API](https://petplanet.co.il/wp-json/wc/store/v1/products?search=רולר&per_page=20&orderby=popularity).
- Zap "רולר שיער חיות": 36 results; InnovaGoods reusable roller ₪89 (Bali Buy), Pet Planet reusable ₪59, adhesive rollers ₪19–35, 3-pack XXL ₪75 — [Zap](https://www.zap.co.il/search.aspx?keyword=רולר%20שיער%20חיות). Zap "מסיר שיער כלבים": 5 results; reusable no-glue roller ₪69 with free shipping at Kama Zol, flagged "purchase from abroad" — [Zap](https://www.zap.co.il/search.aspx?keyword=מסיר%20שיער%20כלבים).
- Other Israeli sellers of the same ChomChom-type roller surfaced by search: Dison ("unique patent, up to 5 days"), A10 at ₪69.90 (price from search snippet), Kama Zol, Ken-Hatuki, Inter-Pet, BuyTheWay, Meshek Damti; Amazon's Hebrew storefront shows the Uproot Cleaner Pro bundle — [Dison](https://dison.co.il/product/רולר-מסיר-שערות-כלבים-כלב-חתול-חתולים), [A10](https://a10.co.il/), [Kama Zol](https://kamazol.com/he/pet-animals-accessories/רולר-מסיר-שערות-ללא-דבק-רב-פעמי), [Amazon](https://www.amazon.com/-/he/dp/B0BN836CX2). (Prices for Dison/Ken-Hatuki/Inter-Pet not read: pages empty or blocked.)
- Anipet (Shopify chain site; 1,500 products fetched, all `created_at` from 2025-12-23, i.e. re-platformed): only an adhesive roller (₪23); no reusable roller or scraper found — [Anipet feed](https://www.anipet.co.il/products.json?limit=250).
- No Israeli seller of an Uproot-style metal-edge carpet/fabric scraper, and no roller+scraper *kit*, was found in Zap, Pet Planet, Anipet or Catopia.

**(2) Cat fountains and filters — FACT, 2026-11-11**
- Catopia: plastic 3 L ₪179 (32 on-site reviews, **#1 best-seller**); stainless 2.2 L ₪248 (compare-at ₪299.90, "in stock for fast delivery"); stainless 4 L ₪320 (labelled "best selling", #3); wireless stainless 3 L ₪330; app-connected ₪399.90. Filters: 6-pack ₪59.90 (page says "replace at least monthly"), 4-pack ₪69.90, 8-pack ₪79.90, stainless-model packs ₪89.90–99.90; spare pump ₪79.90–99.90. In the best-selling order filters sit at #8, #9, #13, #14, #20, #24 and the spare pump at #19. Delivery 3–5 business days, ₪29.90 or free above ₪300 — [feed](https://catopiaa.com/products.json?limit=250), [best-selling](https://catopiaa.com/collections/all?sort_by=best-selling), [shipping policy](https://catopiaa.com/policies/shipping-policy).
- Pet Planet: Catit Pixi ₪235; Pixi filter ₪29, 6-pack ₪50; H2O filter 3-pack ₪35; Catit filters ₪49–55; Drinkwell filter ₪70 (out of stock); Pet Project filter ₪50 — [filters](https://petplanet.co.il/wp-json/wc/store/v1/products?search=פילטר&per_page=40&orderby=popularity), [fountains](https://petplanet.co.il/wp-json/wc/store/v1/products?search=מזרקה&per_page=40&orderby=popularity).
- Anipet: Petex 2.2 L ₪129; Petex sensor 2.5 L ₪189; H2O Plus ₪169; Petex 5-filter packs ₪39–49 (one out of stock) — [Anipet feed](https://www.anipet.co.il/products.json?limit=250).
- Zap "מזרקת מים לחתולים": 56 listings, ₪125–₪319 on page one (smart 1.8 L USB "plus 5 extra filters" ₪125; stainless 2 L ₪169–179; Catit Flower ₪199–235; Pixi ₪235–269) from PetCall, Pet Planet, all4pet, Django and others — [Zap](https://www.zap.co.il/search.aspx?keyword=מזרקת%20מים%20לחתולים). Zap "פילטר למזרקה": 16 results, ₪30–70 — [Zap](https://www.zap.co.il/search.aspx?keyword=פילטר%20למזרקה).
- Biopet is a wholesale catalogue (no prices) listing Petex fountain filter 5-packs WF01/WF08 — [Biopet](https://www.biopet.co.il/wp-json/wc/store/v1/products?search=מזרקה&per_page=40).

**(3) Other small pet items**
- FACT: Catopia's homepage promotes a new dental powder for cats ("Ultra Vet") and lists flea/tick ampoules; its best-selling top-25 also contains AirTag collar ₪59.90 (#4), catnip lick toy ₪29.90 (#5), litter mat ₪49 (#6), electric comb ₪79.90 (#10), automatic feeder ₪349 (#15) — [Catopia](https://catopiaa.com/), [best-selling](https://catopiaa.com/collections/all?sort_by=best-selling).
- FACT: Zap "מאכיל אוטומטי לחתול": 4 results, ₪99–469 — [Zap](https://www.zap.co.il/search.aspx?keyword=מאכיל%20אוטומטי%20לחתול).

**(4) Safe-room / emergency kits — FACT, 2026-11-11**
- Zap "ערכת חירום": 88 results. Mamad kits: ₪528 (i-Success), "war emergency kit" ₪199 and "mamad survival kit" ₪350 (Nextech, 606 Zap reviews), Miracase-branded kit ₪376–412 at three sellers incl. Walla Shops, "speaker + radio + power bank" kit ₪249, Selmor solar lighting kit ₪159–203 — [Zap](https://www.zap.co.il/search.aspx?keyword=ערכת%20חירום).
- Bpower (WooCommerce): mamad kit ₪499; "radio with display" kit ₪299 (out of stock); solar emergency radio with power bank ₪139 (out of stock) **and the same item under "sales and surplus" at ₪59**; XL rechargeable emergency lamp ₪89 **and under "sales and surplus" at ₪29**; rechargeable flashlight in surplus at ₪13; 1+1 emergency lamp ₪149 — [Bpower emergency search](https://bpower.co.il/wp-json/wc/store/v1/products?search=חירום&per_page=30&orderby=popularity), [Bpower top sellers](https://bpower.co.il/wp-json/wc/store/v1/products?per_page=25&orderby=popularity).
- Y-not: mamad kit (power bank, flashlight, battery radio, batteries) ₪299 — out of stock; 20,000 mAh power banks ₪179–199 — out of stock — [Y-not](https://y-not.co.il/wp-json/wc/store/v1/products?search=חירום&per_page=20&orderby=popularity).
- Other sellers of ready mamad kits surfaced: MDA friends association (kit at ₪75 instead of ₪150, page dated Sep 2024), EMS1/Shaag, KMA shops, Ultralife (Miracase bundle), Tactit, 1221 shop, Met — [MDA friends](https://www.ifmda.org.il/he/benefits/item/632-ערכת-מד-א-לממ-ד), [EMS1](https://www.ems1.co.il/product/ערכת-חירום-לממד/), [Ultralife](https://ultralife.co.il/catalog.asp?page=newshowprod.asp&prodid=2713735).
- Components on Zap: "תאורת חירום" category 341 models, from ₪54 (Semicom 120-LED) to ₪188, compared across 7–12 shops each; "תאורת חירום נטענת" 151 results at ₪68–179; "סוללת גיבוי 20000" 207 results at ₪129–299; power stations (Jackery/Bluetti) ₪1,014–3,999 across 13–15 shops — [emergency lighting](https://www.zap.co.il/search.aspx?keyword=מנורת%20חירום), [power banks](https://www.zap.co.il/search.aspx?keyword=סוללת%20גיבוי%2020000), [power stations](https://www.zap.co.il/search.aspx?keyword=תחנת%20כוח%20ניידת).

**(5) Soldier / reservist gifts — FACT, 2026-11-11**
- Miluimnik.co.il (WooCommerce; "Israel's reserve-duty site"; content + shop): top 30 by store popularity are almost all printed/personalised items — 3 funny army T-shirts + booklet ₪149 (#1), T-shirts ₪29–69, copper coffee pot ₪159 (#7), "complete enlistment gift pack" ₪248 (#10), laundry bag ₪52, personalised microfibre towel ₪44, pocket notebooks ₪19.90–44, enamel mugs ₪59, gel eye mask ₪59; every product shows 0 reviews — [Miluimnik API](https://miluimnik.co.il/wp-json/wc/store/v1/products?per_page=30&orderby=popularity).
- Tactit (tactical shop): top sellers are Esbit solid-fuel tablets ₪49–79 and pocket stoves ₪59–99 (consumables again), Nitecore lights ₪225–389, a 100 L duffel ₪309, ballistic plates ₪999–1,195 — [Tactit API](https://www.tactit.co.il/wp-json/wc/store/v1/products?per_page=30&orderby=popularity).
- Zap "מתנה לחייל": 27 results — Hookbox IDF gift box ₪378, printed laundry bag ₪108, figurines ₪198, key rings ₪90 — [Zap](https://www.zap.co.il/search.aspx?keyword=מתנה%20לחייל).
- Other dedicated sellers surfaced: Migvan Alaska (combat-soldier enlistment pack), Richrach ("4 items in one price" enlistment bundle), Monograma, Artishuk (personalised fleece blankets), Gasi embroidery, Giftush, the NGO "Makom Katan BaLev", Pakal.il, Yoh.co.il (reservist gear "importer to consumer", free pickup-point shipping above ₪199), BuyMe gift cards — [Migvan Alaska](https://www.migvanalaska.com/p/מארז-מתנת-גיוס-ללוחם), [Richrach](https://www.richrach.org/product/החבילה-המושלמת-למתגייס), [Yoh](https://yoh.co.il/ezrim/civd-lmilvaim.html), [BuyMe](https://buyme.co.il/categories/מתנות-למילואים).

**(6) Shabbat products — FACT, 2026-11-11**
- Zap "מנורת שבת": 153 results. Original KosherLamp ₪189 (free shipping), "original Shabbos lamp" ₪208, KosherLamp MAX ₪149, travel KosherLamp ₪189, rechargeable Shabbat lamp ₪198 — all at HaMeir (4.8 rating, 3,389 Zap reviews); generic plug-in LED Shabbat lamps ₪84–94; table lamps ₪119–178; wall reading lamps ₪153–187 — [Zap](https://www.zap.co.il/search.aspx?keyword=מנורת%20שבת). KSP has a dedicated Shabbat-lamp category (page blocked, prices not read) — [KSP](https://ksp.co.il/mob/cat/9122).
- Zap hot plates: 221 models; ₪77 (Gold Line) to ₪125 (Sauter 6-pot), each compared across 12–19 shops — [Zap](https://www.zap.co.il/search.aspx?keyword=פלטת%20שבת). Shabbat timers: 233 results; mechanical ₪44, Intermatic ₪155–209, Switcher smart socket ₪88 — [Zap](https://www.zap.co.il/search.aspx?keyword=שעון%20שבת).
- Tzomet Institute itself markets a Shabbat night-lamp ("Tris-Or") and runs a model-approval table plus an "importers and entrepreneurs" section — [Zomet](https://zomet.org.il/product/מנורת-שבת/). Or-Ad sells wall Shabbat reading lamps "approved by Tzomet" — [Or-Ad](https://www.or-ad.com/category/תאורת-פנים/מנורות-קריאה-שבת/).

**(7) Heat and hard water — FACT, 2026-11-11**
- Zap "מאוורר נטען": 215 results, ₪50 (Miracase handheld, 5 shops) to ₪549; Sakal ₪111, Sachs ₪175, Makita ₪498 — [Zap](https://www.zap.co.il/search.aspx?keyword=מאוורר%20נטען).
- Zap "מסנן אבנית": 193 results dominated by water-treatment specialists: boiler anti-scale filter ₪174, filter + anti-scale ₪183, Amiad household units ₪690–720 — [Zap](https://www.zap.co.il/search.aspx?keyword=מסנן%20אבנית).

### Inferences
- Candidate 1 as specified (roller + scraper kit) does not exist locally as a kit, but its hero component is a ₪50–70 commodity sold by at least eight Israeli sites and bundled 2-for-₪79.90 by the one store with sales-rank evidence. A kit priced ₪149–199 would be compared against that.
- Candidate 2 has the only Israeli evidence in this whole project that links a candidate to both a hardware best-seller and refills selling inside the same store. It also shows the price ladder (₪179 plastic → ₪248–330 stainless/wireless) and that the consumer filter price (₪10–25 per filter) is 10–30x the AliExpress price.
- Emergency kits are sold by electronics accessory importers (Miracase, Bpower), first-aid suppliers and tactical shops; the "surplus" pricing at Bpower is direct evidence of post-spike overstock (see §8).
- The soldier-gift market monetises emotion and personalisation (print-on-demand, embroidery), not imported hardware; a generic importer has no edge there.

### Gaps
- No dated review velocity for any competitor (Catopia shows 32 reviews on one product; review dates not read). No traffic or revenue data. Store ages inferred only from Shopify `created_at`.
- Anipet's best-selling order could not be parsed; Petlove, Zoo-Mall, Hav-Hav were unreachable (connection errors); Ivory and KSP not read.
- Judaica stores and holiday gift items (Hanukkah, Rosh Hashana, Pesach) were not scanned — no finding either way.
- Washing-machine descaler / limescale consumables in Israeli supermarkets and pharmacies: not retrieved.

---

## 3. Cheap alternatives reachable by Israelis (AliExpress observed; Temu and Shein not readable)

### Takeaway
AliExpress, priced in ILS for delivery to Israel, sells every pet and emergency component at a small fraction of Israeli retail (rollers ₪1–8, stainless fountains ₪42–83, 12-packs of filters ₪4–7, emergency bulbs ₪12–25, crank radios ₪27–75, branded 20,000 mAh power banks ₪67–92). The exception is the Shabbat lamp: searches for "shabbat lamp" and "kosher lamp" returned no functional equivalent.

### Cited Findings (all FACT as displayed 2026-11-11, region IL, currency ILS, sorted by orders; sold counts are global cumulative)
- Reusable rollers / hair tools: double-sided self-cleaning lint roller ₪1.3 (40K+ sold); another ₪2.2 (30K+); "pet hair remover roller with self-cleaning base" ₪4.3 (10K+ sold); washable sticky roller ₪3.9 (20K+); hair-removal glove ₪1.3 (50K+); "pet hair scraper" lint remover ₪1.3 (10K+) — [AliExpress roller search](https://www.aliexpress.com/w/wholesale-reusable-pet-hair-remover-roller.html?SortType=total_tranpro_desc), [scraper search](https://www.aliexpress.com/w/wholesale-pet-hair-remover-carpet-scraper-lint-cleaner.html?SortType=total_tranpro_desc).
- Fountains: HTMCK USB transparent fountain ₪19.5 (10K+ sold, 4.9); ZYFeeder 2.2 L square stainless with window, no plug, ₪41.51 (10K+ sold, 4.7); 3 L plastic ₪9.84–32.1 (4K+ each); 2.2 L low-noise ₪65.54 (3K+); 3.2 L stainless ₪69.65–73.91; 3 L stainless wireless rechargeable with sensor ₪103.42 (3K+); ROJECO stainless ₪82.88, ROJECO wireless 2600 mAh ₪118.55 — [AliExpress fountain search](https://www.aliexpress.com/w/wholesale-cat-water-fountain.html?SortType=total_tranpro_desc).
- Filters: 12/15-piece carbon-sponge sets for stainless fountains ₪3.57 (5K+ sold); 6/12-piece sets ₪3.57 (2K+); 4/8-pack for square 2 L models ₪6.06; 12-pack ₪3.3 — [AliExpress filter search](https://www.aliexpress.com/w/wholesale-cat-fountain-replacement-filter.html?SortType=total_tranpro_desc).
- Emergency lighting: E27 rechargeable emergency bulb 7–15 W ₪17.96 (50K+ sold); 18650 emergency bulb ₪24.9 (10K+); 7 W bulb ₪12.3 (10K+) — [AliExpress](https://www.aliexpress.com/w/wholesale-rechargeable-emergency-led-bulb.html?SortType=total_tranpro_desc).
- Crank/solar radios: 2000 mAh ₪27.22–69.41 (1K–3K+ sold); 4000 mAh ₪61.34–143 — [AliExpress](https://www.aliexpress.com/w/wholesale-emergency-hand-crank-radio-solar.html?SortType=total_tranpro_desc).
- Power banks 20,000 mAh: Baseus 22.5 W ₪91.64 (20K+ sold); Vention 45 W ₪76.23 (20K+); UGREEN 20 W ₪67.33; no-name ₪25.9–27.76 — [AliExpress](https://www.aliexpress.com/w/wholesale-power-bank-20000mah.html?SortType=total_tranpro_desc).
- Shabbat: "shabbat lamp" returned Judaica decor (candle trays, string lights, top item 1,000+ sold); "kosher lamp" returned ordinary motion-sensor night lights (100K+ sold at ₪2.2–6.2) — no shuttered Shabbat lamp — [shabbat lamp](https://www.aliexpress.com/w/wholesale-shabbat-lamp.html?SortType=total_tranpro_desc), [kosher lamp](https://www.aliexpress.com/w/wholesale-kosher-lamp.html?SortType=total_tranpro_desc).

### Inferences
- Price multiples of Israeli retail over AliExpress delivered: roller about 7–40x (₪50–70 vs ₪1.3–8, promo prices inflate the top of the range); stainless 2.2 L fountain about 3–6x (₪169–248 vs ₪42–66); filters about 10–30x per piece; emergency bulb/lamp about 3–7x; branded power bank about 1.5–3x.
- Israeli sellers nonetheless sell these items (Catopia's ranks), so some buyers pay for speed, Hebrew and trust; but with these multiples any shopper who image-searches will see the gap, and filters are the easiest item to defect on.
- Motion-sensor lights being returned for "kosher lamp" illustrates that Chinese platforms do not understand the Shabbat use case — the one area here where a local seller is not undercut by them.

### Gaps
- Temu and Shein prices and sold counts: not readable (login wall / captcha). Given Temu's share, Temu prices are probably similar or lower — UNVERIFIED.
- Israeli share of AliExpress buyers for these listings unknown; review-by-country not checked; counters not re-observed on a second date.
- Normal (non-11.11, non-new-user) prices not captured.

---

## 4. Israeli demand: Google Trends and Meta Ad Library

### Takeaway
Neither Google Trends nor the Meta Ad Library could be read from this environment, so whether emergency and reservist terms are pure spikes, and how many Israeli advertisers run these products, remains unanswered by direct measurement. The only demand evidence is indirect: store-internal rankings, stock/clearance status and press.

### Cited Findings
- FACT: Google Trends explore, embed and API endpoints returned HTTP 429 on three attempts (plain HTTP and headless Chromium); Meta Ad Library returned HTTP 403 on three attempts. No data obtained.
- FACT (indirect, cats): fountain #1, roller #2, fountain #3 and six filter SKUs within the top 25 of Catopia's best-selling order; one fountain shows 32 on-site reviews — [Catopia](https://catopiaa.com/collections/all?sort_by=best-selling).
- FACT (indirect, emergency, mixed): Bpower's store-popularity #1 is the solar emergency radio (now out of stock at ₪139, while a "surplus" listing of the same radio sits at ₪59 and is also out of stock); Y-not's mamad kit and all power banks are out of stock; Bpower lists emergency lamps in surplus at ₪29 — [Bpower](https://bpower.co.il/wp-json/wc/store/v1/products?per_page=25&orderby=popularity), [Y-not](https://y-not.co.il/wp-json/wc/store/v1/products?search=חירום&per_page=20&orderby=popularity).
- REPORTED (16 Jun 2025): during the first Iran war the "emergency products category grew tenfold"; hundreds of generators and thousands of power-backup units and transistor radios were sold — [ICE](https://www.ice.co.il/consumerism/news/article/1069774).
- REPORTED (search snippet only, article date not confirmed but the URL format is from the 2000s): an older survey also found 27% of Jews in Israel defining themselves as Shabbat-observant, which suggests the observant share is stable — [Ynet](https://www.ynet.co.il/articles/0,7340,L-3417232,00.html).

### Inferences
- Woo "popularity" is all-time weighted, so Bpower's radio at #1 reflects the 2025–2026 war spikes; the surplus listings show what happened afterwards. This is consistent with spike-driven demand, but it is one store.
- Without Trends, the reasonable prior from file 02 stands: emergency = documented spikes (June 2025, March 2026) with unknown baseline; reservist gifts = tied to call-up intensity, which policy is reducing.

### Gaps
- Google Trends IL 5-year series for: מסיר שיער כלבים, מזרקת מים לחתולים, פילטר למזרקה, ערכת חירום לממ"ד, תאורת חירום, מתנה לחייל, מתנה למילואימניק, מנורת שבת — must be pulled manually (10 minutes in a normal browser).
- Meta Ad Library IL: advertisers, start dates and creatives for the same terms — must be checked manually. Whether Catopia, Dison or Bpower currently run ads is unknown.

---

## 5. Sourcing: factory prices, weights, MOQs, battery limits

### Takeaway
No fresh factory quote could be obtained (Alibaba, Made-in-China blocked), so realistic cost is bracketed only from above by AliExpress single-unit delivered prices and from below by the Alibaba listing prices already in file 04. Lithium content splits the candidates: the roller kit and a mains/USB fountain are simple; power banks, radios, rechargeable lamps and wireless fountains are battery goods with a mandatory Israeli battery standard and air-freight restrictions.

### Cited Findings
- Roller: Alibaba listings US$0.68–2.50 per piece, MOQ 2–10 (from file 04; not re-verified today) — [Alibaba](https://www.alibaba.com/product-introduction/Custom-Logo-Self-Cleaning-Chom-Reusable_1601132899295.html). AliExpress single-unit delivered ₪1.3–8 (§3).
- Fountain: dropship-tool cost US$12.01–13.19 (file 04) — [SellTheTrend](https://www.sellthetrend.com/niche/pet-products). AliExpress single-unit delivered: stainless 2.2 L ₪41.51, 3 L wireless stainless ₪103.42 (§3). One Chinese OEM site lists a 1,000-piece MOQ for a 304-stainless circulating fountain, price on request (search-result summary) — [petproducts.com.cn](https://petproducts.com.cn/?p=39595).
- Filters: AliExpress ₪3.3–7 per 6–15 pieces delivered (§3).
- Emergency components: AliExpress single-unit delivered ₪12–25 (bulb), ₪27–75 (radio), ₪67–92 (branded 20,000 mAh power bank) (§3).
- Batteries by air (REPORTED, forwarder/mail-service guides, low reliability, not Israel-specific rate data): standalone power banks are classed as batteries and are the most restricted category in air mail; devices with built-in batteries under 100 Wh can travel via "sensitive goods" channels; one mail-forwarder lists Israel among destinations with lithium restrictions (limit of 2 built-in-battery items per parcel) — [Tenso guide](https://www.tenso.com/en/static/guide_contraband_lithium), [Sino-Shipping](https://www.sino-shipping.com/regulation-batteries-shipments-from-china/), [FedEx Israel lithium page](https://www.fedex.com/he-il/shipping/dangerous-goods/how-to-ship/lithium-batteries.html).
- Freight reference (file 01): air about US$5.31/kg, express US$13.25/kg, sea LCL about US$80/CBM, forwarder marketing figures — [DTFU](https://www.dtfulogistics.com/news/shipping-cost-from-china-to-israel/).

### Inferences
- A ChomChom-size roller is a bulky-light item (roughly 20 x 7 x 7 cm): cheap by unit, expensive by volumetric weight in air freight; a two-roller kit plus scraper should be sea-freighted or its freight cost will exceed the product cost. (Dimensions are my estimate, not sourced.)
- AliExpress retail of ₪42 for a stainless fountain delivered to Israel means the factory price for that grade is plausibly well under US$10; "decent quality" (quiet pump, real 304 steel, spare pump availability) may cost more. Do not use ₪42 as a landed-cost assumption for a branded-quality unit.
- Any kit containing a power bank must ship by sea or a dangerous-goods-capable air line and clear the Israeli battery standard (§6) — that alone removes it from a "cheap pre-investment test".

### Gaps
- No verified FOB price, MOQ, carton size or weight for any item; no 1688/CJ data; no Israel-specific battery-line surcharge. Three real supplier quotes per item are required before any decision.
- No price found for an Uproot-style copper-edge scraper.

---

## 6. Regulation and IP

### Takeaway
The pet-hair kit carries IP risk mainly in the scraper (active US design patents owned by Uproot Lint LLC, asserted via Amazon complaints) and in brand names; the roller's own patent status could not be established. Battery products fall under a mandatory Israeli standard (SI 62133) requiring recognised-lab testing; Shabbat products need rabbinical approval in practice, and the approval body (Tzomet) also sells its own lamp.

### Cited Findings
- Uproot: US design patents USD1009393S (granted 26 Dec 2023, est. expiry 2038) and USD1041113S (granted 3 Sep 2024, est. expiry 2039), "cleaning device component", owner Uproot Lint LLC, status active; two Chinese sellers sued Uproot in S.D. Fla. (case 0:24-cv-62353, filed 16 Dec 2024) after Uproot filed Amazon infringement complaints on 30 Nov and 6 Dec 2024; voluntarily dismissed 10 Mar 2025 — [Patsnap case record](https://www.patsnap.com/resources/blog/litigation/zhanhongtu-v-uproot-lint-llc-pet-hair-removal-rake-design-patents-patsnap/), [Justia docket](https://dockets.justia.com/docket/florida/flsdce/0:2024cv62353/680479).
- ChomChom: trademark "CHOMCHOM ROLLER" registered in the US (reg. no. 5328663); Canadian trademark record shows registered owner Word Ape, LLC d/b/a ChomChom Roller and current owner Cheddar Creations, Inc. (Walpole, MA) — i.e. the brand changed hands; a 2013 press release calls the product "internationally patented" without a number — [Justia TM](https://trademark.justia.com/873/95/chomchom-87395211.html), [CIPO](https://ised-isde.canada.ca/cipo/trademark-search/1918685), [PR Newswire 2013](https://prnewswire.com/news-releases/innovative-new-chomchom-roller-promises-easier-pet-hair-removal-than-ever-before-without-the-need-for-adhesives-or-awkward-vacuum-attachments-190185361.html). No acquisition announcement and no litigation against copycats was found.
- FACT: Israeli sellers describe the roller as "patent" (Catopia: "based on an electrostatic patent"; A10/Dison: "unique patent") — [Catopia feed](https://catopiaa.com/products.json?limit=250), [A10](https://a10.co.il/).
- KosherLamp: based on a US application by Shmuel Veffer filed 28 Jul 2004, published as US 2005/0036322 A1; sold by Kosher Innovations (Toronto); "hundreds of thousands" sold by 2010; later third-party US patents exist for "Shabbat bulb" designs (US 9,541,262; US 10,203,073) — [JTA 2004](https://www.jta.org/2004/06/15/lifestyle/solving-a-sabbath-dilemma), [USPTO 9,541,262](https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/9541262), [USPTO 10,203,073](https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/10203073). Whether the 2004 application was granted and its current status: not confirmed.
- Batteries: SI 62133 parts 1 (nickel) and 2 (lithium) became official, binding standards on 28 May 2022; rechargeable batteries in lighting, communication and household products must be tested in an approved, recognised lab; the Israeli standard is identical to IEC 62133; importer routes depend on holding foreign test certificates (Chamber of Commerce explainer, 23 Mar 2023, citing the Standards Administration and ITL labs) — [Chamber of Commerce](https://www.chamber.org.il/foreigntrade/1109/1112/138455/). A July 2024 order updated the import groups for rechargeable batteries (page not readable today; search summary says it eased supervision) — [Chamber of Commerce](https://www.chamber.org.il/foreigntrade/1109/1112/143707/).
- Shabbat approvals: Tzomet publishes per-model approvals with validity dates and stamps, has a section for importers/entrepreneurs, and markets its own Shabbat lamp — [Zomet](https://zomet.org.il/product/מנורת-שבת/). Local competitors advertise "Tzomet approval" — [Or-Ad](https://www.or-ad.com/category/תאורת-פנים/מנורות-קריאה-שבת/); Bug lists a hot plate with Tzomet approval at ₪99 (file 02) — [Bug](https://www.bug.co.il/פלטה-חשמלית-לשבת-novo-90615455).
- Consumer-law exposure (from file 01, unchanged): 14-day distance-sale cancellation, fee capped at 5% or ₪100; defect cancellation at seller's cost — [Kol Zchut](https://www.kolzchut.org.il/he/ביטול_עסקה_שנעשתה_באינטרנט_או_בטלפון).

### Inferences (verify with an IP lawyer / standards consultant before acting)
- US design patents do not apply in Israel as such; exposure in Israel exists only if Uproot or ChomChom registered designs/patents/trademarks here. That was not checked. Practical rule regardless: no "ChomChom" / "Uproot" wording, no copied creatives, no "patent" claims the seller cannot substantiate (a misleading-claim risk under consumer law).
- Cat fountains: a USB-powered unit sold without a wall adapter avoids the Israeli plug question; a supplied 230 V adapter is a mains charger and would fall under official electrical standards; wireless models add an SI 62133 battery. (Not sourced to a specific Israeli regulation today.)
- Emergency kits are the most regulated candidate: power bank + radio + rechargeable lamps = three battery products needing test documentation for commercial import.
- Shabbat lamp: a mains luminaire (electrical standard) plus halachic approval — two certifications before the first sale, in a market where the approver is also a competitor.
- "Military-style equipment": nothing in a civilian gift pack (socks, towels, mugs, shirts) is restricted; restricted categories (ballistic plates, optics, weapon parts) are sold by licensed tactical shops such as Tactit and are outside this store's scope. No legal source was retrieved on this point.

### Gaps
- Israeli Patent Office design/patent/trademark register not searched (ChomChom, Uproot, KosherLamp). Google Patents unreachable.
- Current import group for power banks and rechargeable lamps, testing cost and lead time: not obtained. Applicability of the "European route" to these items: unknown.
- Cat-fountain materials (food-contact) and pump electrical requirements in Israel: not researched. Veterinary products (flea ampoules, dental powders) registration rules: not researched.
- Tzomet approval fees and process: not obtained.

---

## 7. Repeat purchase and bundles

### Takeaway
The filter refill is real in Israel (filters occupy six of Catopia's top-25 slots and every pet shop stocks them), but its economics are fragile: a ₪50–100 refill order cannot carry a ₪30 delivery, and the same filters cost ₪4–7 per dozen on AliExpress. Bundles are the only lever that moves order value into the ₪250–350 band.

### Cited Findings
- FACT: Catopia filter packs ₪59.90–99.90; page text: "recommended to replace the filter at least once a month"; free shipping only above ₪300, otherwise ₪29.90 — [Catopia feed](https://catopiaa.com/products.json?limit=250), [shipping policy](https://catopiaa.com/policies/shipping-policy).
- FACT: Pet Planet filter packs ₪29–70; Anipet 5-packs ₪39–49 — [Pet Planet](https://petplanet.co.il/wp-json/wc/store/v1/products?search=פילטר&per_page=40&orderby=popularity), [Anipet](https://www.anipet.co.il/products.json?limit=250).
- REPORTED (manufacturer/retailer guidance, marketing content): carbon filters should be replaced every 2–4 weeks; multi-cat homes and hard water shorten the interval; neglected maintenance causes slime and pump failure — [Petlibro](https://petlibro.com/blogs/all/how-often-to-replace-your-cat-fountain-filter), [Petcube](https://petcube.com/blog/how-often-to-change-pet-water-fountain-filter/).
- FACT: Catopia sells spare pumps (₪79.90–99.90) and one ranks #19 in best-selling — pumps fail often enough to be a product — [Catopia best-selling](https://catopiaa.com/collections/all?sort_by=best-selling).
- FACT: existing local bundles — Zap listing "smart fountain 1.8 L + 5 extra filters" ₪125 (PetCall); Catopia roller pair ₪79.90; Catopia has a "deals and bundles" menu — [Zap](https://www.zap.co.il/search.aspx?keyword=מזרקת%20מים%20לחתולים), [Catopia](https://catopiaa.com/).
- FACT: consumables dominate other Israeli stores' rankings too — Esbit fuel tablets at Tactit (#1, #3, #9) — [Tactit](https://www.tactit.co.il/wp-json/wc/store/v1/products?per_page=30&orderby=popularity).

### Inferences
- Realistic reorder behaviour is unknown; marketing says monthly, real owners stretch filters or stop using them. Planning number (ASSUMPTION): 1–2 refill orders per fountain buyer per year, not 12.
- A refill only pays if it ships cheaply (letter-size 12–24 pack via post/pickup point) or rides on another order; subscription with a yearly pack sent once is the simplest design.
- Bundles consistent with observed prices: (a) stainless fountain + 12 filters + cleaning brushes at ₪249–279; (b) the same + roller pair at ₪319–349 (crosses Catopia's ₪300 free-shipping convention); (c) "new cat" pack. For the emergency idea: lamp pair + radio + power bank at ₪299–399, matching Bpower/Miracase.
- The pet-hair roller is better used as a ₪60–80 add-on that raises order value without extra delivery or acquisition cost than as a hero product.

### Gaps
- No measured Israeli repurchase rate for filters or any pet consumable; no subscription data.
- Filter compatibility: whether the chosen fountain uses a generic disc available on AliExpress (no lock-in) or a proprietary shape — to be checked per supplier.

---

## 8. Adversarial review: evidence against each candidate

### Takeaway
Each candidate has a concrete contradicting fact: the roller is already a ₪50 commodity in Israel and ₪1–8 on AliExpress; the fountain niche has a three-year-old Israeli DTC incumbent plus every pet chain; emergency sellers are clearing surplus at 60–70% off between spikes; reservist call-ups are being cut and the gift market is personalisation-led; Shabbat lamps are a mature, approval-gated category with the original brand already at ₪149–208; fans and anti-scale filters are commodity or specialist categories.

### Cited Findings
- Pet-hair: at least eight Israeli sites sell the reusable roller at ₪49.90–89; pair at ₪79.90 — [Catopia](https://catopiaa.com/products.json?limit=250), [Zap](https://www.zap.co.il/search.aspx?keyword=רולר%20שיער%20חיות). AliExpress ₪1.3–8 — [AliExpress](https://www.aliexpress.com/w/wholesale-reusable-pet-hair-remover-roller.html?SortType=total_tranpro_desc). On Zap the reusable roller draws a "purchase from abroad" flag at Kama Zol, i.e. local sellers are themselves drop-shipping it — [Zap](https://www.zap.co.il/search.aspx?keyword=מסיר%20שיער%20כלבים). NextStock's lint/pet-hair brush at ₪39 had 6 reviews (file 02) — [NextStock](https://nextstock.co.il/wp-json/wc/store/v1/products?orderby=popularity&order=desc&per_page=25).
- Fountain: 56 Zap listings; chains sell entry models at ₪125–129 — [Zap](https://www.zap.co.il/search.aspx?keyword=מזרקת%20מים%20לחתולים), [Anipet](https://www.anipet.co.il/products.json?limit=250). Pet Planet's own top-25 contains no gadget at all, only consumables (file 02) — [Pet Planet](https://petplanet.co.il/wp-json/wc/store/v1/products?orderby=popularity&order=desc&per_page=25). Complaint pattern abroad: slime despite weekly cleaning, pump faults replaced under warranty (anecdotal reviews) — [Petco listing](https://www.petco.com/product/catit-pixi-white-fountain-for-cats), [Zooplus reviews](https://www.zooplus.co.uk/feedback/shop/cats/cat_bowls_feeders/cat_fountains/cat_mate/146828?stars=3).
- Emergency: Bpower "sales and surplus": emergency radio ₪139 → ₪59, XL emergency lamp ₪89 → ₪29, rechargeable flashlight ₪13 — [Bpower](https://bpower.co.il/wp-json/wc/store/v1/products?search=חירום&per_page=30&orderby=popularity). MDA's friends association sold a mamad kit at ₪75 — [MDA friends](https://www.ifmda.org.il/he/benefits/item/632-ערכת-מד-א-לממ-ד). In the March 2026 war, AliExpress orders fell 38% and Temu 68% (file 02) — imports are disrupted exactly when demand peaks — [Globes](https://en.globes.co.il/en/article-1001538233).
- Reservists: 2026 cap of 40,000 per day and duty cut to 55 days — [Times of Israel](https://www.timesofisrael.com/idf-says-cutting-back-superfluous-reservists-will-reduce-duty-time/). Aug 2026 survey (search summary, UNVERIFIED): 42% of households say their finances worsened since the war and 63% cut other spending — [ICE](https://www.ice.co.il/consumerism/news/article/1099915). NGOs give equipment to soldiers free of charge — [Yashar LaChayal](https://yasharlachayal.org/projects/needy-soldier-fund/). Miluimnik's products show 0 reviews across the top 30 — [Miluimnik](https://miluimnik.co.il/wp-json/wc/store/v1/products?per_page=30&orderby=popularity).
- Shabbat: only 27% fully observe — [Kipa](https://www.kipa.co.il/חדשות/1205433-0/); 153 lamp listings with the original brand at a 3,389-review seller — [Zap](https://www.zap.co.il/search.aspx?keyword=מנורת%20שבת); hot plates at ₪77–125 compared across up to 19 shops — [Zap](https://www.zap.co.il/search.aspx?keyword=פלטת%20שבת).
- Heat / hard water: rechargeable fans 215 listings from ₪50 — [Zap](https://www.zap.co.il/search.aspx?keyword=מאוורר%20נטען); AC market shrinking and desalinated water moderately soft (file 02) — [Calcalist](https://www.calcalist.co.il/article/r1t0mzpnmg), [HUJI](https://cris.huji.ac.il/en/publications/new-desalinated-drinking-water-regulations-are-met-by-an-innovati/).

### Inferences
- Ethical/brand risk: selling "war kits" with urgency advertising during an escalation invites accusations of profiteering and, if delivery slips, the consumer-authority exposure described in file 02; a store whose other products are pet or household items gains nothing brand-wise from it. A calm-period "preparedness" tone (aligned with the Home Front Command list, no fear creatives) is the only defensible framing.
- Soldier gifts bought by parents/partners are emotional purchases where provenance matters ("from a reservist-owned business", personal dedication); a UV-steriliser store has no credibility there.
- Saturation could not be measured through ads; supply-side saturation is clear for rollers, fans, hot plates, emergency lamps.
- No documented case of a named Israeli seller failing in these exact niches was found; the surplus pricing and out-of-stock patterns are the closest evidence.

### Gaps
- Meta Ad Library check for Israeli advertisers on all seven themes (blocked). Hebrew consumer-complaint data (Facebook groups, forums) for fountains and rollers not accessible.
- Whether Catopia is profitable or even actively advertising is unknown; a three-year product history shows survival, not profit.

---

## 9. Unit-economics scenarios (ILS) for the three strongest structures

### Takeaway
On assumption-heavy but transparent numbers, a pet-hair kit at ₪149 breaks even only at a CPA of about US$19 (below the US$25–40 range), a fountain + filters kit at ₪249 breaks even at about US$28, a combined cat bundle at ₪329 at about US$42, and a mamad kit at ₪299 at about US$24. Only the ₪329 bundle clears the reported Israeli median CPA (US$32), and only if buyers accept that basket.

### Cited Findings (inputs)
- VERIFIED-as-REPORTED: VAT 18% (file 01) — [VATupdate](https://www.vatupdate.com/2025/12/10/israel-approves-2026-budget-vat-stays-at-18-expands-exemptions-eases-bank-entry-rules). Median Meta cost per purchase in Israel about US$31.8 (single vendor source, file 01) — [Superads](https://www.superads.ai/facebook-ads-costs/cost-per-purchase/israel). Courier list price ₪38 standard (file 01) — [D2D](https://www.d2d.co.il/blog/ecommerce-delivery-israel).
- VERIFIED (observed today): competitor price points used to set P — fountain ₪248, roller pair ₪79.90, filter 6-pack ₪59.90, free shipping above ₪300 — [Catopia](https://catopiaa.com/products.json?limit=250), [shipping policy](https://catopiaa.com/policies/shipping-policy); mamad kits ₪299–499 — [Bpower](https://bpower.co.il/wp-json/wc/store/v1/products?search=חירום&per_page=30&orderby=popularity).
- VERIFIED (observed today, single-unit retail delivered, upper bound for cost): AliExpress stainless 2.2 L fountain ₪41.51; 12 filters ₪3.57–7; rollers ₪1.3–8; radio ₪27–69; branded 20,000 mAh power bank ₪67–92; emergency bulbs ₪12–25 — [AliExpress searches in §3](https://www.aliexpress.com/w/wholesale-cat-water-fountain.html?SortType=total_tranpro_desc).

### Inferences (the model — every number not marked VERIFIED above is an ASSUMPTION)
Common assumptions: USD/ILS 3.5 (ASSUMPTION, not checked today) so CPA US$25 / 32 / 40 = ₪87.5 / 112 / 140; seller is VAT-registered; stock held in Israel (Model B); delivery to customer free, cost to seller ₪30 ex-VAT (ASSUMPTION from ₪38 list); payment fees 3% of price (as instructed); returns + service allowance 3% (no electronics), 5–6% (pump/battery) of price (ASSUMPTION); landed cost = product + sea/air freight + clearance share (ASSUMPTION, to be replaced by quotes).

| Line (ILS per order) | A. Pet-hair kit (2 rollers + scraper + mitt) | B. Fountain kit (stainless 2.2 L + 12 filters + brushes) | C. Cat bundle (B + roller pair) | D. Mamad kit (2 lamps + radio + 20,000 mAh bank) |
|---|---|---|---|---|
| Price incl. VAT (set from VERIFIED market prices) | 149 | 249 | 329 | 299 |
| Net of 18% VAT | 126.3 | 211.0 | 278.8 | 253.4 |
| Payment fees 3% (ASSUMPTION) | 4.5 | 7.5 | 9.9 | 9.0 |
| Local delivery (ASSUMPTION) | 30 | 30 | 30 | 35 |
| Returns + service (ASSUMPTION) | 4.5 (3%) | 15 (6%) | 19.7 (6%) | 15 (5%) |
| Landed product cost (ASSUMPTION) | 22 | 62 | 74 | 115 |
| **Contribution before ads** | **65.3** | **96.5** | **145.2** | **79.4** |
| **Break-even CPA** | ₪65 = US$18.7 | ₪96 = US$27.6 | ₪145 = US$41.5 | ₪79 = US$22.7 |
| Profit at CPA US$25 | −22 | +9 | +58 | −8 |
| Profit at CPA US$32 | −47 | −16 | +33 | −33 |
| Profit at CPA US$40 | −75 | −44 | +5 | −61 |
| Max landed cost for zero profit at CPA US$32 | negative (not viable) | 46 | 107 | 82 |
| Max landed cost for ₪30 profit at CPA US$32 | not viable | 16 | 77 | 52 |

Reading the table:
- A fails even at the low end of the CPA range; it works only as an add-on (a roller pair at ₪79.90 added to an existing order contributes roughly ₪50–55 with no extra delivery or CPA — ASSUMPTION-based).
- B is break-even on the first order at CPA US$25–28; its case rests on (i) upsell to C and (ii) filter reorders. A yearly filter pack at ₪99 shipped by post (delivery ASSUMPTION ₪15, cost ₪8) contributes about ₪58 per reorder; if 30% of buyers reorder once a year (ASSUMPTION), that adds about ₪17 per customer — helpful, not transformative.
- C is the only structure with headroom, and its landed-cost ceiling (₪77–107) is plausibly above real cost. Sensitivity: if only half of buyers take the bundle and half buy B alone, blended contribution is about ₪121 → break-even CPA about US$34.5.
- D: break-even CPA US$22.7 before any compliance cost (SI 62133 testing not included); viable only when CPA collapses during an escalation — exactly when replenishment is impossible — and the surplus prices seen at Bpower show the cost of holding stock afterwards.
- All four are highly sensitive to the delivery subsidy: charging ₪20–25 shipping below a ₪300 threshold (Catopia's practice) adds ₪17–21 net to A and B.

### Gaps
- Landed costs, return rates and CPA are assumptions; USD/ILS not verified; installment costs, Shopify third-party fee tier and overheads (subscription, accountant) excluded.
- No evidence on bundle take-rate at ₪329 or on conversion at these prices in Israel.

---

## 10. Verdict per candidate, conditions, failure modes, cheapest validation tests

### Takeaway
One candidate merits a small test — a cat-fountain system with filters and a roller add-on (CONDITIONAL / GO-TO-TEST at minimal stock); the pet-hair kit is rejected as a hero product but kept as an add-on; emergency kits are conditional and opportunistic only; soldier gifts, Shabbat products and heat/hard-water gadgets are rejected for this store on the evidence found.

### Cited Findings (verdict basis; sources in the sections above)

| # | Candidate | Verdict | Decisive evidence |
|---|---|---|---|
| 1 | Pet-hair kit (roller + scraper) | **REJECT as stand-alone; keep as add-on** | Roller sold by 8+ Israeli sites at ₪49.90–89, pair ₪79.90 ([Catopia](https://catopiaa.com/products.json?limit=250)); AliExpress ₪1.3–8 ([AliExpress](https://www.aliexpress.com/w/wholesale-reusable-pet-hair-remover-roller.html?SortType=total_tranpro_desc)); break-even CPA about US$19 (§9); Uproot design patents active ([Patsnap](https://www.patsnap.com/resources/blog/litigation/zhanhongtu-v-uproot-lint-llc-pet-hair-removal-rake-design-patents-patsnap/)). Positive: #2 best-seller at Catopia. |
| 2 | Cat fountain + filters | **CONDITIONAL → GO-TO-TEST (small)** | Fountain #1 and #3, filters x6 in Catopia's top 25 ([best-selling](https://catopiaa.com/collections/all?sort_by=best-selling)); local price ladder ₪179–330; filters ₪10–25 each locally vs under ₪1 on AliExpress; break-even CPA US$28 alone, US$42 as bundle (§9). |
| 3 | Other small pet repeat items | **CONDITIONAL (as catalogue depth, not as a lead)** | Consumables dominate Israeli pet rankings (file 02); Catopia adding dental powder ([Catopia](https://catopiaa.com/)); no sales evidence for any specific small item; veterinary-product rules unresearched. |
| 4 | Safe-room power/light kits | **CONDITIONAL — opportunistic only; REJECT as core** | Official list is commodity items ([Srugim](https://www.srugim.co.il/1139084-פיקוד-העורף-לארגן-תיק-לשהייה-ארוכה-במק)); kits at ₪199–528 from many sellers ([Zap](https://www.zap.co.il/search.aspx?keyword=ערכת%20חירום)); surplus clearance at ₪29–59 ([Bpower](https://bpower.co.il/wp-json/wc/store/v1/products?search=חירום&per_page=30&orderby=popularity)); SI 62133 testing ([Chamber](https://www.chamber.org.il/foreigntrade/1109/1112/138455/)); break-even CPA about US$23. |
| 5 | Soldier / reservist gifts | **REJECT** | Market is personalised print/embroidery and gift cards ([Miluimnik](https://miluimnik.co.il/wp-json/wc/store/v1/products?per_page=30&orderby=popularity), [BuyMe](https://buyme.co.il/categories/מתנות-למילואים)); call-ups capped at 40,000/day for 2026 ([Times of Israel](https://www.timesofisrael.com/idf-says-cutting-back-superfluous-reservists-will-reduce-duty-time/)); zero reviews on the incumbent's top 30. |
| 6 | Shabbat products | **REJECT (lamp, hot plate, timers); holiday gifts not assessed** | 27% fully observant ([Kipa](https://www.kipa.co.il/חדשות/1205433-0/)); original KosherLamp ₪149–208 at a 3,389-review seller, 153 listings ([Zap](https://www.zap.co.il/search.aspx?keyword=מנורת%20שבת)); Tzomet approval needed and Tzomet sells its own lamp ([Zomet](https://zomet.org.il/product/מנורת-שבת/)); hot plates ₪77–125 across up to 19 shops. One positive: no AliExpress substitute. |
| 7 | Heat / hard-water products | **REJECT** | Fans 215 listings from ₪50 ([Zap](https://www.zap.co.il/search.aspx?keyword=מאוורר%20נטען)); anti-scale = specialist plumbing category ₪174–720 ([Zap](https://www.zap.co.il/search.aspx?keyword=מסנן%20אבנית)); AC decline and soft desalinated water (file 02). Descaler consumables not assessed. |

### Inferences
**Candidate 2 — conditions for GO:** (1) Meta Ad Library manual check shows Catopia/others are not saturating the audience, or shows long-running ads (proof the economics work for someone); (2) three supplier quotes put a quiet-pump 304-steel 2.2 L unit + 12 filters at a landed cost of ₪60–75 or less; (3) fountain is USB-powered and shipped without a mains adapter, filters are a shape the store can keep supplying; (4) the offer is a system (fountain + year of filters + cleaning kit + optional roller pair) at ₪249–329, not a bare fountain; (5) measured CPA on a test is at or below about ₪100 for the ₪249 kit or ₪145 for the bundle.
**What could make it fail:** price-checking against AliExpress (₪42) and chain entry models (₪125–129); pump failures and slime complaints driving returns and service load; filter buyers defecting to AliExpress; Catopia and pet chains responding on price; cat-only audience too small for cheap ads; assumptions on landed cost or bundle take-rate proving wrong.
**Candidate 1 — fails as a hero because** the ticket is too low for any CPA in the stated range and the product is a visible commodity; it can add ₪50+ of contribution as an order bump. Do not import an Uproot-shaped scraper without a design-rights check.
**Candidate 4 — conditions:** only if the partners already hold compliant, non-battery or pre-certified stock bought cheaply (e.g. local wholesale/surplus, not a fresh import), sold without fear advertising and without paid ads in calm periods. Fails if a calm period follows purchase (inventory write-down, as at Bpower) or if an escalation blocks replenishment.
**Candidates 5, 6, 7 — what would change the verdict:** Trends showing sustained (not spike) reservist-gift searches plus a personalisation capability the partners own; a genuinely new Tzomet-approved Shabbat product with no local equivalent; evidence of Israeli sales for a limescale consumable sourced locally.

**Cheapest pre-investment validation tests (in order, mostly free):**
1. 20 minutes in a normal browser: Google Trends IL 5-year for the eight Hebrew terms in §4; Meta Ad Library IL for "מזרקת מים לחתולים", "רולר שיער", "ערכת חירום", "מתנה לחייל", "מנורת שבת" — count advertisers, note start dates, re-check after 14 days.
2. Re-run the free checks used here on two dates 2–3 weeks apart: Catopia best-selling order and product availability; AliExpress sold counters for the ZYFeeder 2.2 L stainless fountain and the 12-pack filters (velocity, not cumulative).
3. Order 3–4 fountain samples (two stainless USB, one wireless) and filters from AliExpress to an Israeli address (about ₪300 total): check noise, steel, pump, filter shape, delivery days; this also measures exactly what the competing consumer experience is.
4. Request three factory quotes (2.2 L stainless + filter packs + spare pumps; MOQ, carton size, weight, pump warranty) and one forwarder quote; replace the ASSUMPTION lines in §9.
5. Pre-sale / small-stock ad test: 20–30 units bought locally or via the samples' supplier, one Hebrew landing page with the ₪249 kit and ₪329 bundle, ₪1,500–2,500 of Meta spend; decision metrics: CPA versus the ₪96 / ₪145 break-evens, bundle take-rate, share choosing the roller add-on.
6. For the emergency idea only: ask two local wholesalers for surplus prices on emergency lamps/radios; if stock can be had near the ₪29–59 clearance level it can be listed with zero ad spend as an opportunistic item.

### Gaps
- Verdicts rest on one competitor's sales rank, supply-side price scans and assumption-based economics; no Israeli unit-sales figure exists for any candidate, and ad-saturation and search-trend evidence are missing entirely (blocked sources).
- Jewish-holiday gift items, washing-machine descalers, pet dental/calming consumables and litter accessories were named in the brief but not researched to a level that supports a verdict.
