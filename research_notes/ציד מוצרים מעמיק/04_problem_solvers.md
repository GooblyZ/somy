# Problem solvers: products people say "actually solved it" (2026-11-15)

Lens: `problem_solvers`. JSON: `04_problem_solvers.json` (24 products, every one with an AliExpress URL and an image URL; all 24 image URLs returned HTTP 200 on 2026-11-15).

## How was the evidence gathered, and how reliable is it?

### Takeaway
I could not read Reddit directly. old.reddit.com, the reddit.com JSON API and a mirror all returned 403 or 410, and I did not log in or bypass anything. The repetition signal therefore comes from secondary aggregators that quote Reddit threads, from 2025–2026 sales roundups (NBC Select, TODAY, BuzzFeed), from review press, from AliExpress order-sorted search (scraped 2026-11-15 with IL region and ILS) and from Meta Ad Library (country IL, Hebrew keywords, active ads, 2026-11-15).

### Cited Findings
- Reddit-quoting roundup with 45 "cheap products raved about on Reddit". It is the main repetition source for bidet, motion lights, TubShroom, sheet straps, toilet night light, squat stool, magnetic door screen, nasal strips and the mini fan. It is old: updated Oct 2022 — [Mic](https://www.mic.com/impact/45-cheap-products-that-get-raved-about-the-most-on-reddit-81068714)
- r/AskReddit "under $50 most significant impact" thread, Jan 2024: silicone earplugs for a light sleeper, a silicone pot strainer, a foam roller, a buckwheat pillow — [Upworthy](https://scoop.upworthy.com/25-noteworthy-purchases-under-50-that-have-significantly-impacted-peoples-lives)
- Under-$50 Reddit roundups in 2025 repeat water flossers, blackout curtains and sleep masks — [Upworthy 2025](https://www.upworthy.com/frugal-people-say-these-under-50-dollar-upgrades-saved-them-more-money-than-expected-ex1/); [Comic Sands](https://www.comicsands.com/purchases-under-drastically-improved-lives)
- NBC Select readers' 21 bestselling Amazon products of 2025 (Dec 17 2025). The physical, non-cosmetic entries are AirTags 4-pack at #3, Fyy travel cable organizer at #5 ($9.85) and Caretras bunion corrector at #12 ($29.98) — [NBC Select](https://www.nbcnews.com/select/shopping/bestselling-amazon-products-2025-rcna249695)
- TODAY "Amazon customers loved", Jul 29 2026: motion-sensor stair lights 8-pack ($19.99, 2,424 reviews), magnetic remote holder, microwave cleaner (6,699 reviews). Terro ant bait was "bought 100,000+ times in past month" (a consumable, so excluded) — [TODAY](https://www.today.com/shop/amazon-customer-loved-july-2026-rcna588395)
- BuzzFeed "59 problem-solving products", Oct 21 2026. The #1 item is the Glare Guard sun-visor extender — [BuzzFeed](https://www.buzzfeed.com/maitlandquitmeyer/problem-solving-products-that-require-minimal-effort-2026)
- Babylist 2025 survey of about 11k parents. Its "game changers" are mostly big-ticket items (Snoo, wearable pumps) that do not fit this store — [Babylist](https://www.babylist.com/hello-baby/game-changer-baby-products)

### Inferences
- The same items show up across independent sources from 2021 to 2026: motion-sensor lights, bidets, drain hair catchers, sheet straps, earplugs, sleep masks, water flossers and small fans. That repetition means durable demand, but none of them is new or hyped. They are evergreen problem-solvers.
- The newest 2025–2026 signals are the cable organizer and tracker (travel), the bunion corrector (women 40+) and the visor extender (driving glare).

### Gaps
- I have no first-hand Reddit thread counts or upvotes because every Reddit route was blocked. The Strategist and Wirecutter 2025 year-end lists were not reachable: the mirrors only linked to nytimes.com and nymag.
- I found no YouTube "gadgets that actually work 2026" titles. Search returned only blogs.
- I skipped Kickstarter and Indiegogo; nothing small and retail-ready surfaced in my searches.
- I recorded no Israeli retail prices. I did not check Zap or KSP for this lens.

## What was found per product?

### Takeaway
There are 24 products in the JSON. I dropped four candidates for weak evidence or an irrelevant AliExpress match: the 360 spill-proof toddler cup, the electric baby nail trimmer, the dog lick mat and the vacuum roller cleaner. Meta zeros marked "explicit 0" mean the page said "No ads match". Zeros without that message were re-run with longer waits. Even so, a zero may be a false zero (unverified), especially off-season.

### Cited Findings
How to read each row: Ali = AliExpress order-sorted top listing on 2026-11-15. Where the card showed a ₪3.59 new-shopper promo, the JSON `ali_price_ils` holds the card's pre-promo price instead.

1. **Rechargeable motion-sensor lights.** Ali 100K+ sold at ₪7.54; a cabinet bar has 20K+ sold. On Reddit people say they prevented "stubbed toes or falls" ([Mic](https://www.mic.com/impact/45-cheap-products-that-get-raved-about-the-most-on-reddit-81068714)), and the TODAY Jul 2026 list repeats them ([TODAY](https://www.today.com/shop/amazon-customer-loved-july-2026-rcna588395)). Meta IL: "חיישן תנועה" explicit 0. Strength 5.
2. **Toilet-bowl motion night light.** Chunace has 9,000+ five-star reviews and is praised on Reddit ([Mic](https://www.mic.com/impact/45-cheap-products-that-get-raved-about-the-most-on-reddit-81068714)). Ali 1K+. Meta IL explicit 0.
3. **Slim non-electric bidet.** Reddit: "never going back" ([Mic](https://www.mic.com/impact/45-cheap-products-that-get-raved-about-the-most-on-reddit-81068714)). ESTIMATE: about 121,800 Amazon US units in Jul 2026 ([ASINSight](https://www.asinsight.com/market-analysis/US/bidet)). Counter-signal: US online revenue across tracked retailers fell 20–50% in 2025 ([Grips](https://gripsintelligence.com/insights/industries/home-garden/bidet)). Ali SAMODRA 5,000+ at ₪108.57. Meta IL "בידה" has about 23 active ads from bathroom retailers, so the category is established in Israel.
4. **Loop-style high-fidelity earplugs.** Loop claims 14M+ customers ([Loop](https://www.loopearplugs.com/pages/noise-sensitivity)). ESTIMATE: Loop Quiet 2 and Experience 2 sell about 10k per month each on Amazon US ([ASINSight](https://www.asinsight.com/report/US/loop-earplugs)). Ali 1,000+ at ₪4.92; generic silicone earplugs 10,000+. Meta IL "אטמי אוזניים" has about 65 ads, mostly hearing clinics.
5. **3D contoured blackout sleep mask.** Ali 10,000+, flagged "Top selling". It is a passive mask, so it does not overlap the excluded heated mask or sleep headphones. Meta IL explicit 0.
6. **Bed-sheet straps.** Reddit: "sleep is undisturbed" ([Mic](https://www.mic.com/impact/45-cheap-products-that-get-raved-about-the-most-on-reddit-81068714)). Roundups cite 34,000+ five-star ratings; that figure is a search snippet only. Ali 10,000+. Meta IL about 5 ads.
7. **Shower drain hair catcher.** The TubShroom praise comes from the same Reddit roundup ([Mic](https://www.mic.com/impact/45-cheap-products-that-get-raved-about-the-most-on-reddit-81068714)). Ali 2K+. Meta: none found.
8. **Toilet squat stool.** Squatty Potty is rated 4.7 ([Mic](https://www.mic.com/impact/45-cheap-products-that-get-raved-about-the-most-on-reddit-81068714)). Ali 1,000+, but the pricing is suspicious: ₪6.74 promo against a ₪90.47 list price. Meta IL explicit 0.
9. **Bug-bite suction tool.** It has 32,000+ Amazon reviews ([Yahoo](https://au.news.yahoo.com/bug-bite-suction-tool-review-160958654.html)). Consumer Reports found it works if used immediately ([CR](https://www.consumerreports.org/health/medical-conditions/bug-bite-thing-for-mosquito-bites-review-a1106306834)). Ali 10,000+. Meta IL "עקיצות" has about 36 ads, mostly creams; I saw no device ads.
10. **Bladeless neck fan.** JISULIFE has 9,800+ five-star reviews and is called an "Amazon bestseller" ([E! Online](https://www.eonline.com/ca/news/1334339/this-affordable-neck-fan-with-9-800-five-star-amazon-reviews-is-a-summer-heat-wave-essential)) and "TikTok-viral" ([Hello!](https://www.hellomagazine.com/shopping/843477/viral-neck-fan-amazon-sale)). Ali 10,000+. Meta IL explicit 0 in November, which is off-season.
11. **Clip-on stroller fan.** Ali 10K+. Meta IL "מאוורר לעגלה" has about 6 ads (mommy.mor, SmartCase).
12. **Electric baby nasal aspirator.** NoseFrida Electric has 1,660 reviews; GROWNSY is described as having "18k reviews" in affiliate roundups ([ShopSavvy](https://shopsavvy.com/reviews-tldr/nosefrida-electric-nasal-aspirator-for-babies-and-toddlers)). Ali 1,000+ at ₪49.81. Meta IL "שואב אף" has about 110 ads, so it is crowded.
13. **Travel cable organizer.** It is #5 in the NBC Select 2025 list ([NBC](https://www.nbcnews.com/select/shopping/bestselling-amazon-products-2025-rcna249695)). Ali 5,000+. Meta IL explicit 0.
14. **Wallet tracker card (Find My).** AirTags are #3 in the NBC Select 2025 list ([NBC](https://www.nbcnews.com/select/shopping/bestselling-amazon-products-2025-rcna249695)). Ali 3K+ (iOS) and 6K+ (Android). Meta IL "מכשיר איתור" explicit 0.
15. **Cordless water flosser.** Reddit under-$50 threads repeat it ([Upworthy](https://www.upworthy.com/frugal-people-say-these-under-50-dollar-upgrades-saved-them-more-money-than-expected-ex1/)). Ali D52 10,000+ at ₪52.69. Meta IL "מברשת מים" has about 220 ads, a mix of pressure washers and oral care.
16. **Japanese nylon exfoliating towel.** Salux won a Japanese invention award and costs about $7 ([Marie Claire](https://marieclaire.com/beauty/news/a22088/best-washcloth-for-body); [Zoe Report](https://www.thezoereport.com/beauty/salux-towel-body-care-routine)). Ali has two listings at 20K+ each. Meta IL explicit 0.
17. **Acupressure mat with pillow.** One positive review ([T3](https://t3.com/reviews/core-balance-acupressure-mat)), but the evidence for mats is preliminary ([Superpower](https://superpower.com/guides/acupressure-mats-mechanism-evidence-pain-sleep)). Ali 2,000+. Meta IL "מזרן דיקור" has about 8 ads (Todelo).
18. **Coccyx memory-foam cushion.** Everlasting Comfort has 123k+ reviews per an affiliate roundup, which is low quality ([roundup](https://www.narcosis-the-game.com/best-coccyx-cushions-for-tailbone-pain/)). Ali 5,000+ on three listings. Meta IL about 1 ad.
19. **Foldable laptop stand.** Affiliate roundups cite the "#1 Amazon laptop stand" with 16,645 reviews ([roundup](https://homeofficegearhub.pages.dev/posts/best-laptop-stands-2025/)). Ali 10,000+ at ₪13.3. Meta IL about 8 ads.
20. **Bunion corrector splint.** It is #12 in the NBC Select 2025 list ([NBC](https://www.nbcnews.com/select/shopping/bestselling-amazon-products-2025-rcna249695)). Ali 1,000+; gel separators 5,000+. Meta IL "בוניון" has about 5 ads, mostly clinics.
21. **Sun-visor anti-glare extender.** It is #1 on BuzzFeed's Oct 2026 list ([BuzzFeed](https://www.buzzfeed.com/maitlandquitmeyer/problem-solving-products-that-require-minimal-effort-2026)). Supplier volume is weak: Ali has only 471 sold. Meta IL explicit 0.
22. **Magnetic mosquito door screen.** Reddit: "actually work really well" ([Mic](https://www.mic.com/impact/45-cheap-products-that-get-raved-about-the-most-on-reddit-81068714)). Ali 2,000+. Meta IL explicit 0.
23. **Self-cleaning slicker brush.** Hertzko: "over 61,000 pet owners" ([AOL](https://www.aol.com/lifestyle/over-2-million-self-cleaning-230457560.html)); Apartment Therapy recommends it ([AT](https://www.apartmenttherapy.com/hertzko-self-cleaning-cat-brush-review-37012558)). Ali has two listings at 10,000+. Meta IL about 1 ad.
24. **Camera ear-wax cleaner.** Reviews are mixed on reliability ([Kimola](https://kimola.com/reports/bebird-earsight-plus-unveil-customer-insights-amazon-en-us-155879); [Gadgeteer Apr 2026](https://the-gadgeteer.com/2026/04/03/bebird-earsight-ultra-x-review-4k-smart-ear-camera-for-safer-cleaning/)). Ali 4,000+. Meta IL explicit 0.

### Inferences
- Many of these categories show little or no Hebrew ad competition on Meta: motion lights, cable organizers, trackers, exfoliating towels, sleep masks, door screens, bite tools and visor extenders. The crowded ones are nasal aspirators (about 110 ads), water-flosser-type terms (about 220, mixed) and bidets (about 23, sold by plumbing retailers).
- Seasonality matters. Neck fans, stroller fans, door screens and bite tools are summer products (May–Sep), so a November zero means little. They should be prepared in March and April.

### Gaps
- Hebrew keyword coverage is limited. Israeli sellers may use other terms, such as "איירטאג", "וואטרפיק" or "כפפה טורקית", that I did not test.
- AliExpress "sold" counts are lifetime per listing and region-mixed, not monthly.

## Which five should sell in Israel, and why?

### Takeaway
1. **Bug-bite suction tool, with the heat-pen variant as an upsell.** It solves a universal Israeli summer problem (mosquitoes, kids, the beach). It has big review counts in the US and 10,000+ sold on AliExpress. Israeli ads in this space sell creams, not the device. It is tiny and cheap, and the 5-second before/after demo is easy to film.
2. **Rechargeable motion-sensor lights, sold as 3- or 6-packs.** This has the strongest supplier volume (100K+ sold) and the most repeated "solved it" testimony across Reddit roundups from 2021 to 2026. I found no Hebrew advertisers. It suits small apartments, kids and night-time bathroom trips, and bundling raises the order value.
3. **Bladeless neck fan, plus the stroller clip fan for parents.** Israeli heat makes the need obvious, the US bestseller evidence is strong, and both have 10K+ sold on AliExpress. The Meta zero is off-season, so the product should be lined up for spring. The stroller fan already has some Israeli sellers, so the neck fan is the cleaner opening.
4. **Travel cable organizer and wallet tracker card as a travel bundle.** Both were confirmed among the 2025 Amazon bestsellers (NBC Select #3 and #5), and Israelis travel abroad a lot. I found no Hebrew ads for either. The tracker needs a wireless-certification check and must not use the "AirTag" name.
5. **Japanese nylon exfoliating towel, or alternatively the bunion corrector for women 40+.** The towel has very high AliExpress volume (20K+ on two listings), a cult "can't go back" reputation, zero Hebrew ads and almost no product risk. The bunion corrector is a 2025 Amazon bestseller where Israeli ads come only from clinics.

### Cited Findings
- The evidence for each pick is cited in the per-product section above.

### Inferences
- Avoid as lead products: the nasal aspirator (crowded in Israel and medical-adjacent), the bidet (local plumbing retail already sells it, and fit or leak returns are a risk), the ear camera (injury and reliability risk) and the laptop stand (sold everywhere locally).

### Gaps
- I did not verify a landed cost or an Israeli retail price for any of the top 5.
