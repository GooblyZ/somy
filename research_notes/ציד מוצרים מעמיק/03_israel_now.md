# Lens "israel_now": physical products being advertised and sold to Israelis in Hebrew right now (2026-11-15)

Labels: **FACT** = I saw it myself today in Meta Ad Library (country=IL, active ads), in a store's public product feed, or on an AliExpress results card. **REPORTED** = a claim made by the advertiser or the press. **ESTIMATE** = my own inference. **UNVERIFIED** = plausible but not confirmed. "Days running" counts from the oldest active ad's start date to 2026-11-15.

Method: I ran Meta Ad Library searches with headless Chromium, using a fresh context for each query. Queries that loaded: משלוח חינם, 2+1, מבצע השקה, לכלב, הלהיט, ויראלי, נשארו יחידות אחרונות, גאדג'ט, טיקטוק, נמאס לכם, בלי מאמץ, מתנה מושלמת, לחנוכה, החזר כספי מלא, ימי ניסיון, הזמינו עכשיו, המוצר ש, מטבח, ניקיון. Then I read landing-store feeds (Shopify `/products.json`, WooCommerce `/wp-json/wc/store/v1/products?orderby=popularity`), searched AliExpress sorted by orders, and searched Hebrew press.

## Q1. Which physical products are being advertised to Israelis now, with signs that they work (long-running ads, several advertisers), and are not already covered?

### Takeaway
The strongest signals are **long-running Hebrew ads**: a couples card game (about 561 days), barefoot shoes (about 502), a flying boomerang ball (about 488), an under-sink organizer (about 403), run-proof tights (about 380), a cordless pressure washer (about 341), and a peek-a-boo elephant (about 318). The second strongest are **niches where two or more Israeli advertisers sell the same thing**: women's body shavers (MULAN and Velveta), winter thermal tights (Sahara Shop and Agape), and a back-pain category crowded with persona pages. Newer but sharp problem-solvers: a GLP-1/insulin pen cooling case (45 days), a quiet dog nail grinder (105 days) and AI translator earbuds sold in Hebrew, Russian and Arabic (223 days).

### Cited Findings
**Long-running ads (60+ days)**
- **Couples conversation and dare card game ("מתחברים").** FACT: dareordare.co.il has about 20 active ads in the "נשארו יחידות אחרונות" query alone, with start dates 2025-05-03, 2025-05-25, 2025-06-16, 2025-07-08, 2025-10-17, 2026-01-20 and 2026-07-07. Persona pages "זוגות ממליצים" and "מתנות מומלצות" also run them. REPORTED: the ad copy went from "11,000 couples" to "21,000 couples". FACT (WooCommerce API): the hero sells at 150 ₪ (compare-at 175) with 143 reviews. There are gay and lesbian editions, 99.90 expansions and 249.90–319.90 bundles. yourmoment.co.il also lists a "מתחברים" game at 159 ₪. — [AL](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A0%D7%A9%D7%90%D7%A8%D7%95%20%D7%99%D7%97%D7%99%D7%93%D7%95%D7%AA%20%D7%90%D7%97%D7%A8%D7%95%D7%A0%D7%95%D7%AA&search_type=keyword_unordered), [store API](https://dareordare.co.il/wp-json/wc/store/v1/products?orderby=popularity)
- **Barefoot (wide-toe) shoes.** FACT: marline.co.il has been on Shopify since 2023-07-14 and lists about 40 models at 249.90–379.90 ₪, including kids' models. A new model was added on 2026-10-02. Its ad has run since 2025-07-01 (about 502 days). — [AL "ימי ניסיון"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%99%D7%9E%D7%99%20%D7%A0%D7%99%D7%A1%D7%99%D7%95%D7%9F&search_type=keyword_unordered), [feed](https://marline.co.il/products.json?limit=250)
- **Flying boomerang spinner ball.** FACT: yanshoofi.co.il has run "כדור הבומרנג המבוקש חזר למלאי" since 2025-07-15 (about 488 days). It is #1 by popularity in the store, at 119 ₪. — [AL "גאדג'ט"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%92%D7%90%D7%93%D7%92%27%D7%98&search_type=keyword_unordered)
- **Adjustable under-sink organizer (58–90 cm).** FACT: the "פרזול חצי חינם" ad has run since 2025-10-08 (about 403 days). It appeared in both the "בלי מאמץ" and "מטבח" queries. — [AL "מטבח"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%98%D7%91%D7%97&search_type=keyword_unordered)
- **Run-proof tights.** FACT: the saharashop.co.il ad "גרביונים בלי רכבות – מהפכה ישראלית" has run since 2025-10-31 (about 380 days). The store sells 4 colours at 69 ₪, plus thermal tights at 59 ₪ (compare-at 99). — [AL "הלהיט"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%94%D7%9C%D7%94%D7%99%D7%98&search_type=keyword_unordered), [store API](https://saharashop.co.il/wp-json/wc/store/v1/products?orderby=popularity)
- **Cordless pressure-washer gun ("ג'יטור").** FACT: the "הבית המושלם" ad (taktakatstore.com) offers 2 batteries for 200 ₪ instead of 300 and has run since 2025-12-09 (about 341 days). The store feed returned 404, so price and stock are UNVERIFIED. — [AL "ניקיון"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A0%D7%99%D7%A7%D7%99%D7%95%D7%9F&search_type=keyword_unordered)
- **Peek-a-boo singing elephant ("פילאבו").** FACT: sold at 139.90 ₪ on tinyanglesl.com; its ad has run since 2026-01-01 (about 318 days). — [AL "מתנה מושלמת"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%AA%D7%A0%D7%94%20%D7%9E%D7%95%D7%A9%D7%9C%D7%9E%D7%AA&search_type=keyword_unordered)
- **Wall-mounted folding drying rack.** FACT: the "חנות מבצעים" ad prices it at 180 ₪, or 2 for 250 ₪ including delivery, and has run since 2026-02-15 (about 273 days). — [AL "הלהיט"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%94%D7%9C%D7%94%D7%99%D7%98&search_type=keyword_unordered)
- **Period-cramp heating and vibration belt ("Gal").** FACT: bleesse.com is a single-product store, on Shopify since 2023-01-14, selling it at 199.99 ₪ (compare-at 399.99). Its ad has run since 2026-02-23 (about 265 days) with a 30-day trial. REPORTED: "4,000+ customers, 4.7/5". — [AL "ימי ניסיון"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%99%D7%9E%D7%99%20%D7%A0%D7%99%D7%A1%D7%99%D7%95%D7%9F&search_type=keyword_unordered), [feed](https://bleesse.com/products.json?limit=250)
- **AI translator earbuds and a wallet tracker card.** FACT: try-ravenil.com sells RAVEN ProAI earbuds at 219 ₪ (compare-at 438), with separate Russian (2026-02-03) and Arabic (2026-03-20) product pages. It also sells a tracker card at 79 ₪ (2025-11-12). Its "צרכנים ממליצים" persona ad has run since 2026-04-06 (about 223 days). — [feed](https://try-ravenil.com/products.json?limit=250)
- **Personalised Spotify "music glass" lamp.** FACT: yourmoment.co.il sells it at 209 ₪ (compare-at 259) and it leads the store's popularity ranking. There are 3 ads from 2026-04-30 plus a creator-persona ad. REPORTED: "tens of thousands of customers, made in Israel". — [AL "נמאס לכם"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A0%D7%9E%D7%90%D7%A1%20%D7%9C%D7%9B%D7%9D&search_type=keyword_unordered)
- **Waterless "hotel scent" diffuser.** FACT: the Miyo scent ad has run since 2026-06-03 (about 165 days). — AL "גאדג'ט"
- **Sensory floor mats for toddlers.** FACT: tiptopi.co.il sells them at 80 ₪ per mat, with bundles up to 719 ₪. Its ad has run since 2026-07-15 (about 123 days). — [AL "מבצע השקה"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%91%D7%A6%D7%A2%20%D7%94%D7%A9%D7%A7%D7%94&search_type=keyword_unordered)
- **Quiet dog nail grinder (PawPeace).** FACT: lomarin.com sells it at 169.90 ₪ (compare-at 339.80), with a 39.90 ₪ replacement head as a consumable. Its ad has run since 2026-08-02 (about 105 days). — [AL "לכלב"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9C%D7%9B%D7%9C%D7%91&search_type=keyword_unordered)
- **Titanium cutting board.** FACT: cookitil.com sells it at 1+1 for 249 ₪, plus titanium pans. Its anti-PFAS ad has run since 2026-08-19 (about 88 days). — [AL "החזר כספי מלא"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%94%D7%97%D7%96%D7%A8%20%D7%9B%D7%A1%D7%A4%D7%99%20%D7%9E%D7%9C%D7%90&search_type=keyword_unordered)
- **Lumbar back stretcher.** FACT: painless-online.com sells "פלקסבק" at 229 ₪ (in the store since 2024-10). A testimonial ad has run since 2026-09-12. — AL "החזר כספי מלא"
- **GLP-1/insulin pen cooling case.** FACT: mediguardisrael.com sells it at 159 ₪ (compare-at 249), plus a 49 ₪ gel refill. Its ad has run since 2026-10-01 (about 45 days) with the hook "עט תרופה עולה יותר מ-₪800". — AL "גאדג'ט"

**Several advertisers on the same product**
- **Women's body shaver / safety razor.** FACT: mulancare.com has 40+ SKUs at 199.90 ₪, adds new SKUs almost weekly (soldiers, brides, 1+1) and has run ads since 2026-06-04; REPORTED "35,000+". try-velveta.shop sells VelvetaSkin at 199.90 ₪ with spare heads at 59.90 and has run ads since 2026-02-28. — [mulan feed](https://mulancare.com/products.json?limit=250), [velveta feed](https://try-velveta.shop/products.json?limit=250)
- **Winter thermal tights.** FACT: saharashop.co.il sells them at 59 ₪. agape-style.com sells "Velvet" thermal tights at 120 ₪ (product created 2025-10-26) and Softfit tights at 130 ₪. — [agape feed](https://agape-style.com/products.json?limit=250)

**AliExpress matches (FACT, orders-sorted search, 2026-11-15)**
- Every product in the JSON links to a specific listing. Examples: insulin cooler case with display, 10,000+ sold. HY300 Pro projector, 60K+. Taba squishy, 10,000+. Fleece-lined tights, 10K+. Titanium board, 5,000+. Women's shaver, 5,000+. Boomerang ball, 3,000+. Peek-a-boo elephant, 3,000+. YOFIDRA cordless washer, 3,000+.
- Prices of ₪3.59 are new-shopper promotions; the JSON records the card's regular price instead.

### Inferences
- The products that last in Israeli ads are **cheap gifts with emotion** (couples game, music lamp), **winter women's basics** (tights), **small-home fixes** (under-sink organizer, drying rack, pressure washer), and **body or pain problems** (period belt, back, shaving). This matches the hero-brand file's patterns and widens them beyond it. (ESTIMATE)
- Language segmentation is a real lever. Ravenil runs separate Russian and Arabic pages for the same earbuds, which suggests Russian- and Arabic-speaking Israelis are being targeted on purpose. (ESTIMATE)
- **Top 5 for Israel and why:**
  1. **Couples card game.** It has the longest-running DTC ad found (about 561 days), dozens of creatives, persona pages, 143 reviews and a second reseller. It is cheap to source, but it needs an original Hebrew deck.
  2. **Fleece-lined and run-proof tights.** Two Israeli stores sell them, the ad has lasted over a year (about 380 days), they sell 10K+ on AliExpress, and it is the start of the season now.
  3. **Period-cramp heating belt.** It is a single-product store that has lasted since 2023, with an ad live for about 265 days, a 199.99 ₪ price point and a repeat pain every month.
  4. **Women's body shaver.** Two heroes are scaling it at the same time (40+ MULAN SKUs) at 199.90 ₪. It is crowded but proven.
  5. **GLP-1/insulin pen cooling case.** It is new (45 days), but the pain is sharp (an 800 ₪+ pen ruined by heat), it suits the Israeli climate, it has a consumable refill, and the cheap AliExpress source shows 10,000+ sold.

### Gaps
- Meta Ad Library rate-limited heavily, because other sessions share this IP. Many queries returned false zeros, marked UNVERIFIED: 1+1, כולם מדברים על, מלאי מוגבל, רק היום. I stopped before the category words (רכב, גינה, שינה, ילדים, תינוק, חתול, טיפוח, שיער, איפור, תיק, שעון, טלפון, אוזניות, חורף, חימום). So category coverage is partial.
- I could not get exact ad counts per advertiser, because domain queries were not run under the rate limit. Counts above are only what appeared in the keyword queries.
- Review widgets and "X customers" figures are REPORTED; sales volumes inside Israel are not knowable from these sources.
- AliExpress matches are close look-alikes, not verified identical products. For example, the couples game is English only and the sensory mats are felt rather than rubber.

## Q2. What Israel-specific trend sources (press, retail, deal channels) confirm current demand?

### Takeaway
Hebrew press gave few concrete product signals. The usable ones: ice.co.il's 2025–26 best-seller roundup (projectors, R36S, jump starters, vacuum backpacks, mostly via AliExpress Choice), and Srugim's October 2026 report that squishies are back as a TikTok craze among Israeli kids.

### Cited Findings
- REPORTED, 2026-10-26: ice.co.il lists small home projectors (tied to a TikTok trend), the R36S console, GaN chargers, cordless jump starters, small tyre pumps and vacuum-compression backpacks as best-sellers in Israel, bought mainly through AliExpress/Choice under the 75-dollar VAT exemption. It gives no volumes. — [ice.co.il](https://www.ice.co.il/consumerism/news/article/1135127)
- REPORTED, 2026-10-01: squishies are back among Israeli kids via TikTok, and a Holon creators' festival on 2026-12-06 has a squishy-swap area. — [Srugim](https://www.srugim.co.il/101012365-גם-הילדים-שלכם-משוגעים-על-סקווישים-עכשיו)
- REPORTED: the NeeDoh maker's CEO said it sold a year's stock in the first 9 weeks of 2026. This is a global figure. — [pulse.bot](https://www.pulse.bot/ecommerce/news/tiktok-fuels-needoh-squishy-toy-sellouts-depleting-a-years-stock-in-nine-weeks-194d3a98-2fcd-43d5-86d1-000459cb3bb3/)
- REPORTED, third party: findniche lists the top AliExpress electronics for Israel by orders (dataset 2026-03-01): cable organisers, a mini GPS anti-lost tracker, the R36S, HY300 projectors and sleep-headband earphones. Its method is unclear. — [findniche](https://findniche.com/aliexpress/best-selling-consumer-electronics-products-il)

### Inferences
- The projector, R36S, jump starter and tyre pump are mostly bought directly on AliExpress by Israelis, so a local store has little price advantage there. The R36S and the tyre inflator are on the exclusion list anyway. (ESTIMATE)

### Gaps
- I found no reliable Hebrew roundup of 2026 TikTok products and no press report on Telegram or WhatsApp deal channels. I did not find KSP, Ivory or Max Stock "hot" lists.

## Q3. Excluded or near-miss leads (for the writer)

### Takeaway
Several active Israeli advertisers sell products that overlap exclusions or other lenses, so I left them out of the JSON.

### Cited Findings
- **Left out:**
  - Sahara Oodie wearable blanket: already in the hero-brand file.
  - Tanaor micro-engraved Tanakh jewellery: REPORTED "100,000+ customers"; premium priced (559–604 ₪, gold pieces in the thousands) and no AliExpress equivalent found.
  - Rootfix hair serum and Renew appetite product: cosmetic or supplement.
  - Garlic and vegetable peeler-chopper ("בית אלגנטי", 150 / 2 for 200, since 2026-07-11): the vegetable chopper is excluded.
  - Green Flow laundry and dishwasher sheets (since 2026-05-22): chemical, close to the excluded washing-machine tablets.
  - Gia Milano "Eye Therapy" device (389 ₪, 197 reviews, since 2026-07-23): borderline with the excluded heated eye mask and LED devices.
  - Whipped-cream siphon persona ad (2026-10-20): weak AliExpress sales.
  - GadgetLine large digital wall clocks (ad 2026-11-05): too new.
  - — Sources: AL queries listed above; [tanaor feed](https://tanaorjewelry.co.il/products.json?limit=250)

### Inferences
- If the partners want a premium Israeli-identity product, Tanaor's success with "Tanakh you can wear" during the war years is a notable signal. A sourcing path is UNVERIFIED.

### Gaps
- Not checked: the full Ad Library history of each domain, and the creatives' engagement.
