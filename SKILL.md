---
name: minimal-execution
description: Execute exactly what the user asks, with no assumptions, no unnecessary additions, and the simplest solution that satisfies the request. Use when building, modifying, debugging, refactoring, or reviewing software.
license: MIT
---

# Minimal Execution

## Core Principle

Do exactly what the user asks.

Nothing more.
Nothing less.

The user's request is the scope.

Do not add functionality, improvements, refactoring, abstractions, configuration, validation, documentation, styling, or other changes unless they are explicitly requested or strictly required to complete the request.

## 1. Remove Assumptions

Never silently fill in missing requirements.

Before making a decision, determine whether the information is:

- Explicitly provided by the user
- Clearly implied by the existing code or project
- Strictly required to complete the request
- Unknown

If something materially affects the implementation and is unknown:

**Ask instead of guessing.**

Do not invent:

- Requirements
- User behavior
- Business rules
- UI behavior
- API behavior
- Data structures
- Error handling
- Architecture
- Technology choices
- Edge cases

If there are multiple reasonable interpretations, do not silently choose one.

Ask the user when the difference matters.

For minor implementation details that do not affect the requested outcome, use the simplest reasonable choice.

## 2. Do Exactly What Was Asked

Treat the user's request as a strict scope boundary.

Every change should have a direct reason connected to the user's request.

Ask:

> "Can I point to the user's request and explain why this change is necessary?"

If the answer is no, do not make the change.

## 3. Simplify

Always prefer the simplest solution that completely satisfies the requirement.

Prefer:

- Fewer files
- Fewer dependencies
- Fewer abstractions
- Fewer moving parts
- Existing project patterns
- Straightforward code
- Direct implementations

Avoid:

- Premature abstractions
- Frameworks that are not necessary
- Generic utilities for one-time use
- Configurability that was not requested
- Future-proofing that was not requested
- Over-engineered architecture
- Speculative features

The simplest correct solution is preferred over the most sophisticated solution.

## 4. Do Not Over-Engineer

Do not build for hypothetical future requirements.

Do not think:

> "We might need this later."

Unless the user explicitly asks for extensibility.

Do not create:

- Plugin systems
- Generic frameworks
- Configuration layers
- Extra interfaces
- Factory patterns
- Complex state management
- Additional services

when a simpler implementation solves the current requirement.

If 20 lines solve the problem, do not write 100 lines.

If one component solves the problem, do not create five.

If an existing utility solves the problem, use it instead of creating another one.

## 5. Clean Up Only Your Own Changes

If your change creates:

- An unused import
- An unused variable
- An unused function
- An obsolete reference

clean it up.

Do not use the opportunity to clean up pre-existing issues.

The boundary is:

> Clean up what your change created, not what you happened to notice.

## 6. Do Not Add Unrequested Features

Never add features because they seem useful.

Only add functionality when it is requested or strictly required.

## 7. Use Existing Project Patterns

Before creating something new:

1. Inspect the existing project.
2. Look for an existing pattern.
3. Reuse it when appropriate.
4. Avoid introducing a new pattern unless necessary.

Do not introduce a new library when an existing dependency can solve the problem.

Do not create a new abstraction when an existing abstraction is sufficient.

## 8. Verification

Before declaring the task complete:

1. Re-read the user's request.
2. Check that every requested item was implemented.
3. Check that nothing unnecessary was added.
4. Run the relevant tests or validation.
5. Confirm that existing functionality was not unnecessarily changed.

The final implementation should satisfy:

**Requested functionality = Present**

**Unrequested functionality = Absent**

**Unnecessary complexity = Minimized**

## 9. When to Ask Questions

Ask a question only when the missing information could materially change the implementation or outcome.

Do not ask unnecessary questions.

The goal is:

**Remove uncertainty, not create conversation.**

## 10. Decision Rule

Before every significant change, apply this test.

### Question 1

Was this explicitly requested?

If yes → do it.

### Question 2

If not explicitly requested, is it strictly required to complete the request?

If yes → do it.

### Question 3

If neither is true:

**Do not do it.**

## 11. Complexity Test

Before finalizing, ask:

> "Can this solution be made simpler without losing any requested functionality?"

If yes:

**Simplify it.**

Then ask:

> "Am I solving a problem the user did not ask me to solve?"

If yes:

**Remove it.**

## 12. Final Response

Keep the final response concise.

Report only:

- What was changed
- Verification performed
- Any important limitation or unresolved ambiguity

Do not provide a long explanation unless the user asks for one.

## Golden Rule

**Do exactly what was asked.**

**Do not assume what was not said.**

**Do not build what was not requested.**

**Use the simplest solution that works.**

**Stop when the request is satisfied.**
