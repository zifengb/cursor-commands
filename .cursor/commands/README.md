# Cursor Commands

This directory contains custom slash commands for Cursor IDE. These commands
provide AI-driven shortcuts for common development tasks.

## Available Commands

### Code Quality & Maintenance

- `lint-fix.md` - Automatically lint and fix code formatting issues
- `refactor-code.md` - Refactor code for better quality and maintainability
- `code-review.md` - Perform comprehensive code review with suggestions
- `optimize-performance.md` - Analyze and optimize code performance
- `add-error-handling.md` - Implement comprehensive error handling

### Development & Debugging

- `fix-compile-errors.md` - Analyze and fix compilation errors
- `debug-issue.md` - Systematic debugging assistance
- `write-unit-tests.md` - Generate comprehensive unit tests
- `fix-git-issues.md` - Resolve Git conflicts and repository issues

### Documentation & Process

- `add-documentation.md` - Generate comprehensive documentation
- `generate-pr-description.md` - Create detailed pull request descriptions
- `generate-api-docs.md` - Create comprehensive API documentation

### Security & Accessibility

- `security-review.md` - Perform comprehensive security audit
- `accessibility-audit.md` - Review and improve accessibility compliance

### Database & Infrastructure

- `database-migration.md` - Create and manage database migrations

## How to Use

1. Type `/` in Cursor's AI chat or agent input
2. Select from the available commands
3. The AI will execute the prompt with context from your current code

## Creating Custom Commands

1. Create a new `.md` file in this directory
2. Write a clear, specific prompt describing the task
3. Include context about expected inputs and outputs
4. Use descriptive filenames that match the command purpose

## Best Practices

- **Be Specific**: Write detailed prompts that clearly describe the expected
  outcome
- **Provide Context**: Include information about coding standards, frameworks,
  and project conventions
- **Include Examples**: Show expected input/output formats where helpful
- **Stay Focused**: Each command should have a single, clear purpose
- **Use Descriptive Names**: Command filenames should clearly indicate their
  function

## Command Template

```markdown
# Command Title

Brief description of what this command does.

## Objective
Detailed explanation of the task and expected outcome.

## Requirements
- Specific requirements or constraints
- Coding standards to follow
- Expected formats or structures

## Output
Description of what the AI should produce.
```
