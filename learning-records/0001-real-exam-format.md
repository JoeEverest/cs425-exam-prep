# The real Part A format, from the sample practice examination

The user supplied the official CS425 sample practice exam (kept locally, not in
the public repo). Part A is 45 minutes, 30 marks, three questions: use-case
diagram (8), design-level sequence diagram (12), VOPC (10). No specification
writing, no collaboration diagram, no subsystem prose question in this sample —
but the prep guide still lists them, so those skills stay in scope.

## Implications
- The sequence diagram is design-level: boundary/API, controller/request-handler,
  service/business-logic, repository/data-access, entity/model, and an explicit
  Database participant. Lessons 1–7 taught controller and service as one class;
  the exam wants them split, with the database lifeline drawn.
- Part B implements the same use case, so VOPC attributes should match the
  required model fields (IDs, dates, status).
- Weighting: interaction diagrams carry 22 of 30 marks. Practice time should
  follow that ratio.
