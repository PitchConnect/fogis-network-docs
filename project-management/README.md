# Project Management Guide

This guide outlines the standardized approach to project management across all PitchConnect repositories. Following these guidelines ensures consistency, improves visibility, and enhances collaboration.

## Table of Contents

- [Project Boards](#project-boards)
- [Issue Management](#issue-management)
- [Pull Request Workflow](#pull-request-workflow)
- [Tagging Strategy](#tagging-strategy)
- [Automation](#automation)
- [Regular Reviews](#regular-reviews)

## Project Boards

We use GitHub Project Boards to track work across all repositories. The main organization-level project board is [PitchConnect Development Roadmap](https://github.com/orgs/PitchConnect/projects/1).

### Board Structure

Our project boards use the following columns:

1. **Backlog**: Issues that are not yet scheduled
2. **Todo**: Issues scheduled for the current iteration
3. **In Progress**: Issues actively being worked on
4. **Review**: Issues with open pull requests awaiting review
5. **Done**: Completed issues

### Custom Fields

We use the following custom fields to provide additional context:

1. **Repository**: Which repository the issue belongs to
2. **Priority**: How urgent the issue is (High, Medium, Low)
3. **Complexity**: How complex the issue is (High, Medium, Low)
4. **Iteration**: Which sprint or iteration the issue is scheduled for

## Issue Management

### Creating Issues

- Use descriptive titles that clearly state the problem or feature
- Include detailed descriptions with context and requirements
- Add appropriate labels (see [Tagging Strategy](#tagging-strategy))
- Reference related issues or PRs
- **Always include a reference to CONTRIBUTING.md** in new issues
  - Add a note like: "Please follow the guidelines in [CONTRIBUTING.md](../CONTRIBUTING.md) when working on this issue"

### Issue Templates

We provide standard issue templates for:

- Feature requests
- Bug reports
- Documentation updates
- Refactoring tasks

These templates include prompts for all required information and reminders about tagging.

### Task Tracking

- Use task lists with checkboxes `- [ ]` for tracking progress
- Update these checkboxes as you complete tasks
- If you're an AI assistant, remind users to update task checkboxes

## Pull Request Workflow

### Creating Pull Requests

- Reference the issue number in the PR title (e.g., "Fix login bug (#42)")
- Use the PR template to provide all necessary information
- Request reviews from appropriate team members
- Add appropriate labels

### Review Process

- At least one approval is required before merging
- Address all review comments
- Ensure CI checks pass
- Update the project board status when ready to merge

## Tagging Strategy

Consistent tagging is essential for effective project management. Use the following tags:

### Work Type Labels

- `feature`: New functionality
- `bugfix`: Fixing issues
- `refactor`: Code improvements without changing functionality
- `docs`: Documentation updates
- `test`: Adding or improving tests
- `chore`: Maintenance tasks

### Priority Labels

- `priority:high`: Urgent items that need immediate attention
- `priority:medium`: Important but not urgent
- `priority:low`: Nice to have

### Status Labels

- `status:blocked`: Blocked by another issue or external factor
- `status:needs-review`: Ready for code review
- `status:needs-testing`: Needs additional testing

### Other Labels

- `good-first-issue`: Good for newcomers
- `help-wanted`: Extra attention is needed
- `discussion`: Requires further discussion
- `wontfix`: This will not be worked on

## Automation

We use GitHub Actions to automate project management tasks:

### Automatic Project Board Updates

- New issues are automatically added to the project board
- PRs automatically move issues to "Review" status
- Merged PRs automatically move issues to "Done" status

### Issue Management Automation

- Stale issues are automatically labeled after 30 days of inactivity
- Issues with PRs are automatically labeled with "has-pr"
- New contributors get automatic welcome messages

## Regular Reviews

We conduct regular project management reviews:

- **Weekly**: Quick triage of new issues
- **Bi-weekly**: Project board review and cleanup
- **Monthly**: Comprehensive review of all open issues

During these reviews, we:
- Update priorities
- Adjust estimates
- Close stale issues
- Ensure proper tagging
- Plan for upcoming work

## References

- [GitHub Project Documentation](https://docs.github.com/en/issues/planning-and-tracking-with-projects)
- [GitHub CLI Project Commands](../github-cli/project-boards.md)
- [Contribution Guidelines](https://github.com/PitchConnect/contribution-guidelines)
