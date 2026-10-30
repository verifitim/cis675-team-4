# My Applications — US10

Central Job Seeker view containing four fictional submitted applications: Training Coordinator (Submitted, blue), Operations Coordinator (In review, amber), Customer Onboarding Coordinator (Interview, purple), and Community Program Coordinator (Rejected, gray). Each shows job title, company, application date, a readable status badge, and explanatory text.

Active applications show Submitted → In review → Interview, with current stage marked using words, color, and aria-current="step". Earlier stages show Completed; later stages show Not reached. Rejection is a separate closed state rather than a normal next step in the progress indicator. Layout adapts for mobile.

This 1-point prototype uses fixed sample statuses, not employer updates. It does not submit applications, schedule interviews, send notifications, or connect to the saved posting. Data does not represent real hiring outcomes. No new storage or backend is needed for this read-only demonstration.

## Acceptance checks

1. My Applications is available under Job Seeker → Go to on all seven product pages.
2. All four applications appear centrally, each with job title, company, application date, and status.
3. Submitted is blue; In review is amber; Interview is purple; Rejected is gray. Each includes a text label.
4. The three active applications show the appropriate current progress stage. Rejected shows a closed state without suggesting it is the next stage after Interview.
5. Desktop and mobile layouts have readable labels and usable role/page navigation.
