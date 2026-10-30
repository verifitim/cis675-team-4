# Candidate Records — US8

Recruiter home with six fictional candidate records, two duplicate pairs, and four retained candidates. Automatically detects matching normalized email addresses or phone numbers, groups related records, and retains the earliest record by creation timestamp. Ties use source order. Empty identifiers do not match. Email normalization removes whitespace and ignores case; phone normalization removes non-digits. It does not infer country codes, match names, merge details, or permanently delete records.

The default view excludes two later duplicate records. Review duplicates shows original contacts, record IDs, the retained record, and exact matching identifiers. Show all records reveals the complete source list with duplicate badges. Browser-local storage preserves records and hidden-record IDs; detection is recalculated on load. Nothing is shared across devices or users. These records are a separate fictional recruiter dataset; this feature does not change the Candidate Matches fixtures or conduct real recruiting.

## Acceptance checks

1. First load: six source records, four candidates shown, two duplicates hidden.
2. Review duplicates: Alex matches by email despite case/spacing; Jamie matches by phone despite punctuation/spacing. Earlier records C001 and C003 are retained.
3. Show all records: six records appear, including duplicates C002 and C004; uncheck to return to four.
4. Refresh: cleanup remains applied; all original records are still reviewable.
5. Unique identifiers remain separate; names alone and blank identifiers do not trigger matches.
6. Recruiter → Candidate Records navigation works from all six product pages, and role/page selections remain correct after Back/Forward.


## US13 — Candidate search

Adds a Search candidates form and Clear search. Case-insensitive substring matching checks names, roles, skills, certifications, experience, and profile text. Multiple whitespace-separated words use AND matching across fields. No stemming, synonym expansion, AI ranking, or contender tagging. For example, “training” does not imply that every occurrence of “trained” matches.

Each result places a prominent “Matches your search” box directly below the candidate name and role. It identifies matching fields and uses bold, yellow-backed mark elements for matched substrings. All relevant fields appear in the box, so a multiword match can be explained across fields. Full background details are also shown below it. Text is inserted through DOM text nodes, not HTML interpolation.

Existing browser-local US8 records are enriched with sample background fields when missing, without changing IDs, contacts, or duplicate classification. Duplicate records remain excluded by default; Show all records combines with search. Fixed sample records only, with no external candidate database or real sourcing.

### Search acceptance checks

- “training” returns Alex and Riley; “spreadsheet” returns Alex and Jamie; “safety certificate” returns Alex; “first aid” returns Taylor.
- Multiword AND matching works across fields: “retail safety” returns Alex; “training first aid” returns no candidates.
- Case differences and repeated whitespace do not affect results; clear restores four unique candidates.
- Every search result shows the matching fields and visually emphasized matching terms near the top of its card.
- Unknown keywords show “No candidates found.” Special characters are handled as text.
- Show all records still reveals the two duplicate source profiles, filtered by the active search.
- Refresh retains enriched records and duplicate cleanup. Search itself starts unfiltered on a new load.
