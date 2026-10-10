# Batya's Kitchen — Website Analysis for Mobile App Design

Source: https://www.batyaskitchen.com (crawled 2026-10-10)
Assets downloaded to: `assets/` (same folder structure as the live site)
Full menu data: `data/menu.json` and `data/menu.csv` (367 items)

---

## 1. Business summary

| | |
|---|---|
| Name | Batya's Kitchen (est. 2007), run by Chef Batya Kahan |
| Tagline (logo) | "Homestyle Food With Gourmet Flair" |
| What they sell | Frozen, homemade-style **kosher meat** dishes for Shabbos, Yom Tov and holidays, shipped nationwide |
| Kashrus | Tarnopol Kashrus Hashgacha. Meat facility; all non-meat items made in fleishig keilim. No dairy/pareve dishes offered. Not nut-free. |
| Delivery | FedEx Priority Overnight anywhere in the US (dry ice, insulated boxes); private delivery to Brooklyn, Queens, Five Towns, Manhattan, Staten Island, New Jersey, Monsey; private trucking to Orlando & South Florida |
| Hours | Mon–Thu 9:00am–6:00pm (holidays vary) |
| Phone | 917-525-(FOOD)3663 — call, text or WhatsApp |
| Email | info@batyaskitchen.com (general), orders@batyaskitchen.com (existing orders) |
| Address (checks) | 1278 East 34th Street, Brooklyn, NY |
| Social | Facebook `batyas.kitchen`, Instagram `batyaskitchen`, Twitter `batyakahan` |
| Related sites | Catering: bkevents.com · Charity: yadbatya.org · Cookbook on Amazon (popup) · Pesach: pesach.batyaskitchen.com |

Homepage value props (✓ list):
- Impeccable service
- Highest standards of freshness
- Personalized attention given to every order
- Delicious gourmet homemade food that looks like it came right out of your oven
- Detailed labels on all items
- Hashgocha by Tarnopol Kashrus
- Direct shipping anywhere in the US via FedEx priority overnight
- Private delivery to Brooklyn, Queens, Five Towns, Manhattan, Staten Island, NJ & Monsey
- "Serving the frum community for over 14 years"

---

## 2. Brand / visual style

**Logo:** `assets/img/batya-logo.png` — circular gold seal, large serif "B" centre, ring text "HOMESTYLE FOOD WITH GOURMET FLAIR · BATYASKITCHEN.COM", small Hebrew hashgacha mark.

**Colours (from site CSS, by frequency):**

| Role | Hex | Notes |
|---|---|---|
| Primary (bronze/taupe) | `#847052` | Most used colour — buttons, accents, headings |
| Gold accent | `#c4ac6f` | Logo / category tile text colour (gold on black) |
| Dark plum-brown | `#423338` | Dark sections |
| Charcoal | `#343434` / `#323430` | Header/footer bars |
| Burgundy | `#8a2f40` | Secondary accent |
| Alert red | `#e60000` | "View our testimonials" CTA |
| Light greys | `#f3f3f3`, `#d9d9d9`, `#ccc` | Backgrounds, borders |
| Black | `#000` | Category tile backgrounds |

**Fonts:** Lato (400/700/900, body + UI), Roboto Slab (headings), "Nothing You Could Do" (handwritten script, decorative). Category tiles use a thin, wide-tracked uppercase sans in gold.

**Look & feel:** premium, dark + gold, elegant food photography on white marble/linen (2026 banners). Good direction for the app: black/charcoal + gold + warm bronze, with large food photos.

---

## 3. Site map & navigation

### Header
- Top bar: Facebook / Twitter / Instagram icons · **"MEAT FACILITY"** label · "Call Us: 917-525-(FOOD)3663" · email
- Logo → home
- Main nav:
  - **Shop Menu ▾** — Gluten Free, Tishrei Specials, Partner in Chesed, Prime Meatboards & More, Fish, Salads – Dips, Soups, Soup Condiments, Appetizers, Main Course – Chicken, Main Course – Poultry, Main Course – Meat, Kugels Pies & Crisps, Side Dishes, Dessert, Miscellaneous, Gift Cards, Full Menu
  - **About ▾** — Hashgocha, How It All Began, Testimonials, As Seen in the Mishpacha
  - Gallery · Catering (external bkevents.com) · FAQs · Checkout · Contact

### Footer
"Copyright Batya's Kitchen – Web Design by Braintoaster Interactive | Privacy Policy | Terms & Conditions" + social icons.

### Sidebar (on every inner page)
1. **Your Cart** widget — "Your cart is empty! · 0 items – Total $0 · [View Cart / Checkout]"
2. **Item Search** box (keyword search → `/thumbs.cfm?q=...&SearchType=K`)
3. **Category** list (same as Shop Menu)

### Pages

| Page | URL | Status / content |
|---|---|---|
| Home | `/` | Hero slider, category tiles, promo tiles, about text, kashrus cert |
| Category (×24) | `/category/{slug}` | Product list — see §5 |
| Full Menu | `/thumbsALL.cfm?SearchType=ALL` | All 367 items, grouped by category |
| Gluten Free | `/thumbsGF.cfm?SearchType=ALL` | 158 GF items |
| Product detail | `/product/{slug}` or `/productboard/{slug}` | Breadcrumb, name, size, badges, price, qty + add-to-cart |
| Search results | `/thumbs.cfm?q=…&SearchType=K` | Same list layout |
| Cart | `/viewcart.cfm` | Cart lines, donation box, Edit Cart, Total, Continue Shopping |
| Edit cart | `/editcart.cfm` | Qty edits |
| Hashgocha | `/kashrus.cfm` | Embedded PDF certificate (`KashrutCert25_Tarnopol.pdf`) + cert image |
| How It All Began | `/howitallbegan.cfm` | One tall image containing the brand story (see §6) |
| General Info | `/generalinfo.cfm` | Same story image (`aboutBK.jpg`) |
| Testimonials | `/testimonials.cfm` | ~15 customer letters (see §6) |
| Mishpacha | `/mishpacha.cfm` | Chef Batya article image + PDF + link to mishpacha.com/stir-the-pot |
| Gallery | `/pics.cfm` | 30 food photos (`images/shavuospics/`) |
| FAQs | `/faqs.cfm` | Full FAQ (see §6) |
| Contact | `/contact.cfm` | Phone / text / WhatsApp, email |
| Upstate | `/upstate.cfm` | Upstate menu image (`img/upstatemenu.jpg`) |
| Privacy | `/privacy.cfm` | Privacy policy (eff. Jan 1 2025) |
| Terms | `/terms.cfm` | Terms & conditions (eff. Jan 1 2025) |

---

## 4. Homepage breakdown (top → bottom)

1. **Popup** on load: cookbook (`images/cookbook.jpg`) → Amazon link.
2. **Hero slider** (3 slides, all link to Full Menu):
   - `images/tishreibanner2026a.jpg` — coconut chicken skewers · brisket · sweet potato muffins
   - `images/tishreibanner2026b.jpg` — chocolate chip cookies · dessert table
   - `images/tishreibanner2026c.jpg`
   (1920×640 banners — crop to ~16:9 or 4:3 for mobile)
3. **Category tiles** (black squares with gold text, "SEE MENU" button) in this order:
   Fish · Salads Vegetable · Salads Meat/Fish · Salads Pasta · Soups · Appetizers · Main Course Chicken · Main Course Poultry · Main Course Meat · Side Dishes · Kugels · Dessert · Gluten Free · Meat Boards · Merch ("SEE ITEMS")
   Images: `assets/img/menu_*.jpg`
4. **Promo tiles** (3):
   - `images/shabbos01animate.gif` (animated) → Full Menu
   - `images/3partner.jpg` — "Become a 3 Way Partner! Sponsor a Yom Tov or Shabbos meal for a Flatbush Fund family" → Partner in Chesed
   - `images/some_food.jpg` — 3 foil trays of food (no link)
5. Red CTA: **"CLICK HERE TO VIEW OUR TESTIMONIALS!!!"**
6. About block with ✓ value props + `images/platefood.png` (wine/table setting) + kashrus text.
7. Kashrus cert image `img/kashrutcert23.jpg`.
8. Footer.

---

## 5. Menu / product catalogue

### Product data model (what each item has)
| Field | Example |
|---|---|
| ID | 3771 |
| Name (size is baked into the name) | "Creamy Cauliflower Soup - Quart" |
| Category | SOUPS |
| Price (single) | $15.00 |
| Size label | Quart |
| Heating instructions | "Freezer to oven, uncovered, just till heated through" |
| Dietary badges | Gluten Free · No Sugar · Carb Free · Nut Free (small icon images in `assets/admin/inc/images/`) |
| Photo | **Almost none** — detail pages show a blank `spacer.jpg` |
| Qty input + cart button | — |

There are **no size variants** grouped under one product — each size is a separate item. Product detail has no description beyond name/size/badges/price.

### Categories & item counts (live)
| Category | Items |
|---|---|
| Dessert | 63 |
| Kugels, Pies & Crisps | 58 |
| Tishrei Specials (seasonal) | 56 |
| Side Dishes | 46 |
| Main Course – Chicken | 37 |
| Appetizers | 36 |
| Main Course – Meat | 26 |
| Fish | 24 |
| Chanukah Specials (seasonal, not in nav) | 9 |
| Gift Cards | 8 ($75 – $1,500) |
| Soups | 7 |
| Merch | 5 (BK Sweatshirt S–2XL, $36, has photo) |
| Soup Condiments | 4 |
| Salads – Vegetable | 3 |
| Salads – Dips | 1 |
| Miscellaneous | 1 (Donation) |
| **Empty** ("There were no items found") | Main Course – Poultry, Prime Meatboards, Partner in Chesed, Salads – Meat/Fish, Salads – Pasta, Dairy Dishes, Dessert – Dairy, Rosh Hashanah Specials |

Totals: **367** items in Full Menu, **158** Gluten Free, 173 with at least one dietary badge. Price range $0 (donation) – $1,500 (gift card); food mostly $15–$100.

Common sizes: 9X13 (116), Packed 12 (53), Quart (30), Dozen (24), Packed 5 (18), 9" Round (17), Packed 20, Packed 6, Each, Shallow 9x13, Bundt Cake, Loaf Cake, Pie.

Sample items (full list in `data/menu.csv`):
- Fish: Gefilte Fish Balls in Tomato Sauce (Sweet) – 9X13 $80 · Gefilte Fish Traditional Loaf $35 · Tri-Color 3 App Loaves $50 · Salmon Almondine Packed 5
- Soups: Creamy Broccoli / Cauliflower / Mushroom / Sweet Potato / Zucchini – Quart $15
- Chanukah: Latkes (Potato $48, Sweet Potato, Vegetable, Spinach, Zucchini, Japanese Potato $55, Quinoa $62, Potato w/ Navel Pastrami $65) · Powdered Mini Sufganiyot $40
- Others: Wontons Pulled Beef Brisket Packed 24 · Tiramisu 9X13 · Zucchini Kugel 9X13 · Sweet & Sour Chicken 9x13 · Stuffed Breast of Veal with Mashed Potatoes 9X13

### Cart page
- "Your Cart" list
- **Donation box:** "Please add my donation of $[ ] to go towards a family-in-need. Batya's Kitchen will partner with you and add 18% to your donation! [ADD]"
- Edit Cart · Total · Continue Shopping
- (Checkout steps beyond the cart need a live session — not crawled.)

---

## 6. Content pages (text to reuse)

### How It All Began / About (`images/HowItAllBegan.jpg` — text is inside the image)
Title **"Batya's Kitchen Est 2007"**, sections each with a photo:
1. **How it all began** — "What started out as a small operation in my own home has exploded into a business that has become synonymous with comfort, reliability, and above all else – the taste of home."
2. **The love language of food** — dream to take love of cooking to provide warm, nourishing homemade dinners for those unable to prepare them.
3. Expansion — from simple dinners in 2007 to "the gold standard in home cooked catered food, Pesach and year-round."
4. **A trustworthy experience** — consistency, taste, efficiency, communication.
5. **Kosher Certified** — previously under Rabbi Aaron Mendelson since 2008; now under Tarnopol Kashrus; strictly meat-only kitchen.
6. **White Glove Treatment** — caters parties, simchas, events.
7. **Batya's Kitchen, the perfect gift** — meals for new mothers, shiva, "a pick me up" anywhere in the country.
8. **It's all in the details** — tried-and-true standard of perfection, seasonal offerings.
9. **Nationwide Reach** — FedEx shipping anywhere in the US.
10. **Partner in chesed** — partnership with Flatbush Community Fund; Renewal.
11. **The Gold Standard of Batya's Kitchen**
12. **Batya's Kitchen cares** — "a promise of family, friendship and love."
13. Closing message for Klal Yisroel — signed *Batya Kahan*.

> The story is only available as images. For the app it should be retyped as real text; I can transcribe it fully from the images if needed.

### FAQs (`faqs.cfm`) — sections
- **General Information:** Kosher certified (Tarnopol) · Mostly Yoshon (request all Yoshon) · Bishul Yisroel Bais Yosef on request · Bais Yosef Shechita on request · Meats from Alle Processing; Solomons, SBD, Satmar, CHK on request · Hours Mon–Thu 9–6
- **Production:** meat facility · not dine-in, ship frozen nationwide · not nut-free · everything shipped frozen · no dairy or pareve dishes
- **Pesach Production:** yes, separate Pesach menu
- **Shipping:** FedEx Priority Overnight (dry ice) · Private trucking for Orlando & South Florida
  - Small box: 3 × 9x13 pans — **$102**
  - Large box: 8 × 9x13 pans OR 12 quarts OR 10 rounds + 4 quarts — **$162**
  - FedEx $30 surcharge for boxes > 50 lbs
  - Airplane/suitcase packing: **$60 per box**
- **Additional services:** packing list & heating instructions emailed with every order (invoice by email only) · meal labeling **$250 per order**
- **Payment:** Credit card (+3.5% fee) · Check to 1278 East 34th St, Brooklyn · QuickPay/Zelle Batyaskitchen@gmail.com · Venmo @batya-kahan
- **Contact:** WhatsApp/Text/Call 917-525-3663 · info@ · orders@ (put order # in subject)

### Testimonials (`testimonials.cfm`) — "Nationwide Testimonials"
~15 letters. Short pull quotes for app cards:
- "It was like having a hotel Shabbos without having to leave their house… tasting homemade and delicious." 
- "Everything was out of this world delicious! It really tasted homemade!" — Aydel F.
- "The kids kept complimenting me and I kept having to tell them that I didn't make anything!" — Tehilla D.
- "Everything travelled perfectly and arrived safely and completely frozen… amazing, wonderful kosher meals in the middle of Maine!" — Susan L.
- "Your delivery to our recent vacation location in Edwards, Colorado was perfect and the food delicious." — Vivian F.
- "Thank you so much for your delicious food, packed beautifully and great instructions." — Chanie Z.
- Congregation Anshei Sfard of Louisville, KY — Purim seudah — Rivka L.
- Bonnie & Danny (Jamaica), Mrs. Susan Krochmal, Ilana G., Sonny G. (Lawrence), Ira G.

### Hashgocha
Tarnopol Kashrus certificate — `img/kashrutcerttop23.jpg`, `img/kashrutcert23.jpg`, PDF `KashrutCert25_Tarnopol.pdf`.

### As Seen in the Mishpacha
"Chef Batya – Mishpacha Magazine" — `images/chefbatya.jpg`, PDF `ChefBatya.pdf`, link mishpacha.com/stir-the-pot.

### Contact
"Call, Text or WhatsApp to: 917-525-(FOOD)3663 · info@batyaskitchen.com"

### Privacy / Terms
Standard policies, effective Jan 01 2025 (info collected, use, no selling data; orders subject to availability, payment in full before processing, cancellations/refunds limited due to food prep).

---

## 7. Image inventory (`assets/`)

| Use | Files |
|---|---|
| Logo | `img/batya-logo.png` (200×200, gold seal) |
| Hero banners (2026, high quality) | `images/tishreibanner2026a/b/c.jpg` (1920×640) |
| Category tiles (black + gold text, no photos) | `img/menu_*.jpg` — fish, salads_veg, salads_meatfish, salads_pasta, soup, app, mainchicken, mainpoultry, mainmeat, sides, kugels, dessert, glutenfree, boards, merch |
| Food photos | `images/some_food.jpg`, `images/shavuospics/pic01–pic40.jpg` (30 photos, many with "batyaskitchen.com" text overlay), `images-product/small/quinoa_salad.jpg` |
| Lifestyle | `images/platefood.png` (wine/table), `images/chefbatya.jpg` |
| Promo | `images/3partner.jpg` (Flatbush Fund partner), `images/cookbook.jpg`, `images/shabbos01animate.gif` |
| Story | `images/HowItAllBegan.jpg`, `images/aboutBK.jpg` (tall text-in-image) |
| Kashrus | `img/kashrutcert23.jpg`, `img/kashrutcerttop23.jpg` |
| Merch | `images-product/small/sweatshirt.jpg` |
| Dietary badges | `admin/inc/images/gluten-free1.jpg`, `No-sugar.jpg`, `carb-free1.jpg`, `nut-free1.jpg` |
| Other | `img/upstatemenu.jpg` (upstate menu flyer) |

---

## 8. Issues & gaps to plan around

1. **No product photos** — 367 items, essentially zero real photos. App product cards need either category-level hero photos (from banners/gallery), illustrated placeholders, or the client must supply photos. **Main design decision.**
2. **Category tiles are text-on-black** — they look elegant but carry no food imagery. In the app, swap them for photos where possible.
3. **8 empty categories** in nav/homepage (Poultry, Meatboards, Partner in Chesed, Salads Meat/Fish, Salads Pasta, etc.). The homepage links to 4 of them.
4. **Size is baked into product names** ("…- 9X13", "…- Quart"). The app could group these into one dish with size options; the backend would have to support it.
5. **No product descriptions**, only name, size, heating note, badges.
6. **Story/About content is image-only** — needs retyping for the app.
7. **Gallery includes dairy dishes** (e.g. cheese-stuffed shells, old Shavuos photos), which contradicts the "meat facility, no dairy" message. Pick gallery images carefully.
8. **Broken/dead links:** `onlinemenu.cfm` (404), `/upstate/` (404), `/camp/` (404), `/tishrei/` redirects to home; `thumbsShav` and `thumbsT` are empty.
9. Old ColdFusion site (Bootstrap 3, jQuery 1.11); the app will need an API from whoever runs the backend.

---

## 9. Proposed mobile app screens (for Sleek)

**Onboarding / Auth**
1. Splash — gold seal logo on black
2. Welcome / onboarding (3 slides: Homestyle gourmet · Shipped frozen nationwide · Tarnopol kosher)
3. Login / Sign up / Guest

**Shop**
4. Home — header (logo, search, cart), hero carousel (Tishrei banners), seasonal special strip, category grid, Gluten Free shortcut, Partner in Chesed promo, testimonial card, "Meat Facility · Tarnopol" trust badge
5. Categories (all categories list/grid)
6. Category product list — items with name, size chip, price, dietary badges, quick add (+/–)
7. Filters sheet — Gluten Free / No Sugar / Carb Free / Nut Free, size, price
8. Search (recent searches + results)
9. Product detail — photo, name, size, price, badges, heating instructions, qty stepper, Add to Cart, related items
10. Gift Cards ($75–$1,500 card picker)
11. Seasonal specials (Tishrei / Chanukah / Pesach landing)

**Cart & checkout**
12. Cart — line items, qty edit, donation module ("we add 18%"), subtotal
13. Delivery method — FedEx overnight (box size & fee) / Private delivery (area picker) / Florida trucking; optional suitcase packing $60, labeling $250
14. Address & delivery date
15. Payment — card (+3.5%), Zelle, Venmo, check
16. Order review & confirmation (packing list & heating instructions emailed)

**Account**
17. Orders history & order detail / reorder
18. Profile, addresses, saved payment

**Info**
19. About / Our Story (est. 2007)
20. Kashrus / Hashgocha (certificate viewer)
21. Testimonials
22. Gallery
23. FAQs (accordion by section)
24. Contact (Call · Text · WhatsApp · Email buttons)
25. Partner in Chesed / Donate
26. Catering (link to BK Events)
27. Privacy / Terms

Bottom tab bar: **Home · Menu · Search · Cart · Account**
