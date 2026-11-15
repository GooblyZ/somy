# Lens 02: ads_abroad (long-running Meta ads in the US, UK and Australia)

Date of research: 2026-11-15. Lens: `ads_abroad`. JSON: `02_ads_abroad.json` (23 products, each with ali_url and a checked image_url).

## Method (what was actually done)

- **Meta Ad Library, no login.** I used headless Chromium with a fresh browser context for every query. The URL pattern was `facebook.com/ads/library/?active_status=active&ad_type=all&country=<US|GB|AU|IL>&q=<term>&search_type=keyword_unordered`. Each page was scrolled about 5 times, so roughly 25–30 ad cards were parsed per query.
  - From each card I took the start date, the advertiser, the landing domain, the copy, and "N ads use this creative".
  - I ran about 190 queries in total:
    - 28 generic DTC phrases (e.g. "free shipping today", "50% off today", "as seen on TikTok", "problem solved", "gadget", "game changer", "must have", "best gift", "sold out", "back in stock", "money-back guarantee", "lifetime warranty", "hurry limited stock") plus category words (kitchen gadget, cleaning hack, car accessory, garden tool, posture corrector, sleep better, toddler, dog/cat owners, back/knee pain, home organization, camping, travel). Each was run in US, GB and AU.
    - 20 product-type words (rechargeable, portable, magnetic, waterproof, foot pain, orthopedic, suction hooks, car organizer, dog harness, knife sharpener, cordless, mop, solar lights, phone holder, kids toy, baby must have, pet hair, window cleaning, shower…), each in US, GB and AU.
    - About 35 brand-verification queries.
    - 35 Israel (IL) queries in Hebrew.
  - About 30% of first loads came back empty, which is a false zero. Every query was retried once in a fresh context. A genuine zero shows the text "No ads match your search criteria", and I only report a zero when that text appeared.
- **How to read the numbers.**
  - "Oldest active" is the oldest "Started running on" date among the sampled cards for that brand. These ads are still active today, so the date means continuous running time. It is a lower bound: an older ad may exist outside the sample.
  - "~N ads match X" is the Ad Library's own result count for a keyword search on the brand name in that country. It counts ads that contain the word, so it can include a few other advertisers. I give the share of the sample that belonged to the brand to show this.
  - Days are counted to 2026-11-15.
- **Stores.** I read Shopify `/products.json?limit=250` and `/collections/all?sort_by=best-selling` for 25 landing stores to find the hero product, price and review counts. Two stores were not readable:
  - shop.treatmedy.com is a Funnelish funnel, not Shopify.
  - smiletherapy.co.uk returned an upstream error.
- **AliExpress.** I searched with headless Chromium, sorted by orders, with the IL/ILS cookie, and took title, price, "sold" and image from the result cards. Image URLs were cut back to the base `.jpg`/`.png`, and all 23 returned HTTP 200 on 2026-11-15.
  - **Price note:** "₪3.59" is AliExpress's new-shopper promo. Where the card showed "₪X saved", the JSON `ali_price_ils` is promo + saved, which is the regular price. Where it showed only a strikethrough price, I used that strikethrough price, and it may be inflated.
- **Public "winning products" roundups** were used only as leads:
  - TrendTrack, "The Best Products on Meta for Dropshipping in 2026": https://www.trendtrack.io/blog-post/the-best-products-on-meta-for-dropshipping-in-2026. It gave the Roha Home suction-hooks lead (it reports "running 572 days").
  - Sell The Trend's monthly winners archive: https://www.sellthetrend.com/blog/winning-product-friday-episode-291. It reports revenue estimates only, with no ad data, and none of its items were used without verification.
  - Searches for Minea, Pipiads and Dropship.io 2026 lists returned only vendor how-to pages with no verifiable product-level data, so I found no usable leads there.

## Findings per product (FACT = seen by me in the Ad Library, store or AliExpress on 2026-11-15; REPORTED = advertiser's or third party's claim)

### 1. Electric mason-jar vacuum sealer (משאבת ואקום לצנצנות): Mason Genie
- FACT: the oldest active ad started Jul 27, 2024, which is about 841 days.
- FACT: ~680 AU and ~790 US active ads match "Mason Genie". In the sample, 20 of 30 were the brand's own and the rest were creator pages ("Food Storage Tips", "Saving Food With Sally").
- FACT: the store masongenie.com sells the kit for $49.99. It has 41 products and a sub-brand line (Bread Genie, Vacuum Genie, Genie Dehydrator).
- AliExpress: cordless version, 1,000+ sold, ₪111.39 (item 1005006994621457).
- Israel: 0 IL ads for "וואקום לצנצנות" or "מטהר צנצנות".

### 2. Streak-free "just water" XXL microfiber cloth (מטלית "רק מים"): KoalaCloth (AU)
- FACT: the oldest active ad started Sep 16, 2025 (about 425 days). ~920 AU ads match the name, and 26 of 30 in the sample were the brand's own plus creator whitelisting.
- FACT: the store koalacloth-au.com shows 3,143 reviews on the XXL bundle. The single XXL is A$49.95 and bundles start at A$79.95.
- AliExpress: 8K+ sold, ₪10.27.
- Israel: ~20 IL ads for "מטלית ניקוי", all from general retailers.

### 3. Rolling knife sharpener with magnetic angle block (משחיז סכינים מתגלגל)
- FACT: several brands are running in parallel:
  - Tumbler (tumblerware.com, US): oldest Oct 11, 2025, 17 of 28 sampled.
  - Kimbo Rolling Sharpener (AU): oldest Dec 5, 2025.
  - HORL, active in all three countries.
  - The keyword "knife sharpener" matches ~1,700 US and ~1,600 AU active ads.
- AliExpress: 10,000+ sold.
- Israel: an early competitor appeared. "בשלנים ממליצים" (laven-il.com) has run 5 butcher-testimonial ads for a "ReSharp" rolling sharpener since Oct 19, 2026.

### 4. Mini brushless turbo jet blower (מפוח טורבו-ג׳ט): TurboJet Oz (AU)
- FACT: the oldest active ad started Aug 10, 2025 (about 462 days). ~480 AU ads match "TurboJet".
- FACT: the store sells TurboJet PRO at A$174.99 (was A$269.99) and has spin-offs (Vac, Mini, spare battery).
- AliExpress: the same type of product has 50,000+ sold at ₪69.52.
- Israel: ~24 IL ads for "מפוח טורבו", but these are garden turbo blowers sold inside tool bundles (taktakatstore.com, WhatsApp sellers, 199–900 ₪). The palm-size jet fan did not appear as its own DTC product.

### 5. Pregnancy seat-belt adjuster (מתאם חגורת בטיחות להריון): MimiBelt
- FACT: the oldest active ad started Dec 18, 2024 (about 697 days). ~620 US and ~550 GB ads match the name, and 28 of 28 in the sample were the brand's own.
- FACT: the store mimibelt.com sells it for $35.99 and shows 1,086 ratings.
- AliExpress: 500+ sold, ₪11.11.
- Israel: 0 ads.

### 6. Car door-handle scratch protectors (מגני ידית לרכב): Pinauto
- FACT: GB ads have run since Dec 2, 2024 (about 713 days), localized into Irish, Italian, French and Japanese. ~310 GB and ~100 US ads match "Pinauto".
- AliExpress: 3,000+ sold, ₪3.56.
- Israel: 0 ads.

### 7. Kids LED drawing projector (מקרן ציור לילדים): Tiny Dreams UK
- FACT: drawing-lamp ads have run since May 19, 2025 (about 545 days) and Jul 20, 2025.
- The store (tiny-dreams.uk) is a general kids store with 1,397 products. Searching the store name in GB returned "No ads match", so the evidence is the two sampled ads only.
- AliExpress: 500+ sold.
- Israel: 0 ads.

### 8. Ultrasonic tooth tartar cleaner (מנקה אבנית אולטרסוני): SmileTherapy (UK)
- FACT: ads active since Sep 9, 2024 (about 797 days). ~1,900 GB ads match the name, and 20 of 29 in the sample were the brand's own.
- REPORTED (in the ad): "Over 100,000 happy customers".
- AliExpress: 711 sold, ₪29.77.
- Israel: ~130 ads for "אבנית שיניים", but they are dental clinics and pet-dental supplements. No DTC device seller was seen.

### 9. Bunion corrector (מיישר בוהן): Treatmedy BunionFix
- FACT: the oldest active US ad started Apr 5, 2024 (about 954 days), and an AU ad has run since Aug 7, 2024. ~620 US ads match the name, and 23 of 30 in the sample were the brand's own plus "Blane Schilling, MD with Treatmedy".
- AliExpress: adjustable corrector 1,000+ sold; silicone separators 3–5K+ sold.
- Israel: 0 ads for "בוהן עקומה". I did not check the term "הלוקס ולגוס".

### 10. Instant posture corrector / waist-snatching brace (מתקן יציבה): Axzenia and Corecare
- FACT: Axzenia's oldest AU ad started Nov 8, 2023 (about 1,103 days), and its "Instant Posture Corrector… Snatches Waist" ad started Oct 31, 2024.
- FACT: Corecare/TryCorecare's oldest ad started Jan 26, 2026, with 24 of 30 AU ads in the sample. The store price is $64.90–97.50.
- AliExpress: 10,000+ sold, ₪17.44.
- Israel: ~65 ads for "מתקן יציבה", mostly advertorial funnels.

### 11. Heated vibrating knee massager (מעסה ברכיים): Levide
- FACT: the oldest ad started Jan 5, 2026 (about 314 days). ~720 US and ~690 GB ads match the name, and 29 of 29 in the sample were the brand's own.
- REPORTED (in the ad): "150,000+ customers".
- FACT: the store sells the 4-in-1 device at $199.99 and the Knee Companion 2.0 from $99.99.
- AliExpress: 3,000+ sold, ₪21.9.
- Israel: about 1 ad.

### 12. Orthotic arch-support insoles (מדרסים): Stepprs and OrthoFlexx
- FACT: Stepprs' oldest ad started Jul 29, 2025, with ~350 AU and ~340 GB ads matching the name.
- FACT: OrthoFlexx's oldest ad started Oct 2, 2025, with ~550 AU ads.
- FACT: Peak Footwear has run 19 versions of one ad since Aug 18, 2025.
- AliExpress: 5K+ sold.
- Israel: crowded, with ~530 ads for "מדרסים" (URIEL ישראל and custom-orthotics clinics).

### 13. Arch-support "cloud" slides and clogs (כפכפי ענן): Snuggi (AU) and The Cloudies (US)
- FACT: Snuggi's oldest ad started Apr 30, 2025 (about 564 days). ~920 AU ads match the name, all 16 sampled were its own, and it runs buy-one-get-one offers. Prices are A$59.95–79.95.
- FACT: Cloudies has run since Mar 30, 2025.
- AliExpress: 10K+ sold.
- Israel: about 6 ads (Sahara Shop, since Oct 2026).

### 14. No-pull tactical dog harness (רתמת נו-פול): Team K9 and Dog Friendly Co.
- FACT: Team K9's oldest ad started Mar 21, 2024 (about 969 days). The harness listing has 2,253 reviews, the store 11,097 reviews, and the harness costs $84.99.
- FACT: Dog Friendly Co. has run 19 versions of one harness ad since Jun 23, 2025, and shows 20,047 "verified 5-star reviews".
- FACT: DoggyKings (GB) has run since Oct 31, 2024.
- AliExpress: sales are fragmented, at 300–600 per listing.
- Israel: about 13 ads, all from October 2026.

### 15. Quiet cat hair trimmer (מכונת תספורת שקטה לחתול): Belvedir
- FACT: the oldest ad started Jun 17, 2025 (about 516 days). ~75 GB and ~67 US ads match the name, nearly all its own.
- REPORTED (in the ad): "4.9 by 40,000+ cat parents".
- FACT: the trimmer costs $69.99.
- AliExpress: the quiet clipper has 1,000+ sold.
- Israel: 0 ads for "מכונת תספורת לחתול" or "מכונת תספורת לכלב".

### 16. No-rinse pet wipe gloves (כפפות-מגבון לכלבים): The Groomi (AU)
- FACT: the oldest ad started Jun 29, 2025. ~910 AU ads match the name, and 26 of 28 in the sample were its own. The ad says "31,157+ Love This Hack".
- FACT: the Glove Wipes listing has 387 reviews and costs A$26.99.
- AliExpress: 2K+ sold.
- Israel: not checked with the exact Hebrew term.

### 17. Automatic rolling dog ball with tail (כדור מתגלגל לכלב): Pets Dreams UK
- FACT: the store's oldest ad started Sep 19, 2023. The rolling-ball ad has run since Nov 20, 2024 (about 725 days).
- FACT: ~560 GB ads match the name, and the product is listed first in the store's best-sellers at £7.95.
- AliExpress: 10,000–20K+ sold.
- Israel: about 16 dog-toy ads, none for this product.

### 18. Handheld pressurized steam cleaner (מכשיר קיטור ידני)
- FACT: AthVora's oldest GB ad started Dec 5, 2025. Several other GB sellers are also active (Iviory, H2O).
- AliExpress: 10,000+ sold, ₪152.
- Israel: crowded, with about 40 ads (banana-sale.com since Oct 10, 2026, plus Izzy and Genius).

### 19. AI translator earbuds (אוזניות מתרגמות)
- FACT: Aviorra VerbaBuds has run since Feb 13, 2025, with 5 versions. A Rowgins translator has run in the US since Aug 13, 2025. VerbaBuds costs $69.95.
- AliExpress: the HTC NE25 has 3K+ sold.
- Israel: present. Raven IL (try-ravenil.com) sells 3 pairs for 438 ₪ and has run ads since Apr 2026.

### 20. No-drill vacuum suction hooks (ווים בוואקום): Roha Home
- FACT: ~80 GB ads match the name. The oldest seen started Feb 16, 2026.
- REPORTED by TrendTrack: one Roha ad ran 572 days with 5.1M reach.
- FACT: the store sells 4 hooks for $44.09.
- AliExpress: 10–20K+ sold.
- Israel: 0 ads.

### 21. Ergonomic cervical "cloud" pillow (כרית צווארית): Mellow Sleep CloudAlign
- FACT: the US whitelisted creator ads (a chiropractor persona and a customer persona) started Jan 26, 2026, with 4–24 versions each.
- FACT: the store's top product shows 34,672 reviews, and the pillow costs $49.99.
- AliExpress: 10,000+ sold.
- Israel: crowded, with ~180 ads for "כרית אורתופדית" (URIEL, Orthopedly since Mar 2024).

### 22. Wireless stick-on car ambient LEDs (תאורת אווירה לרכב): GlowRide
- FACT: ad active since Apr 28, 2025 (about 566 days).
- REPORTED by the store: "300 million views".
- FACT: the kit costs $149.99.
- AliExpress: 10,000+ sold.
- Israel: ~33 ads, mostly installation shops.

### 23. Baby head-protector backpack pillow (תיק-כרית מגן ראש): BabiMate
- FACT: ad active since Aug 13, 2024 (about 824 days). The BabiGuard 2-pack costs $50.
- AliExpress: 20K+ sold.
- Israel: about 6 ads from small baby shops.

### Strong long-running leads I left out on purpose
- **Bumzzy butt shaver (bumzzy.com):** oldest ad Sep 24, 2025, ~780 ads, 1,989 reviews. Left out because the product is patented and too close to the "shaver" family already shown.
- **Must Have Ideas UK "Bye Bye Bobbles" fabric shaver:** ads since Nov 2025. Left out because it is the lint-remover family, which was already shown.
- **Lucent Globe laundry detergent sheets:** 8 ads with 25 versions since Feb 2026. Left out because it is near the washing-tablets exclusion and is a chemical product.
- **Already shown to the partners:** KittySpout (cat fountain), Loungon (wireless CarPlay), toddla.co (busy board), Snoozeband (sleep headphones), Bright Legs and Everstride (compression socks), Lumina Pro (TV backlight).
- **Brands without a clear product:** FlexBuddy stretching device (since Jun 2025), Pulsio TENS pod (since Mar 2025), Health & Science "FisioRest" (~860 US ads, but the product was not identifiable from the ads).

## Gaps and caveats
- Ad counts are keyword-match counts, not exact counts per page. The Ad Library also has no spend or reach data for US/AU commercial ads, so I have no sales numbers for these stores, only signals of how long ads run and how many there are.
- Israeli "0 ads" results depend on the exact Hebrew wording I chose. Each zero was a genuine "No ads match", but other phrasings may exist, so treat them as unverified.
- The Ad Library blocked or failed the first load for about 30% of queries; every one was retried, and 5 brand queries still came back empty.
- AliExpress prices are promo-dependent (see the price note above). Review counts on AliExpress were not collected; only "sold" figures were.
- Two store checks failed: Treatmedy (Funnelish funnel) and SmileTherapy (upstream error). AthVora's landing domain was not captured.

## Top 5 for Israel and why
1. **Pregnancy seat-belt adjuster (MimiBelt type).**
   - Evidence: about 2 years of continuous ads, ~550–620 active ads per country, 1,086 ratings at $35.99.
   - Israel: zero Israeli advertisers, and Israel has the highest birth rate in the OECD, so there is a large pool of pregnant women and gift-buyers.
   - Cost and demo: ₪11 on AliExpress, a 5-second demo, and it fits baby-shower and gift angles.
   - Caveat: word the copy carefully, with no unproven safety claims.
2. **Electric mason-jar vacuum sealer (Mason Genie type).**
   - Evidence: the longest runner found (about 841 days), ~700–800 ads in each of US and AU, and a brand that grew into a product line.
   - Israel: zero ads, and it is easy to demo.
   - Caveat: sell it with jars or lids, because wide-mouth mason jars are less common in Israel.
3. **Rolling knife sharpener.**
   - Evidence: three or more brands advertising for 10+ months in US, AU and UK, and 10,000+ sold on AliExpress.
   - Israel: an Israeli copycat ("ReSharp", laven-il.com) only started on Oct 19, 2026, so the window is open but closing. Move fast and target men and gift buyers before the holidays.
4. **Heated knee massager (Levide type).**
   - Evidence: ~700 active ads per country after 10+ months, and a $99–199 price point abroad.
   - Israel: essentially no Israeli ads, and the 50+ Facebook audience is large and buys gifts for parents.
5. **Bunion corrector (Treatmedy type).**
   - Evidence: ads for about 954 days, the longest pain-relief runner in the sample, and ~620 US ads.
   - Israel: zero ads.
   - Cost and demo: costs only a few shekels, it is a clear women-40+ problem, and before/after visuals are easy to make.
   - Runners-up: the KoalaCloth-type streak-free cloth (cheap, rising, no Israeli competitor) and the ultrasonic tooth cleaner (about 797 days and ~1,900 UK ads, but it carries medical-device and claim risk).

Crowded in Israel already, so avoid unless you have a clear angle: insoles, orthopedic and cervical pillows, handheld steam cleaners, translator earbuds (Raven IL), and turbo blowers sold in tool bundles.
