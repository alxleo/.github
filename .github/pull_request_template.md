Issue: <!-- #123 for this repository, or the full URL for an issue in another repository. -->

<!--
Give the reviewer the change, reason, milestone progress where applicable,
risk and review focus in at most 120 words of visible prose, including
prose in tables and diagrams. Short labels, values and legends are exempt.
For low-risk config, value, documentation or revert changes a plain revert
undoes, use at most 60 words, one short comparison, and omit empty sections.
Use the full form for changes to components, dependencies, schemas,
credentials, permissions or authentication, or when rollback is separate.

For a behavior change, compare the same task, starting state and action.
Mark unobserved results as expected. Match the view, viewport and timing
for screenshots. Use a short recording for interactions, a diagram for
flow or failure paths, and a table or code block for exact values or output.
Label units and conditions. Describe visuals in text and use no emoji.
For UI changes, put paired captures in the comparison. Name the affected view
and any capture gap. Use synthetic examples where captures could expose data.
-->

| | |
| --- | --- |
| **What this does** | <!-- One sentence on what changes for the user or maintainer. --> |
| **Why this is needed** | <!-- What happens if we wait? Explain why this approach now. If another option was credible, name what tipped the choice. --> |
| **Milestone progress** | <!-- Link the milestone or its acceptance issue. Name the completion criterion this PR advances and the remaining gap, if any. Omit this row if the work has no milestone. --> |
| **Risk / undo** | <!-- Low, Medium or High, what could go wrong, and how to undo the change. --> |
| **Review** | <!-- Ask the question most likely to change the decision. Link directly to what the reviewer should inspect. If independent review applies, link findings and give the reviewed scope and outcome. --> |

<!--
Keep decisions, failures and material gaps visible here. Lead with when
the item matters, such as Before merge or Before rollout. Name the affected
path, consequence, owner and next action. For a decision, give the choice
and your default. If a physical-device check remains, give it a visible
heading such as Tablet check. Name the user path, expected result, who will
run it and when. Use a single GitHub alert for a consequential action
a reader might otherwise miss while skimming.

> [!IMPORTANT]
> **Before rollout** · Name the check, who runs it and what they need to see.
-->

| Scenario or scope | Before | After |
| --- | --- | --- |
| <!-- Same task or item --> | <!-- Previous result --> | <!-- New result --> |

<details>
<summary>Checks and evidence</summary>

<!--
Start with unresolved items. For consequential behavior, give the starting
state or input, action and expected result so someone can replay the check.
State what you observed and where. Link directly to the relevant run or
preview and say what to inspect. Label author-reported results when the
run is unavailable. Use GitHub Checks for routine CI and link longer
evidence from the claim it supports.

Add the evidence that applies:
- Artifact or build output: Link the job or spec and matched reports from
  the real before and after artifacts. State what the comparison showed.
- Device or live rollout: Give the device or owning system, applied revision
  and observed behavior. Identify simulations or desktop results and say
  which path still needs a physical or live check.
- New dependency, component or process: Link the required decision. Say
  which simpler option was ruled out and the work people can stop doing.
- Project checks: Follow the repository's documented commands. Name checks
  that were skipped or weakened. For agent-run review or checks, name the
  model and effort when that affects how the evidence should be read.

A Gap leaves something important unknown. Failed means you observed a
problem. Pending names a later stage and owner. Verified means you observed
the stated result on the named path.
-->

| Status | Check and expected result | Observed result or next action |
| --- | --- | --- |
| <!-- Gap, Failed, Pending or Verified --> | <!-- Starting state, action and expected result --> | <!-- Observation and evidence, or what to check next --> |

</details>
