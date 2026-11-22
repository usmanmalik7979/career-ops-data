# Usman Ahmed Malik — Triage Brief

## Identity
Technical Project Manager / delivery lead — 7+ yrs in tech (software engineer → data analyst → BA → TPM). London, UK (Europe/London). **UK Skilled Worker visa: needs an employer with a UK sponsor licence.** Available immediately.

## Target Archetypes

| # | Archetype | What they buy (your proof) |
|---|-----------|----------------------------|
| 1 | **Technical Project / Delivery Manager** | 18-building IoT programme on schedule & budget (~£130k ARR live); sole coordinator of 10+ concurrent client programmes |
| 2 | **Technical Program Manager** | Engineering background (Symantec, Techwards, AWS); cross-team Agile delivery; RAG reporting and risk escalation |
| 3 | **Implementation / Client Onboarding Manager** | Onboarding cut 8 → 5 weeks; pre-sales feasibility checks across 9 clients |
| 4 | **Business Analyst (Senior / Technical)** | Discovery workshops, requirements & acceptance criteria, BMS/EMS integration analysis |
| 5 | **Product Owner / Product Manager** (adjacent → score 3) | Built and iterated Jira Copilot (full team adoption); Sales → SoW translation |

Analog titles that count as valid targets: Project Manager (technical/IT/SaaS), Delivery Lead, Programme Manager, Implementation Consultant/Lead, Solutions Delivery Manager, PMO Lead, Technical BA.

## Proof Points (use exact metrics in matching)
- ~£130k ARR brought live via an 18-building IoT and metering programme, on schedule and within budget
- Client onboarding cut from 8 to 5 weeks across 10+ concurrent programmes
- 3 at-risk programmes (7 buildings) recovered via early RAG escalation, protecting ~£50k annual contract value
- Jira Copilot AI assistant: ~5 hrs/week triage saved, 92 backlog items in 5 weeks, full team adoption
- Led company's first ISO 27001 certification (June 2023)
- ETL pipelines enabling a client go-live supporting ~$12k monthly revenue (Afiniti)

## Comp Strategy
| Target | Requirement |
|--------|-------------|
| £52k+  | Any work arrangement |

**Hard floor: £52,000 base. Stated comp ceiling below that → FAIL.** No salary stated → do not penalise.

## Location Scoring
- Remote, hybrid, or on-site in/near London → **5.0**
- On-site elsewhere in the UK requiring relocation → **3.0**
- Outside the UK without relocation + visa support → **1.0**
- High travel (>25%) → **deduct 0.5**

## Hard DQ Criteria — instant FAIL (< 3.0)
- JD says the employer **cannot / will not sponsor**, or requires the right to work in the UK without sponsorship
- Employer confirmed **not** on the GOV.UK register of licensed sponsors (Skilled Worker route)
- Stated salary ceiling below £52k
- Junior / graduate / intern level, or roles that are primarily hands-on software engineering

## Quick Scoring Guide

Bands are relative to `triage_threshold` (`config/profile.yml → pipeline.triage_threshold`,
default **3.5**), matching the verdict table in `modes/triage.md`.

| Score | Verdict | What it means |
|-------|---------|---------------|
| ≥ threshold (default 3.5) | **PASS** | Strong archetype + comp + sponsorship OK |
| 3.0 – (threshold − 0.1) | **MARGINAL** | Borderline — shown to user as one line |
| < 3.0 | **FAIL** | Filtered |

## Soft Red Flags (−0.5 each, additive)
- Requires UK security clearance (SC/DV) — flag for the user; eligibility depends on residency history
- Requires PMP / PRINCE2 Practitioner as mandatory (candidate has PRINCE2 Foundation, result pending)
- Deep domain requirement outside SaaS/IoT/data (e.g. construction PM, clinical, banking regulation)
- Pure product-management role demanding a track record as PM owner of a product

## Priority Override List — always return PASS regardless of score
- (none yet)
