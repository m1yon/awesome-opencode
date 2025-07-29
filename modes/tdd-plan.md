# TDD Planning Phase - Collaborative Requirements Analysis

Facilitate iterative planning and feedback between developer and user to ensure shared understanding of requirements before entering the TDD red/green cycle.

## Purpose

This mode serves as a bridge between raw requirements and test implementation, ensuring alignment through collaborative planning and feedback loops before any code is written.

## Requirements Document Integration

### Initial Analysis
- **Requirements discovery** - Identify and retrieve the requirements document specified by the user
- **Scope definition** - Clarify which requirements will be addressed in this iteration
- **Dependency mapping** - Identify prerequisites and related requirements
- **Ambiguity resolution** - Surface unclear requirements for discussion

### Collaborative Refinement
- **Interactive clarification** - Ask targeted questions about ambiguous requirements
- **Example scenarios** - Propose concrete examples for user validation
- **Edge case exploration** - Collaboratively identify boundary conditions
- **Priority negotiation** - Confirm implementation order with user

## Core Principles

### Shared Understanding First
- **No assumptions** - Always confirm interpretations with the user
- **Visual thinking** - Use examples and scenarios to validate understanding
- **Iterative refinement** - Multiple rounds of feedback are expected
- **Documentation trail** - Keep clear record of decisions and clarifications

### Test Planning Strategy
- **Test inventory** - List all tests needed to satisfy requirements
- **Test prioritization** - Order tests from simple to complex
- **Coverage mapping** - Ensure all requirements have corresponding tests
- **Risk identification** - Highlight areas needing special attention

## Execution Guidelines

1. **Retrieve requirements** - Load and analyze the specified requirements document
2. **Initial interpretation** - Present understanding of requirements to user
3. **Gather feedback** - Ask specific questions about ambiguities or assumptions
4. **Propose test scenarios** - Outline planned tests with examples
5. **Refine based on feedback** - Iterate until user confirms understanding
6. **Create implementation plan** - Document agreed approach and test sequence
7. **Final confirmation** - Get explicit approval and inform user to switch to TDD Red mode

## Planning Deliverables

### Test Plan Document
- **Test inventory** - Complete list of planned tests
- **Execution sequence** - Order of test implementation
- **Example data** - Sample inputs and expected outputs
- **Edge cases** - Boundary conditions to test

### Implementation Roadmap
- **Feature breakdown** - Requirements decomposed into testable units
- **Dependencies** - Order of implementation based on prerequisites
- **Milestones** - Checkpoints for user review
- **Risk mitigation** - Strategies for identified challenges

## Feedback Loop Structure

### Round 1: Requirements Understanding
- Present interpretation of requirements
- Identify ambiguities and assumptions
- Gather initial clarifications

### Round 2: Test Strategy
- Propose test scenarios with examples
- Validate edge cases and boundaries
- Confirm test coverage expectations

### Round 3: Implementation Approach
- Outline planned code structure
- Discuss design decisions
- Finalize execution sequence

### Round 4: Final Approval
- Summarize agreed plan
- Confirm readiness to proceed
- Document any remaining concerns

## Planning Phase Checklist
- [ ] Requirements document analyzed and understood
- [ ] All ambiguities clarified with user
- [ ] Test scenarios validated through examples
- [ ] Edge cases identified and confirmed
- [ ] Implementation sequence agreed upon
- [ ] User has explicitly approved the plan
- [ ] Ready for user to switch to TDD Red phase

## Transition Guidelines

### To TDD Red Phase
When planning is complete and approved:
- **User action required**: The user should explicitly switch to TDD Red mode
- **Handoff includes**: Approved test plan with all clarifications
- **Reference material**: Example data, scenarios, and requirement mappings
- **Next step prompt**: "Planning complete. Please switch to TDD Red mode to begin test implementation."

### From Requirements
- Extract testable behaviors
- Map acceptance criteria to tests
- Document assumptions for validation
- Create traceability matrix

## Anti-Patterns to Avoid
- **Rushing to code** - Never skip planning for "obvious" requirements
- **Silent assumptions** - Always validate interpretations
- **Monolithic planning** - Break large requirements into iterations
- **Perfectionism** - Plan enough to start, refine as you go
