# LLM Test-Oracle Authority Review: Replication Package

Replication data for the article *"LLM-Based Test Oracles: Source-of-Authority
Taxonomy - A Systematic Literature Review"* (Mughal and Bilal), conducted and
reported under PRISMA 2020.

## Search

Three databases (Scopus, IEEE Xplore, ACM Digital Library), executed 31 May 2026,
publication window January 2021 to May 2026. Funnel: 2,436 records identified,
2,245 after de-duplication, 115 taken to full text, **54 included**. Independent
dual human screening reached Cohen's kappa = 0.79. A backward and forward
citation-searching (snowballing) round over the 54 included studies added
**29 more, for 83 included in total**.

## Coding

Every full-text record was coded twice. In the database arm the 115 records were
coded against the locked codebook and then re-assessed in a second pass covering
the two variables the review's conclusions rest on, eligibility and the primary
source of authority, each with its own supporting quotation. In the
citation-searching arm the 32 records coded were taken through two full passes
over all fields. Concordance between the passes was **80.7%** on eligibility
(22 differences over the 114 unique full-text records) and **83.3%** on primary
source (8 differences over the 48 records both passes judged includable) in the
database arm, and **86.2%** on primary source (4 differences over 29) in the
citation-searching arm. Every difference was adjudicated against the
pre-registered boundary rules and is listed in `Coding-Adjudication`.

Note: applying the adjudication revised the database first pass in place, so its
pre-adjudication source codes are not retained. `Coding-Adjudication` records the
pass-1 eligibility decision explicitly and marks source accordingly.

### Reproducing the concordance figures

All three figures reported in the paper can be recomputed from this workbook.

1. **Eligibility, database arm.** In `Coding-Adjudication`, count rows with
   `arm = database` and `variable = eligibility`: **22**. The denominator is the
   114 unique full-text records (115 assessed, 1 duplicate found at full text).
   (114 - 22) / 114 = **80.7%**.
2. **Primary source, database arm.** Count rows with `arm = database` and
   `variable = source_primary`: **8**. For the denominator, count `decision =
   include` in `Database-Coding-Pass2` (**50**), then subtract the eligibility
   rows whose `pass2 = include` and `pass1 = exclude` (**2**: records 0304 and
   0873), leaving the **48** records both passes judged includable.
   (48 - 8) / 48 = **83.3%**.
3. **Primary source, citation-searching arm.** Compare `source_primary` between
   `Snowball-Coding-Pass1` and `Snowball-Coding-Final` across the 29 rows that
   carry an `id`: **4** differ (2256, 2270, 2271, 2272).
   (29 - 4) / 29 = **86.2%**.

## Contents

- `PRISMA-2020-Checklist.pdf`: the completed 27-item PRISMA 2020 checklist with the location of each item.
- `PRISMA-Flow-Diagram.pdf`: the records-flow diagram (identification to inclusion).
- `protocol/Review-Protocol.pdf`: the locked inclusion and exclusion criteria and the 35-field extraction codebook (the legend for the coded data).
- `search/Search-Strategy.pdf`: the frozen search query, per-database renderings, run ledger, and screening log.
- `Stage-1-Screening-Prompt.pdf`: the exact Stage-1 pre-filter screening prompt (model, decoding settings, run date, and the pre-registered inclusion/exclusion criteria).
- `data/Review-Data.xlsx`: one workbook with a sheet per table:
  - `Search-Scopus`, `Search-IEEE`, `Search-ACM`: per-database results, metadata only (391 / 234 / 1,811 records).
  - `Screening-Funnel`: all 2,245 de-duplicated records with screening decision and reason (the PRISMA flow).
  - `Decisions-Ali`, `Decisions-Bilal`, `Decisions-Consensus`: the independent dual-screening record.
  - `Database-Coding-Final`: final per-study coding for the 115 full-text-assessed records of the database arm, after adjudication: the coded taxonomy fields, an anchoring quotation (`key_quote`) per study, and citation metadata.
  - `Database-Coding-Pass2`: the second coding pass over the same 115 records, covering eligibility and primary source of authority, each with its own evidence quotation and a confidence rating.
  - `Snowball-Coding-Pass1`, `Snowball-Coding-Final`: the two coding passes over the 32 records coded in the citation-searching arm; the final pass excluded 3, leaving the 29 that appear in the paper.
  - `Coding-Adjudication`: every difference between the two coding passes (34 in total), with the adjudicated outcome and which pass it followed.
  - `Coding-Sheet-Included`: the 83 included studies (54 database + 29 citation-searching), the same coded fields including anchoring quotations; the `Snowball Gather` column flags the 29 added by snowballing.

Publisher PDFs, raw database exports, and record abstracts are not redistributed
(copyright); the released per-database exports are metadata only.

## License and citation

Licensed under CC BY 4.0 (see `LICENSE`). To cite, see `CITATION.cff`.

## Authors

- Ali Hassaan Mughal, Independent Researcher, USA. ORCID 0000-0002-0724-9197.
- Muhammad Bilal (corresponding), Technical University of Munich, Germany. ORCID 0000-0003-4106-0256.
