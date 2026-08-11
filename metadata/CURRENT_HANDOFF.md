# CURRENT_HANDOFF

Project: Rule the Waves 3 Japanese localisation
Game version: 1.01.38
Current cumulative translations: 2113
Current deployed JPN SHA-256: BF55CD2EC9113D23EEC2483D8B16F394D9535A2B4112A025E2069661B92F575C

Current review task: **NORMAL_CAMPAIGN_VISIBLE_FIXED_BATCH_02_V10138**
Review directory: `chatgpt_handoff/current/`

## What this round is

The final joint batch of the DFM fixed-UI phase: **20 normal-campaign forms,
46 translate candidates**. After this batch is reviewed and applied, every
safe fixed-UI string a player sees in a normal campaign will be in Japanese.

## Files

| File | SHA-256 |
|---|---|
| 01_visible_fixed_batch.md | ED0D02CABBFDB23D9076D218DA838054867D1D9C6A000B9502A6A4B6DB9E6C4F |
| 98_do_not_translate.md | 321EFC848E003BC26EC1C514EABA19F94AD27ADB1636E16F28457856DADCD1EE |
| 99_review_required.md | 4039BE7B0648FC2323216A4A2A4456F37B315CB87EF60BCEDBDAD10B169ABDB8 |
| _batch_source_map.csv | 025BF296675DB8DC1FA99D3DDE7AE7BAB7DC02C9DFCF4D97897DB567202B1DE3 |
| _index.csv | DCC9E6E7D57B7BA57C523DE8FD8130362CB507C6AB1FF3F928758B7D43932265 |

A `SHA256SUMS.txt` with the same values sits next to the files.

## Instructions

- Review **only** `01_visible_fixed_batch.md` (46 items).
- `Recommended Japanese` / `Translation note` are **empty** — filling them in
  is ChatGPT's job. Claude does not author translations.
- `98_do_not_translate.md` is informational (do not translate those items).
- `99_review_required.md` (3 Items entries) may receive draft translations
  but they will NOT be applied without a separate safety round.
- Keep terminology consistent with the established project glossary
  (e.g. Close=閉じる, Cancel=キャンセル, Ship=艦, Division=戦隊,
  Force=部隊, OK stays OK).
- Deliverables per established convention: `00_*_glossary.md`,
  `01_*_reviewed.md`, `98_*_reviewed.md`, `99_*_reviewed.md`,
  `*_review_decisions.csv`, and a short review report.

## Safety rules

- English is matched byte-for-byte against the clean DFM: **exact match
  only** — no fuzzy matching, no trim/strip, no newline normalisation.
  Do not "fix" typos or unusual spacing in the English column.
- `Items.Strings` are never applied without a safety investigation.
- `Font.Name` and internal identifiers are do-not-translate.
- Runtime placeholders are not translated via the DFM.
