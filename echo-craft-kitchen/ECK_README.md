Echo Craft Kitchen – Weekly Specials Workflow
Activation Trigger
Type ECK SPECIALS to begin. Claude will:

Load the ECK templates from project files
Ask you to upload the weekly specials PDF
Output three files: Dark Story HTML, Light Story HTML, Email HTML (light)


Client Info

Restaurant: Echo Craft Kitchen
Website: echocraftkitchen.com
Address: 150 Echo Lake Rd., Watertown, CT 06795


Logos

White logo (dark story): https://echocraftkitchen.com/wp-content/uploads/2022/05/Echo-Craft-Kitchen-bmindfulweb-Rectangle-Logo-Final-White.webp
Black logo (light story): https://echocraftkitchen.com/wp-content/uploads/2026/04/Echo-Logo-black-tranparent.webp
Note: Reference directly via <img src="URL"> -- no base64 needed. Logo does NOT appear in email body.


Colors

Dark background: #000000
Light background: #ffffff
Gold (dark version): #b89a6a
Gold (light version): #C9A84C
Text (dark): #f5f0e8
Text (light): #1a1a18


Drive Folder IDs

Incoming Menus: 1TZhSjZmZIUsqn-CDhaRqmW0L0AKPK8EZ
Output Folder: 14jlQ0NsQpGa6NZHZ52oECbYaE6ox2whu > Echo Craft Kitchen subfolder


PDF Limitation
Claude cannot read PDFs directly from Drive. The PDF must be uploaded in the chat each session.

Output Files Per Session
Every specials session produces three files:

Dark Story HTML -- black background
Light Story HTML -- white background
Email HTML -- light version only (white background, #C9A84C gold, no logo)


CloudConvert Settings (free account, no saved presets)

Story 9x16: Width 1080, Height 1920, Scale 1, Wait Until networkidle0, Wait Time 3000
Facebook 4x5: Width 1080, Height 1350, Scale 1, Wait Until networkidle0, Wait Time 3000


Menu Sections (in order)

Wing of the Week
Starters (Soup of the Day + any featured starters)
Entrees (2-column tile grid, full-width for odd items)
Featured Cocktails (3-column inline)


Design Rules

Title: "This Week's Specials"
Fonts: Barlow Condensed (headings/labels), Barlow (body/descriptions), Playfair Display (prices + title)
Wing bar: Stacked -- "WING OF THE WEEK" small label centered top, flavor name large and bold centered below. No right-side text.
"Ask Your Server" belongs to Soup of the Day only -- never in the wing bar
Entree tiles: Name + italic description + price (large Playfair Display) at bottom
Border dark: rgba(255,255,255,0.16)
Border light: rgba(0,0,0,0.16)


Key changes made:

Removed ECK SPECIALS LIGHT as a separate trigger -- one trigger, three outputs
Removed all Google Doc template IDs -- templates come from project files now
Removed README Doc ID -- no longer needed
Removed dark email output -- light email only
Removed "Read this README from Drive" step -- no longer how it works
Kept Drive folder IDs since those are still useful for file management reference
