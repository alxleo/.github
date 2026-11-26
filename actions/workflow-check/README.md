# Workflow Check

| Caller | Action input | Tools |
| --- | --- | --- |
| GitHub-hosted Linux | Default `toolchain: docker` | Pinned actionlint and zizmor images |
| Linux runner with scanners installed | `toolchain: runner` | The runner's actionlint and zizmor binaries |

Add the action as a step in the required job and grant the job `contents: read`.
The action checks out the caller's code. Trigger on every pull request so
GitHub can report the required check even when the action skips lint and audit.
Keep `merge_group` for a merge queue. Other events run both tools.

Use an exact action SHA for an immutable consumer pin. To follow compatible
releases automatically, use `alxleo/.github/actions/workflow-check@v1`.
A lockfile entry for the action selects the recorded SHA.

Promote the `v1` Git tag after review and successful hosted and preinstalled
runner checks. Record the old and new SHAs so the tag can be rolled back.
Publish immutable releases under their exact version tags, such as `v1.0.0`.
