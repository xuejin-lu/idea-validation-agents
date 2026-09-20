# Review Protocol — ChatGPT Side

The human workflow is:

```
Codex: 開始
→ Codex syncs + researches + commits + pushes a RUN: commit
→ ChatGPT: review
→ ChatGPT reviews latest RUN: commit + artifacts
→ ChatGPT updates specs if needed
→ human returns to Codex and types: 開始
```

## When the user says exactly `review`

The reviewer should:

1. Inspect the latest commits on `startup-research-v1`.
2. Find the latest `RUN:` commit.
3. Read `memory/RUN_MANIFEST.md` and the run's primary output files.
4. Give the user a **short Traditional-Chinese report**:
   - 這次 Codex 做了什麼
   - 找到什麼
   - 哪些是真的有台灣證據
   - 哪些結論還太弱
   - 有沒有違反 FOUNDER_CONSTRAINTS / CONTROL_SPEC
5. Decide whether the research process needs a spec change.
6. If a spec/process change is clearly needed, update the repository directly and commit it with prefix:
   `SPEC:`
7. Do not make the user copy/paste the research report.
8. End by telling the user that the next Codex-side input is simply:
   `開始`

The reviewer should not preserve a flawed idea merely because Codex ranked it highly. Evidence quality and founder constraints override ranking.
