# Workflow Check

| Caller | Action input | Tools |
| --- | --- | --- |
| GitHub-hosted Linux | Default `toolchain: docker` | Pinned actionlint and zizmor images |
| Linux runner with scanners installed | `toolchain: runner` | The runner's actionlint and zizmor binaries |

Check out the caller repository with `contents: read` and
`persist-credentials: false`, then call this action from the checked-out
workspace. Pin `alxleo/.github/actions/workflow-check` to a reviewed commit SHA.

To skip the scanners on Markdown-only pull requests, call the
[shared PR scope workflow](https://github.com/alxleo/coding-standards/blob/main/.github/workflows/pr-scope.yml)
and use its output in the condition on your existing Workflow Check job.
Keep the job name and event triggers so required status checks still report.
Merge queue and manual runs continue to run both scanners.
