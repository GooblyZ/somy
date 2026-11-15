# Deep dive: neck massage and heat pillow (shiatsu U-pillow, shoulder wrap, car 12V, EMS/TENS, gift bundle). Researched 15.11.2026

Scope: one product family for a small Israeli Shopify store. This builds on item 6 in `מוצרים בסגנון Bagly/05_wow_women_beauty_fashion.md` and does not repeat it. That item recorded Neckly at 289 ₪, the AliExpress listing 1005007344904537 at ₪69.07 with 10K+ sold, an estimated 800 g, and +31.4 ₪ profit at a CPA of 86 at a 249 ₪ sale price.

Labels: **FACT** means I saw it on the cited page on the date given. **REPORTED** means a third party states it and I did not verify it. **ESTIMATE** means my own calculation or judgement. **UNVERIFIED** means a plausible claim with no source.

Data collected on 15.11.2026:
- Meta Ad Library: country IL, active ads, keyword_unordered, headless Chromium, fresh context per query.
- AliExpress search sorted by orders, with an IL/ILS cookie.
- Zap search pages rendered in Chromium.
- Shopify `/products.json` for neckly.co.il, tryrelava.com, spinaly.co.il and getters.co.il.
- Pages I could not read:
  - KSP returned 403 and Ivory showed a Cloudflare check. Neither was circumvented.
  - Super-Pharm rendered an empty page.
  - Max Stock search returned its home page.
  - AliExpress item pages did not render (one showed a "Click to feedback" anti-bot stub). Item-level weight, shipping and spec data was therefore not collected.

---

## 1. Who buys and why (audiences, pain strength, review praise/complaints)

### Takeaway
The pain is widespread and tilts toward women aged 45–74, and Israeli office workers report very high musculoskeletal pain. In Israel the product sells as relaxation for screen workers and as a gift for parents or a partner. Review complaints are consistent across brands:
- the unit fails after weeks or months;
- battery or charger problems;
- kneading that works only some of the time;
- weak heat;
- poor fit.

### Cited Findings
- **FACT (GBD 2021, Lancet Rheumatology 2024, vol 6(3) e142–e155):**
  - 203M people had neck pain in 2020 (UI 163–253M), an age-standardised prevalence of 2,450 per 100k.
  - Women 2,890 per 100k vs men 2,000. Prevalence peaks at ages 45–74.
  - Projected 269M cases by 2050 (+32.5%).
  - The summary came from search snippets, and I did not open the full text. — [JCU record](https://researchonline.jcu.edu.au/87316/); [UAEU record](https://research.uaeu.ac.ae/en/publications/global-regional-and-national-burden-of-neck-pain-19902020-and-pro/)
- **REPORTED (Israeli OSH institute publication, 2022 office-worker survey):** 81% reported some musculoskeletal pain in the past year and 44% said it limited daily activity. This covers all body regions, not neck only. — [osh.org.il PDF](https://www.osh.org.il/UploadFiles/02_2023/399_Part_20_21.pdf)
- **REPORTED (Israel J Health Policy Res, 2025):** neck pain was 11.1% of spinal-disorder referrals to physiotherapy in a large HMO, vs 21.2% for low back pain. Women were referred for neck pain more often than men. — [PMC11970003](https://pmc.ncbi.nlm.nih.gov/articles/PMC11970003)
- **REPORTED (Occup Med 2008, 1,185 office workers, not Israeli):** head/neck was the most common work-attributed symptom site (42%). — [PubMed 18544589](https://pubmed.ncbi.nlm.nih.gov/18544589/)
- **REPORTED (Midrag price guides, accessed 15.11.2026):** a shiatsu or medical massage session in Israel costs about 250–350 ₪, with some quotes up to 450 ₪. This supports a "less than one massage" price anchor. — [Midrag](https://www.midrag.co.il/Content/Price/10807)
- **FACT (Meta Ad Library, 15.11.2026): how Israeli sellers frame the buyer.**
  - Neckly: "שעות מול המחשב, הטלפון שמושך את הראש קדימה" (hours at the computer, the phone pulling the head forward), screen workers.
  - Relava: "אם גם את לא מצליחה לישון בגלל כאבי צוואר" (if you also can't sleep because of neck pain), women, written as a first-person story.
  - "חברה ייחודית בתחומה": "מתנה... לאמא, לאבא, לבעל או לאישה" (a gift for mom, dad, husband or wife).
  - netro.gifts: "צוואר תפוס אחרי יום מול המסך" (stiff neck after a day at the screen).
  - Source: [Ad Library query "מכשיר עיסוי לצוואר"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%9B%D7%A9%D7%99%D7%A8%20%D7%A2%D7%99%D7%A1%D7%95%D7%99%20%D7%9C%D7%A6%D7%95%D7%95%D7%90%D7%A8&search_type=keyword_unordered); [query "מעסה צוואר"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%A2%D7%A1%D7%94%20%D7%A6%D7%95%D7%95%D7%90%D7%A8&search_type=keyword_unordered)
- **REPORTED (retailer reviews and a third-party review site; small samples of about 6–24 buyer reviews per product): top complaints.**
  - Units quit after weeks to months. One HoMedics Pro Therapy unit quit after 5 months. A Macy's buyer said the unit stopped and the company could not be reached. A Naipo owner was told to discard a unit that stopped after about 2 years.
  - Battery and charging problems: 9 of 15 buyer reviews of a Snailax 4D cordless model mentioned battery, charging or the unit dying.
  - Kneading worked only intermittently while heat and vibration kept working (Best Buy reviewer).
  - Auto shut-off triggered early.
  - Zyllion's heat was faint compared with its kneading.
  - The neck piece was too small, too wide or uncomfortable.
  - Failures came after the return window had closed.
  - Sources: [Relief Report – Snailax SL-681](https://s3.amazonaws.com/reliefreport/snailax-sl-681-4d-cordless-neck-and-shoulder-massager-review.html); [Relief Report – Zyllion ZMA-28](https://s3.amazonaws.com/reliefreport/zyllion-zma-28-neck-and-back-massager-review.html); [Best Buy HoMedics reviews](https://www.bestbuy.com/site/reviews/homedics-deep-kneading-rechargeable-neck-shoulder-massager-with-heat-gray/6593290); [Macy's HoMedics](https://www.macys.com/shop/product/homedics-pro-therapy-heated-neck-massager?ID=9524037)
- **REPORTED (same sources): top praise.** Deep kneading, and heat combined with kneading that helped back and neck tension, especially for Renpho and Nekteck. One Nekteck buyer got a replacement after the unit quit at 6 weeks. — [Relief Report](https://s3.amazonaws.com/reliefreport/snailax-sl-632nc-cordless-shiatsu-neck-massager-review.html); [ProductReview.com.au – Renpho](https://www.productreview.com.au/listings/renpho-shiatsu-neck-and-shoulder-back-massager-with-heat)
- **FACT (Zap, 15.11.2026): Israeli ratings shown on Zap** belong to the stores, not the product. Examples: BrandsOnSale 4.8 (397 reviews), Walla Shops 2.2 (3,231), LastPrice 2.4 (5,912). — [Zap "שיאצו צוואר"](https://www.zap.co.il/search.aspx?keyword=%D7%A9%D7%99%D7%90%D7%A6%D7%95%20%D7%A6%D7%95%D7%95%D7%90%D7%A8)

### Inferences
- **ESTIMATE: the best Israeli audiences, in order.**
  1. Gift buyers aged 30–50 shopping for parents aged 55–75. This matches the 45–74 prevalence peak, and the buyer is not the sufferer.
  2. Women aged 30–55 who work at screens.
  3. Commuting drivers, a smaller segment that needs a car adapter.
- **ESTIMATE:** older women are the core sufferers. The ad hook should speak to the gift giver about the parent ("אמא שלך מתלוננת על הצוואר", your mom complains about her neck).
- **ESTIMATE:** the complaints are about durability, not about whether the concept works. A store that offers a real 12-month local replacement policy would differentiate itself. Ali-shipped units with a 30-day window will generate post-window complaints.
- **ESTIMATE, timing:** Hanukkah starts 4.12.2026, 19 days after this research. AliExpress delivery to Israel takes 7–20 days (file 10, REPORTED), so cross-border dropship cannot reliably hit Hanukkah. Local stock would be needed, or the target moves to Family Day (late Jan / early Feb 2027, exact date UNVERIFIED) and Mother's Day-type gifting.

### Gaps
- No Amazon review mining was possible. The Kimola Amazon review report returned HTTP 410, and Amazon pages were not fetched. There is no percentage breakdown of praise and complaints.
- No Israeli survey gives neck-specific prevalence.

---

## 2. Product types, quality tiers, brands, prices

### Takeaway
There are four distinct designs:

| Design | Power | Typical use |
|---|---|---|
| U-shaped kneading pillow | corded 12V adapter, often with a car adapter | home and car |
| "Hands" / shawl wrap that grips the trapezius ("4D", "bionic finger") | rechargeable | handbag-portable |
| Heated vibration or airbag-traction pillow | often rechargeable | lying-down relaxation |
| EMS/TENS clip-on | battery | electrical stimulation (see section 5) |

Branded units abroad sell for $28–90. In Israel the branded units (Beurer, Medics Care, HoMedics, Breo, SKG) are widely sold with importer warranties for 105–1,259 ₪.

### Cited Findings
- **FACT (AliExpress search sorted by orders, IL/ILS, 15.11.2026): the four designs and their sales.**
  - "Multi Functional Neck and Shoulder Massager… Hot Compress", shawl type: 7K+ sold (5,000+ in a second query), 4.6★.
  - "Bionic Finger Pressure" shawl: 3K+ sold, 4.5★.
  - "Shiatsu U Shape Deep Kneading Electric Massage Pillow": 2K+ sold, 4.9★.
  - "JAIYORL Trapezius Electric Massage Pillow Wireless Car And Home… Heating… Shiatsu Kneading": 1K+ sold, 4.9★.
  - "Electric Neck Massager Cervical Pillow Hot Compress… Traction" (vibration plus traction): 4K+ sold, 4.5★.
  - "TENS Pulse Neck Massager… No Heating": 5,000+ sold, 4.9★.
  - Source: [AliExpress search "neck shoulder massager kneading"](https://www.aliexpress.com/w/wholesale-neck-shoulder-massager-kneading.html?SortType=total_tranpro_desc&shipCountry=IL)
- **REPORTED (affiliate roundups of low reliability):** Zyllion ZMA-13 is the most frequent "top pick", with Nekteck, RESTECK and Mo Cuishle also named. Most pages are templated affiliate content with unverified "tested" claims. A Yahoo roundup notes the Zyllion's rigid design makes it hard to target neck and shoulders at once. — [Cleveland Heart roundup](https://www.clevelandheart.com/best-shiatsu-neck-massagers/); [yourbestdigs](https://www.yourbestdigs.com/reviews/best-neck-and-shoulder-massager/); [Yahoo](https://www.yahoo.com/lifestyle/alleviate-sore-muscles-shoulder-neck-210059909.html)
- **FACT / REPORTED: brand prices abroad (search summaries of retailer pages, mostly 2026, dates vary).**
  - Comfier 4D cordless neck and shoulder massager with heat: $29.49 (was $62.99), 4.6★ from 459 reviews, Walmart. Another Comfier cordless unit: $45.99. Comfier CF-6419: $86.99. — [Walmart Comfier 4D](https://www.walmart.com/ip/5319721557); [Walmart Comfier cordless](https://www.walmart.com/ip/8481858911)
  - Snailax cordless shiatsu neck/back with heat: $39.99; another Snailax: $49.99. — [Walmart](https://www.walmart.com/ip/Neck-Back-Massager-with-Heat-4D-Shiatsu-Shoulder-Massager-for-Pain-Relief-Gifts-for-Mom-Dad/2534267734)
  - Naipo shiatsu pillow: $33.96 on an Amazon deal (date unclear). Another Naipo: AU$79.99. NAIPO MGP-129A: 4.7★ on Alza. — [Hip2Save](https://hip2save.com/?p=9010005); [Lifehacker AU](https://www.lifehacker.com.au/?p=1059124); [Alza](https://m.alza.at/EN/reviews/naipo-mgp-129a-12664145.htm)
  - Breo iNeck2: €74 plus €13.49 shipping. iNeck 3 Pro: about €149.99. — [Fruugo](https://www.fruugo.ie/breo-ineck2-heat-compression-deep-kneading-portable-shoulder-neck-massager/p-366927757-794399908); [Breo US](https://us.breo.com/products/breo-ineck-3-pro-electric-massage-neck-pillow)
  - Medisana MC 850: €47.99. HoMedics NMSQ-215 (vibration with heat): €27.99. — [aio.lv Medisana](https://aio.lv/en/product--medisana-88947--4441247.md); [aio.lv HoMedics](https://aio.lv/en/product--homedics-nmsq-215a--3460009.md)
  - Renpho: no price found (gap).
- **FACT (Zap, 15.11.2026): branded units in Israel.**
  - Beurer: MG149 massage cushion from 254 ₪ (7 stores), MG145 from 185 ₪, MG135 from 209 ₪, MG21 from 149 ₪.
  - Medics Care: MC-4102 from 105 ₪ (12 stores), MC-9880 from 155 ₪, MC-4800A rechargeable neck 539–728 ₪, MC-4730 528 ₪, N8 HumaFeel 488 ₪.
  - Others: HoMedics SP75H from 611 ₪, SKG neck & shoulder 493 ₪, Breo Neck D5 1,259 ₪, Carbon NPS-6 388 ₪.
  - Sources: [Zap "כרית עיסוי"](https://www.zap.co.il/search.aspx?keyword=%D7%9B%D7%A8%D7%99%D7%AA%20%D7%A2%D7%99%D7%A1%D7%95%D7%99); [Zap "מכשיר עיסוי לצוואר"](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%9B%D7%A9%D7%99%D7%A8%20%D7%A2%D7%99%D7%A1%D7%95%D7%99%20%D7%9C%D7%A6%D7%95%D7%95%D7%90%D7%A8); [Zap "מעסה צוואר"](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%A2%D7%A1%D7%94%20%D7%A6%D7%95%D7%95%D7%90%D7%A8)
- **REPORTED (search summary of the Bug product page): Beurer MG148 shiatsu belt** for back, neck and shoulders, 299 ₪, with a 3-year warranty via the importer Audiocar and a light and heat function. — [bug.co.il](https://www.bug.co.il/brand/beurer/mg148)
- **FACT (Meta ad by zap.co.il, active from 12.11.2026):** "כרית עיסוי בויירר ב־209 ₪ שנה אחריות של מ.ברוכים" (Beurer massage cushion at 209 ₪, one-year warranty from M. Baruchim). — [Ad Library "עיסוי שיאצו"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A2%D7%99%D7%A1%D7%95%D7%99%20%D7%A9%D7%99%D7%90%D7%A6%D7%95&search_type=keyword_unordered)

### Inferences
- **ESTIMATE: which designs to choose.** Corded U-pillows avoid the most common complaint (battery and charging) and usually work in a car, which covers the driver angle. They are heavier and bulkier to ship. Rechargeable shawl units sell best on AliExpress and demo better on video, because they visibly grip the trapezius. They carry lithium batteries and generate the battery complaints. If one SKU is chosen, it should be a shawl with a removable charger or USB-C, or a corded U-pillow that comes with a car adapter.
- **ESTIMATE: generic vs branded.** Generic Chinese units and the branded units (Comfier, Snailax, Naipo, Renpho) mostly come from the same Xiamen and Shenzhen ecosystem. Comfier, for example, is Xiamen Comfier Technology (section 5). The difference is QC consistency, the warranty, and a heat cut-off. In Israel the branded alternative is Beurer or Medics Care with a 1–3 year importer warranty, and it is cheap: from 105–255 ₪.

### Gaps
- Exact Amazon star ratings, review counts and current prices for Naipo, Renpho, Zyllion, Snailax and Medisana were not collected.
- I did not verify which generic AliExpress units have a thermal cut-off or a 15–20 minute auto shut-off, because item pages did not render.

---

## 3. Market in Israel: sellers, prices, ad age, warranties, crowding

### Takeaway
The niche is crowded at both ends.
- Zap lists hundreds of results, with branded units from 105 ₪ carrying importer warranties.
- A new wave of DTC and dropship advertisers started in Oct–Nov 2026: Neckly, Relava, Getters, Spinaly, Out-of-the-box, Atrakzya, netro.gifts, "חברה ייחודית בתחומה" and Gadgetshop.
- Retail prices range from 99–150 ₪ (Getters, WhatsApp sellers) up to 289–319 ₪ (Neckly, Relava).
- Only one product ad has run longer than about 6 weeks (Smart Shop, since 29.6.2026). That suggests most advertisers are still testing.

### Cited Findings
- **FACT: Meta Ad Library, query "מכשיר עיסוי לצוואר", about 22 results, as rendered 15.11.2026.**
  - "חברה ייחודית בתחומה": "ב-150 ש"ח בלבד (כולל משלוח)" (only 150 ₪ including delivery), "מכשיר עיסוי מקצועי לצוואר ולכתפיים" (professional neck and shoulder massager), gift for mom, dad, husband or wife. WhatsApp checkout. Active from 1.10.2026.
  - Neckly (neckly.co.il): Black Friday ad at 289 ₪ vs 413 ₪, "10 דקות של הקלה" (10 minutes of relief), "3 פעולות במכשיר אחד: חימום…" (3 actions in one device: heating…). Active from 13.11.2026, with another ad from 26.10.2026.
  - Relava (tryrelava.com): at least 6 ad versions from 9–10.11.2026, long first-person story copy ("בשתיים ועשרים בלילה, על הספה בסלון, עם בקבוק חם מתחת לעורף", at 2:20 a.m. on the living-room sofa with a hot-water bottle under my neck).
  - Getters (getters.co.il): "מכשיר עיסוי לצוואר ולכתפיים בטכנולוגיית שיאצו, ב-99 ₪ במקום 189 ₪, ועם משלוח חינם לנקודת איסוף" (shiatsu neck and shoulder massager, 99 ₪ instead of 189 ₪, free delivery to a pickup point). From 7.11.2026.
  - Spinaly (spinaly.co.il): from 12.11.2026.
  - מחוץ לקופסא (out-of-the-box.co.il): from 5.11 and 9.11.2026.
  - אטרקציה (atrakzya.co.il), "מכשיר עיסוי חשמלי לצו[וואר]" (electric neck massager): from 9.11.2026.
  - גאדג'טשופ: TOUCHCARE massage series at 303–404 ₪, from 4.11.2026.
  - Source: [Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%9B%D7%A9%D7%99%D7%A8%20%D7%A2%D7%99%D7%A1%D7%95%D7%99%20%D7%9C%D7%A6%D7%95%D7%95%D7%90%D7%A8&search_type=keyword_unordered)
- **FACT: Meta Ad Library, query "מעסה צוואר", about 15 results.**
  - סמארט שופ: "מעסה עכביש… משלוח כלול: 200 ש"ח לעיסוי צוואר וגב עם חום" (spider massager, delivery included, 200 ₪, neck and back massage with heat). Active since 29.6.2026, the longest-running product ad seen.
  - netro.gifts (netro4u.com): "המעסה שמרגיש כמו ידיים של מעסה… חום נעים בשתי דרגות" (the massager that feels like a masseur's hands… pleasant heat in two levels).
  - Neckly.
  - The rest are therapists (Kfar Saba, Ra'anana, sports therapists).
  - Source: [Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%A2%D7%A1%D7%94%20%D7%A6%D7%95%D7%95%D7%90%D7%A8&search_type=keyword_unordered)
- **FACT: Meta Ad Library, query "עיסוי שיאצו", about 81 results.** Mostly therapists, massage chairs (Feel good israel since 13.7.2025, Ultra Brand), Clalit, the Beurer Israel official-distributor page (from 20.4.2026), and the zap.co.il Beurer 209 ₪ ad.
- **FACT: Meta Ad Library, query "כרית עיסוי".** The first run returned 0 and a re-run returned about 170. They are mostly back and sciatica pillows: Ortofix, Jepeta (since 9.11.2025), Verta, mynuma.store, Uriel.
- **FACT, but probably a rendering failure:** "מסאז'ר לצוואר", "מסאז'ר צוואר", "כרית חימום לצוואר", "כרית חימום", "מסאז'ר שיאצו" and "מכשיר עיסוי" returned 0 or errored. Treat these as UNVERIFIED, not as empty niches. "כרית עיסוי" went from 0 to 170 between runs.
- **FACT (neckly.co.il/products.json, 15.11.2026):**
  - Hero product "! הקלו על כאבי הצוואר ב10 דקות - שיטת הטיפול המובילה בישראל" (relieve neck pain in 10 minutes, Israel's leading treatment method): 289 ₪ (compare-at 413), created 15.6.2026, published 16.7.2026.
  - The body offers "60 ימי ניסיון או החזר כספי מלא" (60-day trial or full refund). No formal warranty is stated.
  - Add-ons: memory pillow 189 ₪, heat patches 50 ₪, back stretcher 148 ₪.
  - Source: [neckly products.json](https://neckly.co.il/products.json)
- **FACT (tryrelava.com/products.json):** a single product, "כרית מסאז' מחוממת לשחרור צוואר תפוס וכואב RELAVA" (heated massage pillow for a stiff, aching neck), 319 ₪ (compare-at 456), created 27.8.2026. The copy says "חום מבוקר… בלי כדורים ובלי תורים לקליניקה" (controlled heat… no pills and no clinic appointments) and the "Pressure-Off" method. — [tryrelava products.json](https://tryrelava.com/products.json)
- **FACT (getters.co.il/products.json):** "מכשיר עיסוי לצוואר ולכתפיים מספק עיסוי לישה עמוק בטכנולוגיית שיאצו" (neck and shoulder massager with deep shiatsu kneading), vendor MiniMaxx, 99 ₪ (compare-at 189), created 28.10.2026. Specs: U-shape, 65 cm wide, 3D bidirectional heads, 3 intensities, USB adapter. — [getters products.json](https://getters.co.il/products.json)
- **FACT (spinaly.co.il/products.json):** NeckCalm neck traction device at 239 ₪ (compare-at 299), created 5.8.2022, listed at 1,000 g. The store has run since 2021 with bundles: 2 neck devices for 479 ₪, 3 for 599 ₪, and up to 6 for 839 ₪. — [spinaly products.json](https://www.spinaly.co.il/products.json)
- **FACT (Zap, 15.11.2026): retail spread for "שיאצו צוואר" (62 results).**
  - Office Market: shiatsu pillow 218 ₪, rechargeable 168 ₪, TouchCare TC-606 198 ₪, inflatable travel pillow with shiatsu 728 ₪.
  - Zapstore / Yehudi: "שיאצו, חימום, נייד" (shiatsu, heat, portable) pillow 378 ₪; "כפות ידיים" (palms) neck massager 269 ₪; rechargeable bidirectional with heat 179 ₪.
  - TEKNO 5429 "ידיים" (hands): 154–178 ₪ (OLSale, LastPrice).
  - NAVI shiatsu belt with heat: 216 ₪ (Club Pharm).
  - Walla Shops heated shiatsu: 278 ₪.
  - Kama Zol (ships from abroad): 135 ₪.
  - Source: [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%A9%D7%99%D7%90%D7%A6%D7%95%20%D7%A6%D7%95%D7%95%D7%90%D7%A8)
- **FACT (Zap): "מכשיר עיסוי לצוואר" (172 results).** PULSE 80–95 ₪, THERAPY 109–130 ₪, NAVY NY-8253 54 ₪, Goodest 299–329 ₪, O-PHARM 339 ₪, Next-Stock (from abroad) 98–118 ₪. "מעסה צוואר" (9 results) includes "מכשיר עיסוי וטנס דיגיטלי" (digital massage and TENS device) at 290 ₪ from a medical-supply store, מטוב ציוד רפואי.
- **REPORTED (prior file 02, Nov 2026):** Zap "מעסה צוואר" min/median/max was 59 / 108 / 1,259 ₪. Generic massagers were judged "saturated: many sellers, low medians". — [file 02](../מחקר%20מוצרים%20לאיקומרס%20בישראל/02_israel_demand_signals.md)

### Inferences
- **ESTIMATE:** this niche is crowded. At least 9 product advertisers were active in Nov 2026, Black Friday pricing has started, and there is a 99 ₪ shiatsu U-pillow at Getters. There is also a deep branded shelf on Zap at 105–300 ₪ with importer warranties. A new store cannot win on price.
- **ESTIMATE:** the white space left is positioning. Candidates are a gift-ready bundle with a box and card and a local 12-month replacement promise, and the "for your parents" message. DTC players aim their message at the sufferer (Neckly, Relava), while only a WhatsApp seller pushes the gift angle.
- **ESTIMATE:** Relava's long story ads and Neckly's "method" framing point to an advertorial approach that relies on pain-relief claims, which carries regulatory risk (section 5).

### Gaps
- KSP, Ivory, Super-Pharm, Max Stock and Bug listings were not read (bot protection or empty render). Super-Pharm's own massager range and prices are unknown.
- Ad spend and sales volumes for competitors are unknown. Ad Library shows only start dates.
- I did not check whether Getters' 99 ₪ unit is the same as the AliExpress units.

---

## 4. Supply: AliExpress prices, sold counts, weight, battery

### Takeaway
Decent-looking units with at least 1K sold and at least 4.5★ cost ₪58–192 on AliExpress, shipping to IL, as of 15.11.2026. Shawl-type wraps sell best and cost ₪58–80. Kneading U-pillows cost ₪94–126 and branded-looking JAIYORL units ₪168–192. Weight and battery data could not be read from item pages.

### Cited Findings
- **FACT (AliExpress, sorted by orders, ship to IL, prices in ILS as rendered 15.11.2026). Prices shift between queries for the same item.**

| Item ID | Type | Price ₪ | Sold | ★ |
|---|---|---|---|---|
| [1005006990339856](https://www.aliexpress.com/item/1005006990339856.html) | Shawl "hot compress" kneading | 58.22–68.02 | 5K–7K+ | 4.6 |
| [1005010449094810](https://www.aliexpress.com/item/1005010449094810.html) | Bionic-finger shawl | 44.75–76.05 | 3K+ | 4.5 |
| [1005010208859258](https://www.aliexpress.com/item/1005010208859258.html) | N7 wireless kneading shawl | 72.79–79.16 | 1K+ | 4.5 |
| [1005007805628544](https://www.aliexpress.com/item/1005007805628544.html) | U-shape shiatsu kneading pillow, heated | 126.09 | 2K+ | 4.9 |
| [1005008001015860](https://www.aliexpress.com/item/1005008001015860.html) | Infrared heat kneading pillow | 94.59 | 1K+ | 4.9 |
| [1005007856992621](https://www.aliexpress.com/item/1005007856992621.html) | JAIYORL trapezius pillow, wireless, car and home | 191.69 | 1K+ | 4.9 |
| [1005007957101446](https://www.aliexpress.com/item/1005007957101446.html) | JAIYORL variant | 168.33 | 968 | 4.4 |
| [1005010319131824](https://www.aliexpress.com/item/1005010319131824.html) | Heat, vibration and traction cervical pillow (Relava/Neckly style) | 48.29 | 4K+ | 4.5 |
| [1005011653994293](https://www.aliexpress.com/item/1005011653994293.html) | Same type | 85.69 | 2K+ | 4.9 |
| [1005008806345069](https://www.aliexpress.com/item/1005008806345069.html) | "SPA" wireless warm pillow massager | 189.12 | 1K+ | 4.5 |
| [1005007539967556](https://www.aliexpress.com/item/1005007539967556.html) | Car/home heated vibrating cushion pad (12V type) | 114.44 | 3,000+ | 4.9 |
| [1005008715900199](https://www.aliexpress.com/item/1005008715900199.html) | Airbag-traction neck pillow, car, heat | 144.39 | 2,000+ | 4.9 |
| [1005007345712574](https://www.aliexpress.com/item/1005007345712574.html) | TENS pulse neck massager (no heat) | 5.64 (new-shopper price; regular about 67.93) | 5,000+ | 4.9 |

  - Sources: [search: shiatsu neck shoulder massager](https://www.aliexpress.com/w/wholesale-shiatsu-neck-shoulder-massager.html?SortType=total_tranpro_desc&shipCountry=IL); [neck massager pillow heat](https://www.aliexpress.com/w/wholesale-neck-massager-pillow-heat.html?SortType=total_tranpro_desc&shipCountry=IL); [car neck massager](https://www.aliexpress.com/w/wholesale-car-neck-massager.html?SortType=total_tranpro_desc&shipCountry=IL)
- **FACT:** many cards showed "New shoppers save ₪X" and ₪3.59 entry prices. These are welcome-deal prices, not repeatable cost.
- **FACT (prior file 05, 14.11.2026):** 1005007344904537 at ₪69.07, 10K+ sold. Its item page did not render today.
- **REPORTED (file 10, forwarder data, 2026):**
  - YunExpress bills the greater of actual and volumetric weight.
  - Planning freight to Israel: 1 kg ≈ 55–80 ₪, 2 kg ≈ 95–135 ₪, plus 10–45% for battery items.
  - Above about 1 kg, freight makes Model A (cross-border dropship) unworkable under about 299 ₪ retail.
  - Source: [file 10](../מחקר%20מוצרים%20לאיקומרס%20בישראל/10_unit_economics_verification.md)
- **FACT (spinaly products.json):** NeckCalm (foam traction device) listed at 1,000 g. Getters lists 2,000 g for its U-pillow, which is probably a default value (UNVERIFIED).
- **REPORTED (file 09):** SI 62133 parts 1 and 2 for rechargeable batteries became binding on 28.5.2022. Rechargeable batteries in household products need approved-lab testing for commercial import. — [file 09](../מחקר%20מוצרים%20לאיקומרס%20בישראל/09_deepdive_pets_israel_specific.md)

### Inferences
- **ESTIMATE, weight:**
  - shawl wrap about 0.9–1.3 kg packed;
  - U-pillow with adapter about 1.2–1.8 kg packed, and boxy, so volumetric weight may dominate;
  - car seat-cushion pad about 2–3 kg.
- **ESTIMATE, landed cost (Model A):**
  - shawl ₪60–80 + freight ₪60–95 ≈ ₪120–175;
  - U-pillow ₪95–126 + ₪70–110 ≈ ₪165–235;
  - JAIYORL ₪170–190 + ₪75–110 ≈ ₪245–300.
- **ESTIMATE:** rechargeable shawls add battery-line surcharges and battery-related failures. Corded units need a 12V adapter, and the adapter's plug and safety matter (section 5).

### Gaps
- No item-page weights, dimensions, adapter specs (plug type, CE/UL marks), auto shut-off or battery capacity were collected. No real CJ or agent Israel shipping quote exists for a 1.2–1.8 kg item.
- I did not check Alibaba MOQ pricing.

---

## 5. Regulation and safety (standards, AMAR, claims, EMS/TENS)

### Takeaway
- Ordinary kneading, vibration and heat massagers are household electrical appliances under SI 900 part 2.32, which is the Israeli edition of IEC 60335-2-32. SII says that standard is "in the process of official declaration". The mains or charger adapter brings the electrical-standards regime into play for commercial import.
- EMS/TENS neck units are regulated as medical devices in the US (Class II). They should be treated as medical devices needing AMAR registration in Israel, so avoid them.
- Pain-relief, "treatment" and "method" claims risk turning a plain massager into an unregistered medical-device claim.

### Cited Findings
- **FACT (SII standard page, fetched 15.11.2026):**
  - The standard is ת"י 900 חלק 2.32, "בטיחות מכשירי חשמל ביתיים ומכשירים דומים: דרישות מיוחדות למכשירי עיסוי" (safety of household electrical appliances: particular requirements for massage appliances).
  - Published 15/03/2016, replacing the 2011 edition, which was cancelled 20/03/2016.
  - Notes: "ת"י זה נמצא בתהליך אכרזת רשמיות" (this standard is in the process of official declaration). It also lists Reshumot item יפ 9278 dated 08/12/2020.
  - Scope: electric massage appliances for household use, up to 250 V single-phase.
  - Source: [SII standard page id=3131](https://www.sii.org.il/lobby/standardization/standard-page?id=3131)
- **FACT (IEC):** IEC 60335-2-32 (edition 6, 12.9.2024) covers foot, hand-held, bed, belt, chair and pad massagers. Beauty-care appliances fall under 60335-2-115 instead. — [IECEE](https://www.iecee.org/certification/iec-standards/iec-60335-2-322024)
- **FACT (prior file 10, Israel Customs tariff 85.09):**
  - Mains-powered or charger-bundled household electro-mechanical appliances need a standards release for commercial import under the Free Import Order (SI 900 routes).
  - These rows are marked "does not apply to personal import".
  - Massage apparatus (HS 90.19) is duty-exempt.
  - Source: [Customs tariff item](https://shaarolami-query.customs.mof.gov.il/CustomspilotWeb/he/CustomsBook/Import/ImportCustomsItemDetails?customsItemId=3188); [file 10](../מחקר%20מוצרים%20לאיקומרס%20בישראל/10_unit_economics_verification.md)
- **REPORTED (Goldfarb / UnitedXP via file 01):** since Jan 2025 the "what's good for Europe" reform lets many products be imported on EU conformity documents (DoC) instead of Israeli testing. — [Goldfarb](https://www.goldfarb.com/he/מהפכת-התקינה-בישראל-הרפורמה-האירופית/)
- **REPORTED (State Comptroller via file 07):** Israeli law defines a medical device by its intended use, meaning treatment or assisting treatment. — [Mevaker 2008](https://library.mevaker.gov.il/sites/DigitalLibrary/Documents/1950-2008/2008-58b/2008-58b-219-AvizarimRefuim.pdf)
- **FACT (gov.il service page):** the Ministry of Health has a committee that examines misleading advertising of health products and medical technologies. It takes complaints including ads for "אביזרים רפואיים שלא אושרה להם התוויה רפואית" (medical devices with no approved medical indication). — [gov.il complaint service](https://www.gov.il/he/service/complaint_mislead_medical_advertisement)
- **REPORTED (Emergo by UL; PureGlobal):**
  - AMAR registration is required to market a medical device.
  - It relies on approval in a reference market (US, EU, Canada, Australia) and needs an Israeli Registration Holder.
  - Some electro-medical devices also need SII validation (SI 60601).
  - Licences last 5 years.
  - Sources: [Emergo](https://www.emergobyul.com/services/medical-device-registration-and-approval-israel); [PureGlobal](https://www.pureglobal.com/markets/israel)
- **FACT (FDA 510(k) mirror):**
  - Xiamen Comfier Technology's EMS neck massager, K233492, product code NGX (powered muscle stimulator, 21 CFR 890.5850, Class II), was cleared 20.12.2023 on bench testing only.
  - Combined TENS/EMS units with "temporary relief of pain in the neck, shoulder…" indications are cleared under 21 CFR 882.5890 (TENS, Class II).
  - Sources: [Innolitics K233492](https://fda.innolitics.com/submissions/PM/subpart-f%E2%80%94physical-medicine-therapeutic-devices/NGX/K233492); [510kdatabase](https://www.510kdatabase.net/k233492); [Innolitics EMS/TENS K233040](https://fda.innolitics.com/device/K233040)
- **FACT (Zap):** a "מכשיר עיסוי וטנס דיגיטלי" (digital massage and TENS device) is sold in Israel by a medical-supply store (מטוב ציוד רפואי) at 290 ₪. — [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%A2%D7%A1%D7%94%20%D7%A6%D7%95%D7%95%D7%90%D7%A8)
- **FACT (Meta ads, 15.11.2026): health claims competitors already use.**
  - Neckly: "הקלו על כאבי הצוואר ב10 דקות - שיטת הטיפול המובילה בישראל" (relieve neck pain in 10 minutes, Israel's leading treatment method).
  - Smart Shop: "מקל על כאבי גב ועוויתות שרירים" (relieves back pain and muscle spasms).
  - Spinaly: "להקל על הכאבים, ליישר את הצ[וואר]" (ease the pain, straighten the neck).
  - Relava: "בלי כדורים ובלי תורים" (no pills, no appointments).

### Inferences
- **ESTIMATE:** a kneading, vibration or heat massager with no medical claim is a consumer electrical appliance, not a medical device. Saying "pain relief", "treatment", "cervical", "hernia", "sciatica", "straighten the neck", "instead of physiotherapy" or "method" moves it toward intended medical use.
- **ESTIMATE: claims that are safer in ads.**
  - Safer: "עיסוי מפנק" (pampering massage), "רגע של רוגע אחרי יום מול המסך" (a moment of calm after a day at the screen), "חום נעים" (pleasant warmth), "תחושת שחרור" (a feeling of release), "מרגיש כמו ידיים של מעסה" (feels like a masseur's hands), "מתנה לאמא ואבא" (a gift for mom and dad), "15 דקות של פינוק" (15 minutes of pampering).
  - Avoid: "מקל על כאבים" (relieves pain), "מטפל" (treats), "רפואי" (medical), "פיזיותרפיה" (physiotherapy), disease names, before/after pain scores, doctor endorsements.
- **ESTIMATE:** EMS/TENS is a no-go for this store. In the US it is a Class II medical device, and in Israel it would need AMAR registration through a registration holder. The units are also cheap commodity bait (₪5.64 cards).
- **ESTIMATE, Model A (consumer is importer):**
  - Personal-import parcels largely avoid standards release.
  - The seller still carries consumer-protection, advertising and product-liability exposure for burns or electrical faults.
  - The adapter will probably be an EU or US plug or a USB brick, not an Israeli SI 32 plug, which is a returns and complaint risk.
- **ESTIMATE, Model B (local stock):** expect a standards release under SI 900 (via EU DoC/CE or an approved lab), plus battery testing (SI 62133) for rechargeable units.

### Gaps
- The import group (קבוצת יבוא) of SI 900 part 2.32 and whether it is currently official were not confirmed. The SII page is ambiguous, and the Free Import Order schedule was not read.
- I found no Israeli Ministry of Health guidance specifically on massagers, TENS units or heating pads.
- I did not confirm whether the AMAR self-declaration track (2023) covers TENS.
- I did not check whether a low-voltage heating element (5–12V) changes the standard (e.g. SI 900 2.17 for heating pads).

---

## 6. Marketing: creatives, hooks per audience, bundles

### Takeaway
In Israel two creative styles are running:
- long first-person pain stories in advertorial style (Relava, Neckly), which lean on medical claims;
- price and gift offers (150 ₪ including delivery via WhatsApp; Getters at 99 ₪ vs 189 ₪).

No verified foreign "winning creative" data was found. The natural differentiator for this store is the gift-for-parents angle with a bundle.

### Cited Findings
- **FACT (Meta Ad Library, 15.11.2026): Israeli creative patterns.**
  - Story ad with many versions: Relava, 6+ versions launched 9–10.11.2026, female first person, night pain, hot-water bottle.
  - Time-to-relief hook: Neckly, "10 דקות של הקלה" (10 minutes of relief), with a Black Friday price cut from 413 to 289 ₪.
  - "Like a masseur's hands, no appointment": netro.gifts, and "ללא צורך בקביעת תור" (no need to book an appointment) from "חברה ייחודית בתחומה".
  - Gift list: "מתנה איכותית ושימושית לאמא, לאבא, לבעל או לאישה" (a quality, useful gift for mom, dad, husband or wife).
  - Price anchor: Getters, 99 ₪ instead of 189 ₪ with free pickup delivery.
  - Short videos: 0:18 (Smart Shop), 0:22 ("חברה ייחודית"), 0:43.
  - Source: [Ad Library "מכשיר עיסוי לצוואר"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%9B%D7%A9%D7%99%D7%A8%20%D7%A2%D7%99%D7%A1%D7%95%D7%99%20%D7%9C%D7%A6%D7%95%D7%95%D7%90%D7%A8&search_type=keyword_unordered)
- **FACT (Spinaly products.json):** an Israeli neck-care store running since 2021 relies on multi-unit and cross-category bundles. Examples:
  - "מארז 2 מכשירי צוואר" (2 neck devices): 479 ₪;
  - neck device + ergonomic pillow: 519 ₪;
  - neck + back + pillow: 689 ₪.
  - Source: [spinaly products.json](https://www.spinaly.co.il/products.json)
- **FACT (Walmart titles):** US listings put the gift angle in the product title, e.g. "…Gifts for Mom Dad" and "Gifts for Men Women". — [Walmart Comfier](https://www.walmart.com/ip/Comfier-Shiatsu-Shoulder-Neck-Massager-with-Heat-4D-Deep-Kneading-Back-Massager-Gifts-for-Men-Women/269391251)
- **REPORTED (generic dropshipping ad guidance, not specific to neck massagers):** UGC-style problem → demo → proof → offer structure, a hook in the first 3 seconds, and "relatable person + specific problem" templates. Low-quality sources. — [adadvisor.ai](https://adadvisor.ai/blog/dropshipping-facebook-ad-examples); [denote.net](https://denote.net/blog/10-facebook-dropshipping-ads-2026)

### Inferences
- **ESTIMATE: hooks per audience**, avoiding medical claims.
  - Gift for parents: "אבא תמיד אומר שהצוואר תפוס? תנו לו 15 דקות של ידיים חמות כל ערב" (Dad always says his neck is stiff? Give him 15 minutes of warm hands every evening). Demo: an adult child places it on a parent's shoulders and the parent smiles. Hanukkah or Family Day framing, gift box and card.
  - Office worker: "יום של 9 שעות מול מסך → 15 דקות של עיסוי עם חום, בלי לקבוע תור" (a 9-hour screen day → 15 minutes of massage with heat, no appointment), plus "פחות ממחיר עיסוי אחד" (less than the price of one massage), against 250–350 ₪ per session.
  - Driver: "פקק באיילון? המושב שלך יכול לעשות לך עיסוי" (stuck in an Ayalon traffic jam? your seat can give you a massage). This needs a 12V unit, and the ad must say "use only when parked or as a passenger" for safety (UNVERIFIED legal requirement).
- **ESTIMATE: natural bundles.**
  1. "Two for the parents": a second unit at -30%, or one for mom and one for dad.
  2. Massager + 12V car adapter + travel bag.
  3. "Comfort box": massager + heated eye mask (₪27 on Ali, file 05) + warm socks + card, sold as a Hanukkah gift at about 299–349 ₪.
  4. Massager + memory neck pillow (Neckly's own add-on at 189 ₪).

### Gaps
- No TikTok or Meta data from abroad on winning neck-massager creatives: no view counts, run-lengths or spend.
- No Israeli CPA, CTR or conversion data for this category. File 05's CPA of 86 ₪ is a generic benchmark.

---

## 7. Verdict, conditions, risks, cheapest checks, cost line

### Takeaway
This is a conditional no-go as a plain dropshipped neck massager. The niche is crowded with 99–319 ₪ DTC sellers and a deep branded shelf on Zap from 105 ₪ with importer warranties. The item is heavy, failure-prone and claim-sensitive, and it cannot reach customers by Hanukkah (4.12.2026) via AliExpress.

It becomes a cautious go only as a gift-positioned bundle at 299–349 ₪ under all of these conditions:
- held as local stock, or via a supplier with 7–10 day Israel delivery;
- with a real 12-month replacement promise;
- with relaxation-only claims;
- with no EMS/TENS.

### Cited Findings
- **FACT:** Getters sells a shiatsu U-pillow at 99 ₪ (created 28.10.2026). A WhatsApp seller offers 150 ₪ including delivery. The zap.co.il ad offers Beurer at 209 ₪ with a 1-year warranty. Neckly sells at 289 ₪ and Relava at 319 ₪. Sources are in sections 2 and 3.
- **FACT:** a decent AliExpress unit (at least 1K sold, at least 4.5★) costs ₪58–192 (section 4).
- **REPORTED:** freight is about 55–80 ₪ per kg and 95–135 ₪ for 2 kg, plus a battery surcharge (file 10). AliExpress delivery takes 7–20 days (file 10).

### Inferences
- **ESTIMATE, one-line cost check:** a decent shawl or U-pillow costs about ₪60–126 on AliExpress plus about ₪60–110 freight for 1–1.8 kg, giving ≈ ₪120–235 landed. The typical Israeli price is 99–320 ₪, with the Zap shiatsu median roughly 180–280 ₪. At a 249 ₪ sale price and an 86 ₪ CPA the margin is near zero or negative for anything but the cheapest shawl. Only about 299–349 ₪ with a bundle works.
- **ESTIMATE: main risks.**
  1. Price war and comparison shopping on Zap against branded units with importer warranties.
  2. Early failures and returns (battery, kneading motor) after the supplier window.
  3. Heavy, bulky shipping, with volumetric weight.
  4. Medical-claim exposure if ads copy Neckly's or Relava's style.
  5. Electrical-standard and plug issues for a mains adapter or a rechargeable battery under Model B.
  6. Hanukkah timing: 19 days remain.
- **ESTIMATE: conditions for a go.**
  - Choose one robust design: a corded U-pillow with car adapter, or a shawl with USB-C.
  - Verify a thermal cut-off and a 15–20 minute auto-off.
  - Test samples personally.
  - Sell in a bundle at 299–349 ₪.
  - Offer 12-month replacement, budgeting for about 5–10% failures (ESTIMATE).
  - Use a gift-for-parents creative with no pain claims.
  - Target Family Day and winter if Hanukkah is missed.
- **ESTIMATE: the 3 cheapest checks before investing.**
  1. **Sample order (about ₪350–450):** order 3 shortlisted units to Israel today: shawl 1005006990339856, U-pillow 1005007805628544, and JAIYORL 1005007856992621. Record the real delivery days and charge per unit. Test kneading strength, heat temperature and cut-off, noise, plug type and build quality. Use them on a 60+ parent for a week.
  2. **Compliance email or call (free to about ₪500):** ask a customs broker or standards consultant for the import group and status of SI 900 part 2.32. Ask whether an EU DoC/CE route works for a corded adapter unit and a battery unit. Confirm that the planned ad copy has no medical-device trigger words.
  3. **Smoke-test ads (about ₪300–500 over 4–5 days):** run 2 creatives (gift for parents vs. office worker) to a pre-order or waitlist landing page at 299 ₪ with a bundle. Measure CPA against the 86 ₪ benchmark before buying stock. Also order Getters' 99 ₪ unit (about 99 ₪) to see whether it is the same product as the AliExpress units.

### Gaps
- No real shipping quote, return-rate data or Israeli CPA for this category exists.
- Super-Pharm, KSP and Ivory pricing is unknown.
- The import-group status of SI 900 part 2.32 was not confirmed.
- Meta Ad Library rendering was inconsistent between runs ("כרית עיסוי" returned 0 and then 170), so zero-result terms are not evidence of an empty niche.
