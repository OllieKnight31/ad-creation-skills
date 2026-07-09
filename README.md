# Ad Creation Skills

Claude Code skills for producing full paid-ad batches (Meta/Facebook/Instagram): cold DR video scripts, warm-up content, retargeting sequences, and static image ads.

## What's in here

### `ads-master-skill/` — the orchestrator
The single entry point. Given a client, it produces an Andromeda-compliant batch across all four ad surfaces in one run. Install it as a skill folder (`~/.claude/skills/ads-master-skill/`).

- `SKILL.md` — the skill definition and workflow
- `phases/` — the 4-phase run: voice gate → discovery → plan → produce
- `reference/` — the knowledge base it draws on:
  - `dr-framework-10-parts.md` — the 10-part direct-response SOP
  - `dog-food-exercise.md` — diversification engine (15–20 unique messaging angles)
  - `100-hook-framework.md` + `103-hook-templates.md` — hooks by cognitive bias, fill-in-the-blank templates
  - `14-ad-templates.md` — structural ad backbones
  - `70-headline-swipe.md` — Ogilvy-style headlines for statics
  - `8-sub-frameworks.md` — cold-DR delivery styles
  - `harvester-strategy.md` — stage-segmented retargeting (Jeremy Haynes / Megalodon)
  - `venus-fly-trap.md` — warm-up content strategy
  - `if-this-then-that.md` — campaign troubleshooting playbook
  - `anti-ai-tells.md` — voice rules that keep copy sounding human
- `templates/` — output formats per surface (cold DR script, retargeting ad, static ad, warm-up video, briefing)
- `scripts/detect-client-inputs.sh` — detects which client inputs (voice doc, ICP, offer, proof bank) exist before a run

### `sub-skills/` — standalone skills the orchestrator delegates to
Install these as slash commands (`~/.claude/commands/*.md`). Each also works on its own:

- `direct-response-ads-skill.md` — cold DR video ad scripts
- `ads-research-skill.md` — competitor/ads-library research and strategy
- `hammer-them-skill.md` — post-booking high-frequency retargeting (show-rate booster: scripts + 18-email pre-frame + confirmation-page video)
- `static-ad-skill.md` — static image ad production
- `shortform-ads-skill.md` — short-form video ad scripts

## Install

```bash
cp -r ads-master-skill ~/.claude/skills/
cp sub-skills/*.md ~/.claude/commands/
```

Then trigger with `/ads <client>` (or "build ads for <client>") in Claude Code.
