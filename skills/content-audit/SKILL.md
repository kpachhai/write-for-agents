---
name: content-audit
description: Use when asked to audit external-facing content (product page, README, docs, blog post, launch announcement, profile) for AI-agent legibility, run a compression test, check whether a differentiator survives AI summarization, or score content against the content-readiness rubric. Also fires pre-publish when content will be read by AI assistants answering trust/fit queries about the author or product.
---

# Content Audit (Agent-Legibility Pass)

## Overview

Score a piece of external-facing content for its second reader: the AI that compresses it before any human sees it. The discipline, rubric, and templates live at the plugin root (the repo root, two levels up from this skill directory) - read them, do not paraphrase from memory:

- `content-readiness-rubric.md` - the scored 5-dimension rubric (provable claims, claim-evidence pairing, compression survival, honest wedge, machine-clean structure)
- `how-to-apply.md` - where the rubric fits and how to run the compression test
- `compression-test-template.md` - the compression-test worksheet
- `worked-example.md` + `examples/` - calibration anchors (a 4/10 -> 10/10 rewrite; real articles scored 10/7/6)

## Workflow

1. **Read the rubric and the content.** Read `content-readiness-rubric.md` fully, then the target content fully (no skimming - scoring from a skim produces inflated scores).
2. **Run the compression test first.** Per `compression-test-template.md`, using its canonical question ("should I trust and use this?"): summarize the content in 3 sentences as an AI assistant would answer a buyer. Then check: does anything in those 3 sentences distinguish this from the category average? Name what survived and what got averaged away. The template is written for self-audit with external models; when auditing third-party content or when no second model is available, perform the compression yourself - and when the author's intended differentiator is unknown, treat it as "none stated" and let the test reveal whether one emerges.
3. **Score the 5 dimensions** per the rubric, each with a one-line justification quoting the content. Calibrate against `worked-example.md` and `examples/` - if your scores run higher than those anchors for similar quality, re-score.
4. **Verdict + the three fixes.** Total score, the single weakest dimension, and at most 3 concrete fixes ranked by lift (the worked example shows the fix format: specific rewrite, not "be more specific"). Unverifiable claims get flagged for removal - an agent that cannot check a claim drops it.
5. **Honesty rule:** if the content is genuinely category-average, say so. A 4/10 with three real fixes is the useful output; a courtesy 7/10 defeats the audit.

## Common Mistakes

- Scoring without running the compression test - the test is the evidence the scores rest on.
- Rewriting the author's voice. The truth layer (claims + evidence) serves the agent; voice serves the human. Fix claims, keep voice - the dual-channel discipline.
- Accepting adjectives as claims. "Blazing fast" scores zero; "p99 under 80ms on the public benchmark" scores.

---

**Version:** 1.0.0
