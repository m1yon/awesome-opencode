# TDD Green Phase - Make Tests Pass Quickly

Write the minimal code necessary to satisfy requirements document specifications and make failing tests pass. Resist the urge to write more than required.

## Requirements Document Integration

### Requirements-Driven Implementation
- **Reference requirements context** - Keep requirements document specifications in focus during implementation
- **Validate against acceptance criteria** - Ensure implementation meets requirements definition of done
- **Track progress** - Document implementation progress and blockers
- **Stay in scope** - Implement only what's required by current requirements, avoid scope creep

### Implementation Boundaries
- **Requirements scope only** - Don't implement features not mentioned in the current requirements
- **Future-proofing later** - Defer enhancements mentioned in requirements for future iterations
- **Minimum viable solution** - Focus on core requirements from specification

## Core Principles

### Minimal Implementation
- **Just enough code** - Implement only what's needed to satisfy requirements and make tests pass
- **Fake it till you make it** - Start with hard-coded returns based on requirements examples, then generalise
- **Obvious implementation** - When the solution is clear from requirements, implement it directly
- **Triangulation** - Add more tests based on requirements scenarios to force generalisation

### Speed Over Perfection
- **Green bar quickly** - Prioritise making tests pass over code quality
- **Ignore code smells temporarily** - Duplication and poor design will be addressed in refactor phase
- **Simple solutions first** - Choose the most straightforward implementation path from requirements context
- **Defer complexity** - Don't anticipate requirements beyond current specification scope

## Execution Guidelines

1. **Review requirements document** - Confirm implementation aligns with requirements document acceptance criteria
2. **Run the failing test** - Confirm exactly what needs to be implemented
3. **Confirm your plan with the user** - Ensure understanding of requirements and edge cases. NEVER start making changes without user confirmation
4. **Write minimal code** - Add just enough to satisfy requirements and make test pass
5. **Run all tests** - Ensure new code doesn't break existing functionality
6. **Do not modify the test** - Ideally the test should not need to change in the Green phase.
7. **Document progress** - Update implementation status as needed

## Green Phase Checklist
- [ ] Implementation aligns with requirements document specifications
- [ ] All tests are passing (green bar)
- [ ] No more code written than necessary for requirements scope
- [ ] Existing tests remain unbroken
- [ ] Implementation is simple and direct
- [ ] Requirements acceptance criteria satisfied
- [ ] Ready for refactoring phase
