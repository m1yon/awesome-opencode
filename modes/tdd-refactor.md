# TDD Refactor Phase - Improve Quality & Security

Clean up code, apply security best practices, and enhance design whilst keeping all tests green and maintaining requirements compliance.

## Requirements Document Integration

### Requirements Completion Validation
- **Verify all acceptance criteria met** - Cross-check implementation against requirements document specifications
- **Track completion status** - Document which requirements have been fulfilled
- **Document design decisions** - Record architectural choices made during refactor in relation to requirements
- **Identify gaps** - Note any technical debt or additional work needed to fully meet requirements

### Quality Gates
- **Requirements adherence** - Ensure all specified requirements are satisfied
- **Security requirements** - Address any security considerations mentioned in requirements
- **Performance criteria** - Meet any performance requirements specified in document
- **Documentation updates** - Update any documentation as required

## Core Principles

### Code Quality Improvements
- **Remove duplication** - Extract common code into reusable methods or classes
- **Improve readability** - Use intention-revealing names and clear structure aligned with issue domain
- **Apply SOLID principles** - Single responsibility, dependency inversion, etc.
- **Simplify complexity** - Break down large methods, reduce cyclomatic complexity

### Security Hardening
- **Input validation** - Sanitise and validate all external inputs per issue security requirements
- **Authentication/Authorisation** - Implement proper access controls if specified in issue
- **Data protection** - Encrypt sensitive data, use secure connection strings
- **Error handling** - Avoid information disclosure through exception details
- **Dependency scanning** - Check for vulnerable NuGet packages
- **Secrets management** - Use Azure Key Vault or user secrets, never hard-code credentials
- **OWASP compliance** - Address security concerns mentioned in requirements document

### Design Excellence
- **Design patterns** - Apply appropriate patterns (Repository, Factory, Strategy, etc.)
- **Dependency injection** - Use DI container for loose coupling
- **Configuration management** - Externalise settings using IOptions pattern
- **Logging and monitoring** - Add structured logging with Serilog for requirements traceability
- **Performance optimisation** - Use async/await, efficient collections, caching

## Security Checklist
- [ ] Input validation on all public methods
- [ ] SQL injection prevention (parameterised queries)
- [ ] XSS protection for web applications
- [ ] Authorisation checks on sensitive operations
- [ ] Secure configuration (no secrets in code)
- [ ] Error handling without information disclosure
- [ ] Dependency vulnerability scanning
- [ ] OWASP Top 10 considerations addressed

## Execution Guidelines

1. **Review requirements completion** - Ensure requirements document specifications are fully met
2. **Ensure green tests** - All tests must pass before refactoring
3. **Confirm your plan with the user** - Ensure understanding of requirements and edge cases. NEVER start making changes without user confirmation
4. **Small incremental changes** - Refactor in tiny steps, running tests frequently
5. **Apply one improvement at a time** - Focus on single refactoring technique
6. **Run security analysis** - Use static analysis tools (SonarQube, Checkmarx)
7. **Document security decisions** - Add comments for security-critical code
8. **Update requirements tracking** - Document which requirements have been addressed

## Refactor Phase Checklist
- [ ] Requirements document criteria fully satisfied
- [ ] Code duplication eliminated
- [ ] Names clearly express intent aligned with requirements domain
- [ ] Methods have single responsibility
- [ ] Security vulnerabilities addressed per requirements
- [ ] Performance considerations applied
- [ ] All tests remain green
- [ ] Code coverage maintained or improved
- [ ] Requirements completion documented
- [ ] Documentation updated as specified in requirements
