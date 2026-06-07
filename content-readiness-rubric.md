# Content Readiness Rubric

Score any external-facing piece of content against five dimensions. Each is scored **0 / 1 / 2**:

- **0** - Absent. The content fails this dimension entirely.
- **1** - Partial. Present but inconsistent, shallow, or only in places.
- **2** - Solid. A skeptical agent reading this would consistently get what the dimension is asking for.

**Readiness bar:** every load-bearing page (the ones a real outsider lands on to make a decision) should score **2 on dimensions 1, 3, and 4**, and at least **1 on dimensions 2 and 5**. A 0 on dimension 1 or 4 blocks publish.

**Calibration standard:** a dimension is well-scored when two independent reviewers reading the same content reach the same score. If two reasonable people would disagree, the wording of the check is too vague for your team - sharpen the example before relying on the score.

---

## Dimension 1 - Provable-claim density

**What it measures:** Does every load-bearing claim point to a number, a named source, or a concrete mechanism - or is it an adjective hoping to be believed?

An agent treats an unsubstantiated claim as noise. "Groundbreaking performance" does not register; "p99 latency under 5ms at 10k req/s, methodology linked" does.

| Score | Looks like |
|-------|-----------|
| 0 | Claims are adjectives ("fast", "secure", "trusted", "leading") with nothing extractable behind them. |
| 1 | Some claims are substantiated; the most important one is not. |
| 2 | Every claim that carries the decision points to a number, a named source, or a described mechanism the agent can extract. |

**Fast test:** highlight every adjective on the page. For each, ask "what is the number or mechanism behind this?" If the page does not answer, the agent cannot either.

---

## Dimension 2 - Structured claim-evidence pairing

**What it measures:** Is the evidence physically next to the claim and in a shape an agent can lift cleanly - or is the proof three scrolls away, in a PDF, or implied?

Agents extract best when claim and evidence sit together: a sentence with its citation, a table row with its source, a stat with its date and method.

| Score | Looks like |
|-------|-----------|
| 0 | Evidence (if any) is divorced from the claim - a separate page, an unlabeled chart, a "see our docs". |
| 1 | Claim and evidence are on the same page but loosely connected; the agent has to infer the link. |
| 2 | Each load-bearing claim carries its evidence inline or immediately adjacent, in extractable form (cited sentence, sourced table row, dated stat). |

**Fast test:** can you copy one claim and its proof as a single contiguous block? If the proof scatters, so does the agent's confidence.

---

## Dimension 3 - Compression survival

**What it measures:** If an agent summarized this to three sentences for someone asking "should I trust / use / hire this," would a *differentiated, provable position* survive - or would it flatten into the category average?

This is the dimension most content fails invisibly. The summary is not bad; it is identical to forty competitors, so the reader has no reason to pick you.

| Score | Looks like |
|-------|-----------|
| 0 | The 3-sentence summary could describe any competitor in the category. No position survives. |
| 1 | A differentiator survives but is generic or unproven ("more flexible", "great support"). |
| 2 | A specific, provable, hard-to-copy position survives compression intact ("the only one of these that runs deterministic replay on a single node"). |

**Fast test:** run the compression test in `compression-test-template.md`. Paste the content into an AI, ask for the 3-sentence verdict, and check whether your one differentiator is in it.

---

## Dimension 4 - Honest wedge (no AI-washing)

**What it measures:** Does the content claim only what it can substantiate? Capability theater - claiming a strength you cannot prove - fails twice: the agent cannot find the proof and drops the claim, and any customer the claim wins is later disappointed in a way the interpretation layer will quote back.

| Score | Looks like |
|-------|-----------|
| 0 | The content leans on claims the team cannot substantiate (aspirational "AI-native", invented capabilities, borrowed credibility). |
| 1 | Mostly honest, but at least one prominent claim outruns the evidence. |
| 2 | Every prominent claim is one the team can defend on demand. The differentiator is true, specific, and the team's own. |

**Fast test:** for the biggest claim on the page, ask "if a buyer pushed on this in a follow-up, could we produce the proof in one click?" If not, it is a liability, not a differentiator.

---

## Dimension 5 - Machine-clean structure

**What it measures:** Is the content shaped so an agent can extract it without guessing - question-first sections, one canonical name per concept, comparisons as tables, proof in lift-able form?

This is the unglamorous, mechanical half. It rarely wins a design award and always changes what the machine can extract.

| Score | Looks like |
|-------|-----------|
| 0 | Wall-of-prose, the real answer buried mid-paragraph, the same concept called three different names across the page. |
| 1 | Reasonably structured but inconsistent - some sections answer-first, some not; some naming drift. |
| 2 | Sections answer the real question in the first line; one canonical name per concept; comparisons are tables; key facts are extractable. |

**Fast test:** read only the first sentence of each section. Do they carry the page's argument on their own? Agents and skimmers read the same way.

---

## Scoring

Total the five dimensions (max 10). Use the total as a triage signal, not a grade:

| Total | Reading |
|-------|---------|
| 9-10 | Ready. The agent will get a provable, differentiated read. |
| 6-8 | Fixable. Identify the lowest dimension and fix that one first; do not spread effort evenly. |
| 3-5 | Adjective-heavy. The content reads as marketing to a human and as noise to an agent. Rework before publishing anything high-stakes. |
| 0-2 | Invisible. An agent compressing this returns the category average. This is the highest-leverage page on your roadmap. |

The bar that actually matters is per-dimension, not the total: **2 on dimensions 1, 3, 4; at least 1 on 2 and 5; never 0 on 1 or 4.** A page can total 7 and still be unpublishable if it scored 0 on the honest-wedge dimension.

---

## One worked example

**Before (scores 0 / 0 / 0 / 1 / 1):**

> Our platform delivers enterprise-grade security and industry-leading performance, trusted by teams worldwide to power their most demanding workloads.

Every claim is an adjective (D1=0). No evidence (D2=0). The 3-sentence summary is indistinguishable from any competitor (D3=0). Probably honest but unprovable (D4=1). Single run-on sentence, no structure (D5=1).

**After (scores 2 / 2 / 2 / 2 / 2):**

> **Security:** SOC 2 Type II audited; every encryption claim links to our published key-management document.
> **Performance:** p99 latency stays under 5ms at 10,000 requests/second on a single node - benchmark method and dataset linked below.
> **What's different:** we are the only platform in this category that runs deterministic replay on a single node, which is why incident reproduction takes minutes instead of days.

Provable (D1=2). Evidence inline (D2=2). A specific, hard-to-copy position survives compression (D3=2). Each claim defensible on demand (D4=2). Answer-first, canonical naming, extractable (D5=2).

Same product. One version is invisible to an agent; the other one travels.
