# 🛒 Cash Shop Extended

A Ragnarok Offline mod that fills the Cash Shop and lets you earn Cash Points just by playing 💎 Renewal only.

## 🌟 What It Adds
- 🛍️ **A full Cash Shop**: 552 scrolls, boxes, buffs and convenience items, all in one tab so every client shows them.
- 🎁 **A welcome gift**: 250 Cash Points the first time each account logs in.
- ⏱️ **Points for play time**: 15 Cash Points for every 10 minutes online.
- ⚔️ **Points for kills**: 15 Cash Points for every 100 monsters you defeat.
- 💰 **Cash Point Seller** (Prontera 148, 193): buys 15, 150 or 1,500 Cash Points for 300,000, 3,000,000 or 30,000,000 Zeny.
- 🎰 **Gacha Machine** (Prontera 172, 177): one random Cash Shop item for 200,000 Zeny, 30 Cash Points or 3 Cachua Coupons. Cheap items come up often, expensive ones rarely 🍀
- 📊 **Cash Points** (Prontera 143, 125): your balance and how close you are to the next reward.
- 🏷️ **Names for kRO clients**: 77 iRO-only shop items that a kRO client shows as "Unknown Item" get their real names, icons and descriptions (`System/itemInfo.lua`).

Points and progress are account-wide: every character on the account shares them 👥

## 💾 Installing
In Ragnarok Offline: **Settings → Mods → Find Mods → cash-shop-extended → Install**.
When a new release is out, the Mods tab shows **Update available** 🔔

You can also download `cash-shop-extended-v<version>.zip` from the [Releases](../../releases) page and install it with **Install from a folder…**

## ⚙️ Settings
The rewards are set at the top of `npc/points.txt`, under `OnInit` (1 = on, 0 = off):

| Setting | Default | What it does |
|---|---|---|
| `.StarterEnabled` | 1 | 🎁 the welcome gift |
| `.StarterPoints` | 250 | points in the welcome gift |
| `.PlayTimeEnabled` | 1 | ⏱️ points for time online |
| `.PlayMinutesPerReward` | 10 | minutes per reward |
| `.PlayTimePoints` | 15 | points per reward |
| `.KillRewardEnabled` | 1 | ⚔️ points for kills |
| `.KillsPerReward` | 100 | kills per reward |
| `.KillRewardPoints` | 15 | points per reward |
| `.DailyPointCap` | 0 | most points a day (0 = no limit) |
| `.ShowRewardMessages` | 1 | 💬 a chat line when you earn points |

The shop's items and prices are in `db/item_cash.yml` (rAthena AegisNames), and the Gacha Machine's costs and odds are in `npc/gacha_machine.txt`. Restart Ragnarok Offline after any change 🔄

## 🚀 Releases
- ✅ Every pull request runs [validate.yml](.github/workflows/validate.yml): `mod.json`, every `.yml` with rapidyaml, the release zip's layout, and the scripts on an rAthena map-server `--run-once`.
- 🏷️ Publishing a GitHub Release tagged `v<version>` builds `cash-shop-extended-v<version>.zip` ([release.yml](.github/workflows/release.yml)) and attaches it.

## 🙏 Credits
- 🗡️ Lil Art: the mod
- ⏱️ Alex Rows: the point rewards (`npc/points.txt`)
- 🎟️ MondoTruth: the Episode 13, 14 and 15 Clear Tickets
- 🏷️ akreao: the kRO client names (`System/itemInfo.lua`)
- 🛠️ Flux159: the release workflow

## 📜 License
The scripts, database tables and documentation in this repository are licensed under the [GNU General Public License v3.0](LICENSE), the same licence as rAthena.

- 🏰 Ragnarok Online itself (its items, their names and descriptions in `System/itemInfo.lua`, sprites and everything else from the game) belongs to Gravity Co., Ltd. and is not covered by the GPL.
