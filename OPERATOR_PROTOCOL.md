# Operator Protocol — 「開始」

This file defines the entire normal Codex-side interaction. The user should only need to type:

> 開始

## Non-negotiable ordering

Do not research first. Do not trust a previously loaded CONTROL_SPEC. The order is:

```
sync remote spec
→ clean stale local runtime outputs
→ re-read latest spec from disk
→ execute research
→ audit
→ commit results
→ push
→ tell user to type "review" in ChatGPT
```

## 1. Synchronize before doing any work

Repository control branch:

`startup-research-v1`

Run:

```bash
git fetch origin startup-research-v1
git switch startup-research-v1
git reset --hard origin/startup-research-v1
```

If switching is blocked by unrelated local edits outside generated research paths, stop rather than deleting unknown user work. Under normal operation this should not occur.

Record:

```bash
git rev-parse HEAD
```

as `spec_commit` for the run.

## 2. Remove stale runtime research

The GitHub control/spec files are authoritative. Old **uncommitted generated research** must not influence a new run.

Delete only generated research outputs, never specs or founder constraints.

Clean ignored generated data under `memory/`:

```bash
git clean -fdX memory/
```

Also remove these known non-ignored runtime outputs if present:

```bash
rm -f memory/opportunity_shortlist.md
rm -f memory/opportunity_hypotheses.md
rm -f memory/opportunity_competitor_map.md
rm -f memory/evidence_audit.json
rm -f memory/RUN_MANIFEST.md
rm -rf memory/discovery_runs
rm -rf memory/problem_evidence
```

Do not delete:
- `AGENTS.md`
- `CONTROL_SPEC.md`
- `FOUNDER_CONSTRAINTS.md`
- `OPERATOR_PROTOCOL.md`
- `REVIEW_PROTOCOL.md`
- `workflows/`
- `skills/`
- tracked README / configuration files

## 3. Re-read the freshly synced control files

Even if these files were read earlier in the session, open them again **after sync**:

1. `CONTROL_SPEC.md`
2. `FOUNDER_CONSTRAINTS.md`
3. the workflow specified by CONTROL_SPEC
4. all skills required by that workflow

The newest `CONTROL_SPEC.md` wins over an older in-session understanding.

## 4. Execute autonomously

Run the task in CONTROL_SPEC end-to-end.

Normal behavior:
- do not ask the user to choose a topic;
- do not ask for confirmation;
- use the founder constraints already stored in the repo;
- browse/research as needed;
- do not recommend implementation before required evidence gates pass.

## 5. Produce a run manifest

Write `memory/RUN_MANIFEST.md` containing:

```markdown
# Run Manifest
- spec_commit: <SHA from step 1>
- workflow: <workflow used>
- started_from_keyword: 開始
- status: completed | partial | failed
- primary_outputs:
  - ...
- major_unknowns:
  - ...
```

## 6. Commit the research results

Stage only research results and the run manifest. Generated research under ignored memory paths may require `git add -f`.

At minimum, stage files that were actually produced, such as:

```bash
git add -f memory/RUN_MANIFEST.md
git add -f memory/opportunity_shortlist.md memory/opportunity_hypotheses.md memory/opportunity_competitor_map.md memory/evidence_audit.json 2>/dev/null || true
git add -f memory/problem_evidence 2>/dev/null || true
git add -f memory/market_insights 2>/dev/null || true
git add -f memory/ideas 2>/dev/null || true
```

Do **not** commit secrets, environment files, credentials, logs, or unrelated local files.

Commit message format:

```
RUN: <short description>
```

Example:

```
RUN: Taiwan opportunity discovery
```

## 7. Push

Push the completed run to:

```bash
git push origin startup-research-v1
```

A run is not complete until the push succeeds. If Git authentication or a local security approval blocks the push, state that clearly.

## 8. User-facing completion message

Keep the response extremely short and in Traditional Chinese. Do not dump the English report into chat.

Use:

> 完成，結果已 push 到 GitHub。請回 ChatGPT 輸入「review」。

If the run was partial or push failed, replace that sentence with a concise Traditional-Chinese explanation.
