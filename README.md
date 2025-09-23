# Cursor Commands

Reusable slash-command prompts for the Cursor Agent so teams can standardize common workflows.

## How commands work

Commands are defined as plain Markdown files that can be stored in two locations:

- Project commands: Stored in the `.cursor/commands` directory of your project
- Global commands: Stored in the `~/.cursor/commands` directory in your home directory

When you type `/` in the chat input box, Cursor will automatically detect and display available commands from both directories, making them instantly accessible across your workflow.

## Creating commands

- Create a `.cursor/commands` directory in your project root
- Add `.md` files with descriptive names (e.g., `review-code.md`, `write-tests.md`)
- Write plain Markdown content describing what the command should do
- Commands will automatically appear in the chat when you type `/`

Here's an example of how your commands directory structure might look:

```text
.cursor/
└── commands/
    ├── address-github-pr-comments.md
    ├── code-review.md
    ├── create-pr.md
    ├── light-review-existing-diffs.md
    ├── onboard-new-developer.md
    ├── run-all-tests-and-fix.md
    ├── security-audit.md
    ├── setup-new-feature.md
    └── lint.md
```

## Included examples

- `code-review.md` — End-to-end review flow covering context gathering, quality checks, and security considerations.
- `security-audit.md` — Step-by-step guidance for dependency, code, and infrastructure security reviews.
- `setup-new-feature.md` — Planning workflow for spinning up a new feature end to end.
- `create-pr.md` — Structured outline for preparing and filing a pull request.
- `run-all-tests-and-fix.md` — Process for executing tests, triaging failures, and validating fixes.
- `onboard-new-developer.md` — Onboarding flow and checklist for new teammates.
- `address-github-pr-comments.md`, `light-review-existing-diffs.md`, `lint.md` — Supporting prompts that help close review feedback, surface risks, and maintain code quality.

Each command follows the same structure—**Overview**, **Steps**, and a final checklist—so they read consistently when inserted into Cursor.

Feel free to modify these Markdown files or add new ones—the commands are version-controlled alongside your code, so the whole team benefits from shared workflows.

## License

This project is released under the [MIT License](LICENSE).
