# Chubb APAC QA Take-Home Assessment

## Important
This repository is a submission-ready QA framework/template based on the assessment document.
The actual Chubb application source/repository was not included with the assessment document supplied to me.
Therefore, application-specific selectors, API paths, Kafka topics, WebSocket events, and backend classes must be verified against the provided application before submission.

Do NOT submit invented bugs or invented application behaviour. Replace the marked TODOs after inspecting the real application.

## Assessment goals
- Assess the application and identify highest-risk areas.
- Implement focused component, unit, and integration/E2E tests.
- Document bugs/quality concerns actually discovered.
- Demonstrate DRY, SOLID and clean-code practices.
- Maintain meaningful Git history.
- Document AI collaboration and decisions.

## Suggested structure

```text
chubb-apac-qa-assessment/
├── README.md
├── package.json
├── playwright.config.ts
├── tsconfig.json
├── .gitignore
├── docs/
│   ├── test-strategy.md
│   ├── bugs-found.md
│   └── ai-working-journal.md
└── test/
    ├── e2e/
    │   ├── claims/
    │   │   ├── create-claim.spec.ts
    │   │   ├── search-claim.spec.ts
    │   │   └── claim-status.spec.ts
    │   └── fixtures/
    │       └── test-data.ts
    ├── api/
    │   └── claims-api.spec.ts
    └── websocket/
        └── claim-status-realtime.spec.ts
```

## Prerequisites
- Node.js
- npm
- Docker Desktop or Podman
- Java/JDK if required by the supplied backend
- The application repository supplied by Chubb

## Install

```bash
npm install
npx playwright install
```

## Start the supplied application

Use the Docker Compose file supplied by Chubb:

```bash
docker compose up -d
docker compose ps
```

## Configure base URL

PowerShell:

```powershell
$env:BASE_URL="http://localhost:4200"
```

Windows CMD:

```cmd
set BASE_URL=http://localhost:4200
```

Linux/macOS:

```bash
export BASE_URL=http://localhost:4200
```

Replace the URL with the actual frontend URL from the supplied Docker Compose configuration.

## Run tests

```bash
npm test
npm run test:e2e
npm run test:api
npm run test:websocket
npm run test:smoke
npm run test:regression
npm run test:headed
npm run test:debug
npm run typecheck
npm run report
```

## Before submission

1. Inspect the real source code.
2. Replace every TODO with real selectors/endpoints/classes.
3. Run the complete application locally.
4. Run all tests.
5. Investigate every failure.
6. Keep failures that expose genuine product defects and document them.
7. Do not manufacture bugs.
8. Update `docs/test-strategy.md` with actual findings.
9. Update `docs/bugs-found.md` with actual evidence.
10. Complete `docs/ai-working-journal.md`.
11. Commit in logical increments.
12. Push to the requested Git repository.

## Suggested commit history

```text
chore: initialize QA assessment
docs: add application risk assessment
test: add critical claim component coverage
test: add claim service unit coverage
test: add claim API integration coverage
test: add critical claim E2E flows
test: add real-time status coverage
docs: document discovered defects
docs: add AI working journal
docs: finalize assessment README
```

## Walkthrough structure

### 1. Application understanding
Explain:
- architecture
- critical business flow
- frontend/backend boundary
- messaging boundary
- WebSocket flow

### 2. Risk-based strategy
Explain why the selected tests have the highest business/integration value.

### 3. Test architecture
Show:
- component tests
- unit tests
- API/integration tests
- Playwright E2E tests
- reusable fixtures/helpers

### 4. Execution
Run the smoke suite and then the broader regression suite.

### 5. Defects
For every genuine defect:
- reproduce
- show expected vs actual
- show automated test/evidence
- explain severity and priority

### 6. AI collaboration
Explain what AI generated, what you accepted, what you challenged, and what you changed.

### 7. What you would do next
Prioritise:
- additional business rules
- more integration/message scenarios
- broader negative cases
- visual regression
- load testing if justified

## Critical warning
A green test that does not exercise real application behaviour is not useful. The assessment explicitly values meaningful tests and genuine defect discovery.
