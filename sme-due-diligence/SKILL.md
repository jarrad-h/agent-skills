---
name: sme-due-diligence
description: >
  Australian SME due diligence and market research agent. Takes a business name, ABN, and/or
  owner/director name as input and produces a structured intelligence report consolidating
  public records, financial information, legal history, news, and risk indicators. Designed
  for investment research, lending decisions, partnership assessments, and general due diligence
  on Australian small-to-medium enterprises and their principals.
---

# SME Due Diligence — Australian Business Intelligence Report

## Purpose

Generate a comprehensive due diligence report on an Australian business and/or its owner(s).
The report consolidates publicly available information into a structured, analyst-ready document
covering entity identity, current state, timeline, director profiles, financials, legal records,
and risk indicators.

## Input

The user will provide **one or more** of the following:

- **Business name** (registered or trading name)
- **ABN** (Australian Business Number) or **ACN** (Australian Company Number)
- **Owner / director name**

Any combination is valid. If only an owner name is provided, begin with the owner and discover
their associated entities. If only a business name or ABN is provided, identify directors from
registry data and then research them.

---

## Research Methodology

Follow these phases **in order**. Each phase builds on the previous one. Do not skip phases.

### Phase 1 — Entity Identification & Anchoring

**Goal:** Establish the definitive identity of the business entity and its key people.

1. **ABN Lookup** — Search the Australian Business Register (ABR):
   - Search: `site:abr.business.gov.au [business name or ABN]`
   - Alternatively, fetch: `https://abr.business.gov.au/ABN/View?abn=[ABN]` if ABN is provided
   - Extract: ABN, entity name, entity type (sole trader / partnership / company / trust), GST registration status, GST registration date, state, postcode, business names, active/cancelled status
   - If the ABR lookup doesn't return results via web search, try: `[business name] ABN Australia`

2. **ASIC Company Search** — Search for company details:
   - Search: `[business name or ACN] site:connectonline.asic.gov.au` OR `[business name] ASIC company registration`
   - Extract: ACN, registration date, company type (proprietary / public), company status, registered address, principal place of business
   - Search for officeholder (director/secretary) information: `[business name] ASIC directors` or `[business name] company officers Australia`

3. **Cross-reference** — Confirm the ABN and ACN relate to the same entity. Note any discrepancies.

4. **If starting from an owner name only:**
   - Search: `"[owner name]" director Australia ASIC`
   - Search: `"[owner name]" ABN business Australia`
   - Identify their primary associated entity, then proceed with that entity through the full process.

**Output of Phase 1:** Confirmed ABN, ACN (if company), entity type, status, registered name, trading names, key people names.

---

### Phase 2 — Deep Research

Run **all** of the following search sequences. Aim for a minimum of **10–15 distinct searches** across these categories. Do not stop at the first result — pursue multiple angles.

#### 2a. Registry & Government Sources

- `"[business name]" OR "[ABN]" site:abr.business.gov.au`
- `"[business name]" OR "[ACN]" site:asic.gov.au`
- `"[business name]" ABN GST registration`
- `"[business name]" [state] business registration` (for state-level business name registrations)
- `"[business name]" PPSR` (Personal Property Securities Register — security interests)
- `"[business name]" grants.gov.au OR business.gov.au` (government grants or programs)

#### 2b. News & Media

- `"[business name]" news`
- `"[business name]" site:afr.com OR site:smh.com.au OR site:theaustralian.com.au`
- `"[business name]" site:smartcompany.com.au OR site:brw.com.au OR site:businessnewsaustralia.com`
- `"[business name]" announcement OR launch OR funding OR acquisition`
- `"[business name]" review OR complaint OR controversy`
- `"[owner name]" news Australia`
- `"[owner name]" interview OR profile OR announcement`

#### 2c. Legal & Court Records

- `"[business name]" court Australia`
- `"[business name]" site:federalcourt.gov.au OR site:judgments.fedcourt.gov.au`
- `"[business name]" supreme court [state]` (use the state identified in Phase 1)
- `"[business name]" tribunal Australia`
- `"[business name]" ASIC enforcement OR "infringement notice" OR "disqualification"`
- `"[business name]" insolvency OR administration OR liquidation OR "winding up"`
- `"[business name]" site:gazette.gov.au` (Commonwealth Gazette — insolvency notices)
- `"[owner name]" court OR tribunal OR judgment Australia`
- `"[owner name]" bankrupt OR disqualified director ASIC`
- `"[owner name]" site:asic.gov.au enforcement`

#### 2d. Financial & Commercial

- `"[business name]" revenue OR turnover OR profit`
- `"[business name]" financial statements OR annual report`
- `"[business name]" funding OR investment OR capital raise`
- `"[business name]" employees OR headcount OR hiring`
- `"[business name]" site:linkedin.com` (company page — employee count, description)
- `"[business name]" credit OR debt OR loan`

#### 2e. Industry & Market Context

- `"[business name]" industry OR sector OR market`
- `"[business name]" competitors OR market share`
- `[industry] market Australia [current year]` (using the industry identified from earlier research)

**Important guidance for searches:**
- If a search returns no useful results, rephrase and retry with different terms before marking the category as "no information found."
- Use `web_fetch` to read full articles or pages when search snippets are insufficient.
- Record every URL that contributes information — these go in the Sources section.

---

### Phase 3 — Owner / Director Expansion

For **each director or owner** identified in Phase 1:

1. **Other directorships:**
   - Search: `"[director name]" director Australia ASIC`
   - Search: `"[director name]" ABN business`
   - Search: `"[director name]" company officer`
   - For each associated entity found, determine: entity name, ABN/ACN if available, status (Current / Deregistered / In Administration / In Liquidation / Cancelled), one-sentence description of what the business does.

2. **Personal public records:**
   - Search: `"[director name]" disqualified director site:asic.gov.au`
   - Search: `"[director name]" bankruptcy Australia`
   - Search: `"[director name]" banned OR prohibited OR enforceable undertaking`

3. **Professional profile:**
   - Search: `"[director name]" LinkedIn Australia` or `"[director name]" professional profile`
   - Extract: Current role, career history summary, qualifications, industry experience.

---

### Phase 4 — Synthesis & Analysis

This is the most important phase. Do not simply list data — **synthesize and interpret** it.

1. **Current State Assessment:**
   Write 2–3 analytical paragraphs that assess the business's current position. Consider:
   - Is the entity active and trading? Evidence of recent activity?
   - Growth signals (hiring, expansion, funding, new products) vs decline signals (layoffs, complaints, legal issues, director resignations)?
   - Market position — is the business established, emerging, or struggling?
   - Any red flags or notable strengths?

2. **Timeline Construction:**
   Build a reverse-chronological timeline from all dated events discovered. Include:
   - Entity registration / incorporation
   - Director appointments and resignations
   - ASIC filings and changes (name changes, address changes, status changes)
   - News events (launches, funding rounds, acquisitions, controversies)
   - Legal proceedings (filing dates, hearing dates, outcomes)
   - Insolvency events

3. **Risk Assessment:**
   Evaluate and flag:
   - Director associated with multiple failed/deregistered entities
   - Recent rapid changes in directorship
   - Outstanding legal proceedings
   - ASIC enforcement actions
   - Insolvency history (business or personal)
   - Negative news patterns
   - Absence of expected information (e.g., a company claiming significant revenue but no visible footprint)

4. **Confidence Tagging:**
   Tag each major piece of information with a confidence level:
   - **Confirmed** — sourced from an official government registry (ABR, ASIC, court records)
   - **Likely** — sourced from a reputable news outlet or professional profile with consistent cross-references
   - **Unverified** — sourced from a single informal source, or inferred from limited data

---

### Phase 5 — Report Generation

Generate the report using the template at `templates/report-template.md`.

**Report file:** Save as `[business-name-slugified]-due-diligence-report.md`

- Replace all placeholders in the template with researched content.
- If a section has no information available, do not remove it — instead note: *"No public information identified in this category."*
- Ensure every factual claim has a source URL in the Sources section.
- The Executive Summary should be written **last**, as a distillation of all other sections.

---

## Quality Standards

- **Minimum search depth:** At least 10 distinct web searches per report. More for complex entities.
- **Source diversity:** Information should come from at least 3 different source categories (registry, news, legal, financial, professional).
- **No fabrication:** If information is not found, say so. Never invent or assume details.
- **Australian focus:** All registry lookups and legal searches should target Australian sources. Note if the entity has international operations but keep the research Australia-centric.
- **Recency bias:** Prioritise the most recent information. Clearly date all timeline entries.
- **Plain language:** Write for a business audience, not a legal or technical one. Explain jargon where used.

---

## Edge Cases

- **Sole traders:** These won't have an ACN or ASIC registration. The ABR is the primary registry source. Director expansion becomes owner research.
- **Trusts:** The trustee entity is the legal person. Note the trust structure and research both the trust (if named) and the trustee entity.
- **Deregistered entities:** Still research fully — the historical information is the value.
- **Common names:** If director/owner name is very common, use additional context (state, industry, associated entity) to disambiguate. Flag if disambiguation is uncertain.
- **Newly registered entities:** Limited history is expected. Note the registration date and flag that the entity has a short operating history.
