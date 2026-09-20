# Review Protocol — ChatGPT Side

The human uses only two keywords:

```
Codex: 開始
ChatGPT: review
```

## When the user says exactly `review`

1. Read the latest commits on `startup-research-v1`.
2. The newest unreviewed research commit must have a message beginning with `RUN:`.
3. If there is no new `RUN:` commit, report only that Codex has not successfully delivered a new run to GitHub yet.
4. For a valid run, read:
   - `memory/RUN_MANIFEST.md`
   - the primary outputs listed in the manifest
   - the `RUN:` commit diff when useful.
5. Give a short Traditional-Chinese report:
   - 這輪做了什麼
   - 找到哪些候選
   - 哪些有真正台灣證據
   - 哪些證據不足或推論過頭
   - 有沒有違反 `FOUNDER_CONSTRAINTS.md` / `CONTROL_SPEC.md`
6. Decide whether the workflow/spec itself needs correction.
7. If a process correction is clearly needed, update the relevant spec files directly on `startup-research-v1`. Commit messages must begin with `SPEC:`.
8. Do not ask the human to copy/paste reports or translate Codex output.
9. End with the next action:
   - if a new spec was pushed: tell the human to return to Codex and type `開始`;
   - if no spec change is needed: explain the next research/validation state briefly, while preserving the two-keyword workflow.

Evidence quality and founder constraints override Codex rankings.
