# Deep dive + adversarial review: five beauty / personal-care candidates for a small Israeli Shopify store

Research date: 2026-11-11. Labels: **FACT** = I read it today on the primary page / API; **REPORTED** = a named publication, seller or search summary says so, not independently verified; **ESTIMATE** = modelled; **ASSUMPTION** = my own input, not sourced; **UNVERIFIED** = could not confirm.

Exchange rate used everywhere: USD 1 = ILS 3.172 (**FACT**, Bank of Israel representative rate, 11 Nov 2026 — [BoI API](https://boi.org.il/PublicApi/GetExchangeRates)). At this rate CPA USD 25 / 32 / 40 = ILS 79 / 102 / 127, and the USD 75 VAT-free threshold = ILS 238.

**Sources I could NOT read (do not treat silence as evidence):** Google Trends (HTTP 429 on every attempt, including a browser session), Temu (login wall), Shein Israel (captcha), KSP (403, geo-block), Super-Pharm online (empty response), Alibaba search (slider captcha), gov.il service pages (Cloudflare challenge), TikTok / Instagram (not attempted beyond one web search). Meta Ad Library was readable, but **negative results are unreliable**: identical queries returned "no ads" in a long session and ~310 results in a fresh one, and an exact-phrase search for "מסלסל" returned nothing, which is implausible. Positive findings (advertiser, text, start date) are solid; "no ads found" is weak.

---

## 1. Israeli competition and prices per candidate

### Takeaway
LED masks are the only candidate with a visible, multi-brand, actively advertised Israeli market in the 400-1,000+ ILS band; that is also its problem, because the low end of the band is already held by an official brand (Silk'n at 483 ILS) and by generic stores at 189-799 ILS. Heatless/satin, lashes and press-on nails are sold locally at 8-99 ILS by chains and mass dropshippers; whitening strips have one clear Israeli DTC seller at 189.90 ILS; "nasal strips" exist locally only in the ordinary (non-magnetic) form at 64.90 ILS.

### Cited Findings
**LED face masks**
- FACT (Zap, 11 Nov 2026): 27 results for "מסכת לד". Shark CryoGlow 1,249-1,706 ILS at 7+ shops (sellers with 334-2,044 shop ratings); Dreame Chrona (280 LEDs) 1,239-1,369 ILS; Iborria M226-2 418 ILS and Iborria M5 silicone 618 ILS (shop 1PC); two generic masks at 189 ILS each (shop "כמה זול", one described as 150 LEDs / 7 colours). — [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%A1%D7%9B%D7%AA%20%D7%9C%D7%93)
- FACT: Silk'n Israel: LED Face Mask 483 (compare-at 690), PRO 1,032, EMS 1,272, Chest PRO 903 ILS; all records created 24 Jun-13 Oct 2026. — [silkn.co.il products.json](https://www.silkn.co.il/products.json?limit=250)
- FACT: HomeLuxe (generic Israeli Shopify store, 122 products, oldest record 19 Jun 2025): "LumiGlow Mask Pro – 8 wavelengths" 799 ILS (compare-at 1,599), created 5 Aug 2026; it also sells a 480 ILS "AuraLift" device. — [myhomeluxeshop.com products.json](https://myhomeluxeshop.com/products.json?limit=250)
- FACT (ad text, Ad Library): Bee Skinny "BEE GLOW Pro" silicone mask, 7 wavelengths, 499 ILS "instead of 999", 2 free sheet masks, free shipping, 30 days to decide (ad started 7 Nov 2026). Ulike ReGlow (272 LEDs) 1,349 ILS with up to 12 instalments. Ya-Man Blue Green Mask Lift 6,198 ILS. In.Hub sells a "Nanoleaf" mask (432 LEDs, 7 modes) and claims "FDA approved, dermatologist approved". אמפייר טק sells a 240-LED, 260 g silicone mask. — [Meta Ad Library, IL, "מסכת LED"](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%A1%D7%9B%D7%AA%20LED&search_type=keyword_exact_phrase)
- REPORTED: Bug lists Shark CryoGlow, Ulike ReGlow UM10 and Therabody TheraFace masks; an i24 article says masks are sold in Israel "from a few tens of shekels to several thousand". — [Bug Shark](https://www.bug.co.il/brand/shark/cryoglow/fw312eu); [Bug Ulike](https://www.bug.co.il/brand/ulike/um10); [i24](https://www.i24news.tv/he/news/news/health/artc-20604094)

**Overnight hair (heatless curler, satin bonnet / pillowcase)**
- FACT (Zap): "מסלסל ללא חום" returns 76 results but almost all are heated curlers; the one true heatless curler is 99 ILS at "כמה זול". "כובע סאטן" returns 3 irrelevant results (no bonnet listed). "כרית סאטן" returns 31 results. — [Zap heatless](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%A1%D7%9C%D7%A1%D7%9C%20%D7%9C%D7%9C%D7%90%20%D7%97%D7%95%D7%9D); [Zap bonnet](https://www.zap.co.il/search.aspx?keyword=%D7%9B%D7%95%D7%91%D7%A2%20%D7%A1%D7%90%D7%98%D7%9F)
- FACT: Kitsch's curler + XL bonnet "Nighttime Blowout Routine" bundle is USD 26 on sale (USD 40 list), 1,620 reviews, 4.8 stars (the he-il URL redirected to the USD page in my session). REPORTED: Kitsch Israel shows the single curling set at 84 ILS with free shipping and a satin pillowcase 2-pack at 138 ILS (180 list). — [Kitsch bundle](https://www.mykitsch.com/he-il/products/heatless-satin-curling-set-satin-sleep-bonnet-bundle-charcoal); [Kitsch he-il set](https://www.mykitsch.com/he-il/collections/hair-care/products/satin-heatless-curling-set-sunset-tie-dye); [Kitsch pillowcase](https://www.mykitsch.com/he-il/products/satin-pillowcase-in-blush-2-pack)
- FACT: Sacara (national low-cost beauty chain) sells satin scrunchie packs at 8 ILS; its site search shows no bonnet or heatless curler. — [Sacara search](https://www.sacara.co.il/catalogsearch/result/?q=%D7%A1%D7%90%D7%98%D7%9F)

**DIY lash clusters / press-on and gel nails**
- FACT: Sacara: strip lashes 14.90-15 ILS, individual lashes 15 ILS, 24-piece artificial nail sets 15 ILS, nail glue 24.90 ILS (111 reviews), semi-cured gel nail stickers 30 ILS. A search for "קלאסטר" returns no product. On Zap, Sacara nails are listed at 34 ILS and Ardell-type lashes at 54 ILS (shop "גל טורן"). — [Sacara lashes](https://www.sacara.co.il/catalogsearch/result/?q=%D7%A8%D7%99%D7%A1%D7%99%D7%9D); [Sacara nails](https://www.sacara.co.il/catalogsearch/result/?q=%D7%A6%D7%99%D7%A4%D7%95%D7%A8%D7%A0%D7%99%D7%99%D7%9D%20%D7%9E%D7%9C%D7%90%D7%9B%D7%95%D7%AA%D7%99%D7%95%D7%AA); [Zap nails](https://www.zap.co.il/search.aspx?keyword=%D7%A6%D7%99%D7%A4%D7%95%D7%A8%D7%A0%D7%99%D7%99%D7%9D%20%D7%9E%D7%9C%D7%90%D7%9B%D7%95%D7%AA%D7%99%D7%95%D7%AA)

**Teeth-whitening strips**
- FACT: Fresh Breath (freshbreath.co.il, Israeli oral-care DTC brand; claims "4.9, 30,000+ satisfied Israelis") lists whitening strips tagged "new": "natural formula without peroxide, 7 treatments of 30 minutes", from 189.90 ILS, free shipping, 60-day refund. Its best-seller tag is on an oil-pulling mouthwash from 169.90 ILS. — [freshbreath.co.il](https://freshbreath.co.il/)
- FACT (Zap): only one real result for "רצועות הלבנה": Crest 3D strips at 239 ILS (shop "נקסט-סטוק"). — [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%A8%D7%A6%D7%95%D7%A2%D7%95%D7%AA%20%D7%94%D7%9C%D7%91%D7%A0%D7%94)
- FACT: Bazaria-IL (generic store, 134 products, nearly all 129 ILS with a 260 ILS compare-at, oldest record 28 Sep 2025) added "Mr.Smiles" purple whitening sachets on 10 Nov 2026 at 129 ILS. — [bazaria-il.com products.json](https://bazaria-il.com/products.json?limit=250)
- REPORTED: a PAP+ (non-peroxide) whitening brand is imported to Israel by the dental-imaging chain Citydent. — [Walla](https://finance.walla.co.il/item/3852167)

**Nasal strips**
- FACT: AirStrips Israel (Shopify, 4 SKUs, records created 27-30 Oct 2025) sells ordinary adhesive nasal strips, 30 units for 64.90 ILS, gift pack above 150 ILS; one colour sold out. No magnetic product. — [airstrips.co.il](https://www.airstrips.co.il/collections/all?sort_by=best-selling)
- FACT: Zap "רצועות אף" shows only blackhead pore strips (35-50 ILS); no breathing strips, no magnetic strips. — [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%A8%D7%A6%D7%95%D7%A2%D7%95%D7%AA%20%D7%90%D7%A3)
- No Israeli seller of magnetic nasal strips was found in web search, Zap or the Ad Library. — [search result set](https://www.sciencefocus.com/wellbeing/i-tried-sticking-magnets-to-my-face-to-improve-my-sleep-heres-what-happened)

### Inferences
- The 400-1,000 ILS LED band is squeezed from both sides: an official brand with importer warranty at 483 ILS underneath, generic stores at 189-799 ILS discounting "50%", and Shark / Dreame / Ulike with instalments above. A new no-name mask at ~549 ILS has no obvious reason to be chosen.
- For hair accessories, lashes and nails the local reference price is 8-34 ILS (Sacara) — far below the 100-150 ILS a paid-ads store needs.

### Gaps
- Super-Pharm, KSP, Terminal X beauty, Laline, April and be could not be read or were not reached; their assortment and prices for these items are unknown.
- Review counts with dates per product were not obtainable (review widgets not parsed); store age is known only from Shopify record dates.

---

## 2. Cheap alternatives reachable by Israelis, and what separates a cheap LED mask from an expensive one

### Takeaway
AliExpress, priced in ILS for delivery to Israel, sells look-alikes of every candidate for 2-20 ILS (accessories, lashes, nails, strips) and 19-217 ILS (LED masks), with five-figure sold counts. For LED masks the real differences (wavelength accuracy, irradiance, eye safety, certification) are invisible to a shopper; the only specs consumers see are LED count, "7 colours" and "FDA" — which cheap sellers also claim.

### Cited Findings
- FACT (AliExpress, region Israel, currency ILS, sorted by orders, 11 Nov 2026, during the 11.11 sale; lowest figures such as ₪1.3 are "bundle deal" teaser prices that need 3+ items):
  - LED masks: ₪18.8 (10,000+ sold, 4.9); ₪86.9 with neck (5,000+ sold); ₪67-80 for 7-colour face+neck silicone (600-1,000+ sold each); ₪139.9 for 8-colour red + near-infrared (1,000+ sold); ₪216.39 "PDT" mask (1,000+ sold). — [AliExpress](https://www.aliexpress.com/w/wholesale-led-face-mask-red-light.html?SortType=total_tranpro_desc)
  - Heatless curling rod sets ₪1.3-5.73 (2K-7K+ sold each); curler + bonnet sets ₪2.3-3.57. — [AliExpress](https://www.aliexpress.com/w/wholesale-heatless-curling-rod-headband-satin.html?SortType=total_tranpro_desc)
  - Satin bonnets ₪2.2-9.7 (two listings at 40K+ sold). — [AliExpress](https://www.aliexpress.com/w/wholesale-satin-bonnet.html?SortType=total_tranpro_desc)
  - Lash clusters ₪4.6-8.3 per tray (many at 10K+ sold); full DIY kit with bond & seal, remover, tweezers ₪19.49 (10K+ sold, 4.8). — [AliExpress](https://www.aliexpress.com/w/wholesale-lash-clusters-kit.html?SortType=total_tranpro_desc)
  - Press-on nails ₪2.2-10 per set of 24-600 pieces (10K-50K+ sold). — [AliExpress](https://www.aliexpress.com/w/wholesale-press-on-nails.html?SortType=total_tranpro_desc)
  - Whitening strips (mostly purple "colour-corrector" type) ₪1.3-20.59 (1K-9K+ sold); ratings notably lower (4.1-4.5 on several). — [AliExpress](https://www.aliexpress.com/w/wholesale-teeth-whitening-strips.html?SortType=total_tranpro_desc)
  - Ordinary nasal strips ₪1.3-4.8 for 30-100 pieces (up to 60K+ sold); the only "magnetic" hits are old-style nose clips at ₪5.3 (20K+ sold, 4.2) — no Intake-style kit in the top results. — [AliExpress](https://www.aliexpress.com/w/wholesale-magnetic-nasal-strips.html?SortType=total_tranpro_desc)
- REPORTED (vendor blog citing a May 2026 Spanish university study I could not find): one 155-LED silicone mask measured ~63.7 mW/cm² directly over an LED but ~1.46 mW/cm² averaged across the face. — [Mito Red Light](https://mitoredlight.com/blogs/mito-red-blog/what-almost-everyone-doesnt-understand-about-red-light-therapy-masks)
- REPORTED (sellers' own claims, conflicting): generic Amazon masks ~15 mW/cm² vs ~60 for premium silicone ([EvenSkyn](https://www.evenskyn.com/ko/blogs/skin-beautyarticles/red-light-therapy-dose-2026-led-mask-irradiance-joules-fluence)); "most sub-$100 masks deliver 3-8 mW/cm²" (competitor claim, [RLE Pro](https://redlighttherapy-expert.pages.dev/product/rle-pro-led-mask/)); a lab cited by another seller measured 0.09-2.14 mW/cm² ([LED Esthetics](https://ledesthetics.com/blogs/news/best-clinical-grade-led-face-mask)). Solawave says it tests to IEC 62471 via a contract lab. — [Solawave](https://www.solawave.co/pages/science-wrinkle-retreat-pro)
- FACT: Shark CryoGlow holds US FDA 510(k) K242796 as an OTC LED mask. — [510(k) record](https://510k.innolitics.com/device/K242796)

### Inferences
- Irradiance numbers in the market are not comparable (peak vs average, self-measured). A small store cannot credibly prove superiority, and a consumer cannot verify it. Differentiation therefore collapses to brand, warranty, LED count and price.
- For every non-device candidate the delivered AliExpress price is 3-15% of the retail price a paid-ads store would need.

### Gaps
- Temu and Shein Israel prices and sold counts: unreadable. AliExpress delivery time and shipping fee per listing to Israel were not opened item by item.
- No independent, primary test of cheap vs premium mask irradiance was found.

---

## 3. Israeli demand signals (ads, press, trends)

### Takeaway
Paid-ad activity in Israel is clearly present for LED masks (at least 8 advertisers active in November 2026, led by brands) and for clinic tooth whitening; it is thin for whitening strips (2-3 advertisers), thin and low-quality for heatless/satin (cross-border mass stores), and not found at all for lash clusters, press-on nails or magnetic nasal strips. I have no search-trend data.

### Cited Findings (all FACT from Meta Ad Library, country IL, active ads, read 11 Nov 2026 unless noted)
- "מסכת LED" (exact phrase): ~37 results. Silkn.IL 19 ad cards, start dates 20 Oct-4 Nov 2026 ("Silk'n has arrived in Israel"; "LED Face Mask 100 LEDs at 483 ₪ / official importer warranty"); Bug 3 cards; HomeLuxe 2 (13 Sep and 26 Oct 2026); Dreame Beauty 1; Bee Skinny 1 (7 Nov). Unordered search (~130 results) adds Ulike Israel, Ya-Man Israel, אמפייר טק (14 Oct), In.Hub (25 Jun 2026 — the longest-running generic LED ad found) and one beautician. — [Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%A1%D7%9B%D7%AA%20LED&search_type=keyword_exact_phrase)
- "תלתלים ללא חום" (unordered): ~9 results. Kaufroom (4 cards, 4-11 Nov 2026: extra-long satin bonnet "half price"), Israelwind and Ecouaer (heated wavers, not heatless), LastPrice. Kaufroom and Israelwind are 250+-product stores with records created from Oct / May 2026, priced ~50-180 ILS. — [Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%AA%D7%9C%D7%AA%D7%9C%D7%99%D7%9D%20%D7%9C%D7%9C%D7%90%20%D7%97%D7%95%D7%9D&search_type=keyword_unordered); [kaufroom.com](https://kaufroom.com/products.json?limit=250)
- "סאטן שיער": Avalon Silk (pillowcase, long-form skin-care copy, started 8 Nov 2026) is the only relevant advertiser. — [Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A1%D7%90%D7%98%D7%9F%20%D7%A9%D7%99%D7%A2%D7%A8&search_type=keyword_unordered)
- "ריסים" (exact): ~1,000 results, but the sample is salons, lash-lift courses, mascara (Sacara, L'Oréal) and serums; no DIY cluster kit advertiser in 29 cards. "קלאסטרים", "ריסים מגנטיים", "ציפורניים נדבקות", "ערכת ציפורניים": no relevant ads (weak negative). — [Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A8%D7%99%D7%A1%D7%99%D7%9D&search_type=keyword_exact_phrase)
- "רצועות הלבנה" (exact): 2 results — Fresh Breath (cart-recovery ad, strips 189.90 ILS, started 20 Oct 2026) and Tel Aviv Select / Bazaria (purple sachets, 10 Nov 2026; copy says "I tried whitening strips at 150 ₪"). "הלבנת שיניים": ~280 results, overwhelmingly dental clinics; product sellers in the sample: Freshy il (started 14 Aug 2026; its site was password-locked today), Smiley (running since 19 Oct 2025, "whitening stickers as a gift"), Forever White Israel (B2B). One clinic ad contrasts "home whitening" with "safe whitening by a dentist". — [Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%94%D7%9C%D7%91%D7%A0%D7%AA%20%D7%A9%D7%99%D7%A0%D7%99%D7%99%D7%9D&search_type=keyword_unordered); [freshyil.com](https://freshyil.com/)
- "נחירות" (exact): ~310 results. Anti-snoring is a crowded Israeli ad category (SnoreAway via several pages, ergonomic pillows, tongue device, clinics). AirStrips Israel runs nasal-strip ads since 14 Aug 2026 ("back in stock after crazy demand", "3+1"). No magnetic strip advertiser; "רצועות אף מגנטיות" returned nothing. — [Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%A0%D7%97%D7%99%D7%A8%D7%95%D7%AA&search_type=keyword_exact_phrase)

### Inferences
- LED masks: Israeli demand is real but is being bought by brands with warranty, instalments and November "no-VAT" promotions. Most ads are days or weeks old (launch / Black-November bursts), so longevity of profitable generic campaigns is unproven except In.Hub (since June) and HomeLuxe (since September).
- Whitening strips: a credible local operator (Fresh Breath) added strips as a line extension to an existing oral-care customer base — evidence of perceived demand, but also that strips are being sold as an upsell, not as a hero product.
- Lashes / nails / magnetic nasal strips: absence of Israeli advertisers is either a gap or a sign that the economics do not support ads; given Sacara's 15 ILS prices, the second reading is more likely.

### Gaps
- Google Trends geo=IL (5 years) for all Hebrew terms: not obtained (HTTP 429). Trend direction in Israel is therefore unknown for every candidate.
- TikTok / Instagram Israeli creator activity: not measured. A Hebrew press search found no article on any of these products except general LED-mask coverage (i24) — [i24](https://www.i24news.tv/he/news/news/health/artc-20604094).
- Ad Library gives no spend or impressions for commercial ads in Israel; "advertiser count" is a floor, not a census.

---

## 4. Regulation in Israel

### Takeaway
Whitening is the best-documented trap: the Ministry of Health treats anything above 0.1% hydrogen peroxide as a medical device sold only in pharmacies on a dentist's prescription, so only genuinely peroxide-free strips, notified as cosmetics, are sellable. Lash glue, nail glue/gel and strips all need a registered cosmetics dealer, a responsible representative and a per-product notification. Whether a home LED mask is a medical device (AMAR) in Israel is unresolved in my research.

### Cited Findings
- FACT (Ministry of Health, Dental Health Division position paper dated 5 May 2014, read in full): (1) whitening products up to 0.1% hydrogen peroxide (or equivalent) are cosmetics sold to the public; (2) above 0.1% up to 6% are medical devices, sale conditional on registration and "to the public in a pharmacy only, on a dentist's prescription", age 18+; (3) 6-33% only for dentists; (4) above 33% banned. Whitening another person is dentistry — forbidden to cosmeticians. Products not registered as a cosmetic or medical device must not be used. — [gov.il PDF](https://www.gov.il/BlobFolder/reports/dental-teeth-whitening/he/files_publications_units_dental_dental-teeth-Whitening.pdf)
- FACT (observed listing): Crest 3D strips (a peroxide product) are offered on Zap at 239 ILS outside a pharmacy. — [Zap](https://www.zap.co.il/search.aspx?keyword=%D7%A8%D7%A6%D7%95%D7%A2%D7%95%D7%AA%20%D7%94%D7%9C%D7%91%D7%A0%D7%94)
- REPORTED (gov.il service pages as summarised by search; pages themselves blocked): dealers who import, store or distribute cosmetics must be in the cosmetics dealers register; a responsible representative files a notification before marketing; the European-route notification requires an importer registered as a "proper importer", an appointed responsible representative and a free-sale certificate, and the notification service itself is free of charge. — [gov.il European route](https://www.gov.il/he/service/cosmetics-marketing-europe); [gov.il basic route](https://www.gov.il/he/service/cosmetics-marketing); [gov.il dealer registration](https://www.gov.il/he/service/cosmetics-business); [responsible representatives database](https://www.gov.il/he/service/registration-database-responsible-representatives)
- REPORTED: the EU banned TPO (a gel-nail photoinitiator) in all cosmetics from 1 Sep 2025, including existing stock and professional use. — [Cosmetics Business](https://www.cosmeticsbusiness.com/european-union-bans-popular-ingredient-tpo); [Khaleej Times](https://www.khaleejtimes.com/world/eu-gel-nail-polish-tpo-ban). Sources conflict on HEMA: one says HEMA/Di-HEMA have been professional-use-only in the EU since 2021, another folds HEMA into the 2025 measures. — [Alibaba guide](https://reads.alibaba.com/is-gel-nail-polish-banned-in-europe-the-definitive-guide-for-buyers-businesses/); [Weightmans](https://www.weightmans.com/media-centre/news/chemicals-used-in-nail-products-raising-health-concerns/)
- REPORTED: PAP enamel safety is contested — a 2021 study on Hismile's PAP+ formula (maker-linked, in vitro) found no microhardness loss; a 2025 Portuguese master's thesis found reduced microhardness and higher roughness. EU limit is 0.1% hydrogen peroxide present or released. — [PMC study](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8700120/); [thesis](https://comum.rcaap.pt/bitstreams/9e584026-2331-484c-bf54-9e6b3fec2ae0/download); [Danish EPA](https://www2.mst.dk/Udgiv/publikationer/2021/09/978-87-7038-339-4.pdf)
- REPORTED: Israeli law defines a medical device as any device intended for treatment or assisting treatment of people. — [State Comptroller 2008](https://library.mevaker.gov.il/sites/DigitalLibrary/Documents/1950-2008/2008-58b/2008-58b-219-AvizarimRefuim.docx). An Israeli retailer page says Shark CryoGlow is "approved by the FDA, the Israeli Ministry of Health and the Standards Institute" (seller claim, no registration number). — [Sofer Avi](https://www.soferavi.co.il/מוצרים/אביזרי-טיפוח-שארק-⁦fw312eu⁩/)
- REPORTED: personal import is defined as a reasonable quantity for own use (Personal Import Order 2019). — [Protocol](https://protocol.co.il/personal-import/)
- REPORTED (advertising-claims precedent, UK not Israel): in Nov 2025 the UK ASA upheld rulings against four LED-mask advertisers — Beautaholics, Luyors, Project E Beauty and **Silk'n** — for acne / rosacea claims without medical-device registration; testimonials do not excuse the claim. — [Professional Beauty](https://professionalbeauty.co.uk/asa-bans-led-mask-adverts-over-acne-and-rosacea-claims); [ASA ruling](https://www.asa.org.uk/rulings/project-e-beauty-llc-a25-1293784-project-e-beauty-llc.html); [Osborne Clarke](https://marketinglaw.osborneclarke.com/advertising-regulation/claims-made-for-led-facemasks-scrutinised-by-the-asa/)

### Inferences
- A "purple" colour-corrector strip and a PAP strip are both outside the peroxide rule but both still need cosmetics notification; a store dropshipping un-notified strips to Israelis is exposed (MoH: "do not use products not registered").
- Lash bond (cyanoacrylate / acrylate copolymer near the eye) and nail glue or gel are the regulated parts of those kits; the lashes and plastic nails themselves are not cosmetics. A kit without the adhesive is legally simple but commercially incomplete.
- LED mask: if the importer of the market-leading mask advertises MoH approval, a prudent reading is that at least acne-treating (blue light) masks are handled as medical devices. Marketing a generic mask with "treats acne / rosacea / wrinkles" language is the highest-risk combination. UNVERIFIED — needs a written answer from the MoH medical devices unit.

### Gaps
- AMAR classification of home LED masks; whether a nasal dilator is a medical device in Israel; official electrical-safety / charger standards and import group for a USB-powered mask; licensing fees and timeline for cosmetics dealer registration; responsible-representative service prices; quantity limits for cosmetics in personal-import parcels; whether Israel has adopted the EU TPO ban — none could be confirmed (gov.il blocked, no secondary source found).

---

## 5. Sourcing

### Takeaway
I obtained no fresh factory quotes (Alibaba blocked). Existing asking prices put a decent LED mask at roughly USD 22-32 in volume and USD 72-85 for small-quantity silicone models — a spread that decides whether the product is viable. For everything else, the AliExpress retail price (2-20 ILS) is an upper bound on product cost.

### Cited Findings
- REPORTED (asking prices, undated, not quotes): Global Sources 850/630 nm mask with a "510K" claim USD 24.16 (1,000-4,999 pcs) to 21.52 (10,000+), 30-32 day lead time; Beautetrade OEM 630/850 nm mask FOB USD 25-32, MOQ 2; Alibaba UK custom-logo silicone mask USD 85 (1-100 pcs) / 79 (101-500) / 72 (501+); typical logo-only OEM MOQ 300-500 units. — [Global Sources](https://www.globalsources.com/LED-therapy/LED-Face-1238502344p.htm); [Beautetrade](https://www.beautetrade.com/products/pakiss-professional-standing-8-color-led-facial-mask-with-red-blue-light-therapy-for-skin-care-oemodm-wholesale/92958/); [Alibaba UK](https://www.alibaba.co.uk/product-detail/Custom-Logo-Red-Light-Therapy-Mask_1601395359112.html); [Alibaba guide](https://www.alibaba.com/price-comparison/red-light-face-mask-distributor)
- REPORTED: DIY segmented cluster lashes USD 1.49-2.99 per unit at MOQ 10 with private label; private-label trays USD 1.51-2.00; DIY kits usually MOQ 50-200. No verified price for a complete bond-and-seal kit. — [china.org.ru listing](https://china.org.ru/product/1600892321825); [Alibaba SmartBuy](https://smartbuy.alibaba.com/best-selling/eyelashes-extensions-top-sellers); [Alibaba seller blog](https://seller.alibaba.com/blogs/2026/southeast-asia/beauty/professional-vs-diy-eyelash-extension-procurement-guide-alibaba)
- FACT: a complete DIY lash kit retails on AliExpress at ₪19.49 delivered-price level and curler + bonnet sets at ₪2.3-5.7 (see section 2) — [AliExpress lash kit](https://www.aliexpress.com/w/wholesale-lash-clusters-kit.html?SortType=total_tranpro_desc)
- FACT: one Israeli advertiser states its 240-LED silicone mask weighs 260 g. — [Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%A1%D7%9B%D7%AA%20LED&search_type=keyword_unordered)

### Inferences
- A mask with a real test file (wavelength, photobiological safety, EMC) at a 100-300 unit order is more likely to cost USD 40-80 than USD 22-28; the low figures are 1,000+ unit prices from listings whose "510K" claims are unverified.
- Rechargeable masks contain a lithium battery in the controller, so air freight needs a battery-capable line (ASSUMPTION — confirm with the forwarder).

### Gaps
- No quotes from 1688, CJ Dropshipping or Global Sources for lash kits, press-on kits, non-peroxide strips or hair bundles; no packed weights; no defect or return-rate data for any product; no MOQ for custom-boxed hair bundles.

---

## 6. Intellectual property

### Takeaway
The two patents most often cited against copycats — Intake's magnetic nasal strip patent and Lashify's lash-extension patent — show no Israeli family member on Google Patents, so a direct patent claim in Israel looks unlikely on these two documents; the practical risk is enforcement through US platforms and suppliers. I did not search the Israel Patent Office.

### Cited Findings
- FACT (Google Patents): US 9,510,969 "Nasal element for a breathing system", current assignees Castillo Investments LP and Intake Breathing Technology LLC, priority 20 Dec 2013, anticipated expiry 30 Sep 2034; family countries listed: US, EP, JP, CN, AU, WO — no IL. Claim 1 covers a disposable adhesive nose-mounted element with a metallic member that interacts with a magnet to dilate the nose. — [Google Patents](https://patents.google.com/patent/US9510969B2/en)
- REPORTED: Intake has sued several US sellers and, on 18 Jun 2026, the dropshipping platform Zendrop. — [Justia docket](https://dockets.justia.com/docket/florida/flsdce/9:2026cv80725/716982)
- FACT (Google Patents): US 10,660,388 "Artificial lash extensions", Lashify Inc, priority 28 Jul 2016, anticipated expiry 27 Jul 2037; family: US, EP, JP, KR, CN, AU, DK, ES, HK, WO — no IL. Claim 1 is a method using heat-fused cluster "lash fusions" applied to the underside of the natural lash. — [Google Patents](https://patents.google.com/patent/US10660388B2/en)
- REPORTED: in Lashify v. ITC (Fed. Cir., 5 Mar 2025) the court widened what counts as US "domestic industry" but upheld the finding that Lashify's own products did not practise its utility patent's "heat-fused" limitation; the remand concerned design patents and was terminated in Aug 2025 after settlement. — [Foley](https://www.foley.com/insights/publications/2025/03/federal-circuit-domestic-industry-investment/); [Sterne Kessler](https://www.sternekessler.com/news-insights/insights/2025-federal-circuit-ip-appeals-lashify-inc-v-intl-trade-commn-130-f-4th-948-fed-cir-2025-prost-taranto-chen/); [USITC notice Aug 2025](https://www.usitc.gov/sites/default/files/secretary/fed_reg_notices/337/337_1226_notice08282025sgl.pdf)
- REPORTED: heatless curlers — a US design patent D1,029,387 (Fromm, "heatless volumizing hair rod") was litigated in late 2025 against Overnight Blowout; Kitsch litigates design patents on other products (towels, shower caddies, hair coils), no Kitsch heatless-rod suit found. — [PatSnap](https://www.patsnap.com/resources/blog/litigation/fromm-international-v-overnight-blowout-voluntary-dismissal-in-heatless-hair-styling-patent-dispute-patsnap-eureka/); [PatSnap Kitsch](https://www.patsnap.com/resources/blog/litigation/kitsch-llc-v-schedule-a-defendants-hair-towel-design-patent-patsnap/)
- REPORTED: LED masks — Solawave sued "Schedule A" sellers over a mask design patent (dismissed); DMH Aesthetics pursues trade-dress claims on LED face shields; no Omnilux or CurrentBody patent suit found. — [PatSnap](https://www.patsnap.com/resources/blog/litigation/solawave-inc-v-schedule-a-defendants-light-therapy-device-patent-patsnap/); [The Fashion Law](https://www.thefashionlaw.com/dmh-is-waging-a-trademark-infringement-dilution-case-against-sellers-of-lookalike-face-masks/)

### Inferences
- Israel is not covered by a European patent, so "EP" in a family does not reach Israel (general knowledge, UNVERIFIED here). The exposure for an Israeli store is (a) Shopify / Meta takedowns on a US complaint, (b) losing a US-based supplier, (c) Israeli registered designs or trademarks I did not check.
- Generic masks that copy the look of Shark, Omnilux or CurrentBody carry design / trade-dress risk; a plain OEM silicone mask does not obviously do so.

### Gaps
- Israel Patent Office and Israeli design / trademark registers were not searched for Intake, Lashify, Kitsch, Omnilux, CurrentBody, Dr Dennis Gross or SharkNinja. Other Intake and Lashify patents (they hold several) were not checked for IL members.

---

## 7. Adversarial review — reasons each candidate fails

### Takeaway
Every candidate has at least one serious contradiction. The most damaging are: for LED masks, a brand at 483 ILS plus regulator action on claims plus falling US sales; for hair, lashes and nails, a 10-30x price gap to Sacara and AliExpress; for strips, weak efficacy of legal formulas and refund guarantees as the market norm; for magnetic nasal strips, active US litigation against a dropshipping platform and no Israeli demand signal.

### Cited Findings
- LED masks: most top Amazon US listings fell 33-67% month-over-month in Aug 2026 (ESTIMATE, from the first research round) — [ASINsight](https://www.asinsight.com/report/US/red-light-therapy-mask). UK regulator rulings against four advertisers including Silk'n (REPORTED) — [Professional Beauty](https://professionalbeauty.co.uk/asa-bans-led-mask-adverts-over-acne-and-rosacea-claims). A trade article is titled "Unregulated LED masks 'flooding' the beauty market" (20 Nov 2025; page returned HTTP 410, title only) — [CosmeticsDesign](https://www.cosmeticsdesign-europe.com/Article/2025/11/20/unregulated-led-masks-flooding-the-beauty-market-says-expert). Eye-safety precedent: Neutrogena recalled its light-therapy acne mask in 2019 over eye-injury risk; Health Canada and the Australian TGA acted too (REPORTED) — [FDAnews](https://fdanews.com/articles/192039-jj-recalls-acne-mask-and-activator-over-risks-of-eye-damage). No 2025-2026 FDA or FTC action specific to LED masks was found.
- LED masks, Israel: a 189 ILS mask on Zap, a 483 ILS official-brand mask, 499 and 799 ILS generic offers "at 50% off", and AliExpress at ₪19-217 (FACT, sections 1-2).
- Hair bundle: an Israeli-targeted mass store is already advertising a satin bonnet at "half price"; Kitsch's own curler + bonnet bundle is USD 26 (≈ 82 ILS) (FACT, sections 1 and 3).
- Lashes / nails: Sacara 15 ILS; EU TPO ban and HEMA allergy concerns for home gel kits (REPORTED, section 4).
- Strips: Israeli sellers lead with money-back guarantees ("60 days", "didn't see results — full refund") (FACT, ad texts) — [Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%94%D7%9C%D7%91%D7%A0%D7%AA%20%D7%A9%D7%99%D7%A0%D7%99%D7%99%D7%9D&search_type=keyword_unordered). DrDent strips fell out of the US TikTok Shop top 10 in Q2 2026 (ESTIMATE, first round) — [FastMoss](https://www.fastmoss.com/blog/best-selling-tiktok-shop-products-us-q2-2026/). AliExpress strip ratings of 4.1-4.5 are low for that platform (FACT, section 2).
- Magnetic nasal strips: Intake v. Zendrop (REPORTED) — [Justia](https://dockets.justia.com/docket/florida/flsdce/9:2026cv80725/716982). A Hebrew medical site notes snoring usually originates in the throat, not the nose (REPORTED) — [doctors.co.il](https://www.doctors.co.il/medical-symptom/otorhinolaryngology/nasal-strip/). Ordinary strips sell locally at 64.90 ILS per 30 and on AliExpress at ₪1-5 (FACT).

### Inferences
- Why Israelis would not pay: (1) the same-looking item is one search away at 5-20% of the price; (2) for a 500+ ILS device they can choose a known brand with importer warranty and 12 instalments; (3) results from LED masks and peroxide-free strips are slow or subtle, which drives refund claims under the guarantees the market already offers.
- Saturation is highest exactly where demand evidence is best (LED masks), and demand evidence is absent where saturation is low (cluster lashes, magnetic strips).

### Gaps
- No Israeli complaint data (consumer forums, Facebook groups, small-claims rulings) and no return-rate data were collected.

---

## 8. Unit economics for the three strongest (ILS per order)

### Takeaway
On transparent assumptions, a 549 ILS LED mask breaks even at a CPA of about USD 57 if the landed unit cost is ~178 ILS, but turns loss-making if the unit costs USD 80 or the price must drop to 399 ILS. Peroxide-free strips break even at ~USD 28 for a single 189.90 ILS box and ~USD 45 for a 279 ILS two-box offer. The hair bundle breaks even at ~USD 18 at 149 ILS — below the whole CPA range — and only reaches ~USD 36 as a 249 ILS double bundle.

### Cited Findings (inputs)
| Input | Value | Label and source |
|---|---|---|
| VAT | 18% of price ÷ 1.18 | REPORTED — [VATupdate](https://www.vatupdate.com/2025/12/10/israel-approves-2026-budget-vat-stays-at-18-expands-exemptions-eases-bank-entry-rules) |
| USD/ILS | 3.172 | VERIFIED — [BoI](https://boi.org.il/PublicApi/GetExchangeRates) |
| Payment fees | 3% of price | REPORTED range 2.5-4% — [Sitelink](https://sitelink.co.il/web/ecommerce/payment-solutions-for-businesses-israel-2026/) |
| CPA scenarios | USD 25 / 32 / 40 = 79 / 102 / 127 ILS | REPORTED median ≈ USD 32, single vendor — [Superads](https://www.superads.ai/facebook-ads-costs/cost-per-purchase/israel) |
| Domestic delivery (free to customer) | 38 ILS device; 30 ILS small parcel | REPORTED list price 38 — [D2D](https://www.d2d.co.il/blog/ecommerce-delivery-israel); 30 is an ASSUMPTION |
| Cancellation fee kept | min(5% of price, 100 ILS) | REPORTED — [Bizportal](https://www.bizportal.co.il/financialconsumerism/news/article/20042624) |
| Retail price anchors | mask 483-799; strips 189.90; Kitsch set 84 | VERIFIED (section 1) |
| LED unit cost | USD 28 / 45 / 80 | REPORTED asking prices 22-32 and 72-85 (section 5); USD 45 mid-case is an ASSUMPTION |
| LED freight + clearance per unit | 35 ILS | ASSUMPTION |
| Strips landed cost | 15 ILS per box | ASSUMPTION (no quote; AliExpress retail ₪2-20) |
| Hair bundle landed cost | 30 ILS (curler, bonnet, scrunchies, box) | ASSUMPTION (AliExpress retail ₪5-15 for the parts; better fabric assumed) |
| Regulatory / service reserve | mask 3% of price; strips 8 ILS per box | ASSUMPTION |
| Return / refund rate | mask 10% (unit resold at 50% value); strips 8% (no salvage); hair 3% | ASSUMPTION |

Results (expected contribution before ads = kept orders × margin − returned orders × loss; "profit" = that minus CPA):

| Scenario | Net of VAT | Landed | Pre-ad contribution | Break-even CPA | Profit at CPA $25 / $32 / $40 |
|---|---|---|---|---|---|
| LED mask 549 ILS, unit USD 45 | 465 | 178 | 180 | 180 ILS = USD 57 | +100 / +78 / +53 |
| LED mask 549 ILS, unit USD 28 | 465 | 124 | 231 | USD 73 | +152 / +130 / +104 |
| LED mask 549 ILS, unit USD 80 (small-MOQ silicone) | 465 | 289 | 74 | USD 23 | −5 / −27 / −53 |
| LED mask forced down to 399 ILS, unit USD 45 | 338 | 178 | 73 | USD 23 | −7 / −29 / −54 |
| Strips, 1 box 189.90 ILS | 161 | 15 | 88 | USD 28 | +9 / −13 / −39 |
| Strips, 2 boxes 279 ILS | 236 | 27 | 144 | USD 45 | +64 / +42 / +17 |
| Hair bundle 149 ILS | 126 | 30 | 58 | USD 18 | −21 / −44 / −69 |
| Hair double bundle 249 ILS | 211 | 55 | 113 | USD 36 | +33 / +11 / −14 |
| Lash or nail kit 119 ILS (for reference) | 101 | 20 | 36 | USD 11 | −44 / −66 / −91 |

Maximum viable landed cost (ESTIMATE from the same model): LED mask at 549 ILS — break-even at ≤ 284 / 260 / 234 ILS and a 15% net margin at ≤ 210 / 187 / 160 ILS for CPA USD 25 / 32 / 40. Strips at 279 ILS two-box — 15% margin at ≤ 56 / 34 / 8 ILS. Hair double bundle 249 ILS — 15% margin at ≤ 57 / 34 / 9 ILS.

### Inferences
- The CPA band of USD 25-40 comes from a median across all price points; a 549 ILS considered purchase will probably cost more per order than a 150 ILS impulse item. At CPA USD 60 the mid-case mask loses 11 ILS per order. The mask case is therefore viable only if both unit cost ≤ ~USD 45-55 landed and CPA ≤ ~USD 50 hold at the same time.
- Strips work only as a multi-box offer or with real reorders; a single box is at break-even at the median CPA before any fixed regulatory cost.
- The hair bundle cannot carry paid acquisition on its own at any realistic single-bundle price; it fits as a post-purchase upsell or free-gift add-on.

### Gaps
- No measured CPA, conversion rate or reorder rate for any of these in Israel; no real quotes; return rates are assumptions. Fixed costs (cosmetics dealer registration, responsible representative, test reports, AMAR advice) are not in the per-order figures.

---

## 9. Verdict per candidate, conditions, failure modes, cheapest validation tests

### Takeaway
None of the five earns an unconditional go. Two are worth a cheap demand test before any stock or licence spend: peroxide-free whitening strips as a multi-box offer, and an LED mask only if a documented unit can be landed under ~190 ILS. The overnight-hair bundle is an add-on, not a hero. Lash clusters / press-on nails and magnetic nasal strips should be dropped.

### Cited Findings (evidence each verdict rests on is cited in sections 1-8)
1. **LED red-light mask (400-1,000 ILS) — CONDITIONAL.** For: 8+ Israeli advertisers active this month and three generic stores holding 499-799 ILS price points ([Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%9E%D7%A1%D7%9B%D7%AA%20LED&search_type=keyword_exact_phrase)); model breaks even up to CPA USD 57 in the mid case. Against: Silk'n at 483 ILS with importer warranty ([silkn.co.il](https://www.silkn.co.il/products.json?limit=250)); 189 ILS masks on Zap ([Zap](https://www.zap.co.il/search.aspx?keyword=%D7%9E%D7%A1%D7%9B%D7%AA%20%D7%9C%D7%93)); AliExpress ₪19-217 ([AliExpress](https://www.aliexpress.com/w/wholesale-led-face-mask-red-light.html?SortType=total_tranpro_desc)); unresolved medical-device status; claims enforcement abroad ([Professional Beauty](https://professionalbeauty.co.uk/asa-bans-led-mask-adverts-over-acne-and-rosacea-claims)); falling US sales ([ASINsight](https://www.asinsight.com/report/US/red-light-therapy-mask)).
2. **Overnight hair bundle — REJECT as lead product; keep as add-on.** Break-even CPA USD 18 at 149 ILS; parts at ₪2-10 on AliExpress ([AliExpress](https://www.aliexpress.com/w/wholesale-heatless-curling-rod-headband-satin.html?SortType=total_tranpro_desc)); Kitsch bundle USD 26 ([Kitsch](https://www.mykitsch.com/he-il/products/heatless-satin-curling-set-satin-sleep-bonnet-bundle-charcoal)); a mass store already advertises the bonnet in Hebrew ([Ad Library](https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IL&q=%D7%AA%D7%9C%D7%AA%D7%9C%D7%99%D7%9D%20%D7%9C%D7%9C%D7%90%20%D7%97%D7%95%D7%9D&search_type=keyword_unordered)).
3. **DIY lash clusters / press-on and gel nail kits — REJECT.** Sacara at 15 ILS ([Sacara](https://www.sacara.co.il/catalogsearch/result/?q=%D7%A6%D7%99%D7%A4%D7%95%D7%A8%D7%A0%D7%99%D7%99%D7%9D%20%D7%9E%D7%9C%D7%90%D7%9B%D7%95%D7%AA%D7%99%D7%95%D7%AA)); full kit ₪19.49 on AliExpress ([AliExpress](https://www.aliexpress.com/w/wholesale-lash-clusters-kit.html?SortType=total_tranpro_desc)); no Israeli DIY-kit advertiser found; adhesives and gels need cosmetics notification; break-even CPA ~USD 11.
4. **Non-peroxide whitening strips — CONDITIONAL (best candidate for a demand test).** For: an Israeli DTC brand prices them at 189.90 ILS ([Fresh Breath](https://freshbreath.co.il/)); peroxide products are legally pharmacy-only, which removes Crest-type competition from lawful channels ([MoH paper](https://www.gov.il/BlobFolder/reports/dental-teeth-whitening/he/files_publications_units_dental_dental-teeth-Whitening.pdf)); consumable; two-box offer breaks even at CPA USD 45. Against: cosmetics registration and notification are prerequisites; contested PAP safety and modest results ([thesis](https://comum.rcaap.pt/bitstreams/9e584026-2331-484c-bf54-9e6b3fec2ae0/download)); refund guarantees are the local norm; ₪2-20 on AliExpress ([AliExpress](https://www.aliexpress.com/w/wholesale-teeth-whitening-strips.html?SortType=total_tranpro_desc)).
5. **Magnetic nasal strips — REJECT.** No Israeli family member on the main patent ([Google Patents](https://patents.google.com/patent/US9510969B2/en)), but Intake is suing a dropshipping platform ([Justia](https://dockets.justia.com/docket/florida/flsdce/9:2026cv80725/716982)); no Israeli seller or ad found; no Intake-style kit among AliExpress top results, so supply is thin; possible medical-device status unresolved. Ordinary nasal strips are already sold locally at 64.90 ILS ([AirStrips](https://www.airstrips.co.il/collections/all?sort_by=best-selling)).

### Inferences
- Conditions for the LED mask: a supplier file with wavelength and photobiological-safety reports and a landed cost ≤ ~190 ILS at ≤ 300 units; written MoH guidance on classification; cosmetic-only wording ("appearance of skin"), no acne / rosacea / wrinkle-treatment claims; a 12-month local warranty; opaque eye protection. It fails if CPA exceeds ~USD 55, if Silk'n or a generic store drops to ~399 ILS, or if returns exceed ~15%.
- Conditions for strips: genuinely peroxide-free formula with full ingredient list and safety documentation from the factory, a contracted responsible representative, notification done before any sale, offer built as 2-3 boxes (≥ 249 ILS), honest "brightening / stain" wording. It fails if refunds exceed ~15%, if reorders do not appear, or if the regulatory set-up cost cannot be spread over ~1,000+ boxes.
- Cheapest validation tests before spending on stock or licences (ASSUMPTION on budgets): (1) fake-door Hebrew landing pages for the two conditional products with ~1,500-2,500 ILS of Meta spend each, measuring cost per checkout-initiation against the break-even CPAs above (no payment taken); (2) one email to the MoH medical-devices unit and one call to a cosmetics responsible-representative firm for classification, fees and timeline; (3) three factory RFQs per product asking for test reports, packed weight and a 100-300 unit price; (4) order one AliExpress mask at ~₪70-140 and one at ~₪217 plus the Silk'n 483 ILS mask to see whether any difference is visible to a buyer; (5) re-pull Google Trends for the Hebrew terms from a normal browser; (6) re-check the same Ad Library searches in 30 days — any generic LED or strips ad still running from today's list is a profitability signal.
- Given that all five are weak to conditional, the partners should weigh these against the non-beauty candidates in the other notes before committing.

### Gaps
- No Israeli sales data for any candidate; verdicts rest on price observation, ad presence and a model with assumed costs, refund rates and CPAs.
- Temu / Shein Israel pricing, Google Trends, TikTok creator activity, AMAR status, cosmetics fees and Israeli IP registers remain unverified and could change the LED-mask and strips verdicts in either direction.
