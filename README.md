# RTW3-JP-ChatGPT-Handoff

**Rule the Waves 3 (v1.01.38) 日本語化プロジェクト — Claude Code ↔ ChatGPT レビュー受け渡し専用リポジトリ**

This repository is the dedicated file-handoff channel between **Claude Code**
(which builds and verifies the Japanese localisation) and **ChatGPT** (which
reviews and finalises the Japanese translations) for the Rule the Waves 3
Japanese localisation project.

> This repository intentionally contains **review metadata and translation
> working documents only** (`.md` / `.csv` / `.txt`).
> It does **not** contain the game executable, the resource module (RTW3.JPN),
> proprietary binary assets, game data files, save files, or credentials.

## Layout

```
chatgpt_handoff/
    current/    <- the one review round ChatGPT should work on right now
    archive/    <- completed rounds, one folder per task name (never overwritten)
metadata/
    CURRENT_HANDOFF.md  <- what is in current/, with SHA-256 sums and rules
```

## Workflow

1. Claude Code moves the previous `current/` contents into
   `archive/<TASK_NAME>/`, places the new review files flat into
   `chatgpt_handoff/current/`, regenerates `SHA256SUMS.txt`, updates
   `metadata/CURRENT_HANDOFF.md`, audits, commits and pushes.
2. ChatGPT reads `metadata/CURRENT_HANDOFF.md`, reviews the files in
   `chatgpt_handoff/current/`, and produces the reviewed markdown +
   decision CSV.
3. The reviewed results are stored back into the **private** project tree
   (`reviewed_batches/` / `reviewed_forms/` / `_decisions_archive/`).
   This public repository is a transfer mirror, **not** the project's
   canonical store.

## Review rules (summary)

- English source strings are matched against the clean DFM **byte-for-byte**
  (exact match only — no fuzzy matching, no trim/strip, no newline
  normalisation).
- `Items.Strings` entries are never applied without a safety investigation.
- `Font.Name` and other internal identifiers are never translated.
- Runtime placeholders (design-time captions overwritten at runtime) are not
  translated via the DFM.
- `Recommended Japanese` / `Translation note` fields arrive **empty**;
  filling them in is ChatGPT's job. Claude Code does not author translations.
