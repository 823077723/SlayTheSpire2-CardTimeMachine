# Changelog

## 1.2.6 — stable / 正式版

- Fixed **Tune** (`v0.113.1`) status tooltip: it now describes the old “next cards cost 0” effect instead of the 0.114 “upgrade random cards” text.
- Fixed the **Tune** bug where playing a Ki card left cards stuck in the play area instead of moving to the discard pile. The skipped `TunePower.AfterCardPlayed` patch now returns a completed `Task` instead of `null`.
- Re-tested **Defy** and **Debilitate** old-version upgrades.

## 1.2.5

- Fixed the **empty card library** caused by the Tune free-card cost patch touching canonical card models during the library’s sort; canonical models are now skipped.

## 1.2.4

- Restored the old **Tune** (`v0.113.1`) `TunePower` behaviour: after a turn with a Ki card, the next N cards cost 0. `FreeCardPower` was removed in 0.114, so this is tracked with a counter.

## 1.2.3 — stable / 正式版

- Hardened Harmony bootstrap: the Memento Mori keyword patch now targets `CardModel` and filters by card type; each patch class is applied inside its own `try/catch`, so one broken patch can no longer abort the whole mod.
- Fixed old-version upgrade values for **13 cards / 15 values**, including **Defy**: `v0.98.3` / `v0.99.1` upgrades now correctly give **7 Block and 2 Weak** instead of 1 Weak.
- Card-pool exclusion and preset bans are now part of the stable build.
- Requires **BaseLib** and **CVC - Cross-Version Compatibility**.

## 1.2.2

- Fixed parsing of `DynamicVars.Weak`-style upgrade values (`XxxPower` variable names) that had been silently treated as unchanged.
- Regenerated the version table: 218 cards / 252 version records.

## 1.2.1 — experimental / 实验版

- Added **card-pool exclusion**: any card can be marked **Excluded** in its card-library detail view and will stop appearing in future card rewards, shops and random generation.
- Added preset bans: **Save preset** now stores both card versions and the exclusion list; applying that preset restores both.
- Added the exclusion list and search UI to the settings page.
- Fixed the oversized **Save preset** dialog that pushed its OK button off-screen.
- This is an **experimental preview**. Stable remains **1.0.6**; the GitHub release for 1.2.1 is marked as a pre-release.

## 1.0.6

- Fixed **Rocket Punch** version behaviour:
  - `v0.99.1`: 0 cost this turn or until played (expires at end of turn).
  - `v0.107.1`: 0 cost until played (persists across turns).
- Added a separate `v0.99.1` option for Rocket Punch.

## 1.0.5

- Fixed **Voltaic** (`v0.99.1`): upgraded version no longer keeps **Exhaust**.
- Keyword patching now respects keywords removed by the current card's upgrade.

## 1.0.4

- Added old behaviour for **Sovereign Blade**, **Seeking Edge**, **Summon Forth**, and **Huddle Up**.
- Left **Misery**, **Drum of Battle**, and **Outbreak** unchanged (their old Power classes were removed in 0.114).
- Confirmed **Shining Strike** was already equivalent in 0.114.

## 1.0.3

- Fixed **Tune** (`v0.113.1`): upgrade now reduces cost by 1.

## 1.0.2

- Fixed **Simpleton**, **Fusion**, **Mirage**, and **Recall** cost upgrades.
- Fixed old versions of **Arsenal**, **Quiver**, and **Speedster** incorrectly gaining **Innate** on upgrade.
- Preserved aim/target preview values instead of resetting them to base damage.

## 1.0.1

- Added generic upgrade-cost handling for cards without their own `OnUpgrade` override (e.g. **Stoke**).

## 1.0.0

- First public release.
- 218 cards / 251 version records across 8 official balance versions.
- Card-library preview with ↑/↓ switching and apply button.
- Per-class settings, presets, and auto “Strongest” preset.
