# GitHub Reusable Workflow: Slack Notification

<!-- Row 1: Status - Most Important -->
[![Release](https://github.com/subhamay-bhattacharyya-gha/slack-notification-wf/actions/workflows/release.yaml/badge.svg)](https://github.com/subhamay-bhattacharyya-gha/slack-notification-wf)&nbsp;[![GitHub Action](https://img.shields.io/badge/GitHub-Action-blue?logo=github)](https://github.com/subhamay-bhattacharyya-gha/slack-notification-wf)&nbsp;[![Issues](https://img.shields.io/github/issues/subhamay-bhattacharyya-gha/slack-notification-wf)](https://github.com/subhamay-bhattacharyya-gha/slack-notification-wf/issues)&nbsp;[![Last Commit](https://img.shields.io/github/last-commit/subhamay-bhattacharyya-gha/slack-notification-wf)](https://github.com/subhamay-bhattacharyya-gha/slack-notification-wf//commits)

<!-- Row 2: Code Quality -->
[![Top Language](https://img.shields.io/github/languages/top/subhamay-bhattacharyya-gha/slack-notification-wf)](https://github.com/subhamay-bhattacharyya-gha/slack-notification-wf)&nbsp;[![Commits](https://img.shields.io/github/commit-activity/t/subhamay-bhattacharyya-gha/slack-notification-wf)](https://github.com/subhamay-bhattacharyya-gha/slack-notification-wf/commits)

<!-- Row 3: Tech Stack -->
[![Built with Claude Code](https://img.shields.io/badge/Built_with-Claude_Code-D97757?logo=anthropic&logoColor=white)](https://claude.ai)

<!-- Row 4: Repository Info -->
[![Files](https://img.shields.io/github/directory-file-count/subhamay-bhattacharyya-gha/slack-notification-wf)](https://github.com/subhamay-bhattacharyya-gha/slack-notification-wf)&nbsp;[![Repo Size](https://img.shields.io/github/repo-size/subhamay-bhattacharyya-gha/slack-notification-wf)](https://github.com/subhamay-bhattacharyya-gha/slack-notification-wf/)&nbsp;[![Release Date](https://img.shields.io/github/release-date/subhamay-bhattacharyya-gha/slack-notification-wf)](https://github.com/subhamay-bhattacharyya-gha/slack-notification-wf//releases)

<!-- Row 5: Custom Metrics -->
[![Custom Endpoint](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/bsubhamay/8612993cb0c2464da5255d6018345bd6/raw/slack-notification-wf.json)](https://gist.github.com/bsubhamay/8612993cb0c2464da5255d6018345bd6)

## Slack Notification

## 📋 Description

This GitHub Action sends a message to a Slack channel via webhook when a new GitHub issue or pull request is created. It dynamically formats the message based on the event type.

---

## 🔐 Secrets

| Name            | Description                                  | Required |
|-----------------|----------------------------------------------| -------- |
| `slack-webhook` | Slack incoming webhook URL for notifications | ✅ Yes   |

---

## 🚀 Example Usage

```yaml
name: Notify on Issue or PR

on:
  issues:
    types: [opened]
  pull_request:
    types: [opened]

jobs:
  notify:
    uses: subhamay-bhattacharyya-gha/slack-notification-wf/.github/workflows/slack-notification.yaml@v1
    secrets:
      slack-webhook: ${{ secrets.SLACK_WEBHOOK }}

```

## License

MIT
