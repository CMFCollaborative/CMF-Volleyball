# CLAUDE.md - AI Assistant Guide for CMF-Volleyball

## Project Overview

**Project Name**: CMF-Volleyball
**Organization**: CMFCollaborative
**Repository Status**: 🚧 Initial Development Phase
**Last Updated**: November 23, 2025

This is a newly initialized repository for a volleyball-related project under the CMF (Collaborative Media Framework) umbrella. The codebase is in its early stages and will be built out incrementally.

## Repository Structure

```
CMF-Volleyball/
├── .github/
│   └── copilot-instructions.md    # GitHub Copilot AI instructions
├── .git/                          # Git repository data
├── instructions.md                # Repository setup instructions
└── CLAUDE.md                      # This file - Claude AI assistant guide
```

### Current State
- **Empty codebase**: No application code exists yet
- **Technology stack**: To be determined
- **Architecture**: To be defined
- **Dependencies**: None currently

## Development Workflow for AI Assistants

### Git Branching Strategy

**CRITICAL**: This repository uses a specific branching strategy for AI-assisted development:

- **Feature branches**: Must follow pattern `claude/claude-md-<session-id>-<unique-id>`
- **Example branch**: `claude/claude-md-<session-id>-<unique-id>`
- **Push requirements**: Always use `git push -u origin <branch-name>`
- **Important**: Branches MUST start with `claude/` and end with matching session ID, or push will fail with 403 error

### Git Operations Best Practices

**Pushing Changes:**
```bash
# Always use the -u flag for first push
git push -u origin claude/claude-md-<session-id>-<unique-id>

# If network errors occur, retry up to 4 times with exponential backoff:
# - First retry: wait 2 seconds
# - Second retry: wait 4 seconds
# - Third retry: wait 8 seconds
# - Fourth retry: wait 16 seconds
```

**Fetching/Pulling:**
```bash
# Prefer fetching specific branches
git fetch origin <branch-name>

# For pulls
git pull origin <branch-name>

# Apply same retry logic on network failures
```

### Commit Guidelines

1. **Descriptive messages**: Use clear, concise commit messages that explain the "why"
2. **Atomic commits**: Keep commits focused on single logical changes
3. **No destructive operations**: Avoid force push, hard reset unless explicitly requested
4. **Hook compliance**: Respect pre-commit hooks; never use --no-verify without permission
5. **Safe amendments**: Only amend commits that haven't been pushed

### Development Principles

1. **Read before modifying**: Always read existing code before making changes
2. **Avoid over-engineering**: Keep solutions simple and focused on requirements
3. **No unnecessary changes**: Don't refactor, add features, or make improvements beyond what's requested
4. **Security-first**: Watch for OWASP Top 10 vulnerabilities (SQL injection, XSS, command injection, etc.)
5. **Minimal abstractions**: Don't create helpers or utilities for one-time operations

## Task Management

When working on this project:

1. **Use TodoWrite tool** for multi-step tasks (3+ steps or non-trivial complexity)
2. **Track progress actively**: Mark tasks as in_progress, completed in real-time
3. **One task at a time**: Limit to ONE in_progress task at any moment
4. **Complete fully**: Only mark tasks complete when fully accomplished (tests pass, no errors)

### When to Skip TodoWrite
- Single, straightforward tasks
- Trivial operations (< 3 simple steps)
- Purely informational/conversational requests

## Code Quality Standards

### Security Considerations
- Validate all external inputs (user input, API responses)
- Use parameterized queries for database operations
- Sanitize data before rendering in web contexts
- Implement proper authentication and authorization
- Keep dependencies updated and scan for vulnerabilities

### Code Style (To Be Established)
As the codebase develops, document:
- Language-specific conventions
- File naming patterns
- Code organization principles
- Testing requirements
- Documentation standards

## Technology Stack

🚧 **To Be Determined** - Update this section as technology choices are made:

### Planned Technologies
- [ ] Programming language(s)
- [ ] Framework(s)
- [ ] Database system
- [ ] Testing framework
- [ ] Build tools
- [ ] Deployment platform

### Dependencies
- [ ] Core dependencies
- [ ] Development dependencies
- [ ] Testing dependencies

## Architecture & Design Patterns

🚧 **To Be Defined** - Document as architecture emerges:

### Application Structure
- Entry points
- Module organization
- Component boundaries
- Data flow patterns

### Design Decisions
- Architectural patterns (MVC, microservices, etc.)
- State management approach
- API design principles
- Database schema design

## Key Workflows

### Development Environment Setup
```bash
# To be documented once project structure is established
```

### Running the Application
```bash
# To be documented
```

### Testing
```bash
# To be documented
```

### Building for Production
```bash
# To be documented
```

## Integration Points

🚧 **To Be Documented** as integrations are added:

### External Services
- APIs and services
- Authentication providers
- Third-party libraries

### Internal Services
- Service boundaries
- Communication patterns
- Data contracts

## Project-Specific Conventions

### File Organization
Document conventions as established:
- Directory structure rationale
- File naming patterns
- Module separation logic

### Naming Conventions
- Variables: TBD
- Functions/Methods: TBD
- Classes/Components: TBD
- Files/Directories: TBD

### Documentation Requirements
- Code comments: When and what to document
- README files: Standards for module documentation
- API documentation: Format and tooling

## Common Tasks & Commands

### Git Operations
```bash
# Check current branch
git status

# Create and switch to new branch
git checkout -b claude/claude-md-<session-id>-<unique-id>

# Stage changes
git add <files>

# Commit with descriptive message
git commit -m "Description of changes and why"

# Push to remote
git push -u origin <branch-name>
```

### Future Common Commands
Add here as the project develops:
- Installation commands
- Development server commands
- Test execution
- Linting/formatting
- Database migrations
- Deployment commands

## Debugging & Troubleshooting

### Common Issues
Document as encountered:
- Setup problems and solutions
- Common error messages and fixes
- Performance bottlenecks and optimizations

### Debug Tools
List debugging tools and techniques as established

## Resources & References

### Documentation
- [ ] Add links to external documentation
- [ ] Framework documentation
- [ ] API references
- [ ] Design documents

### Related Files
- `.github/copilot-instructions.md` - GitHub Copilot-specific guidance
- `instructions.md` - Repository setup instructions

## Notes for AI Assistants

### General Guidance
1. **Check this file first** before making assumptions about the project
2. **Update this file** when project conventions or structure change
3. **Ask for clarification** when requirements are ambiguous
4. **Prefer existing patterns** over introducing new ones
5. **Document decisions** that future AI assistants should know

### GitHub CLI Note
The `gh` CLI is not available in this environment. If GitHub issue/PR information is needed, ask the user to provide it directly.

### Testing Philosophy
As testing practices are established:
- Testing levels (unit, integration, e2e)
- Coverage requirements
- Test file organization
- Mock/stub patterns

### Error Handling Patterns
Document as patterns emerge:
- Error logging approaches
- User-facing error messages
- Recovery strategies
- Monitoring and alerting

## Maintenance

### Keeping CLAUDE.md Updated

This file should be updated when:
- ✅ Technology stack decisions are made
- ✅ Architecture patterns are established
- ✅ New conventions are adopted
- ✅ Key workflows are defined
- ✅ Integration points are added
- ✅ Common issues and solutions are discovered

### Review Cycle
Recommend reviewing and updating this file:
- After major feature additions
- When onboarding patterns change
- Following architecture refactors
- Quarterly as a best practice

---

**Version**: 1.0.0
**Created**: November 23, 2025
**Status**: Living document - update as project evolves
