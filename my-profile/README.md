# Team 4 — My Profile

CIS 675 interactive prototype covering US2 (show abilities beyond expected credentials) and US7 (maintain profile and resume).

The product interface intentionally presents the proposed finished experience. All starting candidate data is fictional. This single HTML file uses browser-local state and has no backend or real AI service.

## Included

- Editable profile, work experience, education, and certifications.
- Resume attachment interaction within the profile section. The prototype validates extension and size and remembers only the filename; no document bytes are uploaded, stored, parsed, or shared with employers.
- Suggested skills with supporting experience, transfer context where available, and confirm/edit/dismiss controls.
- An accomplishment input with a staged two-second discovery interaction and three fixed suggestions grounded in the fictional candidate’s existing experience. Input text does not drive analysis; this illustrates the appearance of discovery rather than implementing it.
- Manual skill entry and candidate review.

## Outside this version

Automatic resume parsing and profile population, employer evaluation configuration, verified credentials, employer access, authentication, and server-side persistence are not implemented. Resume-based profile population remains a proposed backlog item rather than an interface promise.

## Validation

JavaScript syntax, referenced element IDs, and the staged discovery state transitions were checked with a DOM stand-in. A browser execution environment was unavailable for visual or end-to-end testing.

## IC feedback: resume upload accessibility

Updated the resume picker with a visible label, programmatically linked PDF/DOCX and 5 MB instructions, a prominent keyboard focus outline, nearby text errors announced through role="alert", and confirmation/removal messages announced through role="status". Invalid selections preserve the current resume. Removing a resume returns focus to the picker. These targeted improvements do not establish whole-page or whole-site WCAG conformance.

Simple review evidence:
1. Tab to Choose File and show the focus outline and instructions.
2. Select a PDF or DOCX no larger than 5 MB and show the filename and confirmation.
3. Select an unsupported or oversized file and show the specific error.
4. With a screen reader, verify instructions and feedback are announced; tab to Remove resume, activate it, and verify focus returns to the picker.

Automated checks passed for JavaScript syntax, accepted PDF/DOCX names, the exact 5 MB boundary, unsupported extensions, oversized files, error recovery, storage failure rollback, removal/focus behavior, and feedback markup. Screen-reader and visual browser checks remain manual.

References:
- https://www.w3.org/WAI/tutorials/forms/labels/
- https://www.w3.org/WAI/WCAG22/Understanding/status-messages.html
