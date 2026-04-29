---
name: publisher-codex
description: Prepares approved social content for publishing from Codex. Use when scheduling, exporting, packaging, QA-checking, or handing off approved posts and creatives to Blotato, Buffer, Later, Metricool, Canva, or a manual publishing workflow.
---

# Publisher For Codex

Package approved content for scheduling. Do not publish without explicit user approval.

## Inputs

Read approved files from:

- `outputs/captions/`
- `outputs/creatives/`
- `outputs/linkedin/`
- `outputs/threads/`
- `outputs/x/`
- `context/content-calendar.md`
- `context/compliance-rules.md`

## QA Checklist

Check:

- Caption approved
- Creative approved
- Platform and date correct
- Link works
- Tags and handles correct
- Hashtags appropriate
- Alt text included where useful
- Required disclaimer included
- No unapproved claims
- Filename and export ratio correct
- Alt text drafted for image posts
- Account/handle mentioned in the caption is correct
- Scheduled date respects time zone and campaign timing
- Creative file visually matches the caption and platform
- Post status is approved, not draft

## Output

Save `outputs/publishing/publishing-plan.md`:

```text
# Publishing Plan

| Date | Time | Platform | Post | Caption file | Creative file | Status | Notes |
|---|---|---|---|---|---|---|---|
```

If a scheduling integration is available, prepare the payload but ask for confirmation before submission.

If no scheduling integration is available, produce a manual handoff with filenames, captions, alt text, dates, and platform notes. Publishing is still useful without Blotato.
