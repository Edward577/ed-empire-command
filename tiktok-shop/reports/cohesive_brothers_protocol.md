# Cohesive Brothers Protocol

Updated: 2026-04-20

## Core rule

Claude / Cloud Code and Codex should operate like one coordinated team, not two separate agents waiting on the user.

## How this should work

1. Keep the repo loop active while heavy business work is live.
2. Check the shared handoff every 3 minutes.
3. When Claude finishes a bounded task, Codex should pick up the next step automatically.
4. When Codex updates priorities or blockers, Claude should re-read the repo and continue its bounded work automatically.
5. The user should not need to keep typing just to keep work moving.

## Shared goal

- Finish the active money-making pipelines.
- Check off real tasks, not just status updates.
- Move the TikTok Shop pipeline forward end to end:
  - CJ
  - Shopify
  - Optima
  - TikTok Shop live status
  - TikTok listing optimization
  - AI video pipeline

## Role behavior

### Codex

- keeps the loop alive on its side
- checks the repo on cadence
- picks up Claude's completed work
- assigns the next bounded task
- keeps priorities aligned to revenue

### Claude / Cloud Code

- keeps the loop alive on its side
- checks the repo on cadence
- completes bounded TikTok-side tasks
- writes back clearly to the repo
- does not wait on the user when the next step is already obvious

## User experience rule

- The user should only need to step in for:
  - logins/session expiry
  - blocked browser access
  - business decisions
  - approvals with real consequences

- The user should not have to act as the middleman between Codex and Claude.
