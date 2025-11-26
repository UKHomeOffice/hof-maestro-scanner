# hof-maestro-scanner

This is a workflow automation repository designed to trigger workflows in other GitHub repositories. It uses GitHub Actions to dispatch events to remote repositories, enabling automated and scheduled processes across multiple projects.

## How It Works

- **Manual Trigger:** You can manually trigger this workflow using the GitHub Actions UI (`workflow_dispatch`).
- **Remote Actions:** When triggered, this workflow sends repository dispatch events to the following repositories e.g these are some of the repos:
  - `UKHomeOffice/AppealRightsExhausted`
  - `UKHomeOffice/modern-slavery`

These events have been used by the target repositories to start their own workflows in response.  The workflow is to run a scan for vulnerabilities using https://github.com/UKHomeOfficeForms/hof-vulnerabilities-scanner

## Example

When the workflow runs, it triggers the `trigger-from-scanmaestro` event in the target repositories, which can be used to start any workflow defined there.

