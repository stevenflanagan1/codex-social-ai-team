# Codex Social AI Team

A Codex-native social media workflow pack for planning, creating, publishing, and reviewing social content.

This pack includes specialist Codex skills for:

- Brand onboarding
- Content calendars
- Captions
- OpenAI/Codex image creative
- Carousels
- Motion creative loops
- LinkedIn
- Threads
- X/Twitter
- Publishing handoff
- Performance review

## Install

From this repository folder, run:

```powershell
.\install.ps1
```

Or copy manually:

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills"
Copy-Item ".\skills\*" "$env:USERPROFILE\.codex\skills" -Recurse -Force
```

Restart Codex after installing.

## Quick Test

In Codex, ask:

```text
Use social-media-manager-codex to set up a test client social media workflow.
```

For specific workflows:

```text
Use carousel-producer-codex to create a 5-slide Instagram carousel.
Use motion-creative-producer-codex to create a looping motion ad.
Use social-creative-designer-openai to create an Instagram visual.
```

## Recommended Client Folder

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

## Image Generation

Inside Codex, use the built-in image generation path where available.

The `social-creative-designer-openai` skill is written for modern OpenAI image workflows and defaults to `gpt-image-2` language in briefs. If you later build a direct API/MCP automation path, use your own OpenAI API key and keep it outside this repository.

Do not commit API keys, `.env` files, generated client assets, or private client folders.

## Motion Creative

The motion workflow supports:

- Coherent frame-by-frame action loops
- Subtle single-image loops
- Stop-motion style posts
- Kinetic type concepts
- GIF preview assembly

MP4 export may require adding `ffmpeg` or a video-capable Python runtime.

## Privacy

Before publishing, run:

```powershell
.\scripts\privacy-check.ps1
```

The repository should contain reusable skills and fake examples only.

