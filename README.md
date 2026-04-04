# Mainely Social – Client Template Repository

This repository stores production HTML templates for weekly specials social graphics and email campaigns. Templates are maintained by Mainely Social Inc. and consumed by Claude AI sessions and Cowork automation workflows.

---

## Repository Structure

```
mainely-social-templates/
  ideal-tavern/
    IT_dark_story.html      # Instagram Story 9x16, dark background
    IT_light_story.html     # Instagram Story 9x16, light background
    IT_email.html           # Weekly specials email body
    IT_README.md            # Workflow instructions for Claude
  echo-craft-kitchen/
    ECK_dark_story.html     # Instagram Story 9x16, dark background
    ECK_light_story.html    # Instagram Story 9x16, light background
    ECK_email.html          # Weekly specials email body
    ECK_README.md           # Workflow instructions for Claude
```

---

## How Templates Are Used

### Claude AI Sessions
At the start of a specials session, Claude fetches the raw template files directly from this repo using the raw GitHub URL format:

```
https://raw.githubusercontent.com/[username]/mainely-social-templates/main/[client-folder]/[filename]
```

Claude reads the template, accepts the weekly specials PDF upload, populates all sections with current menu content, and outputs production-ready HTML.

### Cowork Automation
The Cowork workflow monitors each client's Google Drive incoming folder for a new PDF. When triggered it:
1. Fetches templates from this repo via GitHub API
2. Sends the PDF and templates to Claude for population
3. Writes finished HTML outputs back to the client's Drive output folder

---

## Claude Activation Keywords
- `IT SPECIALS` — triggers Ideal Tavern weekly specials workflow
- `ECK SPECIALS` — triggers Echo Craft Kitchen weekly specials workflow

---

## CloudConvert Settings (free account, no saved presets)
| Format | Width | Height | Scale | Wait Until | Wait Time |
|--------|-------|--------|-------|------------|-----------|
| Story 9x16 | 1080 | 1920 | 1 | networkidle0 | 3000 |
| Facebook 4x5 | 1080 | 1350 | 1 | networkidle0 | 3000 |
| Square 1x1 | 1080 | 1080 | 1 | networkidle0 | 3000 |

---

## Template Update Protocol
When a template is revised:
1. Update the HTML file in this repo
2. Update the corresponding client README with any design rule changes
3. Commit with a clear message, e.g. `IT: update wing bar layout to stacked`
4. The next Claude session or Cowork run will automatically use the updated version

---

## Access
- **Repo:** Private
- **Owner:** Mainely Social Inc.
- **Primary user:** Christian Yanarella
- **Cowork auth:** GitHub Personal Access Token (stored in Cowork workflow settings)
- **Claude access:** Raw URLs (no auth required for read on private repo via token)

---

## Clients

### Ideal Tavern
- 142 Center St., Southington, CT 06489
- idealtavern.com
- Subcontractor: Jasmine (social content)
- Incoming menus folder: `1aXSL8sEXe0KfkU1gdA0NvRHnvoWJG-WC`

### Echo Craft Kitchen
- 150 Echo Lake Rd., Watertown, CT 06795
- echocraftkitchen.com
- Subcontractor: Jasmine (social content)
- Incoming menus folder: `1TZhSjZmZIUsqn-CDhaRqmW0L0AKPK8EZ`

---

*Maintained by Mainely Social Inc. | mainelysocial.com | Saco, ME*
