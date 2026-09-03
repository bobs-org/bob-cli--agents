#fork:k
%model:grok-4.6
%effort:xhigh

%xprompts_enabled:false
# Gate answered

**Decision:** Install inotify-tools on apollo

| | |
| --- | --- |
| **Outcome** | ANSWERED — Install inotify-tools |
| **Answered via** | cli |
| **Opened** | 2026-09-03T21:02:33Z |
| **Answered** | 2026-09-03T21:14:11Z |
| **Commands** | 1 of 1 completed |
| **Gate** | custom/custom-fd3dea3d-aa9a-4216-baa5-29e259cf158d |

## Results

### install — `commands/install`

```json
{
  "inotifywait": true,
  "status": "already_installed"
}
```

## Your next action

The apollo vault-sync plan is already implemented; this gate was only the optional inotify-tools install. Docs are already committed.

Read the gate results and write the final implementation report:
- If status is installed or already_installed, confirm `ssh apollo command -v inotifywait` succeeds. The watch loop picks it up on the next iteration; no service restart.
- If status is needs_password, tell Bryan to run `ssh -t apollo 'sudo apt-get update && sudo apt-get install -y inotify-tools'` (sudo on apollo is password-gated). Leave the service running.
- If skipped, leave bob-vault-sync.service on the ~5s poll fallback and say so.

Do not redo clone, deploy-key, SSH alias, or systemctl enable work. Include the validation already observed: unit enabled+active, vault-sync status timestamps advancing with last_error null, clean git status in ~/bob.
%xprompts_enabled:true