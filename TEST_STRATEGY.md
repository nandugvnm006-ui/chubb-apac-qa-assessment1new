# Test Strategy

## 1. Objective
Provide focused, production-quality automated coverage for the highest-risk behaviours
in the Claims Management application.

## 2. Highest-risk areas
The exact risk areas must be confirmed from the supplied source code. Review first:
- Critical claim/business rules
- API/controller-to-service boundaries
- Persistence behaviour
- Kafka/message flows
- WebSocket real-time updates
- Angular user-facing claim workflows
- Error handling and validation
- Integration points between layers

## 3. Test selection
Prioritise a small number of high-value tests across:
- Component tests
- Unit tests
- Integration tests
- Messaging/integration tests where applicable

## 4. Deliberately excluded
Avoid exhaustive testing of low-risk or repetitive paths within the timebox.
Exact exclusions should be documented after reviewing the real application.

## 5. Defects discovered
Record only defects actually reproduced or supported by source-code review.

## 6. Remaining risk
Document untested areas and why they were not prioritised.

## 7. Future work
With additional time, consider broader integration coverage, visual regression,
and load testing where appropriate.
