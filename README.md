# Spec-Kit Expanded: GitHub's Foundation, Amazon Q's Power

This project is a port of the excellent [GitHub Spec-Kit](https://github.com/github/spec-kit) to work with Amazon Q Developer and GitHub Copilot in your IDE.

## About

Spec-Kit provides a structured workflow for software development using AI agents. This port adapts the original GitHub Actions prompts to work seamlessly with Amazon Q's prompt system.

## Quick Start

1. **Install prompts:**

   ```bash
   # For Amazon Q
   mkdir -p ~/.aws/amazonq/prompts && cp prompts/*.md ~/.aws/amazonq/prompts/

   # For GitHub Copilot
   mkdir -p ~/.github/prompts && cp prompts/*.md ~/.github/prompts/
   ```

2. **Start developing:**
   ```
   @specify Add user authentication system
   @plan
   @tasks
   @implement
   ```

## Example Workflow

**Standard Workflow:**

```
@specify Add JWT-based user authentication with login/logout
@plan
@tasks
@implement
```

**Enhanced with Reference File:**

```
# 1. Create detailed requirements file with:
#    - Primary User Story
#    - Acceptance Scenarios
#    - Edge Cases
#    - Functional Requirements
#    - Key Entities
# Save as: .specify/reference/auth-requirements.md

# 2. Create specification (automatically loads reference file)
@specify Add user authentication ***using auth-requirements.md***

# 3. Generate plan (integrates reference file entities & requirements)
@plan

# 4. Create tasks (includes reference file edge cases & scenarios)
@tasks

# 5. Execute implementation
@implement
```

This generates design documents, creates a task list, and implements the feature following your project's constitutional principles. Reference files in `.specify/reference/` can provide additional context for the entire workflow.

## Reference Files

Place detailed requirements in `.specify/reference/[filename].md` to enhance your entire workflow:

- **Specifications** - Predefined user stories, acceptance criteria, edge cases
- **Planning** - Technical constraints, functional requirements inform design decisions
- **Tasks** - Additional test scenarios and implementation requirements

Reference files are automatically integrated when mentioned in your `@specify` command.

## Available Prompts

- `@audit` - Generate compliance audit and TODO list
- `@constitution` - Update project constitution with versioning
- `@specify` - Create feature specifications from descriptions (optionally using reference files)
- `@plan` - Generate implementation plans and design artifacts
- `@tasks` - Create dependency-ordered task breakdowns
- `@implement` - Execute implementation following task plan

## Documentation

- [Installation Guide](./INSTALL.md)
- [Usage Guide](./AMAZONQ_PROMPTS_HOWTO.md)
- [Prompt Summary](./AMAZONQ_PROMPTS_SUMMARY.md)

## Credits

This work is based on the original [Spec-Kit](https://github.com/github/spec-kit) by GitHub. All credit for the methodology and workflow design goes to the original authors.

## License

Same as original Spec-Kit project.
