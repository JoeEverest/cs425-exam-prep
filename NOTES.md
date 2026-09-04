# Working notes

## User preferences
- The user writes and reads in ASD-STE100 Simplified Technical English.
  Keep lesson prose short, imperative, and active. This also suits drawing
  instructions well.
- The exam is paper-based. Every lesson must end with a draw-on-paper task.

## Teaching plan (professor's order)
1. 0001 — Use-case diagrams (actors, boundary, «include», «extend») ✅ built
2. 0002 — Use-case specification (name, goal, flows, business rules) ✅ built
3. 0003 — Use-case realization: boundary / control / entity classes ✅ built
4. 0004 — Sequence diagrams (lifelines, activations, DAO/repository, alt/opt) ✅ built
5. 0005 — Collaboration diagrams (links, numbered messages, nesting) ✅ built
6. 0006 — VOPC diagrams (deriving operations from messages) ✅ built
   (cheat sheet updated in the same commit: BR-1 check moved from a controller
   self-message to Course.checkPrerequisites, so all artifacts tell one story)
7. 0007 — Subsystem design (façade, service, DAO, repository) ✅ built
8. 0008 — Timed mock (MediBook clinic scenario, 7 tasks, 40 marks) ✅ built
   All eight lessons are complete. Next sessions: grade mock results, redo weak
   topics, and ask the user for a past paper (see RESOURCES.md gap).

## Running example
One scenario carries through every lesson so the artifacts stay consistent
(the professor's "diagram consistency check"):

**University Course Registration System**
- Actors: Student (primary), Registrar, Payment Gateway (external system)
- Use cases: Enroll in Course, Drop Course, Pay Tuition
- «include»: Enroll in Course includes Verify Prerequisites
- «extend»: Join Waitlist extends Enroll in Course (when the course is full)
- Business rule: a student cannot enroll when prerequisites are not met
- Later lessons reuse it: EnrollmentForm (boundary), EnrollmentController
  (control), Student/Course/Enrollment (entities), CourseRepository (DAO).

## Practice example (for the user to draw, distinct from the taught one)
**Library Lending System** — Member, Librarian, Email Service; Borrow Book
(includes Verify Membership), Return Book (extended by Pay Late Fee).

## Design system for lessons
- Concept: an engineering notebook / exam paper. Light, warm paper, graph grid
  under diagrams, "ballpoint ink" blue accent, pencil gray for construction
  marks, red pen only for mistakes/warnings.
- Fonts: Besley (headings), Atkinson Hyperlegible (body), Kalam (handwritten
  annotations). Google Fonts with real fallbacks; pages must print well.
- Keep this identical across all lessons and references.
