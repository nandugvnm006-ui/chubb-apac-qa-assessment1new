# Claims Platform - QA Automation

## Purpose
This repository is the QA automation workspace for the Chubb APAC Claims Management
take-home assessment.

## Assessment-driven deliverables
- Test strategy and risk assessment
- Backend unit tests
- Integration tests for the highest-risk flows
- Angular component tests where applicable
- Messaging/integration tests where applicable
- AI working journal
- Architecture notes
- Reproducible local test instructions

## Important
This repository is a scaffold only until the original claims-platform application source
is copied into it. The assessment requires the supplied application's real source code
to be reviewed before selecting exact tests. Do not invent application behaviour or
claim tests pass until the real application is present.

## Expected root structure

    claims-platform/
    ├── .mvn/
    ├── src/
    ├── .gitattributes
    ├── .gitignore
    ├── AI_WORKING_JOURNAL.md
    ├── ARCHITECTURE.md
    ├── README.md
    ├── TEST_STRATEGY.md
    ├── docker-compose.yml
    ├── mvnw
    ├── mvnw.cmd
    ├── pom.xml
    └── pom.xml.save

## Next step
Add the actual supplied application files (including pom.xml and docker-compose.yml),
then implement tests against the real source.
