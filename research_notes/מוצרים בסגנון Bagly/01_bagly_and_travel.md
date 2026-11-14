# BAGLY teardown and the travel-abroad product niche for Israelis (research date 2026-11-14)

Labels: **FACT** = read directly in this session from a primary system (store JSON feed, Meta Ad Library page, AliExpress search page), with URL and date. **REPORTED** = secondary source or seller's own marketing claim. **ESTIMATE** = my calculation or inference. **UNVERIFIED** = could not be confirmed.
All store and ad data were read on 2026-11-14 unless stated otherwise. Raw files (products.json, ad-library text dumps, AliExpress dumps) are in `/tmp/claude-0/-home-user-somy/56050f0a-2de7-5734-b72d-e7d3e8ae6cb9/scratchpad/bagly/`.
Cost model: the one in `research_notes/מחקר מוצרים לאיקומרס בישראל/10_unit_economics_verification.md` (Model A, sent direct from China). R = P/1.18; refunds r = 5%; payment and Shopify fees f = 3.6% of P; CPA scenarios 35 / 86 / 175 ILS; USD/ILS 3.17. Contribution = R x 0.95 - f x P - L - CPA. Fixed costs are not included.

Access notes: Meta Ad Library loaded without login. I used a fresh browser context for each query. Only about 25-30 ad cards render per query, because scrolling did not load more, so the counts below are Meta's "about N results" keyword totals plus the cards I could see. Queries returning "אין מודעות שמתאימות" are recorded as zero results. They may be true zeros, or Meta may have matched the exact phrase poorly. AliExpress search loaded without a captcha. Prices shown are "Ship to Israel" storefront prices in USD. I did not open individual listings, so shipping on non-"Free shipping" lines is not known. No Zap or KSP price comparison was attempted. No CBS (gov.il) page was opened; all CBS figures come from press write-ups.

---

## 1. What exactly is BAGLY, and how does its hero product work?

### Takeaway
BAGLY (bagly.co.il) is not a single-product store. It is a Shopify bag brand with 286 products, running since October 2022. Its current hero, and the clear focus of its ads, is **BaglyTravel**: an expandable "under-the-seat" personal-item backpack (40x30x20 cm, 26 expanding to 36 L, 900 g) sold at **389.90 ILS**, with a "compare at" price of 500. The pitch is money, not comfort: "stop paying hundreds of shekels for a suitcase on every flight." In other words, the product pays for itself on the first low-cost flight. That makes it a 390 ILS product that feels cheap. It is not a cheap product.

### Cited Findings
**Store and platform**
- **FACT**: Shopify store. `/meta.json` returns name "Bagly", myshopify domain `bagly-2.myshopify.com`, currency ILS, ships_to_countries ["IL"], and a registered address of **Elizabeth, New Jersey, US**. The store description reads "מגוון תיקים איכותיים לכל מטרה…תיקי גב…תיקי נסיעות" - [bagly.co.il/meta.json](https://bagly.co.il/meta.json)
- **FACT**: 286 products in `/products.json` (250 on page 1, 36 on page 2). The earliest `created_at` is **2022-10-26** (the backpacks "Jerrom", "LaptopBag", "Jack"). The store age is therefore about 4 years. The catalogue spans women's bags, laptop bags, diaper bags, kids' and school bags, wallets, lunch boxes and travel accessories. Newest items: tool bags BaglyPro, BaglySling and BaglyFish (2-3 Nov 2026) and a gun-carry bag (14 Sep 2026) - [bagly.co.il/products.json?limit=250](https://bagly.co.il/products.json?limit=250), [page=2](https://bagly.co.il/products.json?limit=250&page=2)
- **FACT**: Best-selling order on `/collections/all?sort_by=best-selling`: 1) תיק טיסות BaglyTravel, 2) תיק טיפוח Cloud Carry, 3) SafeTravel anti-theft side bag, 4) SecureCarry gun bag, 5) תיק גב Adva, 6) Naama laptop shoulder bag … followed by the Lunch Box set and the BAGLY power bank - [bagly.co.il best-selling](https://bagly.co.il/collections/all?sort_by=best-selling)
- **FACT**: Several product handles are untranslated English AliExpress-style titles, for example `6-pcs-travel-storage-bag-set-for-clothes-tidy-organizer-wardrobe-suitcase-pouch-travel-organizer-bag-case-shoes-packing-cube-bag` and `1l-water-bottle-with-time-marker-32-oz-fitness-...`. This is typical of listings imported with a dropshipping app - [products.json](https://bagly.co.il/products.json?limit=250)
- **FACT**: The travel concept existed before the current hero. "comfort - התיק שמחליף מזוודה וחוסך כסף" was created 2024-04-10 at 419.65 ILS, "תיק טיסות מתרחב MoreSpace" on 2025-05-11 at 239.90, "תיק טיסות OnlyBag" on 2025-05-29 at 448.80, and **BaglyTravel on 2026-01-21** - [products.json](https://bagly.co.il/products.json?limit=250)

**Hero product: BaglyTravel**
- **FACT**: Six colour variants (beige, green, yellow, black, white-black, orange), all 389.90 ILS with compare-at 500.00. Stock is tracked in Shopify (`inventory_management: shopify`). The listing has 22 images - [bagly.co.il/products/תיק-טיסות-baglytravel.json](https://bagly.co.il/products/תיק-טיסות-baglytravel.json)
- **FACT** (product copy): "התיק הזה במידות 40×30×20 ס״מ… עומק 20 ס״מ | מתרחב ל-25 ס״מ, נפח 26 ליטר מתרחב ל-36 ליטר, משקל 900 גרם". It is claimed to meet the personal-item size of "Ryanair, Wizz Air, easyJet, EL AL, Arkia, Israir, Emirates, flydubai, Etihad, Lufthansa, Aegean…". It has a padded laptop sleeve, a trolley sleeve and a hidden pocket. The copy argues: "אתם משלמים מאות שקלים לכל כיוון על משהו שאפשר לוותר עליו לגמרי… נכנס מתחת למושב" - [BaglyTravel page](https://bagly.co.il/products/תיק-טיסות-baglytravel)
- **REPORTED** (seller claim on the page, not verifiable): "מעל ל-23,000 ישראלים מרוצים" and "אלפי לקוחות מרוצים" - [BaglyTravel page](https://bagly.co.il/products/תיק-טיסות-baglytravel)
- **REPORTED**: Wizz Air's free under-seat item is 40x30x20 cm according to retailer and search summaries. I did not check the airline's own page. Branded equivalents exist: Roncato Norway 40x30x20, Samsonite Roadseeker underseat, Cabin Max 24 L - [Alza](https://www.alza.hu/EN/sport/roncato-ryanair-wizz-air-vueling-norway-backpack-40-30-20-cm-d13240868.htm), [bymetz Samsonite](https://bymetz.nl/en/products/samsonite-roadseeker-underseat-backpack-40x30x20.oembed)

**Variants, bundles and upsells (FACT, read from the product page and feed)**
- On the product page: "87% מהלקוחות הוסיפו גם:" offers **Bagly Liquid Kit** (5 bottles of up to 100 ml, 49.90, compare-at 80), **BaglyPillow** (a flight pillow you fill with clothes, 89.90, compare-at 190, created 2026-07-23) and a cable organiser. There is also a "stock clearance: buy a bag and get up to 50% off favourite products" add-on block - [BaglyTravel page](https://bagly.co.il/products/תיק-טיסות-baglytravel)
- Site-wide on 14 Nov 2026: a "BLACK FRIDAY עד 40% הנחה + משלוחים חינם, 20% הנחה נוספים בהזמנה מעל 450₪" banner (countdown to 30 Nov) and a free lead magnet, "כל הסודות והטיפים לשלם פחות מכולם בחו"ל" (a 0 ILS travel-savings guide) - [bagly.co.il](https://bagly.co.il/)
- Related travel SKUs (FACT, from the feed): portable luggage scale 49.90 (created 2025-05-04); "סט יוקרתי לארגון וסידור המזוודה" packing set 85 / 80; ShoeGuard shoe pouches ×5 at 45; SafeTravel anti-theft side bag 199.90 (compare-at 300); Cloud Carry toiletry bag 199.90; CareCase medicine organiser 75; TechCase cable organiser 80; home delivery add-on "D2D" 29.90 - [products.json](https://bagly.co.il/products.json?limit=250)
- Ad coupons (FACT, Ad Library): "קופון 20% הנחה - mybagly20 (להיום בלבד)", "עד 30% הנחה על היחידות האחרונות", and creator codes naama199 and adva199 (adva199 says it "מוריד 90₪ מהמחיר המקורי"). The real selling price is therefore often around 273-312 ILS, not 389.90 - [Ad Library "bagly"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=bagly&search_type=keyword_unordered)

**Reviews**
- **FACT** (JSON-LD aggregateRating embedded in the page): BaglyTravel has **16 reviews, 4.9★**. Visible review dates are 2026-01-22, 2026-04-15, 2026-05-19, 2026-05-31 and 2026-06-08. SafeTravel has **154 reviews, 4.8★** (visible dates April 2024 to June 2025). Cloud Carry has 11 reviews, 5.0★ (Feb-Sep 2026). I did not identify the review app - [BaglyTravel](https://bagly.co.il/products/תיק-טיסות-baglytravel), [SafeTravel](https://bagly.co.il/products/safetravel-תיק-צד-מהפכני-נגד-גניבות), [Cloud Carry](https://bagly.co.il/products/תיק-נשיאה-cloud)

**Delivery and origin**
- **FACT**: "משלוח לנקודת איסוף קרובה לבית בחינם 3-14 ימי עסקים". The shipping policy repeats "זמני המשלוח הינם 3-14 ימי עסקים". Home delivery is a 29.90 add-on, or free above 450 ILS - [shipping policy](https://bagly.co.il/policies/shipping-policy)
- **ESTIMATE**: a 3-14 business-day window, the AliExpress-style handles and a US-registered address all point to a dropship or hybrid model, possibly with local stock for the hero. The scarcity ads ("המלאי האחרון… כמעט אזל") and inventory tracking hint at batch stock, but that is not proven. Origin of the hero is **UNVERIFIED**.

**Meta Ad Library (Israel, active ads, 14 Nov 2026)**
- **FACT**: keyword "bagly" returns "כ-290 תוצאות". Of the 28 cards that rendered, **22 are from the page "BAGLY"** (FB page id 100088106884898). The rest are partnership or creator ads that point to BAGLY.CO.IL, from "נעמה סוויסה" (2), "אורלי יגודייב", "דוד אדרי", "המלצות לפני שטסים" and "אליעד ומאיה - מטיילים, בודקים, ממליצים" - [Ad Library "bagly"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=bagly&search_type=keyword_unordered)
- **FACT**: the oldest still-active BaglyTravel ad started **21 Jan 2026** (library ID 1211954014336481, "2 ads use this creative"). Other start dates seen: 16 and 26 Apr; 4, 9 and 31 May; 11 and 17 Jun; 8 Aug; 14, 15, 16, 22 and 30 Sep; 7, 15, 16, 25, 26 and 31 Oct; 3, 4 and 7 Nov 2026. A celebrity ad ("🚨 קובי מחט בעד תיק הטיסות המהפכני BaglyTravel!") started 31 Oct 2026. One ad is in **Arabic** (15 Sep 2026). There is a founder-voice ad ("עדכון חשוב מנועה, מייסדת BAGLY") and a "מבצע סוכות" ad - [Ad Library "bagly"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=bagly&search_type=keyword_unordered); [Ad Library "מתחת למושב"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%AA%D7%97%D7%AA%20%D7%9C%D7%9E%D7%95%D7%A9%D7%91&search_type=keyword_unordered)
- **FACT**: the main hook appears in at least 8 separate active ads: "כמה פעמים התלהבתם שהטיסה זולה ואז נכנסתם להזמנה וקלטתם - עוד מאות שקלים רק על מזוודה?🤔" (with a 0:31 video). Other angles: "רוצה לדעת איפה חברות התעופה באמת מרוויחות? במזוודות שלך… 350. 450. 600", scarcity ("לצערנו, זה נגמר"), creator storytelling ("פעם אחרונה שאני טסה עם בן הזוג שלי… הדיילת מסתכלת על המזוודה שלו"), and "מספיק ל-5–7 ימי טיסה", "מתרחב עד 38 ליטר" - same source
- **FACT**: BAGLY dominates the keyword "מתחת למושב" (180 results; 17 of the visible cards are BAGLY). It also appears under "מזוודה" (740 results; 4 BAGLY cards), "תיק טיסות", "כבודה", "בלי מזוודה" and "טסים" - [Ad Library "מזוודה"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%96%D7%95%D7%95%D7%93%D7%94&search_type=keyword_unordered)
- **FACT**: the "בגלי" and "BaglyTravel" keyword searches returned zero results, so the ads use the Latin name.

**Social and press**
- **FACT**: the site footer links to [instagram.com/bagly.il](https://www.instagram.com/bagly.il) and [facebook.com/profile.php?id=100088106884898](https://www.facebook.com/profile.php?id=100088106884898). I did not open Instagram, so follower count is unknown. I found no TikTok link.
- **FACT** (negative result): web searches for "BAGLY בגלי מזוודה" and "BAGLY תיקים נועה מייסדת" returned no press coverage - [search run 2026-11-14, no URL]

### Inferences
- **ESTIMATE** (sales signal, ranked by strength): (1) one BaglyTravel creative has run continuously for about 10 months (since 21 Jan 2026), and the store keeps adding new creatives of the same hook into November. Advertisers rarely keep losing ads running that long. This is the strongest public signal, but it is still not proof of profit. (2) Paid creator whitelisting from 5+ creators plus a celebrity (Kobi Mahat) and an Arabic version suggest the hero is being scaled. (3) Best-seller position #1. (4) Only 16 on-site reviews in 10 months, against SafeTravel's 154. That count is weak and does not support "23,000 customers" for this SKU. The 23,000 figure is a store-wide marketing claim. **No sales or revenue figure can be stated.**
- **ESTIMATE**: BAGLY is a "brand umbrella" store. A 286-SKU catalogue, 4 years of history and a founder persona let it re-use one audience across seasons: travel in summer and holidays, school bags in July-August, lunch boxes, tool bags in November. The hero is the paid-traffic entry point, not the whole business.

### Gaps
- Real sales volume, ROAS and the actual landed cost or origin of BaglyTravel are not public.
- Instagram follower count and TikTok activity were not checked. Opening Instagram needs a login.
- Total active ads of the page alone. The keyword count of 290 includes other advertisers, and only 28 cards rendered.

---

## 2. Competitors, AliExpress equivalent and BaglyTravel unit economics

### Takeaway
The under-seat bag is already a crowded Israeli niche. In 2026 alone, at least four Israeli Shopify stores launched 40x30x20 "flight bags" at 179-399 ILS, all with the same "stop paying for a trolley" ad copy. The AliExpress equivalent costs about $28-33 delivered (≈ 90-105 ILS). At list price BaglyTravel's landed cost is about 26% of price, inside the model. It survives the median CPA of 86 ILS with about 114 ILS contribution, but only about 54 ILS at the 20% coupon price, and it loses money at a high CPA when discounted.

### Cited Findings
**Israeli competitors running the same angle (Ad Library and their Shopify feeds, 14 Nov 2026)**
- **FACT**: **KitFlow** (kitflow.co.il; Shopify, address Maoz Hayyim IL). First product 2026-05-12. "תיק טיסות AeroFlow" and "SkyFlow" at 369 (compare-at 550). "ערכת טיסה JetSet / FlyEase" bundles at 559. Organiser set 119, bottle kit "Refill" 49, StepPack shoe pouch 139, DreamKit sleep kit 259. Ads have been active since 12 July 2026: "משלמים מאות שקלים על טרולי בכל טיסה?" - [kitflow.co.il/products.json](https://www.kitflow.co.il/products.json?limit=250); [Ad Library "תיק טיסות"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%AA%D7%99%D7%A7%20%D7%98%D7%99%D7%A1%D7%95%D7%AA&search_type=keyword_unordered)
- **FACT**: **Verra / GATE** (verra.co.il redirects to gatebags.com; Shopify, address Dubai AE, currency ILS). "תיק הנסיעות של GATE" at 299 (compare-at 459). "סט הנוסע החכם" 399-429, couple set 529-559, family set 749, "מארז טיסות שלם" 659, organisers 129, flight pillow 89-99, anti-theft bag 149, bottle set 49, and a "smart traveller course" at 479. Ad on 16 Oct 2026: "מזוודה רגילה עולה לך 150-200 שקל לכיוון. בטיסה אחת חסכת את העלות של התיק" - [gatebags.com feed via verra.co.il](https://verra.co.il/products.json?limit=250); [Ad Library "מתחת למושב"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%AA%D7%97%D7%AA%20%D7%9C%D7%9E%D7%95%D7%A9%D7%91&search_type=keyword_unordered)
- **FACT**: **Rovixo** (rovixo-il.com; Shopify, address Bnei Ayish). Launched 2026-09-24. "ROVIXO GO | תיק נסיעות מתקפל" at 179.90 (compare-at 479.90), 40 L, folds to palm size, "נכנס מתחת למושב". Ads active 26 Oct and 5 Nov 2026 - [rovixo-il.com/products.json](https://rovixo-il.com/products.json?limit=250)
- **FACT**: **Lishon** (lishontov.com; Shopify, Tel Aviv). Compression packing cubes at 219-249, anti-theft side bag 269.90, smart tracker card 179, silicone bottles ×4 at 89, luggage scale 89, neck pillow 129.90, "ערכת טיסה עם טרולי" 379.90, foldable trolley bag 119. Ads: "כמה שילמתם על דמי כבודה בשנה האחרונה?", "עד 60% יותר מקום במזוודה. רוכסן כפול…", "קונים מקומי!" - [lishontov.com/products.json](https://www.lishontov.com/products.json?limit=250); [Ad Library "בלי מזוודה"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%91%D7%9C%D7%99%20%D7%9E%D7%96%D7%95%D7%95%D7%93%D7%94&search_type=keyword_unordered)
- **FACT**: **HomeLuxe** (myhomeluxeshop.com; general gadget store) sells "TravelSmart™" 5-piece packing cubes (ads since 13 Aug and 29 Oct 2026) and "FlyBed - מיטת מטוס לילדים" at 169 (compare-at 289, created 2026-10-27) - [myhomeluxeshop.com/products.json](https://myhomeluxeshop.com/products.json?limit=250)
- **FACT**: traditional retailers also advertise under "מזוודה" and "תיק טיסות": טיטניום (luggage chain), Bagstore (Samsonite), המרכז לתיקים ומזוודות, Super-Pharm Online ("מגוון ענק של מוצרים לנסיעות"), and Loopi (luggage, "עד 80% הנחה") - [Ad Library "מזוודה"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%96%D7%95%D7%95%D7%93%D7%94&search_type=keyword_unordered)

**AliExpress equivalent (ship-to Israel, USD, search page, 14 Nov 2026)**
- **FACT**: "Ryanair Cabin Bags 40x30x20 Underseat Travel Backpack…" sells at **US$30.11, free shipping, 1K+ sold, 4.9★**. Other 40x30x20 listings cost $27.82-$36.36 with free shipping. A "20K+ sold" listing shows $10.66, but that is the new-shopper teaser price; the regular price is $27.82 - [AliExpress search](https://www.aliexpress.com/w/wholesale-under-seat-travel-backpack-40x30x20.html?shipCountry=IL)
- **ESTIMATE**: landed cost L ≈ US$30-33 delivered ≈ **95-105 ILS** per unit, retail one-off. Agent or 1688 bulk pricing would likely be lower but is **UNVERIFIED**. A 0.9-1 kg parcel by the cheapest tracked line costs about $24 to ship (KakoBuy calculator, in note 10), so "free shipping" listings have the freight built into the price. Goods value is below $75, so there is no import VAT on Model A.

**BaglyTravel unit economics (ESTIMATE, Model A, L = 100 ILS)**

| Scenario | P | R | Fees 3.6% | Left before CPA | CPA 35 | CPA 86 | CPA 175 | L / P |
|---|---|---|---|---|---|---|---|---|
| List price | 389.90 | 330.4 | 14.0 | 199.9 | **164.9** | **113.9** | 24.9 | 26% |
| With 20% coupon (mybagly20) | 311.90 | 264.3 | 11.2 | 139.9 | 104.9 | 53.9 | **-35.1** | 32% |
| Competitor price point (KitFlow 369, GATE 299) at 299 | 299 | 253.4 | 10.8 | 130.0 | 95.0 | 44.0 | -45.0 | 33% |

- **ESTIMATE**: with the Liquid Kit (49.90, Ali landed ≈ $7 ≈ 22 ILS) attached at the claimed "87%" rate, each attach adds about 18 ILS of contribution (49.9/1.18×0.95 - 1.8 - 22). An attach rate of 87% is a seller claim and should not be planned on.

### Inferences
- **ESTIMATE**: BaglyTravel passes the earlier screen. The price is ≥199, landed cost at list is ≤30%, and CPA 86 is 22% of list price. It only does so because the item can be priced at 300-390. Copying it as-is in November 2026 means entering against 4+ fresh clones and an incumbent with 10 months of creative learning and creator deals. Rovixo is already undercutting at 179.90.

### Gaps
- No CPA or conversion data exists for any of these stores.
- Bulk FOB price for a 40x30x20 bag was not checked.
- Zap and KSP prices were not checked.

---

## 3. Why does BAGLY's hero work? Success criteria to screen new products

### Takeaway
The product wins on a **quantified saving that exceeds its price**, not on the "cheap" price itself. Baggage fees of 150-600 ILS per direction, against a 390 ILS bag, give an "it pays for itself on one trip" frame. Add a universal, recurring trigger moment (booking a cheap flight), an instantly demonstrable demo (fitting the bag in the sizer or under the seat) and a natural accessory basket.

### Cited Findings
- **FACT**: BAGLY's ad copy anchors on fee numbers ("350. 450. 600"; "חוסך מאות שקלים על כבודה בכל טיול… ובשנה? זה כבר אלפי שקלים"). GATE's copy anchors at "150-200 שקל לכיוון". A Lishon creator ad cites someone who "שילמה 480 שקל על מזוודה" - [Ad Library "bagly"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=bagly&search_type=keyword_unordered); [Ad Library "מתחת למושב"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%AA%D7%97%D7%AA%20%D7%9C%D7%9E%D7%95%D7%A9%D7%91&search_type=keyword_unordered); [Ad Library "קוביות אריזה"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A7%D7%95%D7%91%D7%99%D7%95%D7%AA%20%D7%90%D7%A8%D7%99%D7%96%D7%94&search_type=keyword_unordered)
- **REPORTED**: Israelis made 9.42 M departures in 2025 (section 4), so the trigger repeats many times a year across the population - [ias.co.il](https://www.ias.co.il/?p=168134)

### Inferences (ESTIMATE): success criteria checklist, scored for BaglyTravel
1. **Pain with a price tag**: the product saves a stated amount of money larger than its price (baggage fee 150-600 ILS per direction against 390). ✔ This is the strongest criterion; most "convenience" travel gadgets lack it.
2. **Universal and recurring**: anyone flying low-cost carriers (Wizz, Ryanair, easyJet, Israir/Arkia basic fares) faces it on every booking. ✔
3. **Specific moment of need**: the checkout screen where the luggage add-on appears, and the gate sizer. This makes targeting and copy obvious. ✔
4. **10-second demo**: bag fits under the seat or in the sizer, expands, a week of clothes packed. ✔ Creator storytelling also works (the "boyfriend's suitcase got tagged at the gate" story).
5. **Price ≥199 ILS with high perceived value**: 390 list, about 300 with coupon. This clears the 199 threshold and the 86 ILS CPA. ✔ (Note: it is NOT "cheap"; it is cheap *relative to the saving*.)
6. **Light, small to ship, dropshippable**: 0.9 kg, soft, no battery, no liquids, below $75. ✔
7. **Low return or defect risk**: a soft bag with no sizing issues, though airline-dimension disputes are possible. ✔ (mostly)
8. **Not obviously in local chains at that spec or price**: chains sell Samsonite and Roncato; the generic 40x30x20 is mostly online. ✔ partly
9. **Accessory basket**: liquids kit, packing cubes, pillow and shoe pouches raise AOV. ✔
10. **Seasonal peaks with year-round baseline**: summer, holidays and winter ski trips (section 4). ✔
11. **Weak point**: easy to copy. There are already 4+ clones in 2026, there is no IP, and quality differences are invisible in ads. ✘

---

## 4. How many Israelis fly abroad, and when (seasonality)?

### Takeaway
Israeli departures were 7.08 M in 2024 and 9.42 M in 2025, and 2026 has record late-summer months (August ≈ 1.41 M, September ≈ 1.23 M), even though January-June 2026 ran 12.8% below 2025. Ben Gurion handled about 18.4 M international passengers in 2025, and the IAA expects about 22 M in 2026. Peaks are July-September plus the holiday windows; troughs are November and January-February.

### Cited Findings
- **REPORTED** (CBS via ias.co.il): **2024: 7.084 M** departures of Israelis abroad, -21.7% vs 2023 - [ias.co.il](https://www.ias.co.il/?p=168134)
- **REPORTED** (CBS via press summary): **2025: 9.42 M** departures; August 2025 >1.17 M; September 2025 1,050.4 K (751.6 K in September 2024); December 2025 833.6 K (569 K in December 2024) - [ias.co.il Aug 2025](https://www.ias.co.il/?p=179465); [ice.co.il](https://www.ice.co.il/tourism/news/article/1132661)
- **REPORTED** (CBS via ias.co.il, published 7 Jul 2026): **June 2026: 918.4 K** departures (824.8 K by air), against 487.6 K in June 2025 (+88%). **January-June 2026: 3,364.4 K, against 3,856.6 K in January-June 2025 (-12.8%)**. Seasonally adjusted air departures averaged 512.3 K per month in April-June 2026 - [ias.co.il](https://www.ias.co.il/?p=189420). The reason for the weak H1 2026 is **UNVERIFIED** in this session.
- **REPORTED** (Bizportal, secondary): **August 2026 ≈ 1.41 M** (all-time monthly record) and **September 2026 ≈ 1.23 M** (record for September). Top destinations: Greece, Cyprus, Italy, UAE, USA, Germany - [Bizportal](https://www.bizportal.co.il/airlines/news/article/20044223)
- **REPORTED**: other months for scale: August 2024 844.4 K; November 2024 ≈ 429.6 K - [ias.co.il Aug 2024](https://www.ias.co.il/?p=162254); [ias.co.il Nov 2024](https://www.ias.co.il/?p=166814)
- **REPORTED** (IAA via JNS): **18.4 M** international passengers at Ben Gurion in 2025, +33% vs 2024. Greece 2.2 M, USA 1.6 M, UAE 1.5 M, Italy and Cyprus 1.2 M each. El Al's share fell to 37% from 48%. The IAA expects **≈22 M in 2026** - [JNS](https://www.jns.org/israel-news/18-4-million-passengers-travelled-through-ben-gurion-airport-in-2025)

### Inferences
- **ESTIMATE**: El Al's falling share and the top destinations (Greece, Cyprus, Italy: short-haul, heavy on low-cost and charter flights) are exactly where personal-item-only fares apply. That is the structural tailwind behind the under-seat bag.
- **ESTIMATE**, ad calendar: start creatives 3-6 weeks before each peak. That means about late February to March for Passover (April), May for summer (June-September, the largest), August for the Tishrei holidays (September-October), and November for Hanukkah and ski or Christmas-market trips (December). BAGLY's active ad start dates (April, May-June, September-October, November) match this pattern. November itself is a trough month for departures, but Black Friday offsets it for gifting.
- **ESTIMATE**: market size. With about 9-10 M departures per year (a person can count several times), even a 0.1% purchase rate is about 9-10 K units per year across all sellers. This is an illustration, not a forecast.

### Gaps
- Official CBS monthly tables for 2026 were not opened (gov.il was blocked in earlier research). Holiday-specific departure counts for Passover and Sukkot were not found.

---

## 5. Which travel-pain products are sold in Israel via DTC and Meta ads? Product-by-product

### Takeaway
Paid DTC travel activity in Israel clusters around (a) under-seat bags, (b) compression and packing cubes, (c) flight pillows and sleep kits, (d) anti-theft bags and (e) bundles or "flight kits". Small accessories (bottles, scale, AirTag holder, shoe pouch) sell at 39-139 ILS, but only as add-ons. Only items that can carry ≥199 ILS, or bundles, pass the cost model.

### Cited Findings and per-product verdicts
(Israeli prices are FACT from store feeds read on 14 Nov 2026. Ad activity is FACT from Ad Library IL keyword searches on 14 Nov 2026. AliExpress prices are FACT from search pages, regular non-new-shopper price, ship to IL; shipping is included only where the listing showed "Free shipping".)

| Product | Israeli sellers & ILS price | Ad activity seen (IL, active) | AliExpress (USD) | Verdict (ESTIMATE) |
|---|---|---|---|---|
| Under-seat 40x30x20 bag | BAGLY 389.90; KitFlow 369; GATE/Verra 299; Rovixo 179.90 | Heavy: BAGLY 20+ ads plus creators; KitFlow 6+; Rovixo; Verra. "מתחת למושב" 180 results | $27.8-36.4, free shipping; top listing 1K+ sold | Proven demand, now crowded. Enter only with a differentiated bundle or angle |
| Compression / packing cubes | Lishon 219-249; KitFlow organisers 119; GATE 129 (2 sets 179); BAGLY packing set 80-85; HomeLuxe TravelSmart | "קוביות אריזה" 29 results (Lishon, HomeLuxe, an advertorial page "אריאלה זמיר" with 6 ads) | 4-6 pc sets $3-10; BAGSMART 6 pc $25.97; vacuum-style cubes $5.5 | Works at ~219 only with a strong "fit two weeks into a trolley" demo; otherwise an add-on |
| Vacuum bags with pump | none seen in Israeli DTC feeds | "שקיות ואקום": 0 results | $7-13 with USB pump (5K+ sold) | Visual demo, but a battery or pump complicates shipping and quality. Add-on |
| Liquid-bottle kits | BAGLY 49.90; KitFlow 49; GATE 49; Lishon 89 (4 silicone) | Only as upsells ("ערכת נוזלים": 0 results) | $5.9-8.5 sets (700-1,000+ sold) | Add-on only (perfect for raising AOV) |
| Luggage scale | BAGLY 49.90; Lishon 89 | none found ("משקל מזוודה": 0 results) | $0.7-3.7 (100K+ sold) | Add-on or free gift only |
| Tracker / AirTag holder | Lishon smart tracker card 179 | "AirTag" 820 results, almost all foreign (Spotminders, US advertorials) | holders $1.6-6.6 (10K+ sold); tracker cards not checked | A Find-My tracker card at 149-179 might work as "lost luggage" insurance; check certification and battery shipping. Holders: add-on |
| Neck / flight pillow | BAGLY clothes-pillow 89.90; GATE 89-99; Lishon 129.90; Selera gel pillow 199.90; FlyHugz (US brand advertising in IL, $49.90-54.95) | "כרית טיסה" 51 results; FlyHugz and Selera ("טיולים בלי כאב", flight-attendant advertorial) active | clothes-storage pillow $2.9-7.5; | Low price ceiling unless "patented" style (FlyHugz). Add-on or bundle |
| Anti-theft sling | BAGLY SafeTravel 199.90 (154 reviews, the most-reviewed BAGLY item); Lishon 269.90; GATE 149 | Present inside travel stores' ads; "נגד כייסים": 0 results | $6.4-17.4 (1K-10K+ sold) | Passes at ~199 (contribution ≈20 at CPA 86). Good second hero for Europe trips |
| Travel adapter | none seen in DTC | "מתאם חשמל" 24 results, none travel | $11-20 USB-C universal | Electrical; standards and certification risk; low ad presence. Skip |
| Kids' flight bed / footrest | HomeLuxe FlyBed 169 (compare-at 289) | "מיטת מטוס": 0 results | $7.6-23 (inflatable and footrest; 1K-10K+ sold) | Family niche with clear demo; sell as a 2-pack or with a kids' kit at 299-349 |
| Toiletry / hanging bags | BAGLY Cloud Carry 199.90 (#2 best-seller); KitFlow CareCase or HangCase 149; Rovixo organiser 119.90; GATE 119 | Inside travel brand ads | hanging toiletry $6-13 | Good add-on; can be a ≥149 item for women's audiences |
| Shoe bags | BAGLY ShoeGuard 45 (×5); KitFlow StepPack 139; Lishon 59.90 | none seen | (not checked) | Add-on |
| Medicine organiser / cooler | BAGLY CareCase 75; Lishon 89.90; MediGuard Israel (medication cooling, ad 1 Oct 2026) | small | (not checked) | Niche; MediGuard shows a medical-travel angle |
| Bundles / "flight kits" | KitFlow JetSet / FlyEase 559; GATE "סט הנוסע החכם" 399-429, couple 529-559, family 749, "מארז טיסות שלם" 659; Lishon "ערכת טיסה עם טרולי" 379.90 | KitFlow and GATE ads | sum of parts | The clearest AOV route; competitors already do couple and family sets |

Sources for the table: [kitflow.co.il feed](https://www.kitflow.co.il/products.json?limit=250), [verra.co.il / gatebags feed](https://verra.co.il/products.json?limit=250), [lishontov.com feed](https://www.lishontov.com/products.json?limit=250), [rovixo-il.com feed](https://rovixo-il.com/products.json?limit=250), [myhomeluxeshop.com feed](https://myhomeluxeshop.com/products.json?limit=250), [selera.co.il feed](https://selera.co.il/products.json?limit=250), [flyhugz.com feed](https://flyhugz.com/products.json?limit=250), [bagly.co.il feed](https://bagly.co.il/products.json?limit=250); Ad Library IL keyword searches for [כרית טיסה](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9B%D7%A8%D7%99%D7%AA%20%D7%98%D7%99%D7%A1%D7%94&search_type=keyword_unordered), [AirTag](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=AirTag&search_type=keyword_unordered), [מתאם חשמל](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%AA%D7%90%D7%9D%20%D7%97%D7%A9%D7%9E%D7%9C&search_type=keyword_unordered), [כבודה](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9B%D7%91%D7%95%D7%93%D7%94&search_type=keyword_unordered); AliExpress searches for [travel bottles](https://www.aliexpress.com/w/wholesale-travel-bottles-set-tsa.html?shipCountry=IL), [luggage scale](https://www.aliexpress.com/w/wholesale-digital-luggage-scale.html?shipCountry=IL), [compression cubes](https://www.aliexpress.com/w/wholesale-compression-packing-cubes.html?shipCountry=IL), [pillow storage](https://www.aliexpress.com/w/wholesale-travel-pillow-storage-clothes.html?shipCountry=IL), [vacuum bags](https://www.aliexpress.com/w/wholesale-vacuum-compression-bags-travel.html?shipCountry=IL), [kids airplane bed](https://www.aliexpress.com/w/wholesale-airplane-bed-for-kids-inflatable-footrest.html?shipCountry=IL), [AirTag holder](https://www.aliexpress.com/w/wholesale-airtag-luggage-tag-holder.html?shipCountry=IL), [travel adapter](https://www.aliexpress.com/w/wholesale-universal-travel-adapter-usb-c.html?shipCountry=IL), [anti-theft sling](https://www.aliexpress.com/w/wholesale-anti-theft-sling-bag-travel.html?shipCountry=IL), [hanging toiletry](https://www.aliexpress.com/w/wholesale-hanging-toiletry-bag-travel.html?shipCountry=IL).

### Inferences
- **ESTIMATE**: a "zero results" search here means no Israeli advertiser uses that Hebrew phrase in its copy, not that there is no demand. Small accessories show no Israeli ad activity because they cannot carry a CPA alone. Sellers place them in carts as upsells.
- **ESTIMATE**: the Israeli travel-DTC wave is very recent. KitFlow (May 2026), GATE travel bags (May 2026), Lishon (December 2025 onwards; travel items July-November 2026), Rovixo (September 2026) and HomeLuxe FlyBed (October 2026) all appear to have launched after summer 2025, when departures surged. Expect fast copying of any new winner.

### Gaps
- TikTok Ads Library and TikTok organic were not checked.
- AliExpress shipping for non-free-shipping listings, and supplier quality, were not checked.
- Prices for Find-My tracker cards on AliExpress were not checked.
- KSP, Zap and local-chain shelf prices (Super-Pharm, ACE, טיטניום) for these accessories were not checked.

---

## 6. Shortlist: the 3-5 best travel products or bundles, with profit scenarios

### Takeaway
Do not clone the BAGLY bag head-on. The better options sit next to it: (1) a differentiated under-seat bag plus flight-kit bundle at about 449, (2) a kids' flight comfort pack sold for families at about 349 for two, (3) an anti-theft sling at about 199 aimed at Europe city trips, and (4) a "fit two weeks into a trolley" compression system at 199-249, best used as an AOV booster. Every scenario turns negative at a 175 ILS CPA, and only the 449 bundle and BAGLY-level pricing absorb a CPA of 86 comfortably.

### Cited Findings
Inputs as cited above: Ali prices (FACT, search pages 14 Nov 2026), competitor prices (FACT, feeds), and the cost model from note 10.

### Inferences: profit scenarios (ESTIMATE, Model A, r = 5%, fees 3.6%, contribution per order in ILS before fixed costs)

| # | Offer | P | Landed L (basis) | L/P | Left before CPA | CPA 35 | CPA 86 | CPA 175 | Competition |
|---|---|---|---|---|---|---|---|---|---|
| 1 | "Fly carry-on only" bundle: 40x30x20 expandable bag + liquids kit + 3-piece compression cubes (+ luggage scale as a free gift) | 449 | 155 (bag ~100 + bottles ~22 + cubes ~30, ~$49 total, under $75) | 35% | 190.3 | 155.3 | **104.3** | 15.3 | High (KitFlow 559 kits, GATE 399-659 sets) |
| 1b | Same bag alone, BAGLY price | 389.90 | 100 | 26% | 199.9 | 164.9 | **113.9** | 24.9 | Very high |
| 1c | Same bag alone, at the competitor-war price 299 | 299 | 100 | 33% | 130.0 | 95.0 | 44.0 | -45.0 | Very high |
| 2 | Kids' flight bed / inflatable footrest, family 2-pack (+ kids' activity pouch) | 349 | 96 (2 × ~$15 delivered) | 28% | 172.4 | 137.4 | **86.4** | -2.6 | Low (only HomeLuxe at 169 seen) |
| 2b | Kids' flight bed, single | 199 | 48 | 24% | 105.0 | 70.0 | 19.0 | -70.0 | Low |
| 3 | Anti-theft sling (slash-proof, RFID, hidden zip), Europe-trip angle | 199.90 | 48 (~$15 delivered) | 24% | 105.7 | 70.7 | 19.7 | -69.3 | Medium (BAGLY SafeTravel 199.90 with 154 reviews, Lishon 269.90, GATE 149) |
| 4 | Compression packing system (6 cubes + shoe bags + bottles) | 199 | 63 (~$20 delivered from one supplier) | 32% | 90.0 | 55.0 | 4.0 | -85.0 | Medium (Lishon 219-249, KitFlow 119, GATE 129-179) |

Comments (all ESTIMATE):
- **#1 bundle** is the best fit to the "BAGLY criteria" and the cost model. It keeps the quantified-saving hook (no suitcase fee), and the bundle makes the offer harder to compare with BAGLY, KitFlow or Rovixo on price. A couple or "2 bags" pack (≈ 749-799) lifts contribution further but may exceed the $75 import threshold if shipped as one parcel; check the 72-hour aggregation rule from note 10. The angle needs to be differentiated: for example "family of four flies carry-on" sets, or a stated airline-by-airline fit guarantee.
- **#2 kids' flight pack** has a strong 10-second demo (child lying flat across the seat), an emotional pain (long-haul flights with toddlers), almost no Israeli competition in ads and a natural 2-pack. Risks: some airlines restrict inflatable footrests (needs checking per airline, **UNVERIFIED**), and parents of small children are a narrower audience than all flyers.
- **#3 anti-theft sling**: BAGLY's own 154-review count on SafeTravel since 2024 is the only review-volume evidence in this research that a travel item sells repeatedly in Israel at about 199. Margin at a CPA of 86 is thin (≈20), so it needs a low CPA or an add-on such as an RFID passport cover.
- **#4 compression system** barely breaks even at the median CPA. Use it as an order bump or upsell, or price it at 249 with a strong before/after video. Lishon prices at 219-249.
- Not shortlisted: luggage scale, AirTag holders, bottles and shoe bags (price ceilings 39-139), travel adapters (electrical certification), vacuum bags with electric pumps (battery or shipping hassle). A Find-My tracker card at 149-179 (Lishon) is a possible fifth candidate pending certification and battery-shipping checks.

### Gaps
- Real CPAs for travel products in Israel are unknown. The 35 / 86 / 175 ILS scenarios are the general Israeli store range.
- Landed costs are retail AliExpress prices with free shipping, not agent or CJ quotes.
- Airline rules on kids' inflatable footrests were not verified.
- Whether the partners can differentiate the bag (custom design or logo, minimum order quantity) was not checked.
