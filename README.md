# Cursor Commands

A collection of custom slash commands for Cursor IDE that provide AI-driven shortcuts for common development workflows. These commands enable consistent, shareable, and version-controlled AI prompts across your development team.

## What are Cursor Commands?

Cursor Commands are reusable AI prompts saved as `.md` files in the `.cursor/commands/` directory. When you type `/` in Cursor's AI chat, these commands appear as options for quick execution. They act as AI-driven shortcuts that can automate repetitive development tasks, maintain coding standards, and streamline workflows.

## Features

- **🚀 Quick Access**: Type `/` to instantly access all commands
- **🔄 Reusable**: Save time with consistent, reusable prompts
- **👥 Team Sharing**: Version-controlled commands shared across teams
- **🎯 Focused Tasks**: Each command targets a specific development task
- **📝 Customizable**: Easy to create and modify for your specific needs

## Available Commands

### Code Quality & Maintenance
- **`lint-fix`** - Automatically analyze and fix linting issues
- **`refactor-code`** - Improve code quality while maintaining functionality
- **`code-review`** - Perform comprehensive code review with suggestions

### Development & Debugging
- **`fix-compile-errors`** - Analyze and resolve compilation errors
- **`debug-issue`** - Systematic debugging assistance with step-by-step guidance
- **`write-unit-tests`** - Generate comprehensive unit tests with proper coverage

### Documentation & Process
- **`add-documentation`** - Create comprehensive documentation for code/features
- **`generate-pr-description`** - Generate detailed pull request descriptions

## Quick Start

1. **Clone this repository** or copy the `.cursor/commands/` directory to your project
2. **Open your project in Cursor IDE**
3. **Type `/` in the AI chat** to see available commands
4. **Select a command** and let the AI execute the prompt with your code context

## Installation

### Option 1: Clone this repository
```bash
git clone https://github.com/hamzafer/cursor-commands.git
cd cursor-commands
```

### Option 2: Copy to existing project
```bash
# Copy the .cursor directory to your project root
cp -r cursor-commands/.cursor /path/to/your/project/
```

### Option 3: Manual setup
1. Create a `.cursor/commands/` directory in your project root
2. Copy the `.md` files from this repository's `.cursor/commands/` directory

## Creating Custom Commands

### 1. Create a new command file
```bash
touch .cursor/commands/my-custom-command.md
```

### 2. Write your prompt
```markdown
# My Custom Command

Brief description of what this command does.

## Objective
Detailed explanation of the task and expected outcome.

## Requirements
- Specific requirements or constraints
- Coding standards to follow
- Expected formats or structures

Provide clear instructions for the AI to follow.
```

### 3. Use your command
Type `/` in Cursor and select your new command!

## Command Examples

### Example 1: API Documentation Generator
```markdown
# Generate API Documentation

Create comprehensive API documentation for the current code. Include:

- Endpoint descriptions and HTTP methods
- Request/response schemas with examples
- Authentication requirements
- Error codes and responses
- Rate limiting information

Format as OpenAPI/Swagger specification.
```

### Example 2: Security Audit
```markdown
# Security Audit

Perform a security audit of the current code. Check for:

- SQL injection vulnerabilities
- XSS attack vectors
- Authentication and authorization issues
- Input validation problems
- Sensitive data exposure

Provide specific remediation steps for each issue found.
```

## Best Practices

### Writing Effective Commands
- **Be Specific**: Clearly describe the expected outcome
- **Provide Context**: Include project conventions and standards
- **Set Boundaries**: Define scope and limitations
- **Include Examples**: Show expected formats when helpful

### Organization
- **Use Descriptive Names**: Filenames should clearly indicate purpose
- **Group Related Commands**: Consider subdirectories for large collections
- **Document Commands**: Include README files explaining command purposes

### Team Collaboration
- **Version Control**: Commit commands to share across team
- **Review Process**: Review command changes like code changes
- **Standardization**: Establish team conventions for command structure

## Common Use Cases

- **Code Quality**: Automated linting, formatting, and refactoring
- **Testing**: Generate unit tests, integration tests, and test data
- **Documentation**: API docs, README updates, code comments
- **Debugging**: Systematic debugging assistance and error analysis
- **Deployment**: Generate deployment scripts and configurations
- **Security**: Security audits and vulnerability assessments

## Contributing

1. Fork this repository
2. Create a new command file in `.cursor/commands/`
3. Follow the command template and best practices
4. Submit a pull request with your new command

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

- Create an [issue](https://github.com/hamzafer/cursor-commands/issues) for bug reports or feature requests
- Check the [`.cursor/commands/README.md`](.cursor/commands/README.md) for detailed command documentation