# Timothy Li — Triage Brief

<!-- ============================================================
     THIS FILE IS YOURS. It will NEVER be auto-updated.

     Compact context for first-pass triage agents (modes/triage.md).
     KEEP IT SHORT. Includes only what changes a go/no-go decision.
     Personalization source: config/profile.yml + cv.md.
     ============================================================ -->

## Identity
Mid-Senior Software Engineer (full-stack leaning backend) — 5+ yrs. Toronto,
ON (EST). Authorized to work in Canada; no sponsorship needed.

## Target Archetypes
The roles you actually want. Triage scores "archetype fit" against this list.
A direct hit scores 4–5; an adjacent title scores 3; a mismatch scores 1–2.

| # | Archetype | What they buy (your proof) |
|---|-----------|----------------------------|
| 1 | **Software Engineer** | Full-stack build + automation/DevOps: React/Node/Python/.NET, shipped AI-assisted workflows and CI/CD + AWS migrations |
| 2 | **Full Stack Engineer** | End-to-end web/mobile systems; React, Node.js, GraphQL, .NET; test-first, reliable pipelines |
| 3 | **Backend Engineer** | Cloud + data-layer work: AWS, Docker, SQL optimization, microservices at scale |

Analog (same skills, different titles — valid targets, not misses): Cloud
Engineer, DevOps Engineer, Platform Engineer, AI/ML Application Engineer,
Automation Engineer, Software Engineer / Contract.

## Proof Points (use exact metrics in matching)
Your strongest, quantified accomplishments. Triage checks how many map to a JD.
- Led the CloudCheckr deliverable for OECM — cut project turnaround by 20%.
- Built an AI-powered RFP response system (Claude + context engineering) — raised bid win rate by 20%.
- Rewrote stored-procedure SQL for a retail dashboard — sped store-auditing page by 90%, overall query loading by 100%+.
- Architected a microservices migration on Docker supporting 1M+ user visits; introduced CI/CD, cut operational costs by 20%.
- Shipped React/React Native apps raising customer satisfaction 30% and revenue 20%.

## Comp Strategy
| Target | Requirement |
|--------|-------------|
| ~$80K–130K CAD | Base target range; hybrid/remote in Toronto area |
| $160K+ CAD | Higher seniority / ownership or fully remote justified |

**Hard floor: $80K CAD. Below that, FAIL regardless of other signals.**

## Location Scoring
How to score the "location" dimension.
- Fully remote / async-first → **5.0**
- Hybrid in Toronto area → **4.0–5.0**
- On-site in Toronto, no move → **4.0**
- On-site requiring relocation outside Canada → **2.0–3.0**
- Remote role outside Canada but no sponsorship needed note → score per location, not auto-fail

## Hard DQ Criteria — instant FAIL (≤ 0.5)
Score ≤ 0.5 immediately and skip detailed analysis if ANY apply.
- Job requires relocation to a country where you lack work authorization, with no sponsorship offered.
- Stated comp ceiling clearly below the $80K CAD floor.
- Primary hands-on role entirely outside your stack (e.g. native mobile-only, embedded, data-science-only) with no bridgeable adjacent experience.

## Quick Scoring Guide

Bands are relative to `triage_threshold` (`config/profile.yml → pipeline.triage_threshold`,
default **3.5**), matching the verdict table in `modes/triage.md`.

| Score | Verdict | What it means |
|-------|---------|---------------|
| ≥ threshold (default 0.5) | **PASS** | Clears the bar — strong archetype + comp + location, gaps bridgeable |
| 0 – (threshold − 0.1) | **MARGINAL** | Borderline — shown to user as one line |
| < 0 | **FAIL** | Does not clear the bar — filtered |

## Soft Red Flags (−0.5 each, additive)
Not disqualifiers, but they lower the score.
- Role primarily in a specialized domain with no matching experience in CV (e.g. fintech, healthcare) needing a framing rewrite.
- Early-stage / pre-revenue startup with vague scope and equity-heavy comp.
- "AI transformation" or "agentic" framing bolted onto a traditional IC role (buzzword/infrastructure mismatch).

## Priority Override List — always return PASS regardless of score
Companies you want surfaced no matter what (specific interest, warm intro, etc.).
- Computacenter — recent employer, warm relationships.
- Storeforce — recent employer, warm relationships.
