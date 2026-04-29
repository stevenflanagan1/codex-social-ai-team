# Review Of Original Social AI Team For Codex

## What The Original Repo Does Well

- Clear team structure: one manager plus specialist skills.
- Good workflow order: brand setup -> calendar -> content -> creative -> publishing -> review.
- Strong handoff files: `brand-style.md`, `content-calendar.md`, `workflow-status.md`, and `best-performers.md`.
- Approval gates are explicit, which matters for client work.
- Platform-native writers are separate from the generic caption writer.
- Creative workflow protects real product packaging by preferring composite/edit mode over pure generation.
- Performance review loops learnings back into next month.

## What Needed To Change For Codex

- Claude slash commands do not directly map to Codex. Codex needs skill folders in `~/.codex/skills`.
- Source paths like `~/.claude/skills/...` needed to become Codex skill references.
- Nano Banana-specific instructions needed to become OpenAI `gpt-image-2` image instructions.
- The manager needed to route to Codex skill names, not slash commands.
- The team needed stronger install guidance for Codex users.
- Optional MCP/tool assumptions needed softer fallback behavior.

## What Needed Improvement Beyond The Original

- Add `context/compliance-rules.md` for regulated claims, disclaimers, approval rules, and banned phrases.
- Add `context/asset-library.md` for approved photos, logos, brand assets, usage rights, and source-of-truth product images.
- Add a publishing QA checklist before scheduling.
- Add platform export specs and alt text requirements.
- Keep `gpt-image-2` as the image default, with manual layout only for exact legal/product/URL text.
- Make workflow recovery reliable by updating `context/workflow-status.md` after every phase.

## Current Codex Pack Status

Created:

- `social-media-manager-codex`
- `brand-onboarding-codex`
- `content-calendar-codex`
- `caption-writer-codex`
- `social-creative-designer-openai`
- `linkedin-writer-codex`
- `threads-writer-codex`
- `x-writer-codex`
- `publisher-codex`
- `social-performance-review-codex`

The first Codex pass was structurally complete but too light in places. This review document records the broader review so future edits are based on the whole team, not only the creative designer.

