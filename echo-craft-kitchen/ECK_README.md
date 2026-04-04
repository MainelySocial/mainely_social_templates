# Echo Craft Kitchen – Weekly Specials Workflow

## Activation Triggers
- **`ECK SPECIALS`** -- dark version (black background)
- **`ECK SPECIALS LIGHT`** -- light version (white background)

When triggered, Claude will:
1. Read this README from Drive
2. Fetch the appropriate Story template Google Doc
3. Ask you to upload the weekly specials PDF
4. Output all three files: Story HTML, Email Body HTML (light), Email Body HTML (dark)

---

## Client Info
- **Restaurant:** Echo Craft Kitchen
- **Website:** echocraftkitchen.com
- **Address:** 150 Echo Lake Rd., Watertown, CT 06795

---

## Logos
- **Dark version (white logo, black background):**
  `https://echocraftkitchen.com/wp-content/uploads/2022/05/Echo-Craft-Kitchen-bmindfulweb-Rectangle-Logo-Final-White.webp`
- **Light version (black logo, white background):**
  `https://echocraftkitchen.com/wp-content/uploads/2026/04/Echo-Logo-black-tranparent.webp`
- **Note:** Reference directly via `<img src="URL">` -- no base64 needed. Logo does NOT appear in email body.

---

## Colors
- **Dark background:** #000000
- **Light background:** #ffffff
- **Gold (dark version):** #b89a6a
- **Gold (light version):** #C9A84C
- **Text (dark):** #f5f0e8
- **Text (light):** #1a1a18

---

## Drive Folder IDs
- **Incoming Menus:** `1TZhSjZmZIUsqn-CDhaRqmW0L0AKPK8EZ`
- **Output Folder:** `14jlQ0NsQpGa6NZHZ52oECbYaE6ox2whu` > Echo Craft Kitchen subfolder
- **README Doc ID:** `1UUNrteeD6NiRwDUz84otJXFzrRD_fPNcGZA7IW5HdZs`

---

## Template Google Docs
- **Story 9x16 Dark:** `1x4flSIoXqR0WlOk27ADhnwQi6hrcIPV99LkkuaFSSUQ`
- **Story 9x16 Light:** *(not yet created -- use dark template and swap colors)*
- **Facebook 4x5:** *(pinned for later)*

---

## PDF Limitation
Claude cannot read PDFs directly from Drive. PDF must be uploaded in the chat each session.

---

## Output Files Per Session
Every specials session produces three files:
1. **Story 9x16 HTML** -- dark or light depending on trigger
2. **Email Body HTML Light** -- white background, #C9A84C gold, no logo
3. **Email Body HTML Dark** -- black background, #b89a6a gold, no logo

---

## Email Body Rules
- No logo -- starts with divider, then title
- Title: "This Week's Specials"
- Subtitle: "Specials Run Friday – Thursday" in small gold uppercase
- White background with dark text (light version)
- Black background with light text (dark version)
- Table-based HTML for email client compatibility

---

## CloudConvert Settings (free account, no saved presets)
- **Story 9x16:** Width 1080, Height 1920, Scale 1, Wait Until networkidle0, Wait Time 3000
- **Facebook 4x5:** Width 1080, Height 1350, Scale 1, Wait Until networkidle0, Wait Time 3000

---

## Menu Sections (in order)
1. Wing of the Week
2. Starters (Soup of the Day + any featured starters)
3. Entrees (2-column tile grid, full-width for odd items)
4. Featured Cocktails (3-column inline)

---

## Design Rules
- **Title:** "This Week's Specials"
- **Fonts:** Barlow Condensed (headings/labels), Barlow (body/descriptions), Playfair Display (prices + title)
- **Wing bar:** Stacked column -- "WING OF THE WEEK" small label centered on top, flavor name large and bold centered below. No right-side text.
- **"Ask Your Server"** belongs to Soup of the Day only -- never in the wing bar
- **Entree tiles:** Name + italic description + price (large Playfair Display) at bottom
- **Border dark:** rgba(255,255,255,0.16)
- **Border light:** rgba(0,0,0,0.16)
