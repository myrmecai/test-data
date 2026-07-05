# Java Coding Guidelines

## Naming
- Use camelCase for variables and methods, PascalCase for classes.
- Constants in UPPER_SNAKE_CASE.

## Structure
- One class per file. Package declaration first, then imports.
- Prefer composition over inheritance.
- Keep methods under 30 lines. Extract helpers for complex logic.

## Error Handling
- Never swallow exceptions. Log or rethrow.
- Use custom exception types for domain errors.
- Validate inputs at the boundary (controller), not in services.

## Testing
- Write JUnit 5 tests for all service methods.
- Use AssertJ for fluent assertions.
- Test names: `methodName_scenario_expectedResult`.