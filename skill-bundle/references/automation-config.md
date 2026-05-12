# Automation Config Snapshot

## Name

`反共识商业局 AI商业新闻周榜`

## Type

`heartbeat`

## Schedule

`FREQ=WEEKLY;BYDAY=MO;BYHOUR=8;BYMINUTE=30;BYSECOND=0`

## Destination

`thread`

## Purpose

Generate one weekly China-market AI business news roundup for WeChat Channels:

- 5 `news event` items from the past 7 days
- primary audience: marketing and communications leaders/practitioners
- secondary audience: CEOs / owners
- each item includes:
  - one-line event summary
  - contrarian interpretation
  - what marketing should do next

## Runtime Prompt Source

The full prompt used by the automation is mirrored in:

- `agent-runtime-prompt.md`

If we later formalize this as a real Codex skill, this file should become part of the skill's docs or setup notes.
