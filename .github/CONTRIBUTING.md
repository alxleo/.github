# Planning in GitHub

| Use | When |
| --- | --- |
| Milestone | Several issues contribute to the same outcome. Assign them to the milestone. |
| Issue | Work needs its own scope and a way to verify the result. Choose **Issue** from **New issue**. |
| Sub-issue | One part of an issue needs to be tracked separately. Choose **Sub-issue** from **New issue**, then select **Add existing issue** on the parent. |

From a checkout of the relevant repository, `gh issue create --template "Sub-issue" --parent PARENT_NUMBER` fills in the template and links the parent when you submit.

## Issue body

| What the reader needs | Show it with |
| --- | --- |
| What changed | Use a familiar convention first. Mark a comparison with `−` and `+`, and align matching items. For a UI change, pair screenshots at the same scale. |
| How parts relate | Use grouping for shared scope. Draw an arrow when its direction conveys a dependency, flow, or other real relationship. |
| What passed or needs action | Put a checkmark beside each verified target. Keep the next action, blocker, or decision visible in one precise line. |
| Where to verify it | Link the evidence to the result it supports. Put completed checks, logs, and supporting PRs in the collapsed evidence section. |

Keep words that identify an item, qualify a result, or tell the reader what
to do. A short sentence can carry a simple issue. Give images alt text and
diagrams an accessible description.

Start from the effective template in GitHub or pass its name with
`gh issue create --template`. For a complete CLI or API body, read the
template with `repository.issueTemplates` in the GitHub GraphQL API.

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
