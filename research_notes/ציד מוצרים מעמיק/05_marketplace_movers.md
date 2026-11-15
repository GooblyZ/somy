# Marketplace movers: physical products with high, recent order volume (AliExpress, Temu, CJ, Amazon, TikTok Shop), as of 2026-11-15

Lens: `marketplace_movers`. JSON: `05_marketplace_movers.json`, 24 products, each with `ali_url` and a verified `image_url` (HTTP 200, checked 2026-11-15).

How the data was gathered:
- **AliExpress.** I scraped AliExpress with headless Chromium, sorted by orders (`SortType=total_tranpro_desc`), with the IL/ILS cookie set. I covered about 90 keywords: categories, plus targeted terms for the trends found in the press. All "sold" counts are FACT as displayed on 2026-11-15.
- **Recency signal.** AliExpress item IDs are sequential. IDs starting 100501**2**/100501**3** were created in 2026, and 100501**0**/100501**1** in late 2025 to 2026. A high sold count on a new ID means a fast riser. ₪3.59 prices are new-shopper promos, so the JSON uses the struck-through list price where shown.
- **Trend sources.** I cross-checked with FastMoss, TokConnect (TikTok Shop US), Exploding Topics, Google Holiday 100, ASINSIGHT (Amazon), CJ blog, SellTheTrend, and press.
- **Israeli presence.** Meta Ad Library, country=IL, active ads, Hebrew keyword, fresh browser per query, 2026-11-15. Zero results are often false. One query ("חזיית ג'לי") returned about 110 results in one run and 0 in another, so every zero is marked "unverified".
- **Not used directly.** Amazon Movers & Shakers and Temu best-seller tabs were not reached; I used press and mirrors only. Nothing was logged into, and no captchas were bypassed.

## Q1. Which physical products show very high AND recent order volume on the marketplaces right now?

### Takeaway
The strongest new movers in November 2026 are these: the **squishy wave**, led by glitter dumplings with a steamer box (AliExpress 100K+ on a 2026 listing), plus taba/cheese, crunchy ASMR and advent/countdown boxes; **mini turbo jet fans** (100K+/20K+); **LED keyboard fidget keychains**; **cat-eye nail magnets** (50K+ on a 2026 listing); **wire-free trunk LED strips** (70K+); and **tactical insulated foldable camping bags** (three listings at 10,000+ each). Several US TikTok hits are only starting on AliExpress: the electric fascia ring (600+) and the induction speaker stand (28 to 50 sold). That makes them early movers, not yet saturated.

### Cited Findings
AliExpress (FACT, scraped 2026-11-15; listing URL = https://www.aliexpress.com/item/<id>.html):
- Glitter Dumpling Squishy with steamer box, 1005012967864709: **100K+ sold**, ₪68.88. Simulation Flash Dumpling, 1005011924246101: 30K+. More than 20 other dumpling listings from 2026 at 1K to 8K each. — [AliExpress search "dumpling squishy"](https://www.aliexpress.com/w/wholesale-dumpling-squishy.html?SortType=total_tranpro_desc)
- 5 cm Cheese squishy "2026 New", 1005012181795214: 10,000+. Taba Cheese Cube, 1005012062436481: 10,000+. Taba Yogurt Cake, 1005010493813951: 10,000+. — [AliExpress "taba squishy"](https://www.aliexpress.com/w/wholesale-taba-squishy.html?SortType=total_tranpro_desc)
- Crispy Mango crunchy ball, 1005012650031695: 10,000+. Eleven or more crunchy/crispy listings from 2026 (potato, mangosteen, lemon, pistachio) at 1K to 5K. — [AliExpress "crispy squeeze ball"](https://www.aliexpress.com/w/wholesale-crispy-squeeze-ball.html?SortType=total_tranpro_desc)
- Squishy advent calendars, all created in 2026: "2026 NEW NeeDoh Christmas 24 Days" 4K+ (brand risk), dumpling advent 1005013324625016 1K+ at ₪37.82. — [AliExpress "advent calendar 2026"](https://www.aliexpress.com/w/wholesale-advent-calendar-2026.html?SortType=total_tranpro_desc)
- LED keyboard keychain fidget: 1005010144266156, 1005010285489453, 1005010037256637, 1005011587297264 and 1005010037161866 ("2026 New") all at 10,000+. — [AliExpress "fidget keychain"](https://www.aliexpress.com/w/wholesale-fidget-keychain.html?SortType=total_tranpro_desc)
- Turbo jet fan: X8, 1005011782834397, **100K+** (displayed ₪523.96, probably a bundle variant). M18, 1005010089170369, 20K+ at ₪61.86. Gisam 10K+. More than 20 listings at 1K to 7K. — [AliExpress "turbo jet fan"](https://www.aliexpress.com/w/wholesale-turbo-jet-fan.html?SortType=total_tranpro_desc)
- Cat-eye nail magnet pen, 1005013255503759 (2026): **50,000+**. LULAA set 20K+. Several more at 10K+. — [AliExpress "cat eye magnet"](https://www.aliexpress.com/w/wholesale-cat-eye-magnet.html?SortType=total_tranpro_desc)
- Wire-free sensor trunk LED strip, 1005010285553270: **70K+** in the trunk-light search and 50,000+ in the car-accessories search on the same day. — [AliExpress "car trunk light"](https://www.aliexpress.com/w/wholesale-car-trunk-light.html?SortType=total_tranpro_desc)
- Tactical insulated foldable camping bag 30/42/56L: three separate listings at 10,000+ each (1005012477719675, 1005009481102235, 1005009045188656). — [AliExpress "camping gadget"](https://www.aliexpress.com/w/wholesale-camping-gadget.html?SortType=total_tranpro_desc)
- Lymphatic contour face brush: three listings at 10,000+ (1005010278789787, 1005012177010694, 1005009984705392). — [AliExpress "lymphatic drainage face brush"](https://www.aliexpress.com/w/wholesale-lymphatic-drainage-face-brush.html?SortType=total_tranpro_desc)
- Magnetic power banks: Baseus 5000mAh 10K+, Baseus 10000/5000 10K+, Essager 6K+. — [AliExpress "magnetic power bank 5000mah"](https://www.aliexpress.com/w/wholesale-magnetic-power-bank-5000mah.html?SortType=total_tranpro_desc)
- Open-ear clip earbuds: QCY Crossky C50 10,000+, Baseus MC1 Pro 5,000+, Baseus Inspire XC1 (2026) 4,000+. — [AliExpress "open ear earbuds"](https://www.aliexpress.com/w/wholesale-open-ear-earbuds.html?SortType=total_tranpro_desc)
- AI camera glasses: 1005010096355987 10K+ at ₪209. "2026 4K 8MP" 3K+. — [AliExpress "ai glasses camera"](https://www.aliexpress.com/w/wholesale-ai-glasses-camera.html?SortType=total_tranpro_desc)
- Electric fascia ring: the top listing (1005013195099460, 2026) shows only **600+**, and dozens of 2026 listings show 20 to 290. This is an early stage. — [AliExpress "fascia massager ring electric"](https://www.aliexpress.com/w/wholesale-fascia-massager-ring-electric.html?SortType=total_tranpro_desc)
- Induction speaker phone stand: 5-in-1 auto-induction (1005012671846469) 28 sold, 360° dock 50. This is nascent. — [AliExpress "wireless induction speaker"](https://www.aliexpress.com/w/wholesale-wireless-induction-speaker.html?SortType=total_tranpro_desc)
- Other high sellers that are evergreen or out of scope, not selected: RGB LED strip 100K+, kitchen thermometer 100K+ (excluded category), HY300 projector 50,000+, honeycomb gel cushion 50,000+, shoe-repair paint pen 50,000+, tactical auto-buckle belt 70K+, cable straps 100K+.

Temu, CJ, other marketplace reports:
- Temu Japan 30-day best sellers (10,000+ units, ≥4.5★, ≥500 reviews, as of 2026-10-09): quick-dry diatomite-style bath mat 550,000 units, washable pet bed 200,000, fluffy bath mat 150,000, storage rack and non-slip hangers 100,000 each, sun-visor glasses clip 80,000, suction dashboard phone holder 78,000. These are mostly evergreen basics. — [pricey.jp](https://www.pricey.jp/web/articles/7342)
- The CJ Dropshipping "Trending Dropshipping Products 2026" post (24.12.2025) gives no sales data, only categories: smart plugs, motion lights, posture and massage tools, pet feeders. — [CJ blog](https://cjdropshipping.com/blogs/winning-products/Trending-Dropshipping-Products-2026)
- The CJ blog (21.1.2026) says that, per Shopify, more than 100,000 copies of the Kollide-type magnetic collision game sold on TikTok Shop. — [CJ TikTok viral 2026](https://cjdropshipping.com/blogs/winning-products/TikTok-Viral-products-2026)
- SellTheTrend's AliExpress top-sellers report (updated 15.11.2026) lists M25 TWS earbuds at 51,256 orders and mentions trunk light strips in its weekly picks. Some figures in this report look wrong, with duplicated FIFINE rows and a $999 "cost". — [SellTheTrend](https://www.sellthetrend.com/reports/top-selling-aliexpress)

### Inferences
- High sold counts on IDs created in 2026 are the clearest "new and fast" signal. Dumpling squishies, cat-eye magnets, crunchy squishies and squishy advent boxes all meet it.
- When a product is huge on TikTok US but small on AliExpress (fascia ring, induction speaker), the Chinese supply chain is only now catching up. Israeli sellers who start now are early. Product quality from new suppliers is untested.

### Gaps
- I could not reach Temu's live best-seller tab, Amazon Movers & Shakers or the CJ "hot selling" product pages directly, which are blocked or need a login. No Temu Israel data was found.
- AliExpress sold counts are lifetime per listing, not monthly, so recency is inferred from listing age (the ID).

## Q2. Do these items cross-check with TikTok Shop / Amazon / Google trend data?

### Takeaway
Yes, for most of them. The strongest double signals are the squishy wave (FastMoss, ASI, AliExpress), the fascia ring (FastMoss Q3 units #10, Amazon US 21.7K a month), the magnetic power bank (#1 in its TikTok category), the jelly bra (TikTok units #8, Exploding Topics +5,000%), the lymphatic face brush (Google +400%, AliExpress 10K+ x3), the turbo jet blower (TokConnect 31K in 30 days, AliExpress 100K+) and the foldable lanterns (TokConnect 70K in 30 days).

### Cited Findings
- FastMoss, TikTok Shop US Q3 2026, top revenue: #3 SEESE Cordless Pressure Washer Gun $7,084,880; #6 Comfrt blanket; #7 bamboo cooling topper; #10 Shark StainForce. By units: #8 OEAK Jelly Bras 221,032; #10 ADDWIN Fascia Ring R10 204,575 ($4.89M). — [FastMoss Q3](https://www.fastmoss.com/blog/best-selling-tiktok-shop-products-us-q3-2026/)
- FastMoss, week of 19–25.10.2026: XMWUS 5000mAh magnetic power bank was #1 in Phones & Electronics with 13,207 units; PUTARE 5-in-1 induction speaker stand was #3 with 8,214 units; R36S console was #4 (already shown to partners). — [FastMoss by category](https://www.fastmoss.com/blog/best-selling-products-by-category/)
- FastMoss gift list, October 2026 units:
  - 24-squishy advent calendar 35,294; NeeDoh Teenie 34,167; energy-drink can plush 25,515.
  - Christmas dumpling set 23,649; mochi DIY kit 21,844; cheese cube squishy 15,725.
  - Magnetic power bank 45,489; PUTARE stand 34,961; plush dumpling phone charm 23,464; wireless doorbell camera 27,757.
  - Toys & Hobbies total: 199,452 units. — [FastMoss gifts](https://www.fastmoss.com/blog/tiktok-shop-holiday-gift-ideas-2026/)
- FastMoss toys: Julutile mochi squishy kit was #1 in October with $574,622. The dumpling advent calendar was #1 in the week of 2.11.2026 with 30,355 units, against only 3,955 in stock. — [FastMoss toys](https://www.fastmoss.com/blog/best-selling-toys-on-tiktok-shop-what-sold-last-christmas-and-whats-trending-for-2026/)
- TokConnect, 30 days to 11.11.2026 (US, estimates):
  - 4-pack foldable LED lanterns: 70,245 units, $1.33M.
  - SEESE Turbo Jet leaf blower: 31,042 units, $939K.
  - PUTARE induction speaker stand: 41,582 units, $790K.
  - XMWUS magnetic power bank: 65,731 units.
  - OEAK jelly bras: 97,675 units.
  - Sudrov 42800mAh solar power bank: 12,411 units.
  - Translator pen: 14,322 units.
  - Monster open-ear headset: 9,191 units.
  - Wireless doorbell camera: 21,420 units.
  - Merach vibration plate: 7,899 units. — [TokConnect](https://tokconnect.com/trends/products/best-sellers/)
- TT123, using FastMoss data: ADDWIN 2026 fascia ring R10 has sold 240,600 units cumulatively, about $6.15M GMV, with 6,313 linked videos and 1,622 creators. — [TT123](https://www.tt123.com/t/DO6Gfnwg). Pitched as a hands-free alternative to massage guns. — [Baijing](https://www.baijing.cn/article/56536)
- ASINSIGHT: "fascia ring" on Amazon US sold 21,700 units in July 2026 (-0.2% MoM), averaging $23.71. — [ASINSIGHT](https://www.asinsight.com/market-analysis/US/fascia-ring)
- Exploding Topics (updated 23.10.2026), 5-year growth:
  - Toe Spacers: 36.3K searches a month, +279%.
  - Jelly Bra: 71.2K, +5,000%.
  - Hall Effect Joystick: 18.8K, +6,300%.
  - 20K Power Bank: +6,600%.
  - Water Bottle Charms: +8,600%, but the source link is wrong.
  - Bag Charms: 147.2K (already shown to partners). — [Exploding Topics](https://explodingtopics.com/blog/trending-products)
- Google Holiday 100 (9.11.2026): lymphatic sculpting face brush searches up 400%; roller skates +180%; classic toy train +240%; podcast microphone +115%. — [Google blog](https://blog.google/products-and-platforms/products/shopping/holiday-100-gift-guide-2026/)
- Squishy trend:
  - RMS claims more than 40M Mystery Dumplings sold worldwide. This is a company claim, unverified. — [Business Wire 19.3.2026](https://www.businesswire.com/news/home/20260319125442/en/A-Viral-Sensation-Turned-Retail-Juggernaut-RMS-USAs-Mystery-Dumpling-Continues-Its-Sell-Out-Streak)
  - Dumplings sold out "within the hour" after restocks. — [Axios 4.4.2026](https://www.axios.com/2026/04/04/needoh-squishy-toys-dumplings-easter)
  - Searches for "dumpling" rose 184% from Q2 to Q3 2026, and "fidget" rose 26% year over year. — [ASI 19.10.2026](https://members.asicentral.com/news/strategy/october-2026/viral-squishy-trend-dominates-fastest-growing-esp-searches-in-q3/)
  - A buyer expects a crash after Christmas. — [Galaxus](https://www.galaxus.fr/en/page/dumplings-are-doomed-43768)
  - UK recall of "Squeezy Dumplings" (benzene, June 2026), and counterfeit listings. — [BrandShield](https://www.brandshield.com/2026/07/29/)
- Amazon viral list, Oct 2025 to Oct 2026: AquaSonic pink toothbrush; Ninja SLUSHi; Kodak FZ55 camera; ZELUS weighted vest; NeeDoh, whose maker sold a year's inventory in 9 weeks. — [Netpeak 17.10.2026](https://netpeak.us/blog/which-products-went-viral-on-amazon-in-the-last-12-months/)
- Fidget keychains: Google interest for "fidget keychain stress relief" spiked to 100 in February 2026 and fell to 18 in March. — [Accio](https://www.accio.com/business/fidget-keychain-trends-2026)
- Open-ear audio: OWS shipments grew 12% in Q2 2026 while TWS was flat, and clip-on held the majority. — [Omdia](https://omdia.tech.informa.com/pr/2026/sep/ows-shipments-grow-12percent-as-tws-market-remains-broadly-flat-in-2q26). Q2 2026 open-ear shipments were 11.1M units. — [GCN](https://gcn.com/conventional-wireless-earbuds-slipped-million-shipments/21836/)
- AI glasses: 4.2M shipped in H1 2026, up 127%, with Meta holding 81.3%. — [Omdia](https://omdia.tech.informa.com/pr/2026/sep/global-ai-glasses-shipments-more-than-doubled-in-1h26-hitting-a-record-4point2-million). Counterpoint puts growth at +263%, with 96% having no display. — [Counterpoint](https://counterpointresearch.com/cn/insights/global-ai-glasses-shipments-surge-263-percent-yoy-with-display-less-ai-glasses)
- Mini turbo fans: Accio describes rising TikTok Shop sales but rates the category "cautious" because of motor quality. — [Accio](https://www.accio.com/business/handheld-blower-best-sellers)

### Inferences
- In terms of category timing, the squishies peak in November and December. The fascia ring, pressure washer gun, open-ear earbuds and lymphatic brush are mid-climb. Keyboard fidget keychains already peaked on Google in February 2026 and are only an add-on now.
- The TikTok US units are US-only. Israel usually lags by 3 to 9 months, which supports being early on the fascia ring, induction speaker and pressure washer gun.

### Gaps
- No Israeli sales data exists for any of these. FastMoss and TokConnect figures are vendor estimates. One search summary said IDC reported a 35.4% drop in cheap audio and camera glasses in China in Q2 2026, but I did not open the primary page, so it is unverified.
- I found no TikTok number for cat-eye magnets, trunk lights, tactical camping bags or the window robot, so their evidence rests on AliExpress only.

## Q3. Are they already present or crowded in Israel (Meta Ad Library, IL, Hebrew, 15.11.2026)?

### Takeaway
The crowded ones are the **jelly bra** (about 110 results, 8 advertisers) and **toe spacers** (about 22 ads, 5 advertisers). The **window robot** is sold as branded ECOVACS by retailers. Categories that are present but not yet crowded: **squishy**, where about 13 ads come mostly from toy shops, workshops and a Delek promo, and the **fascia ring**, where only foreign dropshippers run Hebrew ads. Turbo blower, pressure washer gun, induction speaker, trunk light, magnetic game, emergency sleeping bag and solar power bank showed 0 or 1 relevant ads, all unverified.

### Cited Findings
Meta Ad Library, IL, active ads, 15.11.2026. Search URL pattern: `https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=<term>&search_type=keyword_unordered`
- "סקווישי": about 13 ads. Delek (4.11), Shusha Hanukkah craft (1.11 and 10.11), Trendy toys (14.11), Toy Center (2.11), Ayoli (11.11), party and workshop operators.
- "דאמפלינג סקווישי": 0.
- "טבעת עיסוי": about 6 ads. Ecouaer US, in Hebrew, "טבעת הפאשיה הרב-תכליתית 3 ב-1" (since 26.8 and 11.9.2026). Ybaou shop (started 14.11.2026). GadgetLine 3D.
- "חזיית ג'לי": about 110 results. Yael Raz (7 ads), Virella (7, "25% off jelly bras"), LAOR (4), Ha-Bayit LeHalbasha Tachtona, LiftUp 360, LIORA, Seeya Active. A repeat query in a different batch returned 0, so the tool gives false zeros.
- "מפריד אצבעות": about 22 ads. Michal Levi (12), healthy-feet guide, Kindo, Active-Comfort, Lotem barefoot (Oct to Nov 2026).
- "משקפיים חכמים מצלמה": 2 ads, both from "Smart Glasses IL" (Meta Capri, 13.11.2026).
- "אוזניות קליפס": SmartCase (4.11 and 15.11) and Ecouaer US (Hebrew, 29.7.2026).
- "פנס קמפינג": about 13 results. SmartCase, Ecouaer, Derech Eretz.
- "מחזיק מפתחות מקלדת": 4 ads, all Giftme3D (personalised, since 14.10.2026).
- "מברשת לימפטית": 1 ad (SAG clinic, 19.1.2026).
- "מגנט עין חתול": 1 ad (Agam Beauty, professional supply, 3.11.2026).
- "רובוט לניקוי חלונות": about 5 results, all retail for ECOVACS WINBOT: Machsanei Chashmal, Electro-Gal, Petcom Eilat, Shayish Berger.
- "תיק אחסון טקטי": 1 ad (Asitek).
- "טבעת חכמה": about 33 results. Mostly Oura and Ultrahuman via KSP, Bug and Machsanei Chashmal. Branded and crowded, so I dropped the generic smart ring.
- "משטח רטט": about 9, mostly health advertorials.
- 0 results (unverified) for: מפוח טורבו, רמקול אינדוקציה, סוללה מגנטית, אקדח שטיפה נטען, עט מתרגם, תאורה לתא מטען, משחק אבנים מגנטיות, שק שינה חירום, וסט משקולות, מחמם ידיים נטען, מצלמה דיגיטלית רטרו.
- "מטען סולארי": 1 irrelevant result.
- Israeli retail prices:
  - Homecenter sells GT AIR WIND MAX cordless turbo blower at 249 ₪. — [Homecenter](https://www.homecenter.co.il/products/1747663220252)
  - Shein IL has mini turbo blowers from about ₪23. — [Shein IL](https://m.shein.com/il/Blower-c-13542.html)
  - Bug sells a unicorn squishy at 42 ₪. — [Bug](https://www.bug.co.il/brand/diamant/unicorn/squash)

### Inferences
- An AliExpress price of about ₪62 against a local shelf price of 249 ₪ makes the turbo blower a credible "good deal" story.
- Foreign dropshippers running Hebrew ads for the fascia ring (Ecouaer, Ybaou) prove there is demand to test. A local seller with fast delivery and Hebrew service would have an edge.

### Gaps
- Zero-ad results are not reliable. Shopify-store and Instagram-only competitors are not visible in the Ad Library. I could not check price points for most items on ZAP or KSP.

## Q4. Top 5 for Israel and why

### Takeaway
1. **Electric fascia ring** (women 30–55). It is huge in the US now (204,575 TikTok units in Q3), early on AliExpress (600+), and only foreign dropshippers advertise in Hebrew. Sell it as recovery and massage, not as "fat burning".
2. **Mini turbo jet fan/blower** (men, car owners, BBQ). AliExpress 100K+ and 20K+; TikTok US 31K units in 30 days. About ₪62 on AliExpress against 249 ₪ at Homecenter is a clear good-deal angle, and no Hebrew ads were found. The demo sells itself.
3. **Glitter dumpling squishy + "8-candle" countdown box** (kids and teens). This is the 2026 mega-trend (AliExpress 100K+, FastMoss #1 toy weekly). Israel is aware of it (Shusha ties squishy to Hanukkah), but the dumpling/advent product is not advertised yet. It is a short window through Hanukkah, early December 2026. It needs toy-safety checks.
4. **Lymphatic contour face brush** (women). Google search is up 400%, three AliExpress listings are at 10,000+, there is 1 Israeli ad, and the risk is almost zero (no battery, no certification). It costs a few shekels and works as a gift add-on.
5. **Cordless pressure washer gun** (men, homeowners). It was #3 by revenue on TikTok Shop US in Q3 ($7.08M), and no Hebrew ads were found. Car washing in the parking lot and balcony cleaning fit Israeli habits. Check carefully whether the battery is included before listing.

Honourable mentions: foldable 4-blade lantern (emergency and the safe room, 70K TikTok units in 30 days); induction speaker stand ("no-pairing" gift for parents, but AliExpress supply is thin); cat-eye magnet pen and keyboard keychain as cheap cart add-ons.

### Cited Findings
- The numbers above come from [FastMoss Q3](https://www.fastmoss.com/blog/best-selling-tiktok-shop-products-us-q3-2026/), [TokConnect](https://tokconnect.com/trends/products/best-sellers/), [FastMoss toys](https://www.fastmoss.com/blog/best-selling-toys-on-tiktok-shop-what-sold-last-christmas-and-whats-trending-for-2026/), [Google Holiday 100](https://blog.google/products-and-platforms/products/shopping/holiday-100-gift-guide-2026/), [Homecenter](https://www.homecenter.co.il/products/1747663220252), the AliExpress scrapes and Meta Ad Library IL (15.11.2026), all listed above.

### Inferences
- Avoid as lead products: the jelly bra (Israel already crowded, with returns and sizing issues), the magnetic power bank (crowded local electronics retail, lithium shipping) and AI camera glasses (privacy, quality, wireless approval). They are listed in the JSON for completeness.

### Gaps
- I did not verify which suppliers' quality matches the TikTok hero products (ADDWIN, SEESE, PUTARE). Samples are recommended before scaling.
