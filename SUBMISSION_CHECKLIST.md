# Submission Checklist

## Application
- [ ] Actual Chubb application source is present/available locally.
- [ ] Docker Compose starts successfully.
- [ ] Frontend URL confirmed.
- [ ] Backend/API URLs confirmed.
- [ ] Kafka configuration reviewed.
- [ ] WebSocket configuration reviewed.

## Tests
- [ ] Component tests added where appropriate.
- [ ] Unit tests added for important business logic.
- [ ] API/integration tests added.
- [ ] Critical Playwright E2E tests added.
- [ ] WebSocket flow tested if applicable.
- [ ] Tests use real selectors/contracts.
- [ ] No fake/passing-only assertions.
- [ ] All failures investigated.

## Documentation
- [ ] README complete.
- [ ] Test strategy complete.
- [ ] Bugs/quality concerns complete.
- [ ] AI journal complete.
- [ ] Limitations documented.

## Git
- [ ] Meaningful commit history.
- [ ] No node_modules committed.
- [ ] No secrets committed.
- [ ] Tests run locally.
- [ ] GitHub repository is accessible to the hiring team.

## Final commands

```bash
npm install
npx playwright install
docker compose up -d
docker compose ps
npm run typecheck
npm run test:smoke
npm test
npm run report
```

Then:

```bash
git status
git add .
git commit -m "docs: finalize QA assessment submission"
git push
```
