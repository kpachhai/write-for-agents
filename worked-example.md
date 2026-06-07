# Worked Example: The Same Announcement, Before and After

A short, generic before/after to make the rubric concrete. The company and product are invented; the patterns are the ones that show up in almost every product announcement and press release.

The failure isn't bad writing. It's *average* writing - the kind an AI reads, finds nothing specific in, and compresses into the category. Watch what changes when you apply three fixes from the rubric.

---

## Before

> **Northpeak launches Atlas, the best-in-class data pipeline for modern teams**
>
> Northpeak today announced Atlas, a best-in-class data pipeline platform that gives engineering teams enterprise-grade reliability and seamless scale. Trusted by leading teams, Atlas has processed billions of events and is the most complete solution for modern data infrastructure. "We're thrilled to give teams a powerful, intuitive way to move their data," said the CEO.

**Compression test - what an AI tells someone asking "should we use this?":**
> "Atlas is a data pipeline platform that claims reliability and scale for engineering teams."

That verdict could describe forty other products. Nothing specific survived. In a consideration set, "indistinguishable" is "excluded."

**Rubric: 4/10** - Provable density 1, claim-evidence 0, compression survival 0, honest wedge 1, structure 2.

---

## The three fixes

1. **Source the proof point.** "Billions of events" and "trusted by leading teams" are the strongest claims in the post, and neither is checkable. Attach a number, a name, and a link.
2. **Replace the adjective with the property behind it.** "Best-in-class reliability" tells an agent nothing. The specific guarantee that *makes* it reliable tells it everything.
3. **Add one sentence that survives compression.** Name the one thing Atlas does that a competitor can't copy into their own page without lying.

---

## After

> **Atlas: exactly-once data delivery that survives downstream outages**
>
> Northpeak today launched Atlas, a data pipeline that guarantees exactly-once delivery with a replayable per-partition log - even when a downstream system goes down mid-stream. Most pipelines drop or duplicate events under backpressure; Atlas holds the guarantee through the outage and replays on recovery. It processes 4B+ events per day across 200 production deployments at a measured 99.99% delivery rate ([live status page](#)). "Teams pick Atlas when losing or double-counting an event is not an option - payments, billing, audit logs," said the CEO.

**Compression test - same question, rewritten post:**
> "Atlas is a data pipeline whose differentiator is exactly-once delivery that holds through downstream outages, with a replayable per-partition log - proven at 4B+ events/day across 200 deployments at 99.99%. Strong fit when dropped or duplicated events are unacceptable (payments, billing, audit)."

A specific, provable, hard-to-copy position now survives.

**Rubric: 10/10** - Provable density 2, claim-evidence 2, compression survival 2, honest wedge 2, structure 2.

---

## What changed (and what didn't)

The product didn't change. No new feature shipped. The team stopped hiding its actual differentiator behind "best-in-class" and gave the agent something true to extract. Cost: one sourced proof point, one property swapped in for an adjective, one differentiator sentence.

That's the whole kit in one example. Run the [compression test](compression-test-template.md) on your own highest-stakes page and see which verdict you get.
