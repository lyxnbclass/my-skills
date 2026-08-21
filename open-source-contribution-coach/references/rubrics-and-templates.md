# Rubrics and templates

Read the relevant section when ranking projects/issues, preparing a PR, or recording experience.

## Project scorecard (100 points)

Use evidence from the last 90 days when possible. Scores support judgment; they do not replace it.

| Dimension | Weight | Strong signal |
|---|---:|---|
| Stack and learning fit | 25 | Core code matches the user's skills and target role |
| Maintainer activity | 20 | Recent commits/releases and active maintainers |
| Review responsiveness | 15 | Recent issues/PRs receive substantive replies |
| Newcomer readiness | 15 | Clear contributing docs, setup, tests, starter labels |
| Task availability | 15 | Multiple current, unclaimed, well-scoped issues |
| Local feasibility | 10 | Setup and test suite fit the user's time and machine |

Apply explicit penalties:

- archived or read-only: reject;
- no identifiable license: reject until clarified;
- no meaningful maintainer activity for 6+ months: usually reject;
- unclear build requiring private services: −15;
- many unanswered starter PRs: −15;
- mandatory CLA/DCO the user cannot accept: reject;

## Issue scorecard (100 points)

| Dimension | Weight | Strong signal |
|---|---:|---|
| Availability | 20 | Open, unassigned, unclaimed, no competing PR |
| Clarity | 20 | Reproduction or acceptance criteria are concrete |
| Scope control | 20 | Small integration surface and explicit non-goals |
| Testability | 15 | Existing harness can prove the behavior |
| Skill fit | 15 | User can understand and implement the main path |
| Maintainer value | 10 | Solves a recognized problem rather than cosmetic churn |

Reject or pause when security implications are undisclosed, expected behavior is disputed, required infrastructure is unavailable, or the issue explicitly asks contributors not to start yet.

## Contribution ledger

```markdown
# Contribution ledger

- Repository:
- Issue:
- Goal:
- Status: candidate | discussing | local implementation | PR open | changes requested | approved | merged | closed
- User-owned work:
- Maintainer direction:
- Codex assistance:
- Branch / commits:
- PR:
- Verification commands and results:
- CI:
- Review feedback:
- Merge commit / release:
- Measured outcome:
- Honest resume wording:
- Next action:
- Last verified at:
```

## Maintainer alignment comment

```text
Hi! I reproduced/confirmed <problem> in <location or version>. I am considering a focused change that <approach>, with tests covering <cases>. I would keep <non-goals> out of scope. Would this direction be useful, and is there any existing work or design constraint I should account for before starting?
```

Adapt to the repository's tone. State facts only and keep it below roughly 150 words.

## Pull request template

```markdown
## Problem

<What behavior or maintenance problem exists? Link the issue.>

## Solution

<What changed, why this approach, and what stayed out of scope?>

## Changes

- <Focused change 1>
- <Focused change 2>

## Testing

- `<exact command>` — <result>
- <manual or edge-case verification>

## Notes for reviewers

<Tradeoff, compatibility note, untested area, or specific review request.>
```

Use the repository's own PR template when present; merge these fields into it instead of replacing it.

## Experience evidence rules

- “Identified” requires an issue/repository link.
- “Implemented” requires a diff or commit plus test evidence.
- “Submitted” requires a public PR link.
- “Approved” requires an approving review or equivalent maintainer signal.
- “Merged” requires the merged PR or merge commit.
- Performance, coverage, latency, token, or reliability claims require reproducible before/after evidence.
- Quotes from maintainers must be short, exact, linked, and clearly attributed.
