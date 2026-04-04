# Ideal Tavern – Weekly Specials Workflow

## Activation Trigger
Type **`IT SPECIALS`** to begin. Claude will:
1. Read this README
2. Fetch the Story and Facebook template Google Docs
3. Ask you to upload the weekly specials PDF
4. Populate all templates with this week's menu content
5. Output Dark Story HTML, Light Story HTML, and Email HTML

---

## Client Info
- **Restaurant:** Ideal Tavern
- **Website:** idealtavern.com
- **Address:** 142 Center St., Southington, CT 06489

---

## Logos
- **White logo (dark story):** `https://idealtavern.com/wp-content/uploads/2023/03/cropped-IT-Logo-White-S.png`
- **Black logo (light story):** `https://idealtavern.com/wp-content/uploads/2026/04/Ideal-Tavern-Transparent-Black-Logo.png`
- **How to use:** Reference directly via `<img>` -- no base64 needed

---

## Drive Folder IDs
- **Incoming Menus:** `1aXSL8sEXe0KfkU1gdA0NvRHnvoWJG-WC`
- **Output Folder:** `14jlQ0NsQpGa6NZHZ52oECbYaE6ox2whu` > Ideal Tavern subfolder

---

## Template Google Docs
- **Dark Story 9x16:** `16LfzY2ePUbmdmJYdrjuIhoQ6Q89iLSie3Caqvm08jvo`
- **Light Story 9x16:** `1O29xpCLRsWqWB9lJ5OPH7h7vIiBc3T6vXI4k9G0PM4Q`
- **Email body:** `14fx2S4rp-kAiTzuWlBcFog155JDaw83tR3GgtEs19qQ`
- **Facebook 4x5:** `IT_Facebook_Template_4x5` -- paste approved Facebook HTML here

---

## PDF Limitation
Claude cannot read PDFs directly from Drive. The PDF must be uploaded in the chat or shared as a direct file link. Do not attempt to fetch it from the folder.

---

## CloudConvert Settings (free account, no saved presets)
- **Story 9x16:** Width 1080, Height 1920, Scale 1, Wait Until networkidle0, Wait Time 3000
- **Facebook 4x5:** Width 1080, Height 1350, Scale 1, Wait Until networkidle0, Wait Time 3000
- **Square 1x1:** Width 1080, Height 1080, Scale 1, Wait Until networkidle0, Wait Time 3000

---

## Menu Sections (in order)
1. Wing of the Week
2. Starters (if any)
3. Entrees (2-column tile grid)
4. Dessert (if any)
5. Featured Cocktails (3-column inline)

---

## Design Rules

### Dark Story
- **Background:** #1a1a18
- **Gold accent:** #b89a6a
- **Logo:** White logo URL above
- **Title:** "This Week's Specials" (Playfair Display, 88px)
- **Wing bar:** Stacked -- "Wing of the Week" badge centered top, flavor name large centered below
- **Fonts:** Barlow Condensed (headings/labels), Barlow (body/descriptions), Playfair Display (prices + title)
- **Border:** rgba(255,255,255,0.16)

### Light Story
- **Background:** #f5f1eb
- **Page background:** #e8e4de
- **Gold accent:** #C9A84C
- **Logo:** Black logo URL above
- **Title:** "This Week's Specials" (Playfair Display, 88px, color #1a1a18)
- **Wing bar:** Stacked -- "Wing of the Week" badge centered top, flavor name large centered below
- **Tile background:** rgba(255,255,255,0.6) with soft shadow
- **Border:** rgba(0,0,0,0.12)

### Email
- **Background:** #ffffff inner, #f0ede8 outer
- **Gold accent:** #C9A84C
- **Font stack:** Helvetica Neue, Helvetica, Arial, sans-serif
- **Price font:** Georgia, serif
- **Subheading:** "Specials Run Friday – Thursday"
- **Entrees:** 2-column tile grid (48% / 4% gap / 48%)
- **Cocktails:** Stacked list with name, price right-aligned, italic description below
- **Footer:** Idealtavern.com | 142 Center St. Southington, CT 06489

### Shared Rules (all templates)
- **"Ask Your Server"** belongs to Soup of the Day only -- never in the wing bar
- **Entree tiles:** Name + italic description + price (large) at bottom
- **Tile notes** (e.g. add-ons): gold color, uppercase, smaller font, above price
