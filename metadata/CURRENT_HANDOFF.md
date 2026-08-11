# CURRENT_HANDOFF

Project: Rule the Waves 3 Japanese localisation
Game version: 1.01.38
Current cumulative translations: 2158
Current deployed JPN SHA-256: 34D58299963CDCA891F9A9DE85FF338949F6B5673C9B3111E6461EAE971611A4

Current review task: **PLAYER_VISIBLE_ITEMS_SAFETY_ROUND_01_V10138**
Review directory: `chatgpt_handoff/current/`

## What this round is

The normal-campaign DFM fixed-UI phase is practically complete (A+B residual
= 0). This round is the **Items safety round**: 30 player-visible held Items
were investigated read-only. Only **2 items** were proven safe
(`TDLGPICKFORCE/rgStartRange`: Classic / Long — a complete TRadioGroup).
Those 2 are the only translation-review targets.

## Files

| File | SHA-256 |
|---|---|
| 01_safe_items_chatgpt_review.md (2 items, REVIEW THIS) | 92346AB9FEA5D26BBAFB6C414987A99D86A7B3A384FB9DC83280D678DD81D574 |
| 98_unsafe_items.md (22, informational — do not translate) | F6B15DD077692D31155E39EC1B94D05D8BD79C758813D741A836247D746BF3D2 |
| 99_unresolved_items.md (6, informational — still held) | 51A8CF60186FA2E8CBFCEA4B3707F4E7BD212A0839AAA55E4A5E0697ECCBCAB0 |
| items_safety_classification.csv (30 rows, full evidence) | 2C1343CEEBA5EB15E916D87824A4C64111B9329201EF5D12A00591739C629E08 |
| _index.csv | 96153D6CA9A5902A6213740186788B94DAEC4C3332E1B615CAFFF4F5731C3C57 |

`SHA256SUMS.txt` sits next to the files.

## Instructions

- Review only `01_safe_items_chatgpt_review.md` (2 items).
- `Recommended Japanese` / `Translation note` are **empty** — filling them in
  is ChatGPT's job. Claude does not author translations.
- rgStartRange is the battle start-range radio group (`Classic` / `Long`).
  Translate the whole group consistently.
- Deliverables per convention: reviewed markdown + a small decision CSV
  (stable_id, english, recommended_japanese, decision) + short report.

## Safety rules

- Exact byte-for-byte English matching; no fuzzy matching, no trim/strip.
- The 22 UNSAFE and 6 UNRESOLVED items stay untranslated regardless of any
  draft translations that may exist.
- Font.Name / internal identifiers: do-not-translate.
- Runtime placeholders are not translated via the DFM.
