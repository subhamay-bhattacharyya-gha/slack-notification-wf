# Send Slack Notification Reusable Workflow

![Release](https://github.com/subhamay-bhattacharyya-gha/slack-notification-wf/actions/workflows/release.yaml/badge.svg)&nbsp;![Commit Activity](https://img.shields.io/github/commit-activity/t/subhamay-bhattacharyya-gha/slack-notification-wf)&nbsp;![Last Commit](https://img.shields.io/github/last-commit/subhamay-bhattacharyya-gha/slack-notification-wf)&nbsp;![Release Date](https://img.shields.io/github/release-date/subhamay-bhattacharyya-gha/slack-notification-wf)&nbsp;![Repo Size](https://img.shields.io/github/repo-size/subhamay-bhattacharyya-gha/slack-notification-wf)&nbsp;![File Count](https://img.shields.io/github/directory-file-count/subhamay-bhattacharyya-gha/slack-notification-wf)&nbsp;![Issues](https://img.shields.io/github/issues/subhamay-bhattacharyya-gha/slack-notification-wf)&nbsp;![Top Language](https://img.shields.io/github/languages/top/subhamay-bhattacharyya-gha/slack-notification-wf)&nbsp;![Custom Endpoint](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/bsubhamay/8612993cb0c2464da5255d6018345bd6/raw/slack-notification-wf.json?)

A template GitHub repository implementing a composite action to send Slack notifications for new issues or pull requests.

## 🛠️ Action Name

**Slack Notification**

## 📋 Description

This GitHub Action sends a message to a Slack channel via webhook when a new GitHub issue or pull request is created. It dynamically formats the message based on the event type.

---

## 🔐 Secrets

| Name            | Description                                 | Required |
|-----------------|---------------------------------------------|----------|
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
