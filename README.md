# Codex Social AI Team

A shareable Codex skill pack for running a social media workflow inside Codex.

It turns Codex into a small social media team that can onboard a brand, plan a content calendar, write posts, create image concepts, build carousels, create looping motion creative, prepare publishing handoffs, and review performance.

This repo contains reusable skills and blank templates only. It does not contain API keys, private client files, generated media, test outputs, or real client data.

## What This Does

The pack gives Codex these roles:

| Skill | Purpose |
|---|---|
| `social-media-manager-codex` | Orchestrates the full workflow and routes work to the right specialist. |
| `brand-onboarding-codex` | Creates the brand foundation: voice, visuals, pillars, compliance notes. |
| `content-calendar-codex` | Builds monthly or weekly content calendars. |
| `caption-writer-codex` | Writes Instagram/Facebook/TikTok-style captions. |
| `social-creative-designer-openai` | Creates creative briefs and image-generation prompts for social visuals. |
| `carousel-producer-codex` | Builds story-led social carousels with relevant visuals and exact slide copy. |
| `motion-creative-producer-codex` | Builds short looping motion creatives from frame sequences or subtle loops. |
| `linkedin-writer-codex` | Writes LinkedIn-native posts and thought leadership. |
| `threads-writer-codex` | Writes Threads-native posts and short conversational threads. |
| `x-writer-codex` | Writes X/Twitter posts and threads. |
| `publisher-codex` | Prepares approved posts for scheduling or manual publishing. |
| `social-performance-review-codex` | Reviews social analytics and feeds learnings into the next calendar. |

## What It Can Run

Inside Codex, this workflow can help you run:

1. Brand onboarding
2. Content strategy and calendars
3. Caption writing
4. Platform-specific writing
5. Image creative
6. Carousel production
7. Motion creative planning and GIF/loop assembly
8. Publishing handoff
9. Performance review
10. Next-month recommendations

The intended loop is:

```text
Brand guide -> calendar -> captions -> creative -> QA -> publishing handoff -> performance review -> next calendar
```

## Install

Clone this repo:

```powershell
git clone https://github.com/stevenflanagan1/codex-social-ai-team.git
cd codex-social-ai-team
```

Run the installer:

```powershell
.\install.ps1
```

If Windows blocks scripts, run:

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File .\install.ps1
```

Then restart Codex.

Manual install:

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills"
Copy-Item ".\skills\*" "$env:USERPROFILE\.codex\skills" -Recurse -Force
```

Then restart Codex.

## First Test

After restarting Codex, open a folder for a test client and ask:

```text
Use social-media-manager-codex to set up a test client social media workflow.
```

Then try:

```text
Use content-calendar-codex to plan a one-week social calendar.
```

```text
Use carousel-producer-codex to create a 5-slide Instagram carousel.
```

```text
Use motion-creative-producer-codex to create a looping motion ad.
```

## Recommended Client Folder

For each client, create a folder like this:

```text
client-name/
  context/
    brand-style.md
    content-calendar.md
    workflow-status.md
    compliance-rules.md
    asset-library.md
    best-performers.md
  assets/
    products/
    lifestyle/
    logos/
  outputs/
    captions/
    creatives/
    carousels/
    motion/
    linkedin/
    threads/
    x/
    publishing/
    reviews/
```

The skills will use the `context/` files as the source of truth and write production work into `outputs/`.

Blank starter files are included in:

```text
templates/client-context/
```

## Optional Tools To Add

You can use the skills with plain Codex only, but a full production setup benefits from extra tools.

### Image Generation

Use Codex's built-in image generation where available.

The creative skill is written around modern OpenAI image workflows and refers to `gpt-image-2` for production-style briefs. You usually do not need to add your own OpenAI API key just to test inside Codex.

Add an OpenAI API key only if you build a direct API/MCP automation path outside the normal Codex image tool.

Never commit API keys or `.env` files.

### Publishing

For direct scheduling, connect a publisher such as:

- Blotato
- Buffer
- Later
- Metricool
- Hootsuite

Without a scheduling integration, the `publisher-codex` skill still prepares a manual publishing handoff with captions, creative filenames, platform notes, alt text, dates, and QA checks.

### Website And Competitor Research

Useful optional tools:

- Firecrawl for clean website scraping and research
- Playwright for browser inspection, screenshots, and website QA
- Search/browser tools for public social and competitor review

These are optional. The workflow still works if you paste website copy, screenshots, brand notes, or analytics exports into the client folder.

### Analytics

The performance review skill can work from:

- CSV exports
- screenshots
- copied platform summaries
- manually entered metrics

For more automation, connect platform analytics or scheduling-tool exports later.

## How Carousels Work

The carousel producer should create a story-led carousel, not a set of random quote cards.

Typical flow:

```text
Choose story arc -> write slide plan -> generate relevant visuals -> add exact text -> QA -> export ordered slides
```

Example arcs:

- Hook -> tension -> insight -> steps -> CTA
- Problem -> mistakes -> better way -> example -> CTA
- Myth -> truth -> proof -> application -> CTA
- Case study -> context -> action -> result -> takeaway

## How Motion Creative Works

The motion producer supports two useful patterns:

1. Frame-by-frame action loop  
   Same scene, tiny changes each frame, played quickly. Best for food, product, pours, steam, bubbles, hands, rotations, and other social ad motion.

2. Subtle single-image loop  
   One strong visual with small pan/zoom/light movement. Best when you want a gentle animated post.

For production motion ads, prefer frame-by-frame action loops. They should feel like a short video, not a slideshow of unrelated creatives.

## Privacy And Sharing

This repo should contain:

- reusable skills
- blank templates
- install scripts
- documentation

It should not contain:

- API keys
- `.env` files
- private client folders
- generated client media
- local user paths
- real client analytics

Run this before sharing:

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File .\scripts\privacy-check.ps1
```

The included `templates/client-context` files are blank starter files only.

## Notes

This is a skill pack, not a hosted app. Other users install it by copying the folders in `skills/` into their own Codex skills directory. After installation, Codex will trigger the skills by name or by matching the task.
