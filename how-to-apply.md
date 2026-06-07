# How to Apply the Readiness Rubric

The rubric (`content-readiness-rubric.md`) is the what. This is the how: where it fits in a content workflow, how to run the compression test, and how to integrate it into review without turning it into a bottleneck.

## Where it fits

Run the readiness pass at one of three points, depending on your adoption tier (see `README.md`):

```
draft  ->  [readiness pass]  ->  publish  ->  (optional) monitor
```

- **At draft time (best):** if you draft with an AI assistant, fold the five dimensions into the drafting prompt or skill so the first draft is already readiness-aware. Fixing the cause is cheaper than catching the symptom.
- **At review time:** add the rubric to your content-review or docs-PR checklist. Score the five dimensions; a failing dimension blocks publish.
- **As an audit:** run the rubric across already-published high-stakes pages to find the ones an agent currently renders invisible. Start with the page a real outsider lands on to make a decision.

Do not run it on everything. Reserve it for **load-bearing content** - the pages, docs, and profiles where an agent's reading changes an outcome. A throwaway changelog entry does not need it.

## The single most important step: the compression test

Dimensions 1, 2, 4, and 5 you can check by reading. Dimension 3 - compression survival - you have to *run*, because it is the one your own familiarity hides from you. You know your differentiator is on the page; the question is whether it survives an agent throwing 90% of the page away.

Use `compression-test-template.md`. The shape:

1. Paste the content into an AI assistant.
2. Ask it for the 3-sentence verdict a buyer/hirer/partner would get: "Based only on this, should I trust and use this? Answer in three sentences."
3. Read the three sentences. Ask: **is my one differentiator in there, and is it stated as something specific and provable?**
4. If yes - dimension 3 passes. If the summary could describe any competitor, you just found your highest-leverage fix.

Run it on at least two different models if you can; they compress differently, and a differentiator that survives both is robust.

A stronger variant - the **summarize-then-diff**: have the model summarize, then list every claim from your original that did *not* make the summary. The dropped claims are the ones with no extractable substance. That list is your fix queue, ranked.

## Fixing a low score - one dimension at a time

When a page scores low, resist the urge to rewrite everything. Find the lowest-scoring dimension and fix that one first; the others often improve as a side effect.

| Lowest dimension | First move |
|------------------|-----------|
| 1 - Provable density | Replace the most prominent adjective with its number, source, or mechanism. |
| 2 - Claim-evidence pairing | Move the proof next to the claim it supports; cite inline. |
| 3 - Compression survival | Write one sentence stating your differentiator as a specific, provable fact, and put it where an agent reads first. |
| 4 - Honest wedge | Cut or qualify the claim you cannot defend on demand. Replace it with the true one. |
| 5 - Machine-clean structure | Rewrite each section's first sentence to answer its real question; pick one canonical name per concept. |

## Integrating into review without a bottleneck

The failure mode of any new gate is that it becomes paperwork people route around. To avoid it:

- **Scope it.** The gate applies to load-bearing external content, not every edit. Say so explicitly.
- **Score fast.** The five dimensions are a five-minute read-through, not an audit. The compression test is one paste and one read.
- **Block on cause, not polish.** A 0 on provable density or honest wedge blocks publish. A 1 on structure is a note, not a blocker. Do not let the gate argue about commas.
- **Make the author run it.** The person who wrote the content runs the rubric and the compression test before review. The reviewer spot-checks. This keeps the gate from becoming a second team's job.

## What this is not, operationally

- **It is not a substitute for a GEO/AEO monitoring tool**, and a monitoring tool is not a substitute for it. The rubric fixes whether your content has anything to extract; the monitor tells you whether models pick it up after publish. If you only do one, do this one first - a monitor on un-fixed content measures your invisibility in high resolution.
- **It is not a one-time pass.** Re-run it when a load-bearing page changes materially, when you launch a new claim, or when a model generation changes how aggressively things get compressed.
- **It does not require an engineer.** Every check is a reading task or a paste-and-read task. The discipline is editorial, not technical.

## A 10-minute version

If you adopt nothing else:

1. Pick your single highest-stakes public page.
2. Run the compression test (paste, ask for the 3-sentence verdict, read it).
3. If the summary sounds like every competitor, write one provable differentiator sentence and put it where the agent reads first.
4. Re-run the compression test. Confirm the differentiator now survives.

That loop, on your most important page, captures most of the value of the entire bundle.
