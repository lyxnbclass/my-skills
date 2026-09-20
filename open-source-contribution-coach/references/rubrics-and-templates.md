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

## GitHub comment style

Write comments like a developer responding in an active thread, not like a formal report or customer-service message.

Default rules:

- Keep routine replies to one sentence; use two only when a reason or test result matters.
- Lead with the status or decision: `Fixed:`, `Updated:`, `I agree`, `I’ll fix it`, or the direct question.
- State only what changed or what is blocking progress. Do not repeat the reviewer’s full request.
- Match the maintainer’s language, punctuation, and level of formality. Contractions are fine.
- Use plain text for simple replies. Do not add headings, bullet lists, greetings, or sign-offs unless the content genuinely needs structure.
- Avoid generic filler such as `Thank you for your valuable feedback`, `I have carefully reviewed your suggestion`, `Great catch!`, or `Please let me know if you have any further concerns`.
- Do not thank the reviewer in every thread. A short `Thanks` is enough when acknowledgement is useful.
- Do not say `Fixed` until the change is pushed. Do not promise a fix when it has already been made.
- Mention tests only when they were actually run and the result helps the reviewer.
- Preserve necessary technical precision; concise does not mean vague.

Prefer:

```text
Fixed: switched the fallback to `SKIP` and added a regression test.
```

```text
Thanks for the review — I'll fix it.
```

```text
Updated the test to cover the empty-input case.
```

```text
I kept this check here because the value can change after deserialization. Would you prefer it in the converter?
```

```text
Do you want this to cover nested records too, or keep it scoped to top-level fields?
```

Avoid:

```text
Thank you for your valuable feedback. I have carefully reviewed your suggestion and implemented the requested changes. I also added comprehensive tests to ensure the solution is robust. Please let me know if you have any further concerns.
```

For several related changes, one compact list is acceptable, but do not turn a review reply into a PR summary. A structured PR body may be longer; these rules mainly govern issue comments, review-thread replies, and follow-ups.

## Maintainer alignment comment

```text
Hi, I reproduced <problem> in <location or version>. I'm planning to <approach> and add tests for <cases>. Does that direction look right?
```

Adapt to the repository's tone. Add non-goals or design constraints only when they materially affect the decision. State facts only and keep it as short as the context allows.

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
