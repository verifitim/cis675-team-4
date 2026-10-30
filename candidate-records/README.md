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
