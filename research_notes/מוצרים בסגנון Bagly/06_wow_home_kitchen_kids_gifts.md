# "Wow" product catalog: home ambience, kitchen/coffee, sleep, kids fun, gifts, adult hobby (research date 2026-11-14)

Labels: **FACT** = read directly in this session (scraped page or Meta Ad Library, 2026-11-14). **REPORTED** = secondary source (press, blog, Amazon-mirror site). **ESTIMATE** = my inference or a planning value. **UNVERIFIED** = not confirmed.

Machine-readable companion file, with an image URL for every item (all 15 image URLs returned HTTP 200 image/webp): `06_wow_home_kitchen_kids_gifts.json`.

Method and access notes:
- **AliExpress.** I searched with headless Chromium using the IL region and ILS currency cookie, and read the result cards (title, prices, sold count, image).
  - Item pages came back empty (bot wall), so I did not try to get around it, and no item page was read.
  - The cards come in two formats:
    - **(A)** "₪low ₪high … New shoppers save ₪X". Here the low price is a new-user promo, so I used the **struck (regular) price**.
    - **(B)** "₪P … New shoppers – ₪Y / Save ₪Y". Here I used the displayed ₪P. I could not verify whether existing customers pay the same price, so each such item is flagged.
  - Where a card did not say "Free shipping", I added an **ESTIMATE** of shipping cost. It is the upper bound from the KakoBuy rates in `10_unit_economics_verification.md` (no-battery ePacket: 300 g 38, 500 g 49, 1 kg 76, 2 kg 130 ILS; battery line 300 g ≈ 47, 100–200 g ≈ 29–47 ILS).
- **Meta Ad Library.** Search settings: IL, active ads, keyword (unordered). I used a fresh browser context for every query and hit no captcha.
  - Numbers are the "~N results" header (ads, not advertisers), the advertisers seen on the loaded cards, and the oldest "Started running" date among the loaded cards.
  - Keyword matching is loose, so I read the ad text to judge relevance.
- **Israeli prices.** Zap.co.il search pages (scraped), Bug.co.il and PayNGo (via search results), and prices shown inside Meta ads.
- **Profit formula** (per the brief): price/1.18 − 3.6%×price (fees) − 5%×(price/1.18) (returns) − landed − CPA 86.
- **Weights** are ESTIMATES (product plus packaging).

## Q1. Which 12–15 "I need this" candidates exist, and what is the evidence abroad?

### Takeaway
I collected 15 candidates. The strongest emotional and gift ideas are:
- the **WiFi photo frame for grandparents** (Frameo)
- the **R36S retro console** (50,000+ sold per AliExpress listing)
- the **wireless meat thermometer** (fits Israeli mangal culture)
- the **kids instant-print camera**
- the **TV camera-sync backlight**
- the **water-ripple lamp**

Evidence abroad is strong for the R36S, the Govee-type TV backlight, Perytong sleep headbands and kids print cameras. It is thin (sales trackers or blogs only) for the ripple lamp and the gravity grinders.

### Cited Findings
(Image URLs are in the JSON. Ali prices are ILS as displayed on 2026-11-14.)

| # | Item (HE / EN) | Driver | Str. | 10-sec demo | AliExpress listing (price ILS, sold) |
|---|---|---|---|---|---|
| W01 | מנורת אדוות מים / Water ripple projection lamp | wow/style/gift | 4 | Dark room, tap, and the ceiling fills with moving blue waves | [1005008472522106](https://www.aliexpress.com/item/1005008472522106.html), 47.59 regular (9.07 new-user), 487 sold. FACT |
| W02 | מקרן גלקסיה אסטרונאוט / Astronaut galaxy projector | wow/gift | 2 | Lights off, and a nebula swirls on the ceiling | [1005009890378414](https://www.aliexpress.com/item/1005009890378414.html), 59.21 regular, 1,000+ sold. FACT |
| W03 | תאורת טלוויזיה מסתנכרנת / TV backlight with camera sync | wow | 4 | Split screen: plain TV vs. a wall glow that follows an explosion or a goal | [1005007076413168](https://www.aliexpress.com/item/1005007076413168.html), 92.39 (no promo), 68 sold. FACT |
| W04 | מנורת ירח מרחפת / Levitating moon lamp | wow/gift | 3 | The moon "catches" in mid-air and spins; a hand passes under it | [1005008077604490](https://www.aliexpress.com/item/1005008077604490.html), 237.09 (format B), 728 sold, free shipping. FACT |
| W05 | אספרסו ידני נייד / Wacaco Minipresso GR2 | money-saving/wow | 3 | Desert rock, 8 pumps, espresso with crema; caption "14 ₪ at a café vs 2 ₪" | [1005007129358838](https://www.aliexpress.com/item/1005007129358838.html), 184.74 regular (110.81 new-user), 500+ sold. FACT |
| W06 | מדחום בשר אלחוטי / Wireless BT meat thermometer | frustration/gift | 4 | Probe into entrecôte, lid closed, beer; phone beeps "ready 54°"; perfect pink slice | [1005007471287015](https://www.aliexpress.com/item/1005007471287015.html), 63.71 (format B), 2K+ sold, free shipping. FACT |
| W07 | מטחנות כבידה חשמליות / Gravity salt & pepper set (LED) | style/gift | 3 | Slow-mo tilt over a steak; light on, pepper falls | [1005010228728911](https://www.aliexpress.com/item/1005010228728911.html), 91.39 per set (no promo label), 690 sold, free shipping. FACT |
| W08 | אוזניות שינה בסרט ראש / Sleep headphones headband | frustration/gift | 3 | Partner snoring; she puts on the band and falls asleep smiling | [1005008190790031](https://www.aliexpress.com/item/1005008190790031.html), 20.87 regular (3.59 new-user), 800+ sold. FACT |
| W09 | שעון מעורר זריחה / Sunrise alarm clock | frustration/style | 3 | Time-lapse: dark room, orange glow rises, she wakes up smiling | [1005007498135174](https://www.aliexpress.com/item/1005007498135174.html), 140.21 (format B), 219 sold, free shipping. FACT |
| W10 | מצלמה מדפיסה לילדים / Kids instant-print camera | gift/wow | 4 | Kid snaps the dog; a paper strip comes out; she screams with joy | [1005006861140002](https://www.aliexpress.com/item/1005006861140002.html), 85.8 (format B), 423 sold, free shipping. FACT |
| W11 | רמקול קריוקי + 2 מיקרופונים / Karaoke speaker + 2 mics | gift/fun | 3 | Two kids singing a duet with voice effects and RGB lights | [1005013175308007](https://www.aliexpress.com/item/1005013175308007.html), 47.52 (format B), 218 sold, free shipping. FACT |
| W12 | מסגרת תמונות דיגיטלית WiFi / Frameo WiFi photo frame 10.1" | gift/emotion | 5 | Grandchild sends a photo from a phone; cut to grandma's living room as the frame updates; tears | [1005007526279962](https://www.aliexpress.com/item/1005007526279962.html), 148.11 (format B), 177 sold. FACT |
| W13 | קונסולת רטרו R36S / R36S retro handheld | gift/emotion | 4 | Dad switches it on, Mario appears, the kid grabs it | [1005006966123998](https://www.aliexpress.com/item/1005006966123998.html), 107.47 (no promo label), 50,000+ sold. FACT |
| W14 | מאכיל ציפורים חכם / Smart AI bird-feeder camera | wow/gift | 2 | Phone alert "a bulbul has arrived!" with a slow-mo close-up | [1005012746702398](https://www.aliexpress.com/item/1005012746702398.html) (JOOAN), 253.24 (format B), 4 sold, free shipping. FACT |
| W15 | מסכת עיניים מחממת / USB heated eye mask | comfort | 2 | After a Zoom call, glasses off, mask on, she leans back | [1005006059381999](https://www.aliexpress.com/item/1005006059381999.html), 82.2 regular (36.46 new-user), 101 sold. FACT |

Evidence abroad:
- R36S:
  - **FACT:** two AliExpress listings show "50,000+ sold" ([1005006966123998](https://www.aliexpress.com/item/1005006966123998.html), [1005006966152990](https://www.aliexpress.com/item/1005006966152990.html)).
  - **REPORTED:** Amazon MSRP is $84.99, with a sale at $59.49 ([Notebookcheck](https://www.notebookcheck.net/R36S-retro-handheld-console-on-sale-for-30-off-for-limited-time.812891.0.html)).
  - **REPORTED:** Walmart shows a "Best seller" tag ([Walmart](https://www.walmart.com/ip/18364523027)).
- TV camera backlight. **REPORTED:** Govee TV Backlight 3 Lite has 4.5★ from 9,600+ reviews and "2,000+ sold last month" on Amazon, priced at $69, down from $89 ([Gizmodo](https://gizmodo.com/this-govee-tv-backlight-turns-any-movie-into-a-cinema-experience-amazon-just-hit-a-record-low-2000759074)). GearBrain calls DreamView one of Govee's best sellers ([GearBrain](https://www.gearbrain.com/govee-dreamview-tv-backlights-rgbic-2657638384.html)).
- Sleep headband. **REPORTED** (Amazon mirror): Perytong has 56,897 reviews at 4.2★ ([ShopSavvy](https://shopsavvy.com/reviews-tldr/perytong-sleep-headphones)), and a BSR snapshot of #474 in Electronics (desertcart mirror, UNVERIFIED date).
- Kids print camera. **REPORTED** (desertcart Amazon mirror): ESOXOFFORE has 7,283 ratings at 4.4★ and BSR #133 in Electronics ([desertcart](https://www.desertcart.co.th/products/530366366)). No TikTok Shop ranking was found.
- Frameo frame. **REPORTED:** US local-TV consumer segments call it "the perfect gift for grandparents", with a Frameo 10.1" at $59.99 ([10News](https://www.10news.com/digital-frame-is-perfect-gift-grandparents)).
- Water ripple and ambient lights:
  - **REPORTED / ESTIMATE-grade:** EchoTik says an LED ambient night light sold 11.4k units in a month on TikTok Germany ([EchoTik](https://www.echotik.live/blog/tiktok-2026-emotional-consumption/)).
  - A Chinese report says #ambientlight is near 1B views ([baijing](https://www.baijing.cn/article/53072)).
  - A TikTok Shop "ocean wave projector" listing exists ([TikTok Shop](https://www.tiktokshop.com/pdp/ocean-wave-projector-light-by-brand-16-color-touch-control-aurora-lamp/1730385559667118172)).
  - Nothing found is specific to this SKU.
- Gravity grinders:
  - **REPORTED:** Livingetc found them through a TikTok creator ([Livingetc](https://livingetc.com/news/aesthetic-salt-and-pepper-shakers)).
  - **UNVERIFIED:** a blog claims about 3,000 Amazon reviews at 4.4★ for UNNEES ([blog](https://theaestheticfinds786.blogspot.com/2026/04/future-of-seasoning-unnees-gravity.html)).

### Inferences
- These best match the brief's "Bagly test" (universal, obvious, emotional, 10-second demo):
  - **W12 Frameo frame.** Every family has grandparents, the demo is emotional, and Hanukkah 2026 starts Dec 4, so it is a dated gift.
  - **W13 R36S.** Nostalgia, proven volume.
  - **W06 meat thermometer.** Mangal culture, and a clear "never ruin a 150-₪ entrecôte again" money angle.
- W02 (astronaut projector) and W15 (eye mask) are listed for completeness. They fail on price room or on "wow".
- Hanukkah timing (ESTIMATE): ePacket transit is 15–20 days (per file 10). Orders placed from around Nov 15 arrive close to Dec 4. Local stock or a faster line would be needed for Hanukkah gifting.

### Gaps
- There is no Amazon BSR or TikTok Shop sales figure read directly for any item. Amazon and TikTok were not opened; the figures above come from mirrors or press.
- There is no Kickstarter evidence (bird-feeder cameras and portable espresso were Kickstarter categories historically, UNVERIFIED).
- AliExpress item pages were blocked, so the price existing customers pay for format-B listings is unverified.
- The long-distance "friendship lamp" was dropped: the AliExpress search returned no real touch-sync lamps.

## Q2. How crowded is Israel (Meta Ad Library) and what are local prices?

### Takeaway
Hebrew Meta advertising for almost all of these items is **near zero** (0–3 relevant ads). The exception is karaoke microphones: about 15 ads from 7 advertisers, including a 299.90 ILS bundle.

Local shelf prices exist, and they cap pricing for:
- the astronaut projector (69–100 ILS)
- sleep headbands (about 99)
- grinders (59–153)
- R36S (289)
- kids print camera (Innova 129.9)

There is **wide headroom** for the Frameo frame (425–520) and the meat thermometer (brands at 330–745).

### Cited Findings
Meta Ad Library: IL, active ads, 2026-11-14, **FACT**. Each line gives the query, then the "~results" count, then advertisers and the oldest loaded ad.
- Water ripple lamp. 'מנורת אדוות': 0 ("No ads match").
- Star projector:
  - 'מקרן כוכבים': ~3 (Toysim baby-projector ad, plus an unrelated ad; oldest 2026-07-30).
  - 'מקרן גלקסיה': ~1, unrelated (a gaming store).
- TV lighting:
  - 'תאורה לטלוויזיה': ~1. הבית הזהב, started 2026-11-09, text: "ערכת תאורת LED חכמה לטלוויזיה 5 מטרים RGBIC … 150 ₪". Camera sync is not stated.
  - 'תאורת אווירה': ~350, but these are cars and furniture, not relevant.
- Portable espresso. 'אספרסו נייד': 0; 'מכונת קפה ניידת': 0.
- Meat thermometer. 'מדחום בשר': ~2, both from פחמי ישראל, Weber grill ads (oldest 2026-11-04). There is no thermometer seller.
- Grinders. 'מטחנת פלפל חשמלית': 0; 'מטחנה חשמלית': ~1, unrelated.
- Sleep headphones. 'אוזניות שינה': 0; 'אוזניות לשינה': 0.
- Sunrise alarm. 'שעון מעורר זריחה': 0; 'שעון מעורר': 0.
- Kids camera. 'מצלמה מדפיסה': ~2 (Clicktoy, oldest 2026-10-31); 'מצלמה לילדים': 0.
- Karaoke. 'מיקרופון קריוקי': ~15 ads, 7 advertisers:
  - Advertisers: אטרקציה – מהיבואן לצרכן, Clicktoy, שלבי, TRP, The Blackbox, RockPhonic and a voice coach.
  - Oldest ad: 2026-10-08.
  - Ad text includes "רמקול קריוקי + מיקרופון … במקום 600 ₪ – רק 299.90 ₪".
- Photo frame:
  - 'מסגרת תמונות דיגיטלית': ~6 ads from תחביבן, אלבום בקליק ("סורקים 1000 תמונות ומקבלים מסגרת דיגיטלית במתנה") and Epic D.M; oldest 2026-08-06.
  - 'מסגרת דיגיטלית': 0.
- Retro console:
  - 'קונסולה רטרו': ~3. One is משחקי רטרו, "279 ש"ח בלבד כל משחקי הרטרו בקונסולה מתקדמת אצלכם בטלוויזיה" (a TV stick, not a handheld); oldest 2026-10-29.
  - 'קונסולת משחקים': ~7 from 4 advertisers (Enjoystick, ITechStore, …).
- Bird feeder. 'מאכיל ציפורים': 0.
- Eye mask. 'מסכת עיניים מחממת': ~1, a dry-eye advertorial (2026-10-26).
- Moon lamp:
  - 'מנורת ירח מרחפת': 0.
  - 'מנורת ירח': ~14 ads from 2 advertisers (Babybuff, Kiklak; oldest 2026-10-14).
- Friendship lamp. 'מנורת חברות': 0.

Israeli prices, **FACT** from Zap search pages scraped 2026-11-14 unless another source is named:
- Star projector: 69–100 ILS ([Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%A7%D7%A8%D7%9F%20%D7%9B%D7%95%D7%9B%D7%91%D7%99%D7%9D)).
- Wacaco: 212 / 335 / 395 / 499 ILS ([Zap](https://www.zap.co.il/search.aspx?keyword=Wacaco)).
- Wireless meat thermometers ([Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%93%D7%97%D7%95%D7%9D%20%D7%91%D7%A9%D7%A8%20%D7%90%D7%9C%D7%97%D7%95%D7%98%D7%99)):
  - Inkbird INT-11P-B 330 ILS; Inkbird 4-probe WiFi 634.
  - MEATER 699; ARMEATOR A1 499; Bosch 745.
- Electric grinders: results at 59–153 ILS ([Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%98%D7%97%D7%A0%D7%AA%20%D7%9E%D7%9C%D7%97%20%D7%A4%D7%9C%D7%A4%D7%9C%20%D7%97%D7%A9%D7%9E%D7%9C%D7%99%D7%AA)). It was not checked that every hit is a gravity model.
- Sleep headphones: 98 ILS (a headband/eye-mask type) and Monster Sleep Ear100 at 99 ILS ([Zap](https://www.zap.co.il/search.aspx?keyword=%D7%90%D7%95%D7%96%D7%A0%D7%99%D7%95%D7%AA%20%D7%A9%D7%99%D7%A0%D7%94)).
- R36S-type console "עם 21000 משחקים": 289 ILS ([Zap](https://www.zap.co.il/search.aspx?keyword=R36S)).
- Searches with no relevant hit on Zap: water ripple lamp, sunrise clock, TV camera backlight, levitating moon lamp, heated eye mask.
- Kids print camera. **REPORTED** (search-result snippets of Bug.co.il):
  - Innova kids printing camera 129.9 ILS ([Bug](https://www.bug.co.il/מצלמת-ילדים-מדפיסה-כחול-itotal-7290115796643)).
  - myFirst Camera Insta 2: 379 ILS ([Bug](https://www.bug.co.il/brand/myfirst/color/blue/camera/insta/2)).
  - Kodak Printomatic 299 ILS.
- Frameo frames. **REPORTED** (search snippets):
  - QUE WF-12T 10.1" at 425 ILS ([PayNGo](https://www.payngo.co.il/338420.html)).
  - Packard Bell Luna 10.1" WiFi at 520 ILS ([Bug](https://www.bug.co.il/brand/packardbell/digital/frame/10/1/luna/wifi/black)).

### Inferences
- Low ad counts mean there is open space in Hebrew advertising. They do not prove demand: the counts are keyword-based, and sellers may use other words.
- The ads that do exist are recent (mostly started after Oct 2026). That points to pre-Hanukkah testing (ESTIMATE).
- The Frameo frame has the best "price anchor" story: Israeli retail is 425–520 versus AliExpress at about 148.
- The meat thermometer can be positioned as "MEATER-style for a third of the price" (MEATER is 699 ILS on Zap).

### Gaps
- Meta counts are ads, not unique advertisers. Only advertisers on the loaded cards were captured (up to about 30 cards).
- Bug and PayNGo prices came from search snippets and were not re-read on the page.

## Q3. Unit economics at CPA 86 ILS: which candidates clear the bar?

### Takeaway
At CPA 86, only items with **landed ≤ ~30% of a ≥249 ILS price** make money. Under conservative shipping (an ESTIMATE where the card did not state free shipping), **clear positives** are:
- the meat thermometer (+41.8 at 249)
- the kids camera (+19.7)
- karaoke (+19.5)
- the grinder set (+14.1)
- the moon lamp (+99.1 at 549)
- the bird feeder (+121, but no demand evidence)

The **Frameo frame (+111), Wacaco (+75), TV backlight (+52), ripple lamp (+58) and R36S (+37) turn positive only if shipping is free or consolidated.**

### Cited Findings
Formula: price/1.18 − 3.6% fees − 5% returns − landed − 86. "Landed" is the Ali card price (FACT) plus a shipping ESTIMATE from the KakoBuy table in file 10 where the card did not show free shipping.

| # | Price (ILS) | Arithmetic | Profit | Landed % |
|---|---|---|---|---|
| W01 ripple | 249 | 211.0 − 9.0 − 10.6 − (47.59 + ship 76) − 86 | **−18.1** (with free shipping: +57.9) | 50% |
| W02 astronaut | 199 | 168.6 − 7.2 − 8.4 − (59.21 + 49) − 86 | **−41.2** (free: +7.8) | 54% |
| W03 TV backlight | 299 | 253.4 − 10.8 − 12.7 − (92.39 + 49) − 86 | **+2.6** (free: +51.6) | 47% |
| W04 moon lamp | 549 | 465.3 − 19.8 − 23.3 − 237.09 − 86 | **+99.1** | 43% |
| W05 Wacaco | 449 | 380.5 − 16.2 − 19.0 − (184.74 + 76) − 86 | **−1.4** (free: +74.6) | 58% |
| W06 meat thermometer | 249 | 211.0 − 9.0 − 10.6 − 63.71 − 86 | **+41.8** | 26% |
| W07 grinder set | 249 | 211.0 − 9.0 − 10.6 − 91.39 − 86 | **+14.1** | 37% |
| W08 sleep headband ×2 | 199 | 168.6 − 7.2 − 8.4 − (2×20.87 + 47) − 86 | **−21.7** (free: +25.3) | 45% |
| W09 sunrise clock | 299 | 253.4 − 10.8 − 12.7 − 140.21 − 86 | **+3.7** | 47% |
| W10 kids print camera | 249 | 211.0 − 9.0 − 10.6 − 85.8 − 86 | **+19.7** | 34% |
| W11 karaoke set | 199 | 168.6 − 7.2 − 8.4 − 47.52 − 86 | **+19.5** | 24% |
| W12 Frameo frame | 449 | 380.5 − 16.2 − 19.0 − (148.11 + ship 130) − 86 | **−18.8** (free: +111.2) | 62% |
| W13 R36S | 299 | 253.4 − 10.8 − 12.7 − (107.47 + 47) − 86 | **−10.5** (free: +36.5) | 52% |
| W14 bird feeder | 599 | 507.6 − 21.6 − 25.4 − 253.24 − 86 | **+121.4** | 42% |
| W15 heated eye mask | 199 | 168.6 − 7.2 − 8.4 − (82.2 + 38) − 86 | **−53.2** (free: −15.2) | 60% |

- Shipping rates used: KakoBuy agent calculator, 2026-11-11, per `10_unit_economics_verification.md` (an upper bound; CJ rates are unverified there).
- Certification flags (ESTIMATE, from product type; not checked against the standards institute):
  - **Toy SI 562:** W10 kids camera, W11 karaoke, W02 projector (if marketed to kids).
  - **Food contact:** W05 espresso, W06 thermometer probe, W07 grinders.
  - **Electrical / adapter safety:** W01, W03, W04, W09, W12, W15.
  - **Wireless (Ministry of Communications type approval):** W03 (BT app), W06, W08, W11, W12 (WiFi), W14 (WiFi camera).
  - **Copyright:** W13 (preloaded ROMs).

### Inferences
- The only items that clear the ~25–30% landed bar on card prices today are **W06 meat thermometer (26%) and W11 karaoke (24%)**. W10 is close at 34%.
- W12 Frameo has the strongest "I need this" and price-anchor case. It needs a real freight quote: at about 1.1 kg, shipping decides the outcome. With free or consolidated shipping it earns about +111 per order at 449, or more at 479–499, still under PayNGo/Bug's 425–520.
- R36S: proven volume, but Zap already sells at 289. Better as a 349 "Hanukkah set" (console, case, second controller) once ROM and IP risk is resolved; this is ESTIMATE.
- Bundling to ≥199 is needed for the headband (two-pack for couples) and grinders (set plus gift box).

### Gaps
- Real shipping per SKU from a CJ account, or whether AliExpress free shipping to IL applies, was not obtained.
- The price existing customers pay for format-B listings is unverified (W04, W06, W09, W10, W11, W12, W14). The real cost could be higher.
- Weights are estimates; none were read from item pages.
