Issue: <!-- #123 for this repository, or the full URL for an issue in another repository. -->

<!--
Give the reviewer the change, reason, risk and review focus in at most
120 words of visible prose, including prose in tables and diagrams. Short
labels, values and legends are exempt. A small change can use one short
comparison. Remove sections that add no information.

For a behavior change, compare the same task, starting state and action.
Mark unobserved results as expected. Match the view, viewport and timing
for screenshots. Use a short recording for interactions, a diagram for
flow or failure paths, and a table or code block for exact values or output.
Label units and conditions. Describe visuals in text and use no emoji.
-->

| | |
| --- | --- |
| **What this does** | <!-- One sentence on what changes for the user or maintainer. --> |
| **Why this is needed** | <!-- The problem or consequence that makes the change worthwhile. --> |
| **Risk / undo** | <!-- Low, Medium or High, what could go wrong, and how to undo the change. --> |
| **Review** | <!-- Ask the question most likely to change the decision. Link directly to what the reviewer should inspect. --> |

<!--
Keep decisions, failures and material gaps visible here. Lead with when
the item matters, such as Before merge or Before rollout. Name the affected
path, consequence, owner and next action. For a decision, give the choice
and your default. Use a single GitHub alert for a consequential action
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
-->

| Status | Check and expected result | Observed result or next action |
| --- | --- | --- |
| <!-- Gap, Failed, Pending or Verified --> | <!-- Starting state, action and expected result --> | <!-- Observation and evidence, or what to check next --> |

</details>
