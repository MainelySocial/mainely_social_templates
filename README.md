Mainely Social – Client Template Repository
This repository stores production HTML templates for weekly specials social graphics and email campaigns. Templates are maintained by Mainely Social Inc. and consumed by Claude AI sessions and Cowork automation workflows.

Repository Structure
mainely-social-templates/
  ideal-tavern/
    IT_dark_story.html      # Instagram Story 9x16, dark background
    IT_light_story.html     # Instagram Story 9x16, light background
    IT_email.html           # Weekly specials email body
    IT_README.md            # Workflow instructions reference
  echo-craft-kitchen/
    ECK_dark_story.html     # Instagram Story 9x16, dark background
    ECK_light_story.html    # Instagram Story 9x16, light background
    ECK_email.html          # Weekly specials email body
    ECK_README.md           # Workflow instructions reference

How Templates Are Used
Claude AI Sessions
Templates are synced into the Claude project. At the start of each session Claude loads the templates from project files, accepts the weekly specials PDF upload, populates all sections with current menu content, and outputs production-ready HTML.
When a template is updated in this repo, re-sync the project files in Claude to pick up the changes.
Cowork Automation
The Cowork workflow monitors each client's Google Drive incoming folder for a new PDF. When triggered it:

Fetches templates from this repo via GitHub API
Sends the PDF and templates to Claude for population
Writes finished HTML outputs back to the client's Drive output folder


Claude Activation Keywords

IT SPECIALS -- triggers Ideal Tavern weekly specials workflow
ECK SPECIALS -- triggers Echo Craft Kitchen weekly specials workflow

Both keywords always produce three output files: Dark Story HTML, Light Story HTML, and Email HTML (light).

CloudConvert Settings (free account, no saved presets)
FormatWidthHeightScaleWait UntilWait TimeStory 9x16108019201networkidle03000Facebook 4x5108013501networkidle03000Square 1x1108010801networkidle03000

Template Update Protocol
When a template is revised:

Update the HTML file in this repo
Update the corresponding client README with any design rule changes
Commit with a clear message, e.g. IT: update wing bar layout to stacked
Re-sync the project files in Claude so the updated version is picked up


Access

Repo: Private
Owner: Mainely Social Inc.
GitHub username: MainelySocial
Primary user: Christian Yanarella
Cowork auth: GitHub Personal Access Token (stored in Cowork workflow settings)
Claude access: Project file sync


Clients
Ideal Tavern

142 Center St., Southington, CT 06489
idealtavern.com
Subcontractor: Jasmine (social content)
Incoming menus folder: 1aXSL8sEXe0KfkU1gdA0NvRHnvoWJG-WC

Echo Craft Kitchen

150 Echo Lake Rd., Watertown, CT 06795
echocraftkitchen.com
Subcontractor: Jasmine (social content)
Incoming menus folder: 1TZhSjZmZIUsqn-CDhaRqmW0L0AKPK8EZ


Maintained by Mainely Social Inc. | mainelysocial.com | Saco, ME

Key changes made:

Updated "How Templates Are Used / Claude AI Sessions" -- replaced GitHub fetch description with project sync workflow
Updated "Template Update Protocol" step 4 -- now says re-sync project files instead of automatic fetch
Updated "Claude access" in Access section -- changed from raw URL fetch to project file sync
Removed ECK SPECIALS LIGHT from activation keywords -- one trigger per client now
Updated both keyword descriptions to note three output files each
