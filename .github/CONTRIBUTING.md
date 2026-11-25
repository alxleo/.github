# Planning in GitHub

| Use | When |
| --- | --- |
| Milestone | Several issues contribute to the same outcome. Assign them to the milestone. |
| Issue | Work needs its own scope and a way to verify the result. Choose **Issue** from **New issue**. |
| Sub-issue | One part of an issue needs to be tracked separately. Choose **Sub-issue** from **New issue**, then select **Add existing issue** on the parent. |

From a checkout of the relevant repository, `gh issue create --template "Sub-issue" --parent PARENT_NUMBER` fills in the template and links the parent when you submit.

## Write for the reader

Lead with the result, blocker or decision. Use plain English, active voice and
concrete details. Cut setup and context the reader already has. When someone
needs to act, say who should do what. Link evidence beside the result.

| What the reader needs | Show it with |
| --- | --- |
| One result or request | One short sentence. |
| What changed or how options compare | A small table with matching items aligned. Mark removals and additions with `−` and `+`. |
| What a UI change looks like | Before and after screenshots at the same scale. |
| How parts relate | A small diagram. Group related parts and use arrows for flow or dependencies. |
| Which checks passed | A short list or table with one result per target. Put a checkmark beside each verified target. |

Give images alt text and diagrams an accessible description. For repeated statuses,
use one plain-text legend beside the visual. Use distinct symbols so color is optional.

● kept · × dropped · ⚑ flagged · ✓ allowed · ↷ skipped · — N/A

## Issue body

Use the [layout guide](#write-for-the-reader) to show the change and next
action. Put detailed checks, logs, and supporting PRs in the collapsed evidence
section.

Check length before publishing or updating. Count prose, including sentences
in tables. Visualizations, icons, short labels, values and legends are exempt.

| Format | Word limit |
| --- | ---: |
| Issue body | 120 |
| Issue artifact | 150 |

Start from the effective template in GitHub or pass its name with
`gh issue create --template`. For a complete CLI or API body, read the
template with `repository.issueTemplates` in the GitHub GraphQL API.

## Pull request body

Start implementation PRs with `Issue: #123` for an issue in the same repository
or `Issue:` followed by the full issue URL for work tracked elsewhere.

Start from the repository's effective PR template. The
[account default](pull_request_template.md) opens with the change, reason,
risk and review focus. It pairs Before and After, keeps decisions and blockers
visible, and folds supporting checks under **Checks and evidence**.

## Issue and PR comments

For routine updates, one or two sentences usually cover what changed and what
happens next. Link to the check or artifact for details. Use a brief list or table
when there are several results to scan. Give a decision request its own line.

> **Alex, approve the one-site pilot.**
>
> Staging passed both checks.

## Milestone description

In **Issues → Milestones → New milestone**, give the milestone an outcome-oriented title. Paste and fill in this description.

```markdown
<!-- In one sentence, say what will be possible once this milestone is complete. -->

| Today | At completion |
| --- | --- |
| Current state | Observable result |

## Done when

- [ ] Completion check

## Plan and evidence

<!-- Link to the issue that holds the milestone-wide plan and artifacts. Omit this section when there are no links. -->
```

## Issue artifacts

| What you want to show | Format |
| --- | --- |
| Detailed architecture, data flow, or sequence | A Markdown artifact with the full diagram, or self-contained HTML for an interactive diagram. Put the overview in the issue body. |
| Dependencies or rollout order | A Mermaid or HTML map when the order needs explaining. Set the actual issue blockers in **Relationships → Mark as blocked by** so they appear in GitHub. |
| Plan, decision, or research | A versioned Markdown artifact. |
| UI proposal, comparison, or verification report | Self-contained HTML when readers benefit from filters, drill-down, or toggling views. |

Add the artifact from the owning issue’s **Artifacts** section and link it where it supports a decision or result. Edit the same artifact as the work evolves so its URL and history carry forward. For HTML, open the artifact and select **Preview**.

| When | Run from the repository checkout |
| --- | --- |
| Attach an HTML report or Markdown document | `gh issue artifact create ISSUE_NUMBER PATH_TO_FILE` |
| Update an existing artifact | `gh issue artifact edit ISSUE_NUMBER ARTIFACT_NUMBER --body-file PATH_TO_FILE` |
