# Card Time Machine / 卡牌时光机

An unofficial **Slay the Spire 2** mod that lets you roll individual cards back to any of **eight official balance versions** — from `v0.98.3` to `v0.114.0`.

一个《杀戮尖塔 2》的民间平衡回退模组：把单张卡牌切回八个官方版本中的任意一版，不必被最新一次削弱绑死。

> Current release: **1.0.6** · Game branch: `public-beta` (v0.114.0) · Requires **BaseLib**

---

## Download / 下载

- **[CardTimeMachine-1.0.6.zip](CardTimeMachine-1.0.6.zip)** — ready-to-install package (DLL + PCK + manifest).

## Requirements / 前置

- Slay the Spire 2 **v0.114.0** on the `public-beta` branch.
- **BaseLib** — Steam Workshop item `3737335127`.
- The mod is loaded from the game's `mods` folder.

## Install / 安装

1. Subscribe to **BaseLib** on the Steam Workshop.
2. Download `CardTimeMachine-1.0.6.zip` and extract it.
3. Put the `CardTimeMachine` folder here:

   ```text
   ...\Slay the Spire 2\mods\CardTimeMachine\
       CardTimeMachine.dll
       CardTimeMachine.pck
       CardTimeMachine.json
   ```

4. Launch the game. In the **card library**, click a card, then use the **↑ / ↓** keys (or the on-screen buttons) on the large card view to cycle versions, and press **Apply this version**.

## Features / 功能

- **218 cards / 251 version records** across `v0.98.3`, `v0.99.1`, `v0.103.2`, `v0.103.3`, `v0.107.1`, `v0.111.1`, `v0.113.1`, `v0.114.0`.
- Per-card version preview inside the card library — numbers, keywords, costs and descriptions update live.
- Per-card selection, remembered in `CardTimeMachineConfig.json`.
- Settings page grouped by class, with search, presets, and an auto **“Strongest”** preset.
- Includes the pre-July **Compact + Fuel draw** version (`Fuel` at `v0.107.1`), the first Fool build (`v0.113.1`), and other historically notable cards.
- Does not modify save files; only card data/behaviour. Back up your saves anyway.

## Notes / 注意

- **Multiplayer is untested.** The mod changes local card behaviour; use it in multiplayer at your own risk.
- Some very old versions (0.98/0.99) do not have separate localized descriptions for every language; those cards fall back to the closest available text while keeping the old numbers.
- This is a fan project and is **not affiliated with Mega Crit**. Slay the Spire 2 and its card text belong to Mega Crit.

## Credits / 致谢

- **jiegec / Revert Anthony** — the original per-card revert mod and architecture that inspired this project. Some old implementations were adapted from it: <https://github.com/jiegec/STS2RevertAnthony>
- **BaseLib** — config UI and mod plumbing.
- **Mega Crit** — Slay the Spire 2.
- Everyone who tested the early builds and reported card-specific bugs.

## License / 授权

No open-source license is granted for this repository. The packaged mod is provided for personal play. Third-party code and game assets remain the property of their respective authors. If you are a rights holder and want something removed or credited differently, please open an issue.
