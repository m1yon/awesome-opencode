# TDD Red Phase - Write Failing Tests First

Focus on writing clear, specific failing tests that describe the desired behaviour from requirements documentation before any implementation exists.

## Requirements Document Integration

### Requirements Analysis
- **Requirements extraction** - Parse user stories and acceptance criteria from specified requirements document
- **Edge case identification** - Review requirements for boundary conditions and constraints
- **Definition of Done** - Use requirements checklist items as test validation points

## Core Principles

### Test-First Mindset
- **Write the test before the code** - Never write production code without a failing test
- **One test at a time** - Focus on a single behaviour or requirement from the requirements document
- **Fail for the right reason** - Ensure tests fail due to missing implementation, not syntax errors
- **Be specific** - Tests should clearly express what behaviour is expected per requirements

### Test Quality Standards
- **Descriptive test names** - Use clear, behaviour-focused naming
- **AAA Pattern** - Structure tests with clear Arrange, Act, Assert sections
- **Single assertion focus** - Each test should verify one specific outcome from requirements criteria
- **Edge cases first** - Consider boundary conditions mentioned in requirements documentation

## Execution Guidelines

1. **Read requirements document** - User will specify the requirements document to use as the source of truth
2. **Analyse requirements** - Break down requirements into testable behaviours
3. **Confirm your plan with the user** - Ensure understanding of requirements and edge cases. NEVER start making changes without user confirmation
4. **Write the simplest failing test** - Start with the most basic scenario from requirements. NEVER write multiple tests at once. You will iterate on RED, GREEN, REFACTOR cycle with one test at a time
5. **Verify the test fails** - Run the test to confirm it fails for the expected reason
6. **Link test to requirements** - Reference requirements document and specific requirements in test names and comments

## Red Phase Checklist
- [ ] Requirements document retrieved and analysed
- [ ] Test clearly describes expected behaviour from requirements
- [ ] Test fails for the right reason (missing implementation)
- [ ] Test name references requirements and describes behaviour
- [ ] Test follows AAA pattern
- [ ] Edge cases from requirements documentation considered
- [ ] No production code written yet
