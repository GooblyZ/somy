# Lens "tiktok": what is selling in high volume on TikTok Shop now (Aug–Nov 2026), and does it fit Israel

Prepared 2026-11-15. JSON: `01_tiktok.json` (25 products, each with ali_url + image_url; all 25 image URLs returned HTTP 200 on 15/11/2026).
Labels: FACT = primary/first-party; REPORTED = third-party article citing an analytics tool; ESTIMATE = analytics-tool estimate (TokConnect / FastMoss / FindNiche / Kalodata all estimate from public TikTok data); UNVERIFIED = could not confirm.

## Q1. Which sources were usable, and which were blocked?

### Takeaway
TikTok Creative Center gave no product data without a login, so the hard numbers come from public pages of FastMoss, TokConnect, FindNiche and Kalodata (via NetInfluencer). Recent product-level data was found for the **US only**. For UK, Germany and SEA, the only data found is older or category-level.

### Cited Findings
- **TikTok Creative Center "Top products" was BLOCKED/REDIRECTED.** In headless Chromium, `ads.tiktok.com/business/creativecenter/top-products/pc/en` landed on the "Creative Studio / Symphony" marketing page, with only a "Log in" option and no product table. The Top Ads page also returned no ad data. I did not log in. (Tested 15/11/2026.)
- TokConnect "Best Sellers", TikTok Shop US, 30 days to 11/11/2026, estimated revenue and units for 50 products (retrieved 13/11/2026) — [TokConnect](https://tokconnect.com/trends/products/best-sellers/)
- FastMoss "Holiday Gift Ideas 2026: 42 Top Sellers": US units for 1–31 Oct 2026, prices as of 4/11/2026 — [FastMoss](https://www.fastmoss.com/blog/tiktok-shop-holiday-gift-ideas-2026/)
- FastMoss "Best-Selling Products by Category (US)": week of 19–25 Oct 2026 — [FastMoss](https://www.fastmoss.com/blog/best-selling-products-by-category/)
- FastMoss toys article (10/11/2026): Oct 2026 and week-of-2-Nov-2026 toy ranks, plus daily-unit trends — [FastMoss](https://www.fastmoss.com/blog/best-selling-toys-on-tiktok-shop-what-sold-last-christmas-and-whats-trending-for-2026/)
- Kalodata data for the top 10 of Sept 2026, via NetInfluencer (published 15/10/2026) — [NetInfluencer](https://www.netinfluencer.com/top-10-products-sold-on-tiktok-shop-in-september-2026/)
- FindNiche trending Home Supplies US (dataset 1/11/2026; its GMV column is internally inconsistent for some rows) — [FindNiche](https://findniche.com/tiktok/trending-home-supplies-products-us)
- UK: FastMoss UK Jan–May 2026 (updated 19/6/2026) is the most recent UK product list I found — [FastMoss UK](https://www.fastmoss.com/blog/best-selling-tiktok-shop-products-uk-2026/). FindNiche UK Home Supplies (1/11/2026) ranks shops only, with no products — [FindNiche GB](https://findniche.com/tiktok/top-sellers-home-supplies-gb)
- Germany: household appliances were the largest TikTok Shop category in Germany, 17.1% of GMV in Q2 2026 (Lengow/Kalodata, as summarised in search results) — [Lengow](https://blog.lengow.com/tiktok-shop-europe-q2-2026-e500m-across-four-markets/)
- SEA: the latest EchoTik weekly list with product types is week 26 (22–28 Jun 2026). Thailand #1 was UV umbrellas; Malaysia included portable fans and bubble wrap. It gives no units — [EchoTik](https://www.echotik.live/blog/tiktok-shop-weekly-ranking/)
- SellTheTrend "Top Selling TikTok Shop" (15/11/2026) shows implausible numbers (about 9.5M identical units for two medicube SKUs), so I **discarded** it — [SellTheTrend](https://www.sellthetrend.com/reports/top-selling-tiktok-shop)
- Press: BuzzFeed's 21/10/2026 "useful TikTok-famous products" (Laundry Turtle, Deli ProKeeper, foaming drain cleaner) is affiliate content with no sales data, so it is used as leads only — [BuzzFeed](https://www.buzzfeed.com/dayshavedewi/useful-tiktok-famous-products-oct-2026-an)

### Inferences
- The US data covers three overlapping windows (Sept monthly, Oct monthly / 19–25 Oct weekly, and the 30 days to 11 Nov). A product that appears in two or more windows is treated as sustained rather than a spike: magnetic power bank, speaker stand, jelly bra, shapewear bodysuit, Comfrt blanket, fleece tights, squishy advent.
- Beauty (medicube, perfume, supplements) dominates US GMV. Under the brief I left out cosmetics, perfume and supplements.

### Gaps
- No public Oct–Nov 2026 product-level ranking was found for the UK, Germany, Indonesia, Thailand, Vietnam, the Philippines or Malaysia. Kalodata, Tabcut, Shoplus, Pipiads and Minea product lists need a login or paywall and were not accessed. No Oct–Nov 2026 NYPost, Business Insider or TODAY TikTok roundup with sales data turned up.
- First-week Black Friday 2026 data (campaign 11–30 Nov) is not yet published.

## Q2. Which physical, non-excluded products show high, sustained TikTok Shop volume now? (per-product evidence)

### Takeaway
The strongest non-beauty volume is in: **power and lighting gadgets** (magnetic power bank about 66K units in 30 days, 4-pack foldable LED lanterns about 70K), **winter comfort and fashion** (shapewear bodysuit about 103K, jelly bra about 98K, fleece tights about 46K, Comfrt wearable blanket about 34K at $90), and **squishy toys** (the #1 US toy trend: squishy advent calendar about 35K in October and about 30K in the first week of November). Home and cleaning items are smaller but steady.

### Cited Findings
Unit numbers are TikTok Shop US estimates unless stated otherwise. "30d" means the 30 days to 11/11/2026 ([TokConnect](https://tokconnect.com/trends/products/best-sellers/)). "Oct" means Oct 2026 ([FastMoss gifts](https://www.fastmoss.com/blog/tiktok-shop-holiday-gift-ideas-2026/)). "Wk" means 19–25 Oct 2026 ([FastMoss category](https://www.fastmoss.com/blog/best-selling-products-by-category/)).

**Gadgets / power / car**
1. Foldable LED lanterns 4-pack: 30d about 70,245 units, $1.33M, #12 overall (ESTIMATE) — [TokConnect](https://tokconnect.com/trends/products/best-sellers/)
2. XMWUS 5000mAh magnetic power bank: 30d 65,731 units / $723K; Oct 45,489; Wk 13,207 (#1 Phones & Electronics) (ESTIMATE) — [TokConnect](https://tokconnect.com/trends/products/best-sellers/); [FastMoss](https://www.fastmoss.com/blog/tiktok-shop-holiday-gift-ideas-2026/); [FastMoss](https://www.fastmoss.com/blog/best-selling-products-by-category/)
3. SEESE turbo-jet cordless blower: 30d 31,042 units / $939K (ESTIMATE). AliExpress jet-fan listing shows 50K+ sold — [TokConnect](https://tokconnect.com/trends/products/best-sellers/)
4. SEESE cordless pressure washer gun: #6 in Sept 2026, $1.67M, −26% vs Aug (REPORTED, Kalodata). EchoTik also lists car-washing tools in the US top for week 26 — [NetInfluencer](https://www.netinfluencer.com/top-10-products-sold-on-tiktok-shop-in-september-2026/); [EchoTik](https://www.echotik.live/blog/tiktok-shop-weekly-ranking/)
5. PUTARE 5-in-1 induction speaker + wireless-charger stand: 30d 41,582 units / $790K; Oct 34,961; Wk 8,214 (#3) (ESTIMATE) — [TokConnect](https://tokconnect.com/trends/products/best-sellers/); [FastMoss](https://www.fastmoss.com/blog/tiktok-shop-holiday-gift-ideas-2026/)
6. $12.60 wireless 1080P doorbell camera (Lunelyx): Oct 27,757 units (ESTIMATE) — [FastMoss](https://www.fastmoss.com/blog/tiktok-shop-holiday-gift-ideas-2026/)
7. Drizzly 5000mAh mini power bank: Oct 19,127 units (ESTIMATE) — [FastMoss](https://www.fastmoss.com/blog/tiktok-shop-holiday-gift-ideas-2026/)

**Toys / Q4 gifts**
8. Advent calendar with 24 mini squishies: Oct 35,294 units, #1 toy in the gift guide. "Dumpling Squishy Christmas Advent Calendar": #1 toy in the week of 2 Nov 2026 with 30,355 units / $424,970, and #2 in Oct with $535,649. The Classic & Novelty squishy subcategory sold 1,671,880 units in Oct 2026 (ESTIMATE) — [FastMoss toys](https://www.fastmoss.com/blog/best-selling-toys-on-tiktok-shop-what-sold-last-christmas-and-whats-trending-for-2026/); [FastMoss gifts](https://www.fastmoss.com/blog/tiktok-shop-holiday-gift-ideas-2026/)
9. Dumpling squishies: JOYIN Christmas dumpling set Oct 23,649; dumpling-in-steamer phone charm Oct 23,464; Noodle squishy #3 in the week of 2 Nov ($184,646) (ESTIMATE) — same sources
10. DIY mochi squishy kit: Julutile 30d 26,512 units / $701K and #1 toy GMV in Oct ($574,622); PlayMagix kit Oct 21,844 units (ESTIMATE) — [TokConnect](https://tokconnect.com/trends/products/best-sellers/); [FastMoss toys](https://www.fastmoss.com/blog/best-selling-toys-on-tiktok-shop-what-sold-last-christmas-and-whats-trending-for-2026/)
11. Cheese-cube squishy: Oct 15,725 units (ESTIMATE). The AliExpress listing shows 30K+ sold — [FastMoss gifts](https://www.fastmoss.com/blog/tiktok-shop-holiday-gift-ideas-2026/)
12. Energy-drink-can plush: Oct 25,515 units (#3 toy in the gift guide) (ESTIMATE) — [FastMoss gifts](https://www.fastmoss.com/blog/tiktok-shop-holiday-gift-ideas-2026/)
13. Hand-casting kit (Luna Bean): 24,898 units in Dec 2025. Daily units rose from 95 to 118 (+24%) between 28 Oct–3 Nov and 4–10 Nov 2026 (ESTIMATE) — [FastMoss toys](https://www.fastmoss.com/blog/best-selling-toys-on-tiktok-shop-what-sold-last-christmas-and-whats-trending-for-2026/)

**Fashion / winter**
14. KKPeople tummy-control bodysuit: 30d 103,451 units / $2.59M; Wk 21,399 (#1 Womenswear) (ESTIMATE) — [TokConnect](https://tokconnect.com/trends/products/best-sellers/); [FastMoss](https://www.fastmoss.com/blog/best-selling-products-by-category/)
15. OEAK jelly wirefree bra: 30d 97,675 units / $1.54M; Wk 19,698 (ESTIMATE) — same sources
16. Fleece-lined "magic skin" translucent tights: 30d 46,048 units / $646K; SWEET MAYHEM Wk 13,552 (ESTIMATE) — same sources
17. HOMUG men's fleece-lined tactical cargo pants: 30d 24,855 units / $671K (ESTIMATE) — [TokConnect](https://tokconnect.com/trends/products/best-sellers/)
18. Comfrt "Dreamer" oversized wearable blanket: 30d 34,043 units / $3.07M (#3 overall); Sept #2 at $2.56M (+13%, Kalodata); Oct 27,798 units. A double-sided fleece robe did 30d 20,018 units — [TokConnect](https://tokconnect.com/trends/products/best-sellers/); [NetInfluencer](https://www.netinfluencer.com/top-10-products-sold-on-tiktok-shop-in-september-2026/); [FastMoss](https://www.fastmoss.com/blog/tiktok-shop-holiday-gift-ideas-2026/)
19. TYMO automatic curler: 30d 19,468 units / $876K (ESTIMATE) — [TokConnect](https://tokconnect.com/trends/products/best-sellers/)

**Home / cleaning / kitchen / sleep**
20. Gap-cleaning tool (SOPAMI): #1 in Home Supplies in the week of 19–25 Oct 2026. FastMoss excluded it from the table and gave no units (REPORTED rank only) — [FastMoss](https://www.fastmoss.com/blog/best-selling-products-by-category/)
21. Dryer-vent lint cleaner kit: #5 trending home supplies, 90.29K cumulative units, 1.64K orders in 7 days, $14.99 (ESTIMATE) — [FindNiche](https://findniche.com/tiktok/trending-home-supplies-products-us)
22. African net bath sponge (2-pc): #1 trending home supplies, 151.32K cumulative units, 2.43K orders in 7 days, $6.99 (ESTIMATE) — [FindNiche](https://findniche.com/tiktok/trending-home-supplies-products-us)
23. Overnight-oats containers: #8, 33.11K cumulative units, 1.47K orders in 7 days (ESTIMATE) — [FindNiche](https://findniche.com/tiktok/trending-home-supplies-products-us)
24. Cooling memory-foam neck/contour sleep pillow (VIPfree): Oct 46,017 units (#1 bedding). Nuzzle 20,115; DeepAir contour 12,012 (ESTIMATE) — [FastMoss](https://www.fastmoss.com/blog/tiktok-shop-holiday-gift-ideas-2026/)
25. UK handheld pressurised steam cleaner (Redhut): £939,884 from 36,254 orders in Jan–Feb 2026, then faded (REPORTED) — [FastMoss UK](https://www.fastmoss.com/blog/best-selling-tiktok-shop-products-uk-2026/)

**Seen but left out:** press-on nails, R36S, the magnetic car phone holder ($59.99, probably the excluded vacuum MagSafe mount), and the initial charm bracelet (too close to the excluded name necklaces and Italian charms). Also left out because they are bulky or high-ticket: Shark vacuum, EcoFlow/Jackery, the bamboo mattress topper and wiggle cars. Cosmetics, perfume and supplements are out per the brief.

### Inferences
- The Q4 lift is real at category level. In 2025, US toys units rose 87.5% and Phones & Electronics 35.7% from October to November (FastMoss, [gifts article](https://www.fastmoss.com/blog/tiktok-shop-holiday-gift-ideas-2026/)). Squishies, power banks and winter wear should keep rising through December.
- The pressure washer gun looks seasonal (summer) and fading. The steam cleaner peaks in January in the UK, which maps to Pesach cleaning in Israel (Mar–Apr 2027).

### Gaps
- There are no unit numbers for the #1 gap-cleaning tool. The PUTARE speaker stand has no close AliExpress twin: I matched a generic "wireless charger with speaker stand" (258 sold), so treat that match as approximate.

## Q3. AliExpress matches and Israeli presence (Meta Ad Library, country=IL)

### Takeaway
All 25 products have an AliExpress listing (headless search sorted by orders, IL/ILS cookie, 15/11/2026). In Israeli Meta ads the crowded items are the jelly bra (about 110 ads), turbo blower (about 24) and emergency lanterns (about 190 under "פנס חירום"). Wearable blanket, hand-casting kit, fleece tights, the doorbell camera and the squishy advent calendar showed little or no Hebrew advertising, but several of those zeros may be false.

### Cited Findings
- AliExpress method: `aliexpress.com/w/wholesale-<terms>.html?SortType=total_tranpro_desc`. `ali_price_ils` in the JSON is the regular or strike-through price shown on the card. `ali_promo_price_ils` is the new-shopper promo price (for example ₪3.59), so the true regular price is somewhere between the two. Sold counts are as shown on the card (for example "50K+", "10,000+").
- Meta Ad Library IL, active ads, keyword search, fresh browser context per query, 15/11/2026 (count shown by the library):
  - "חזיית ג'לי" ~110 (יעל רז, Virella, LAOR, הבית להלבשה תחתונה, Seeya Active)
  - "פנס חירום" ~190 / "פנס קמפינג" ~13
  - "מכנסי דגמח" ~91 (Terminal X, Delta, Mania Jeans)
  - "מפוח טורבו" ~24 (טול מרקט, ציוד הבית המודרני, שלבי)
  - "בגד גוף מחטב" ~13 (Zohara Tights, NoodySkin, BunnyTummy)
  - "מנקה קיטור" ~11 (Uwant Israel, הידרו סטאר, אלקטרו גל)
  - "סקווישי" ~13 / "squishy" ~590
  - "גרביונים חמים" ~4
  - "מטען נייד קטן" ~3
  - "מטען נייד מגנטי" ~2
  - "מסלסל שיער אוטומטי" ~2
  - "ניקוי מייבש כביסה" ~2 (שופרסל)
  - "מברשת חריצים" ~2
  - "אקדח שטיפה נטען" ~1
- **False-zero warning:** these queries returned an identical short page (571 characters, no result count), so they are UNVERIFIED rather than true zeros: פנס קמפינג מתקפל, רמקול אינדוקציה, פעמון וידאו (אלחוטי), גרביונים פליז, מכנסיים טקטיים, שמיכה עם קפוצ'ון / שמיכה לבישה, מברשת ניקוי חריצים, ספוג אפריקאי, יציקת ידיים / ערכת יציקה, כרית ארגונומית / אורתופדית, אוברנייט, לוח אדוונט, בובת פחית, מטען אלחוטי רמקול. When I re-ran one such query ("ספוג רשת") it returned ~38 results, which confirms the load failures.

### Inferences
- I found no Israeli retail prices in this pass, so `price_israel` is null throughout.

### Gaps
- The false-zero Meta queries should be re-checked manually in a normal browser. I did not check Israeli marketplaces (KSP, Ivory, Shufersal online, Zap price comparison).

## Q4. Top 5 for Israel and why

### Takeaway
1. **Oversized wearable sherpa blanket hoodie (tiktok-17).** US sales are high and sustained across Sept–Nov (Comfrt is #3 overall at $3.07M over 30 days), the Israeli winter gift season is starting, and I saw no targeted Hebrew ads (unverified). It works for couples, students and parents, and the demo is easy. Watch the bulky shipping and avoid copying the Comfrt brand.
2. **Foldable LED lantern 4-pack (tiktok-1).** At about 70K units in 30 days it is the top gadget by units. It fits the Israeli emergency/ממ"ד kit plus camping, and the 4-pack reads as a deal. The generic "פנס חירום" category is crowded (~190 ads), but the collapsible 4-pack format looks free. Sell it as "פנס לכל חדר" (a lantern for every room).
3. **Squishy surprise box adapted to Hanukkah, "8 לילות 8 הפתעות" (tiktok-8, with 9, 11).** Squishies are the #1 US toy trend right now (1.67M units in October in the subcategory, the advent calendar #1 toy in the week of 2 Nov). In Israel there are only about 13 Hebrew "סקווישי" ads, and I found no Hanukkah version. **This is time-critical:** Hanukkah begins on the evening of about 4/12/2026, so it needs local stock or fast shipping now. Toy standards (ת"י 562) apply.
4. **Fleece-lined "translucent" tights (tiktok-13).** About 46K units in 30 days plus a week-of-Oct-19 top-5 rank, so the demand is sustained. It solves a real winter problem (wearing dresses or skirts to work, religious-modest dress), costs little on AliExpress (10K+ sold), and only about 4 Hebrew ads came up. The risk is the short Israeli winter, so the sales window is Nov–Feb.
5. **3D hand-casting kit for couples and families (tiktok-22).** It is rising into gift season (+24% daily units in early November), it is an emotional gift with no electrical or battery certification issues, and I found no Hebrew ads (unverified). It also fits Tu B'Av, Valentine's, new babies and grandparents all year. Pick a 4.9-rated supplier and add Hebrew instructions.

### Cited Findings
- See the per-product citations in Q2 and the Meta counts in Q3.

### Inferences
- Honourable mentions:
  - Slim magnetic power bank: the strongest sustained gadget, but likely saturated in Israeli phone shops, and lithium shipping limits apply.
  - Shapewear bodysuit: huge volume and moderate Israeli competition.
  - Crevice brush plus steam cleaner as a Pesach-cleaning bundle for March 2027.
  - Turbo blower: strong, but already about 24 Israeli advertisers.

### Gaps
- Most Israeli-presence checks for the top 5 are unverified zeros because of Meta page-load failures. Confirm manually before committing.
