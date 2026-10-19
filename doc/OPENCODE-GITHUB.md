# OpenCode GitHub integration

Workflow: `.github/workflows/opencode.yml`. Comment on an issue, PR, or PR review line
(owners, members, and collaborators only):

- `/oc-openai <task>` runs `openai/gpt-5.4` using `OPENAI_API_KEY`.
- `/oc-zen <task>` runs `opencode/gpt-5.4` (OpenCode Zen) using `OPENCODE_API_KEY`.

The generic `/oc` and `/opencode` mentions are intentionally not handled.

## One-time setup (manual)

1. Install the GitHub App at https://github.com/apps/opencode-agent on `kaelingray/paperclip`
   (an org owner must approve if the repo is in an org).
2. Add repository secrets (Settings > Secrets and variables > Actions):
   - `OPENAI_API_KEY` from https://platform.openai.com/api-keys
   - `OPENCODE_API_KEY` from https://opencode.ai/auth (Zen)
3. Edit the `model` inputs in the workflow to change models (`provider/model`).

No keys are stored in the repository.
