# Multi-Model Audit Pipeline

## Overview

This is the quality control system I use for all AI-generated creative content. It is modeled on professional film production workflows where multiple independent reviewers — the director, the DP, the editor — each evaluate the same material from different perspectives before anything is locked.

The core insight: **a single model cannot objectively audit its own output.** You need separation.

---

## The Pipeline

```
BRIEF → DRAFT PROMPT → PRE-AUDIT → REVISIONS → DEEP THINK RUN → OUTPUT AUDIT → HOSTILE AUDIT → DELIVERY
```

### Stage 1 — Draft Prompt
Write the initial prompt from the creative brief using the cinematography framework. Do not run it yet.

### Stage 2 — Pre-Audit
Review the draft prompt against the cinematography checklist:
- Lens specified?
- Lighting package defined?
- Camera movement noted?
- Diegetic sound considered?
- Emotional tone clear?

Revise until all boxes are checked.

### Stage 3 — Deep Thinking Pro Model Run
Process the finalized prompt through **ChatGPT Pro** or **Claude** with extended/deep thinking enabled. These models are used for their reasoning depth — they catch logical inconsistencies in the prompt that a quick model misses.

### Stage 4 — Output Audit
When the asset is produced, immediately review against:
- Does it match the brief?
- Is the quality bar professional or amateur?
- Does the sound design (if applicable) match the visual tone?
- Would this pass as real production content?

If it fails any check, return to Stage 2 with specific revision notes.

### Stage 5 — Hostile Audit
Run the approved output through a **completely separate AI model** with the following prompt:

```
You are a hostile creative director reviewing this asset for a major brand campaign. 
Your job is to find every flaw, every amateur tell, every reason a client would reject this. 
Be merciless. Do not look for what works — find what fails.
```

Only assets that survive the hostile audit move to delivery.

---

## Why This Works

Most AI creative content fails because the person producing it is too close to it. They see what they intended, not what was produced. The hostile audit forces an adversarial perspective that surfaces problems invisible to the original creator.

This system was developed from 20+ years of professional film production experience where the cost of getting it wrong on set is measured in hundreds of thousands of dollars per day. The discipline transfers directly to AI content production.

---

## Tools Used

| Stage | Tool |
|-------|------|
| Draft & Pre-Audit | Claude |
| Deep Think Run | ChatGPT Pro (o1/o3) or Claude |
| Generation | Sora 2 |
| Hostile Audit | Separate Claude or ChatGPT instance with fresh context |
| Final Edit | Adobe Premiere Pro |
