# Operator Protocol — 「開始」

The human should only need to type:

> 開始

A run is complete **only after the research commit is verified on GitHub**.

## Fixed pipeline

```
開始
→ protect any unrelated local work
→ fetch/reset to latest remote control branch
→ delete stale generated research
→ re-read the freshly synced specs
→ research
→ write RUN_MANIFEST
→ stage only generated research
→ commit with RUN:
→ push
→ verify remote SHA == local RUN commit SHA
→ tell user to type review
```

## 0. Safety check: never destroy unrelated local work

Before any reset:

```bash
git status --porcelain
```

Delete only known generated research outputs under `memory/`.

If other local changes remain, preserve them automatically:

```bash
git stash push -u -m "AUTO-BACKUP before 開始"
```

Never silently destroy edits outside generated research paths.

## 1. Synchronize FIRST

The authoritative branch is:

`startup-research-v1`

Run:

```bash
git fetch origin startup-research-v1
git switch startup-research-v1
git reset --hard origin/startup-research-v1
```

Then record:

```bash
git rev-parse HEAD
```

as `spec_commit`.

Research must not begin before this succeeds.

## 2. Clear stale generated research

Delete only runtime outputs:

```bash
git clean -fdX memory/
rm -f memory/opportunity_shortlist.md
rm -f memory/opportunity_hypotheses.md
rm -f memory/opportunity_competitor_map.md
rm -f memory/evidence_audit.json
rm -f memory/RUN_MANIFEST.md
rm -rf memory/discovery_runs
rm -rf memory/problem_evidence
```

Never delete control/spec files.

## 3. Re-read the latest specs from disk

Even if they were read earlier in the same Codex session, explicitly open these files again after synchronization:

1. `CONTROL_SPEC.md`
2. `FOUNDER_CONSTRAINTS.md`
3. the workflow named by `CONTROL_SPEC.md`
4. every skill required by that workflow

Do not rely on an older in-session copy.

## 4. Execute autonomously

Run the current `CONTROL_SPEC.md` end-to-end.

Do not ask the user to choose a topic or repeat stored founder constraints.

## 5. Write the run manifest

Create `memory/RUN_MANIFEST.md`:

```markdown
# Run Manifest
- spec_commit: <SHA>
- workflow: <workflow>
- started_from_keyword: 開始
- status: completed | partial | failed
- primary_outputs:
  - ...
- major_unknowns:
  - ...
```

## 6. Stage ONLY run outputs

Stage generated research, forcing ignored runtime files when necessary:

```bash
git add -f memory/RUN_MANIFEST.md
git add -f memory/opportunity_shortlist.md memory/opportunity_hypotheses.md memory/opportunity_competitor_map.md memory/evidence_audit.json 2>/dev/null || true
git add -f memory/problem_evidence 2>/dev/null || true
git add -f memory/market_insights 2>/dev/null || true
git add -f memory/ideas 2>/dev/null || true
```

Inspect:

```bash
git diff --cached --name-only
```

Rules:
- every staged file must be a generated research artifact under `memory/`;
- no spec, config, secret, log, or unrelated file may be staged;
- if there is no staged research output, the run failed and must not be reported as complete.

## 7. Commit — mandatory

Commit message must start with `RUN:`.

```bash
git commit -m "RUN: Taiwan opportunity discovery"
```

Capture:

```bash
RUN_SHA=$(git rev-parse HEAD)
```

A run without a `RUN:` commit is incomplete.

## 8. Push — mandatory

```bash
git push origin HEAD:startup-research-v1
```

If push fails, do not say the run is complete.

## 9. Verify GitHub received it — mandatory

After push:

```bash
REMOTE_SHA=$(git ls-remote origin refs/heads/startup-research-v1 | awk '{print $1}')
test "$REMOTE_SHA" = "$RUN_SHA"
```

Only when this comparison succeeds is the run complete.

If it fails:
- diagnose and retry a safe push once if appropriate;
- otherwise report a concise failure in Traditional Chinese;
- never claim completion.

## 10. Final message

On verified success, respond only with a short Traditional-Chinese completion message:

> 完成，RUN 已 commit、push 並確認 GitHub 收到。請回 ChatGPT 輸入「review」。

Do not paste the English research report into chat.
