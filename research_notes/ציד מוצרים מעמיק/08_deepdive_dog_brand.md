# Deep dive: a Hebrew DOG niche brand (hero + add-ons + consumables) for the Israeli Shopify store

Research date: **2026-11-15**. Builds on (and does not repeat) `research_notes/חנויות דרופשיפינג לחיות בישראל/pet_dropship_census.md` (13 Nov 2026), `research_notes/מחקר מוצרים לאיקומרס בישראל/09_deepdive_pets_israel_specific.md` (11 Nov 2026), and records ads_abroad-14/-16/-17 and problem_solvers-23.

Labels: **FACT** = observed by me today on a primary page, feed, PDF or Ad Library card. **REPORTED** = a named publication or the seller says so. **ESTIMATE** = my calculation. **UNVERIFIED** = plausible, not confirmed.

**How the data was collected, and what failed**
- **Worked:**
  - the Ministry of Agriculture dog-registry PDF
  - Shopify `products.json` feeds: Anipet, WildPet, Petrix, Petit Loup, PetSolutions, Zylarx, Kaufroom, Hazel/physiotechs, Pet Plus, Doggy
  - Pet Planet WooCommerce Store API
  - AliExpress search sorted by orders (headless Chromium, ILS/IL cookie)
  - Meta Ad Library, country=IL (headless Chromium, a fresh context per query, 75 s between queries)
  - web search
- **Ad Library queries that returned data in the second batch:** רתמה לכלב (13), כדור לכלב (23), מברשת לכלב (16), מגבונים לכלבים (9), כפפות לכלב (1, unrelated). Not completed: כפות הכלב, בעלי כלבים, מוצרים לכלבים (stopped for time).
- **Meta Ad Library was rate-limited in my first batch.** The first 5 queries (and a retry of "רתמה לכלב") returned the "no ads match" shell. This was a false zero: the same query had ~13 results earlier today in file 02, and it returned 13 again 15 minutes later. **Every Ad Library result below comes from the second batch.**
- **Failed (no data):**
  - Amazon search (empty page in headless; no ranks or review counts read directly, so Amazon figures below are REPORTED via third parties)
  - Zap (not attempted: blocked by a bot check in the census pass, and bypassing it is not allowed)
  - Hav-Hav (havhav.co.il is WordPress, but its Store API returned 404)
  - Zoo-Mall (no DNS response at zoomall.co.il)
  - Google Trends (not attempted; blocked in earlier passes)
- **AliExpress price caveat.** "New shoppers" prices (₪3.59 etc.) are welcome-deal prices. The **regular** price is the new-shopper price plus the "saved" amount, and it is what I quote as "regular" below. Sold counts are global and cumulative.
- Scripts and raw dumps: `/tmp/claude-0/-home-user-somy/56050f0a-2de7-5734-b72d-e7d3e8ae6cb9/scratchpad/dd_dogs/` (`adlib.js`, `ali.js`, `feeds.py`, `woo.py`, `parse.py`, `out/`).

---

## 1. The Israeli dog market: size, owners, where they buy, what hurts

### Takeaway
- **Size and trend.** Israel has an official **636,542 active registered dogs at end-2025**, up from 604,874 in 2023. That is a FACT from the Ministry of Agriculture registry, and the real number is higher because not every dog is registered. The pet food and supplies market is REPORTED at close to ₪2bn a year (2023).
- **Who sells.** Retail is dominated by specialty chains (Anipet ~37–39 branches and ~₪130m in sales; Zoo Eretz Zo ~28–30 branches and ~₪100m) and roughly 500 specialty shops, plus supermarkets for food.
- **The online opening.** No source gives an online share. Online, the chains sell mostly commodity accessories at ₪35–150, so a **branded, problem-solving gadget/harness line is not what they push**.
- **The pains Israeli advertisers lean on right now:**
  - pulling on the leash (an advertorial harness brand and Petrix)
  - boredom/separation when owners are out (VetCalm persona ads)
  - fear of thunder and booms (Pet Plus)
  - winter rain on walks (Pet Plus)
  - dental/bad breath (Pups, Woof)
  - itchy skin (Arava Dead Sea Pet SPA)

### Cited Findings
**Dog numbers and owners**
- FACT (PDF read today, data to 31/12/2025): the National Dog Registration Center (Ministry of Agriculture) lists **active dogs 604,874 (2023), 610,478 (2024), 636,542 (2025)**; 1,325,138 dogs registered since 2004; 325,736 males / 310,806 females, 59% of males neutered and 70% of females spayed. Rabies vaccinations: 444,097 (2023), 272,760 (2024), 314,279 (2025). The drop is because the legal duty changed to once every two years from 2024. "Dangerous breed" dogs: 16,886 (2.65%). Reported bites: 2,453 (2023), 3,026 (2024), 3,580 (2025). The counts cover active dogs born from 2011 onward. Source: [gov.il dog_stats_2025.pdf](https://www.gov.il/BlobFolder/guide/dog_stats/he/dog_stats_2025.pdf).
- REPORTED (Maariv, 17 Aug 2026): "more than 636 thousand dogs are registered". This matches the PDF. Pet food is bought in supermarket chains (Rami Levy, Shufersal, Yochananof, etc.), specialty stores and vet clinics. The same 3 kg Bonzo bag costs ₪44.90 at Rami Levy and ₪65 at Unipet — [Maariv](https://www.maariv.co.il/economy/israel/article-1356648).
- UNVERIFIED (search-engine summary only; original page not reached): 58,149 new dogs registered in 2025 (−9.5% vs 2024); Shih Tzu the top breed with 49,019 dogs, then Pomeranian and Belgian Shepherd; 44,186 dogs in Tel Aviv. If true, **small breeds dominate**, which favours small-dog sizes for the ball and the harness. Needs checking against the ministry's breed table.
- No current survey of Israeli dog-owner demographics (age, income, apartment vs house) was found. The only government household pet-spending survey found is from 2011 (file 09).

**Market size and chains**
- REPORTED (Calcalist, 9 Mar 2023): the pet food and supplies market is "close to ₪2bn a year". There are about 500 specialty stores, half of them in chains. Anipet is the leader with 39 stores and ₪130m turnover (Maabarot/Biopet bought 55% in Dec 2022). Zoo Eretz Zo has 28 branches and ~₪100m in sales (Apax Israel was buying 75% at a ₪70–80m valuation) — [Calcalist](https://www.calcalist.co.il/market/article/ryteo7iy2).
- REPORTED (ynet, undated, on the Anipet sale; same era): Anipet has 37 branches, ~₪130m sales and 13,540 deliveries per month. Toys, collars and accessories are "trending up". A monthly bag of food for a medium-to-large dog costs ₪250–300 — [ynet](https://www.ynet.co.il/economy/article/rkro5r7y2).
- Other chains seen advertising on Meta today (FACT, Ad Library): Zoolu ("the urban chain", zoolu.co.il), Dr. Food (shop + clinic), Top Dog (chain), Pet Sale, WildPet (premium/outdoor; "delivery in 2 business days in the Sharon and the centre"). Easy.co.il also lists Jungle and Speedog among chains — [Easy chains list](https://easy.co.il/list/Equipment-And-Animal-Feed-Chains).

**Spending per dog**
- REPORTED (commercial and guide sites, not surveys): ₪350–500 a month for a small dog and ₪700–1,000 for a large one (finance guide), or ₪4,000–8,000 a year. Dog health insurance runs about ₪72–200 a month by insurer — [moneyplan](https://moneyplan.co.il/cost-of-raising-dog/), [Walla](https://finance.walla.co.il/item/3863059), [habituach](https://habituach.co.il/comparison/pet-insurance/). Treat these as rough.

**Pains (what Israeli advertisers and press push now; FACT = ad seen 15 Nov 2026)**
- Pulling on the leash:
  - Advertorial by "הייזל" (Hazel, physiotechs.com), started 22 Oct 2026: a 3:24 video telling "Naama R." waking at night with shoulder pain; "harness with a front attachment"; "100-day trial".
  - Petrix: "walk without holding a leash" (ads from 27 Oct and 9 Nov 2026).
  - Source: [Ad Library "רתמה לכלב"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A8%D7%AA%D7%9E%D7%94%20%D7%9C%D7%9B%D7%9C%D7%91&search_type=keyword_unordered).
- Boredom/separation and destruction when the owner is out: VetCalm persona ads ("I installed a camera in the living room to see what my dog does when I'm out", "I thought my dog starts wrecking the house after an hour alone"), started 21–25 Oct 2026. A dog-boarding business sells a mechanical treadmill: "the dog wrecks the house, barks or gained weight? Usually it lacks an outlet for energy" (11 Nov 2026) — [Ad Library "כדור לכלב"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9B%D7%93%D7%95%D7%A8%20%D7%9C%D7%9B%D7%9C%D7%91&search_type=keyword_unordered).
- Thunder and boom fear: Pet Plus "another thunder outside and your dog is frightened again" (14 Nov 2026). REPORTED in Israeli press, 2024–2025: vets describe dogs trembling, panting and hiding during sirens and booms, with chronic stress after repeated exposure. At the start of an Iran-war operation, the "Let the Animals Live" hotline was flooded by owners wanting to give up dogs — [Maariv guide](https://www.maariv.co.il/lifestyle/the-experts/article-1303138), [Mako](https://www.mako.co.il/news-israel/2025_q2/Article-4070b46e8b88791027.htm).
- Winter rain and walks: Pet Plus "it's raining, cold and windy; the dog doesn't hurry out" (14 Nov 2026), selling a winter coat ₪85–130 — [Pet Plus feed](https://petplusshop.com/products.json?limit=250).
- Dental/breath and skin: Pups ("fed up with your dog's bad breath?"), Woof, and Arava Dead Sea Pet SPA ("stop the scratching", 8 Nov 2026) — [Ad Library "מברשת לכלב"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%91%D7%A8%D7%A9%D7%AA%20%D7%9C%D7%9B%D7%9C%D7%91&search_type=keyword_unordered).
- Pulling in forums: on the Midrag Q&A forum, owners ask how to stop pulling. Trainers there split on collar vs anti-pull harness, and a non-representative poll had 66.8% answering "collar" — [Midrag](https://www.midrag.co.il/Expanel/Question/2990).

### Inferences
- About 640k registered dogs (likely 700k+ actual, UNVERIFIED) is a **small total market**. A niche brand needs a **broad pain**: pulling, mess or boredom. A breed-specific angle is too small.
- Israeli Meta pet advertising in Oct–Nov 2026 is dominated by **story/persona advertorials**: VetCalm, Hazel, Pups, and "בעלי כלבים משתפים" pages. That is the creative bar a new brand must meet.
- Israel-specific hooks worth using:
  - winter mud and rain (Nov–Mar) for wipes and paw cleaning
  - summer heat and shedding for the brush
  - war/sirens stress for enrichment and calming, but avoid medical claims

### Gaps
- No Israeli online share for pet supplies, no Hav-Hav/Zoo-Mall data, no Israeli Facebook group names or member counts (search returned only shelter pages), and no Google Trends.
- The breed and city figures are UNVERIFIED.
- No survey on how many owners work full days away from home.

---

## 2. The 4 hero candidates: good vs bad, foreign leaders, proof, Israeli competition, sourcing

### Takeaway
| | Rolling ball (9/10) | Wipe gloves (9/10) | No-pull harness (8/10) | Self-cleaning slicker (8/10) |
|---|---|---|---|---|
| Demo strength | Very high | High | High (before/after walk) | Very high ("fur carpet" drop) |
| Israeli competition (Meta, today) | General dropshippers already sell it at ₪59.99–80 (Zylarx, Kaufroom, Pet Plus). No rolling-ball ad seen today | **None seen** for the glove format. Chains sell flat wipes ₪25–39 | **Crowded and growing**: Petrix, Hazel (advertorial), Pet Plus, WildPet/Ruffwear, all ads from Oct–Nov 2026 | No dedicated advertiser. Chains sell ordinary slickers ₪35–77; dropshippers ₪59.99 |
| Price you can charge (ESTIMATE) | ₪79–119 | ₪49–69 per 3-pack | ₪149–199 | ₪69–89 |
| Return/complaint risk | **Medium-high** (chewing, dead battery, charge port) | Low (drying out, scent irritation) | **High** (sizing, escapes) | Low (button failure, pins) |
| Repeat purchase | No (replacement only) | **Yes** | No | No |

### Cited Findings

**A. Automatic rolling ball (with tail)**
- **Good vs bad (REPORTED reviews):**
  - Weak points are the outer cover and battery housing. Dogs "chewed through it and broke the battery pack within five minutes"; fabric cover off "in about twenty minutes"; balls stopping after a charge or after ~2.5 weeks (Chewy/mirrored Amazon reviews summarised by search) — [Chewy Potaroma](https://www.chewy.com/potaroma-rechargable-automatic-ball/dp/2277686), [Chewy allforpaws](https://www.chewy.com/allforpaws-motion-activated-ball-dog/dp/1631086).
  - PetDroid (Amazon): ~3.9★ from ~13.3–13.6K reviews (mirror sites, UNVERIFIED as current). Main complaint is the **USB-C port cover**; others report failure after ~1 month and torn tennis covers. Kinship names it best interactive ball but "not chew-proof" — [Kinship](https://www.kinship.com/dog-shopping/best-interactive-dog-toys-reviews), [SheKnows](https://www.sheknows.com/living/articles/1234876561/petdroid-interactive-dog-ball-amazon/).
  - Cheerble: durability is the most cited weak point (chewing), and run time per charge is short (~1 hour measured on the SE). The battery warranty is 6 months — [Doba (reseller guide)](https://www.doba.com/blog/find-products-and-suppliers/finding-suppliers/are-cheerbles-smart-pet-toys-reliable-what-sellers-should-know-before-stocking-them-39849), [Trustpilot](https://www.trustpilot.com/review/www.cheerble.com?page=2).
  - **What a good version needs:** a sealed charging port; a solid TPU/PE shell (no fabric); a size per dog (Cheerble PE is 3.1", for dogs of 35 lb+); and play/rest auto-cycles (Cheerble PE: 10 min active / 30 min rest; ~4 h battery) — [Currys](https://www.currys.co.uk/products/cheerble-wicked-ball-pe-green-10259523.html), [Harvey Norman NZ](https://www.harveynorman.co.nz/networking-smart-home-and-home-phones/smart-home/smart-pet/cheerble-wicked-ball-physical-exercise-smart-pet-toy-light-purple.html), [YOHO](https://www.yohohongkong.com/en-us/product/119461-Cheerble-Wicked-Ball-PE-Pet-Ball-Purple).
- **Foreign leaders and prices:**
  - Cheerble Wicked Ball PE AUD 62.38 (PB Tech), $55.97 (reach.dog), NZ$31 clearance — [PB Tech](https://www.pbtech.com/product/PETCHE0024/Cheerble-Wicked-Ball-PE---Purple-31---IP65-Water-P).
  - Pets Dreams UK "Active Rolling Ball with Tail" £7.95, ad since 20 Nov 2024 (file 02, FACT).
  - TikTok Shop US: SPOVEN rolling ball, cat and small-dog version, ~89.5K sold, $7.49–12.99 (seller listing) — [TikTok Shop](https://www.tiktokshop.com/pdp/spoven-cat-toy-interactive-usb-rechargeable-motion-activated-ball/1730724953250763627).
- **AliExpress (FACT, 15 Nov 2026, sorted by orders):**
  - Top listing 1005008861976362 "Automatic Rolling Dog Ball": **20K+ sold, 4.6★**, regular ~₪15.4 (welcome price ₪3.59) — [AliExpress](https://www.aliexpress.com/item/1005008861976362.html).
  - Tail versions 9K+, 6K+ and 5K+ sold (mostly cat-oriented).
  - "Hot Intelligent Pet Toy Ball… Moving Bounce" 10,000+ sold, regular ₪25.6.
  - A "decent" dog version with LED/2 modes costs ₪21–32 regular (264–604 sold). **No Cheerble-grade dog ball was found among the top orders.**
- **Israeli competition (FACT):**
  - Zylarx "automatic rechargeable rolling ball for cats and dogs" ₪65–130, created 12 Nov 2026 — [Zylarx feed](https://zylarx.com/products.json?limit=250).
  - Kaufroom "interactive ball for cats and dogs, rolls and bounces by itself" (50% off framing) and "smart dog toy – electronic ball" — [Kaufroom feed](https://kaufroom.com/products.json?limit=250).
  - Pet Plus "ActiveBall™" ₪80 (CJ SKU, "up to 21 business days") — [Pet Plus](https://petplusshop.com/products.json?limit=250).
  - Anipet sells only a non-electronic KONG rolling ball, ₪45 — [Anipet feed](https://www.anipet.co.il/products.json?limit=250).
  - On the Ad Library query "כדור לכלב" (~23 results), **no rolling-ball ad** was seen today; the results were chains plus VetCalm/Pups funnels.
- **Shipping/certification:** a small rechargeable Li-ion cell (~300–500 mAh). Weight is ~100–200 g (ESTIMATE from listings). Battery-in-device shipping from AliExpress to IL works routinely (many sold), but rules for **commercial** import (Standards Institute, wireless approval if Bluetooth/app) were **not confirmed**, so this is a gap. Prefer a non-app, touch-activated model.

**B. No-rinse wipe gloves**
- **Good vs bad (REPORTED):**
  - Common failures: packs that **don't reseal and dry out**, "not moist enough", and **fragrance or propylene glycol** irritating sensitive dogs. Fragrance-free and hypoallergenic formulas are praised — [Rover](https://www.rover.com/blog/dog-wipes-reviewed), [Hepper](https://www.hepper.com/best-dog-wipes/).
  - **What a good version needs:** a thick non-woven mitt, a resealable or single-wrapped pack, an unscented or mild option, a stated ingredient list and paw/lick-safe claims (no alcohol).
- **Foreign leaders:**
  - **HICC Pet** (Chewy, Tractor Supply 4.8★/143 reviews; Walmart $24.99 for 20 ct; Chewy $17.54 for 3×6) — [Chewy](https://www.chewy.com/hicc-pet-portable-deodorizing-glove/dp/1815078), [Tractor Supply](https://www.tractorsupply.com/tsc/product/hicc-pet-20-ct-coconut-pet-glove-wipe).
  - Petkin glove wipes 30 ct — [Chewy](https://www.chewy.com/petkin-pet-glove-wipes-dog-cat/dp/1492958).
  - **The Groomi (AU)** sells Glove Wipes at A$26.99 (387 reviews) **as the consumable add-on to a hero grooming system**: a vacuum pet brush at A$89.99, a "No-Bath Bundle" at A$69.99 and a 10-in-1 system at A$349.99 — [thegroomi.com](https://thegroomi.com/), FACT 15 Nov 2026. In file 02, Groomi's oldest active ad dates from 29 Jun 2025 (~910 AU ads).
- **AliExpress (FACT):**
  - SEAMETAL 6-pc thick glove wipes: **2K+ sold, 4.9★, regular ₪28.05** (new-shopper ₪10.75) — [AliExpress](https://www.aliexpress.com/item/1005008660155779.html).
  - Others: 519, 441 and 390 sold, regular ₪21–32 per 6 pcs. Retail AliExpress is ~₪4–5 per glove, so **real margins need Alibaba/1688 wholesale or a private label** (not checked).
- **Israeli competition (FACT):**
  - Anipet: Absorb charcoal wipes, 80 pcs, ₪35 (several scents) — [Anipet feed](https://www.anipet.co.il/products.json?limit=250).
  - Pet Planet: pet wipes ₪25 (lavender, flowers, lemon); My Turf antibacterial 100 pcs ₪39 — [Pet Planet API](https://petplanet.co.il/wp-json/wc/store/v1/products?search=%D7%9E%D7%92%D7%91%D7%95%D7%A0%D7%99%D7%9D&per_page=20&orderby=popularity).
  - PetSolutions: "silicone paw cleaner" ₪69.9–99.9 (created 1 Oct 2026) and bath glove ₪44.9 — [PetSolutions feed](https://petsolutions.co.il/products.json?limit=250).
  - **No Israeli seller of the glove format was found.** Flat wipes anchor the price low (₪25–39 for 80–100 wipes).
  - Ad Library (FACT, 15 Nov 2026):
    - "מגבונים לכלבים" (~9 results): every card was a persona page ("מיכל בן דוד", started 29–30 Oct 2026) in the Pups-style funnel. There was **no wipe or glove-wipe seller**.
    - "כפפות לכלב": only an unrelated knitting ad.
    - So **zero Israeli Meta competition for wipe gloves today** — [Ad Library "מגבונים לכלבים"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%92%D7%91%D7%95%D7%A0%D7%99%D7%9D%20%D7%9C%D7%9B%D7%9C%D7%91%D7%99%D7%9D&search_type=keyword_unordered).
- **Regulation:** a liquid product with expiry. Hebrew labelling and ingredient requirements for animal grooming products were **not researched** (gap). Any "antibacterial" or "anti-itch" claim may drift into veterinary-product territory (UNVERIFIED).

**C. Tactical / front-clip no-pull harness**
- **Good vs bad (REPORTED):**
  - Rabbitgoo (Amazon): ~196K reviews, 4.5★, ~$15–26. A June 2026 tracker estimates ~6,000 units/month for one large-dog variant (ESTIMATE by tracker). **Sizing is the most common complaint** ("runs slightly small", XL fit issues); plastic buckles are criticised; escape-artist breeds need a belly strap or the escape-proof model — [ASINsight tracker](https://www.asinsight.com/report/US/dog-no-pull-harness), [Yahoo deal page](https://www.yahoo.com/entertainment/dog-harness-virtually-impossible-snake-213028109.html), [a-z-animals](https://a-z-animals.com/reviews/best-rabbitgoo-dog-harness/), [Rebarkable](https://rebarkable.com/rabbitgoo-harness-honest-review/?et_blog).
  - **What a good version needs:** a front **and** back clip, metal D-rings, 4–5 adjustment points, a padded chest, a size chart by chest girth with a video, and a free size exchange.
- **Foreign leaders:**
  - Ruffwear Front Range ~$39.95 / £40 — [comparison](https://dogsupplyfinder-com.pages.dev/compare/ruffwear-front-range-vs-julius-k9).
  - Julius-K9 IDC Powerharness $50–54.99 at Chewy (back clip) — [Chewy](https://www.chewy.com/julius-k9-idc-powerharness-dog/dp/167496).
  - Team K9 $84.99 with ad since 21 Mar 2024, and Dog Friendly Co. with 20K reviews (file 02, FACT).
  - TikTok Shop US "Pet Harnesses" is #13 in Animals & Pet Supplies by sales score (relative index) — [AfterShip](https://ecommerce.aftership.com/product-trend-list/best-animals-pet-supplies-product-to-sell-tiktok-shop-us).
- **Israeli prices (FACT, feeds 15 Nov 2026):**
  - **Petrix** (Israeli brand): no-pull harness with handle ₪149; silicone "no-pull, exclusive in Israel" harness ₪165; **full hands-free leash + harness + bag pouch set ₪289–319**; leash + collar sets ₪139–249; bag pouch ₪60; 6 poop-bag rolls ₪24.9–44.9 — [Petrix feed](https://petrix.co.il/products.json?limit=250).
  - **Hazel** (physiotechs.com, 3 products, created 23 Aug 2026): "anti-pull harness" **₪179.9** (compare-at ₪359, 45 variants), bungee leash ₪79.9, "shipping insurance + 1-year warranty" ₪19.9 — [physiotechs feed](https://physiotechs.com/products.json?limit=250).
  - **Pet Plus** (CJ dropship SKUs; "supplied within 21 business days"): FreePull™ harness ₪140–180; bungee leash ₪89; hands-free running leash ₪130 — [Pet Plus feed](https://petplusshop.com/products.json?limit=250), [shipping policy](https://petplusshop.com/policies/shipping-policy).
  - **Petit Loup** (Israeli designer brand): harnesses ₪110–150, anti-pull ₪150, matching poop-bag pouches ₪45 — [Petit Loup feed](https://petitloup.co.il/products.json?limit=250).
  - **WildPet**: Ruffwear Front Range ₪254 in the ad (₪274 for Front Range Flex in the feed), Flagline ₪337.5–374, Web Master ₪374, Ridgeline ₪594 — [WildPet feed](https://www.wildpet.co.il/products.json?limit=250).
  - **Anipet**: Ruffwear Front Range ₪249; BOBO harness ₪35–55 — [Anipet feed](https://www.anipet.co.il/products.json?limit=250).
  - **Pet Planet**: padded harness S/M/L/XL ₪79/99/120/150; Easy Walk ₪105 — [Pet Planet API](https://petplanet.co.il/wp-json/wc/store/v1/products?search=%D7%A8%D7%AA%D7%9E%D7%94&per_page=20&orderby=popularity).
  - Zylarx: "harness with protection against pulling" with a Black Friday 50% framing (feed).
- **Israeli ads (FACT, "רתמה לכלב", ~13 results):**
  - Petrix IL: 4 cards started 27 Oct and 9 Nov 2026. Video ads claim "2500+ dog owners already switched"; "free shipping from ₪229 · size exchange on us".
  - Hazel advertorial started 22 Oct 2026.
  - WildPet: catalogue ads started 8 Nov 2026.
  - Pet Plus: started 14 Nov 2026.
  - **All are recent (≤ 4 weeks), so the ads show activity, not proof of profit.**
- **AliExpress (FACT):**
  - **TRUE LOVE TLH5654** (a known Chinese brand, step-in no-pull): 2K+ sold, 4.9★, regular ~₪130 (new-shopper ₪67).
  - Tactical MOLLE no-pull: 2K+ sold, regular ~₪90; tactical Oxford waterproof: 1K+ sold, regular ~₪72; the record's 1005009651197949 listing: 464 sold, regular ~₪83.
  - Cheap vests at 3K–5K+ sold go for ₪20–36 regular.
  - Source: [AliExpress search](https://www.aliexpress.com/w/wholesale-no-pull-dog-harness.html?SortType=total_tranpro_desc).
- **Returns/shipping:** sizes run XS–XL, Hazel has 45 variants, so **stock-keeping and exchanges are the real cost**. Weight ~200–450 g (ESTIMATE).

**D. Self-cleaning slicker brush (Hertzko style)**
- **Good vs bad (REPORTED):**
  - Hertzko: ~9,700+ Amazon reviews, 4.6★ (one article; counts vary, and "61,000 pet owners" is in file 04). Pins are described as gentle, but they **can scratch if pressed hard over bony areas**. The retract button can fail, and soft pins struggle on heavy mats — [PetsRadar](https://petsradar.com/review/hertzko-self-cleaning-slicker-brush), [Hepper](https://www.hepper.com/best-slicker-brush-for-dogs/), [Business Insider](https://www.businessinsider.in/the-best-dog-brushes/the-best-dog-brush-overall/slideshow/71748889.cms).
  - **What a good version needs:** ball-tipped bent pins, a metal (not plastic) retract mechanism, and two sizes (small and large dog).
- **AliExpress (FACT):** 1005006967384548 has **10,000+ sold, 4.9★, regular ₪18.45**. A second listing has 1,000+ sold at a regular ₪20.88 — [AliExpress](https://www.aliexpress.com/item/1005006967384548.html).
- **Israel (FACT):**
  - Anipet (Ferplast and BOBO slickers): ₪39–76.9.
  - Pet Planet: brushes ₪35–49.
  - Kaufroom "slicker brush for cleaning pets" ₪59.99–79.99 (vendor `firstroost-us`).
  - Pet Plus "MistGroom™" ₪85–93.7, "FurFar™" ₪85.
  - **No advertiser** seen on "מברשת לכלב" (~16 results, all chains and supplement funnels), and file 04 found 1 ad on "מברשת לחתול".

### Inferences
- **The ball** is the best video but the weakest *brand* product. It is already a commodity in Hebrew general stores at ₪59.99–80; its real quality problems (chewing, charge port) cause bad reviews; and it is a one-off purchase. Using it as an add-on or "home alone" line item is safer than making it the hero.
- **The harness** solves the clearest and most painful problem and carries the highest ticket (₪149–199 vs ₪60–80 for the others). It is also where Israeli DTC brands are already fighting (Petrix, Hazel, Petit Loup), so it is **the proven Israeli category, but not an empty one**.
- **The wipe gloves** are the cleanest **consumable**, and no Israeli seller was found. But they are a low-ticket product with a cheap price anchor (flat wipes ₪25–39), liquid and expiry handling, and labelling homework.
- **The slicker** is a reliable, low-risk add-on with a great demo, but chains already sell the category.

### Gaps
- Amazon BSR and review counts were not read directly.
- No Alibaba/1688 MOQ or private-label quotes, and no TikTok Shop data for Israel (TikTok Shop does not operate in Israel, UNVERIFIED).
- Israeli regulation for Li-ion toys and pet grooming wipes was not confirmed.
- No return-rate data for harnesses.

---

## 3. Brand and line design: hero, add-ons, consumables, bundles, Israeli DTC examples

### Takeaway
**My recommendation is a "walks" brand**: clean, calm walks, before and after.
- **Hero:** a quality front+back-clip no-pull harness at **₪169–199**.
- **Attached add-ons:** a bungee or hands-free leash and a bag pouch.
- **Repeat consumables:** wipe gloves ("after the walk, before the sofa") and poop bags.
- **Second-wave hero for "home alone" days:** the rolling ball.
- **Cross-sell:** the slicker brush.

The rationale: the harness has the clearest value and highest AOV, and it creates natural refill moments (bags, wipes). The leading Israeli examples (Petrix, Hazel) prove Israelis buy this bundle at ₪179–319. The ball-first route is cheaper to test but sits in a commodity gadget lane.

### Cited Findings
- **Petrix** (petrix.co.il, Israeli Shopify brand; FACT):
  - 210 product variants-as-products, almost all walk gear: silicone harness ₪165, no-pull ₪149, hands-free leash sets ₪229–319, bag pouch ₪60, 6 poop-bag rolls ₪24.9–44.9.
  - Products created from Jun 2025 to Nov 2026; Judge.me reviews installed.
  - REPORTED in ads: "2500+ dog owners already switched", "size exchange on us", free shipping from ₪229.
  - **This is the closest existing Israeli model to the idea**: one material story (odour-proof silicone), sets as the main SKU, and bags as the refill — [feed](https://petrix.co.il/products.json?limit=250), [Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A8%D7%AA%D7%9E%D7%94%20%D7%9C%D7%9B%D7%9C%D7%91&search_type=keyword_unordered).
- **Hazel** (physiotechs.com; FACT):
  - Products created 23–30 Aug 2026.
  - A single-hero funnel: harness ₪179.9 + bungee leash ₪79.9 + ₪19.9 shipping insurance/warranty.
  - A 3.5-minute advertorial ad since 22 Oct 2026; "100-day trial".
  - Strength unknown: about 3 weeks of ads, no review data — [feed](https://physiotechs.com/products.json?limit=250).
- **Petit Loup** (FACT): an Israeli design-led harness brand, ₪110–150, with matching bag pouches ₪45 that create "collect the set" add-ons. 67 products; created from Oct 2025 — [feed](https://petitloup.co.il/products.json?limit=250).
- **Supplement-funnel brands** are the Israeli "consumable" DTC players (subscription-style, persona ads): Pups, Woof, VetCalm, Doggy. Doggy, for example, has salmon oil at ₪99 (compare ₪200), a probiotic snack at ₪199.9 and "shipping insurance" at ₪19.9, products from Sep–Oct 2026 — [Doggy feed](https://try-doggy.com/products.json?limit=250). Census file: Pups had 12 ads and Woof 7 ads.
- **Arava Dead Sea Pet SPA** (arava-psp.com) advertises Dead Sea skin-care for itchy dogs (ad from 8 Nov 2026). It is an Israeli-origin pet consumable brand; not researched further.
- **Groomi (AU)** is the clearest foreign template for "hero + consumable": the vacuum brush is the hero and glove wipes are the add-on and refill (A$26.99), sold through bundles (A$69.99–199.99) — [thegroomi.com](https://thegroomi.com/).
- **Food/treats are regulated (FACT/REPORTED):**
  - Animal-origin food (meat or fish treats) needs **importer registration and a prior import permit** from the Veterinary Services; "do not ship to Israel without a prior import permit".
  - Personal import of pet food has its own procedure (Oct 2021), with some food types excluded.
  - Sources: [gov.il animal-derived food import](https://www.gov.il/he/service/animal-derived-food-product-importation), [importer registration](https://www.gov.il/he/service/animal-derived-food-importer-registration), [personal pet-food import procedure PDF](https://www.gov.il/BlobFolder/policy/personal-pet-import/he/import_import-of-food-for-animals_yevu-mazon-hayot-mahmad.pdf).
  - **So treats and supplements should not be part of a dropshipped line.** Source them from a local Israeli distributor if wanted.
- **Consumable price anchors in Israel (FACT):**
  - poop bags: PetEx 16 rolls ₪32 and dispenser ₪12.9 (Anipet); GreenPaw 360 bags ₪35 (WildPet); Petrix 6 rolls ₪24.9–44.9
  - flat wipes: ₪25–39 per 80–100
  - AliExpress biodegradable bags: 10,000+ sold, regular ~₪14
  - paw balm: AliExpress mostly under 300 sold

**Suggested line and Israeli price points (ESTIMATE; one-line cost vs price)**

| Item | Role | Suggested price | Landed cost guess (AliExpress regular, single unit) |
|---|---|---|---|
| Front+back-clip no-pull harness (metal D-rings, 5 sizes) | **HERO** | ₪169–199 | ₪70–130 (TRUE LOVE/tactical grade). Private-label wholesale would be lower (not quoted) |
| Bungee / hands-free leash | Attach | ₪79–99 | ₪20–40 (UNVERIFIED; not searched) |
| Bag pouch + 8 rolls of bags | Attach + refill | ₪49 / refill ₪29–39 | bags ~₪14 for a 10K-sold listing |
| Wipe gloves, 3×6 pack ("after-walk") | **Consumable** | ₪59–69 per 3-pack; subscribe & save | ~₪84 at AliExpress retail (₪28 per 6): **needs wholesale or it loses money** |
| Self-cleaning slicker brush | Cross-sell | ₪69–89 | ₪18–21 |
| Rolling ball, dog-grade | 2nd hero ("home alone") | ₪89–119 (or 2-pack ₪149) | ₪15–32 |
| Silicone paw-cleaner cup (winter) | Seasonal add-on | ₪69–89 (PetSolutions ₪69.9–99.9) | ₪18–42 (3K+ sold listing, regular ~₪42) |

**Bundles:**
- **"Walk Kit"**: harness + leash + pouch + bags, ₪249–279. Anchor: Petrix full set ₪289–319.
- **"Clean Dog / Winter Kit"**: 2× glove-wipe packs + paw cup + slicker, ₪149–169.
- **"New Puppy Kit"**: small harness + ball + slicker + bags, ₪249–299.
- **"Home Alone Kit"**: ball + snuffle/lick mat, ₪139–159 (PetSolutions sells lick and enrichment items at ₪109.9–139.9).

### Inferences
- Consumables in this category are **thin**. Poop bags and wipes are cheap in Israeli chains, so they work as **AOV and retention glue** (refill reminder emails or WhatsApp, a "free bags for life" hook), not as a profit engine.
- The real repeat buyers are multi-dog homes and gift buyers. Expect 1–2 refill orders per customer per year (ASSUMPTION, consistent with file 09's fountain-filter logic).
- To beat Petrix and Hazel, the brand needs **local stock of the hero in Israel**. It should offer 2–4-day delivery and free size exchange, against Pet Plus's 21 business days and the census's 7–18 days for dropshippers, and run **better proof creatives** (UGC from Israeli dogs, before/after pulling).

### Gaps
- No sales or review counts for Petrix, Hazel or Petit Loup (Judge.me counts not read).
- No CPMs or CPAs for Israeli pet ads.
- No wholesale quotes.
- Leash/AliExpress prices for bungee and hands-free leashes not checked.

---

## 4. Verdict, failure modes and 5 cheap validation steps

### Takeaway
**A Hebrew dog niche brand is a reasonable bet, better than a general store, but only as a *quality + local stock + exchange-guarantee* brand, not as a dropship gadget shop.**
- The market is small (~640k registered dogs), but owners spend ₪4–8k a year per dog.
- Specialist DTC competition exists but is young: every competing ad seen started between 22 Oct and 14 Nov 2026.
- **Hero first: the no-pull harness**, because it has the clearest pain, the highest ticket and proven Israeli willingness to pay ₪149–319. The ball is the fastest cheap *test creative*, and wipe gloves are the retention product.
- If the partners would rather avoid sizing logistics, the fallback is a **"clean dog" line**: the slicker brush as the demo hero, plus glove wipes and the winter paw cup. It is lower risk, has no Israeli advertiser yet, and carries a lower ticket.

### Cited Findings
- Competing harness ads are all 1–4 weeks old: Petrix 27 Oct, Hazel 22 Oct, WildPet 8 Nov, Pet Plus 14 Nov 2026 (FACT, [Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A8%D7%AA%D7%9E%D7%94%20%D7%9C%D7%9B%D7%9C%D7%91&search_type=keyword_unordered)).
- Ball competitors already sell at ₪59.99–80 (FACT, feeds above), while AliExpress itself advertises in Israel (census file).
- Sizing is the #1 harness complaint abroad (REPORTED, Rabbitgoo sources above). Petrix advertises "size exchange on us" (FACT).

### What could make it fail
- **Harness returns and exchanges.** Five sizes × colours means dead stock; dropship exchanges take 3–6 weeks round trip.
- **Ad economics.** Small audience, advertorial-heavy competitors, Black Friday CPMs now. A ₪179 ticket with ~₪80–100 gross margin leaves little room for a high CPA (ESTIMATE).
- **Quality blowback.** Chewed balls and dead batteries, plastic buckles snapping, wipes drying out or irritating. In a small market, bad reviews spread in dog groups.
- **Copycats.** The same AliExpress items appear in general stores within weeks at "50% off" (census file).
- **Regulatory traps.** Treats, supplements and medical/"anti-itch" claims; Li-ion import rules (unverified); Hebrew labelling for wipes (unverified).
- **Delivery expectations.** Chains deliver in 1–4 days (WildPet 2 days in the centre).

### 5 cheapest validation steps
1. **Samples (about ₪400–600):** 2 harness grades (TRUE LOVE step-in vs tactical front-clip), 2 ball models, 2 glove-wipe brands, 1 slicker. Test on a small dog and on a big puller or chewer. Check stitching, D-rings, buckles, glove moisture after a week open, and scent. Film the tests; this becomes the first UGC.
2. **Manual Ad Library check in a normal browser** (5 min per term): רתמה לכלב, רתמה נגד משיכה, כדור לכלב, כפפות ניקוי לכלב, מגבונים לכלב, ניקוי כפות. Note Petrix and Hazel start dates and **re-check in 3–4 weeks**: ads still running after 6–8 weeks are the best cheap profit signal.
3. **Fake-door or pre-order landing page plus a ₪1,000–1,500 Meta test over 5–7 days.** Run 3 creatives each for harness (pulling before/after), ball (home-alone) and clean-dog (muddy paws). Compare CTR, cost per add-to-cart and email/WhatsApp sign-ups, and pick the hero on data.
4. **Ask owners directly:** a poll in 2–3 Israeli dog Facebook/WhatsApp groups plus 15–20 owners at a dog park. Rank 6 pains (pulling, shedding, muddy paws, boredom alone, bathing, smell) and the price they'd pay for a harness kit vs a ball.
5. **Sourcing quote and size-exchange plan:** ask 2–3 Alibaba harness factories for MOQ and private-label prices with metal hardware, and price holding 30–60 harnesses in Israel (local 3PL or home stock) for 2–4-day delivery and free exchange. Pull Google Trends IL for רתמה לכלב / כדור לכלב / מגבונים לכלב manually.

### Inferences
- If step 3 shows the ball creative with a much cheaper add-to-cart than the harness, flip the order: start with "home alone" (ball + enrichment) and add walk gear second. Keep the brand name broad enough to cover both, e.g. a "daily life with your dog" brand rather than "harness brand".

### Gaps
- No profitability data for any Israeli competitor. Ad presence only.
- Black Friday (Nov 2026) distorts both ad volume and prices seen this week.
