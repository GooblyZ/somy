# Shared brief for the deep product hunt (2026-11-15)

## Goal
Three partners run a small Israeli Shopify store (Hebrew, ILS). They want to find products that will REALLY sell in Israel:
trending products, things that clearly work (proven sellers), a good deal for the customer, or something that solves a
real problem. They judge best by seeing the product (a visual catalog will be built from your JSON), so each product needs a
real AliExpress listing and a working product image URL.

They explicitly asked NOT to obsess over margin math. Focus on: does it sell in volume NOW (evidence), why does it catch,
who buys it, is it rising or fading, is it already crowded in Israel. Still record the AliExpress price and one Israeli retail
price if you see one. Physical products only.

## Avoid repeats
These products were already shown to the partners — do NOT include them (or near-identical variants) unless you have
exceptionally strong new evidence, in which case mark "repeat": true:
5-in-1 bald-head shaver; heated beard straightener; beard bib; magnetic screw wristband; thermal label printer; MagSafe
vacuum suction phone mount; wireless lavalier mic; wireless CarPlay adapter; windshield umbrella sunshade; cordless tire
inflator; meat thermometers; plasma lighter; sand-free beach mat; cooling towel; mini massage gun; cordless straightening
brush; heated root-volume clip; heated eyelash curler; blackhead vacuum; heated eye mask; scalp massager; neck massager
pillows/wraps; Italian charm bracelet; bag charms; magnetic phone strap; nylon crossbody bag; instant print cameras; pocket
printer; sunset lamp; galaxy/astronaut projector; claw clips; water ripple lamp; TV backlight sync; levitating moon lamp;
Minipresso; gravity salt grinder; sleep headphones; sunrise alarm; karaoke mic speaker; WiFi photo frame; R36S console;
bird feeder camera; drill flex shaft / 90° adapter / universal socket; magnetic pickup claw; contour gauge; COB headlamp;
magnetic work light; drill brush; screw extractor; stud finder; electrician multi-pliers; dent puller; seat gap filler;
caulking tool; weeding rake; fishing knot tool; tool wall rack; spin scrubber; vegetable chopper; jar opener; oil sprayer;
silicone stretch lids; lint remover; vacuum storage bags; LED magnifier; reading glasses; needle threader; heel gel socks;
compression socks; dermaplaning razors; ice roller/gua sha; photo diamond painting; LCD writing tablet; LED candles; pill
organizer; self-watering stakes; shower filter; washing-machine tablets; LED face mask; lash clusters; press-on nails;
whitening strips; heatless curlers; name necklaces; flight backpacks; pet hair roller; cat fountain; crochet kits; book nooks;
busy boards; Shabbat lamps. HARD EXCLUSION: scented body cream and pheromone products.

## Output schema (JSON array, UTF-8, Hebrew fields in natural Hebrew)
{ "id": "<lens>-<n>", "audience": "men|women|kids|young_men|young_women|everyone|parents|pets",
  "subarea_he": "...", "name_he": "...", "name_en": "...",
  "what_he": "one line: what it does",
  "why_catches_he": "the hook — why people buy (problem / deal / trend / wow / gift)",
  "demo_he": "5–10 second video idea",
  "volume_evidence": "concrete numbers with source + date (label FACT/REPORTED/ESTIMATE)",
  "volume_strength": 1-5, "trend": "rising|stable|fading|unknown",
  "israel_presence": "Hebrew advertisers / Israeli sellers seen, with date; or 'none found (unverified)'",
  "price_israel": "e.g. '149 ₪ at X' or null", "price_abroad": "e.g. '$29.99 Amazon' or null",
  "ali_price_ils": number or null, "ali_sold": "as shown, e.g. '10,000+'",
  "ali_url": "https://www.aliexpress.com/item/....html", "image_url": "direct https image link from the AliExpress card",
  "risk_he": "main risk (IP/brand copy, certification for electrical/battery/wireless/toys/cosmetics, quality, fit)",
  "lens": "<your lens name>", "repeat": false }

## Methods that work in this environment
- AliExpress search via headless Chromium (Node: require('playwright'); chromium.launch() needs no options; do NOT run
  playwright install). Sort by orders: https://www.aliexpress.com/w/wholesale-<terms>.html?SortType=total_tranpro_desc .
  Set IL region/ILS cookie if possible. Extract title, price, sold, item URL, image src from result cards. Prices like
  ₪1.3–3.59 are usually new-shopper promos — record the regular price if shown. Get image_url for EVERY product.
- Meta Ad Library: https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=<IL|US|GB>&q=<term>&search_type=keyword_unordered
  — FRESH browser context per query; an empty page may be a false zero (say "unverified").
- Web search for trend reports (FastMoss, Kalodata, EchoTik, Tabcut, Shoplus blog rankings, TikTok Creative Center, Exploding
  Topics, Google Trends articles, Amazon Movers & Shakers mirrors, press). Amazon itself often blocks headless browsers.
- Do NOT circumvent captchas or log in anywhere. If a source is blocked, say so.
- Keep scripts ONLY in your own scratchpad subfolder (given in your task). Stay within ~45 tool calls.

## Deliverables
- Notes: <your file>.md — sources, what you found per product (FACT/REPORTED/ESTIMATE/UNVERIFIED, URL + date), and at the end
  "Top 5 for Israel and why".
- JSON: <your file>.json — 15–25 products in the schema above, each with ali_url and image_url.
