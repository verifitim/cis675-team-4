# CIS675 Team 4

Interactive hiring-platform prototype for CSU CIS 675. Uses fictional data and browser-local interactions; no production backend or live AI service.

## Live site

https://verifitim.github.io/cis675-team-4/

## Pages

- [My Profile](my-profile/): US2 and US7
- [Job Search](job-search/): US6
- [Job Posting](job-posting/): US14
- [Candidate Matches](candidate-matches/): US4 and a preview of US9

## Team workflow

1. Pick a user story and agree on acceptance criteria.
2. Create a branch for your change.
3. Edit the relevant page, using Copilot if helpful.
4. Open a pull request and ask another team member to review it.
5. Test the agreed interactions and navigation before merging.

Read AGENTS.md before changing a page. Each page README describes simulated behavior and limitations. Keep fictional data only.

## Hosting

Configure GitHub Pages to deploy from main, repository root. The root page opens My Profile. Page navigation uses relative links so it works under this repository URL. Main branch updates publish the site automatically once Pages is configured.

## Local preview

Serve the repository with any local static web server and open my-profile/. Use one browser and origin to test shared local state. File URLs can behave differently for browser storage.

## Origin

Copied from the cis-675 directory of verifitim/csu-grad-coursework. Other coursework is not included. The original site remains separate; changes here do not synchronize back automatically.
