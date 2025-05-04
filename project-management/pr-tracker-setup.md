# Organization Pull Request Tracker

This document provides instructions for setting up and using the Organization Pull Request Tracker project board.

## Project Board URL

The Organization Pull Request Tracker is available at:
https://github.com/orgs/PitchConnect/projects/3

## Recommended Views

After the project board is populated with pull requests, you can create the following custom views:

### 1. All Open PRs

This view shows all open pull requests across the organization:

1. Click "New view" in the project
2. Name it "All Open PRs"
3. Select "Table" layout
4. Add filter: "PR Status" is "Open" or "Needs Review" or "Changes Requested" or "Approved" or "Draft"
5. Group by: "Repository"
6. Sort by: "Updated" (newest first)

### 2. Needs Review

This view shows PRs that need review:

1. Click "New view" in the project
2. Name it "Needs Review"
3. Select "Board" layout
4. Add filter: "PR Status" is "Needs Review"
5. Group by: "Repository"

### 3. My PRs

This view shows PRs created by you:

1. Click "New view" in the project
2. Name it "My PRs"
3. Select "Table" layout
4. Add filter: "Creator" is "@me"
5. Group by: "PR Status"

### 4. Recently Updated

This view shows recently updated PRs:

1. Click "New view" in the project
2. Name it "Recently Updated"
3. Select "Table" layout
4. Sort by: "Updated" (newest first)
5. No grouping

## Automation

The PR Tracker is automatically updated through GitHub Actions:

1. New PRs are automatically added to the project
2. PR status is automatically updated based on PR events:
   - When a PR is opened: Status → "Open"
   - When a PR is converted to draft: Status → "Draft"
   - When a PR is ready for review: Status → "Needs Review"
   - When a PR is merged: Status → "Merged"
   - When a PR is closed without merging: Status → "Closed"

## Manual Updates

You can manually update the following fields as needed:

- **PR Status**: Update to "Changes Requested" or "Approved" based on reviews
- **Labels**: Add relevant labels to categorize PRs
- **Assignees**: Assign PRs to specific team members

## Adding Existing PRs

To add existing PRs to the project board:

1. Go to the PR in GitHub
2. Click the "Projects" section on the right sidebar
3. Select "Organization Pull Request Tracker" from the dropdown
4. The PR will be added to the project with the appropriate status

## Troubleshooting

If a PR is not automatically added to the project:

1. Check if the GitHub Actions workflow ran successfully
2. Try adding the PR manually as described above
3. If issues persist, check the GitHub Actions logs for errors
