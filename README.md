# STS2 Card Advisor Dashboard

Real-time card recommendation and deck synergy analysis dashboard for **Slay the Spire 2**.

> Languages: **English** · [한국어](README.ko.md) · [中文](README.zh.md)

🎮 **Mod download**: [Nexus Mods](https://www.nexusmods.com/slaythespire2/mods/627)
📊 **Dashboard**: [ing-gom.github.io/sts2-card-advisor](https://ing-gom.github.io/sts2-card-advisor/)

---

## About the mod

A Slay the Spire 2 mod that overlays each card on the reward screen with **tier, synergy score, and reason tags**.

### Features

- **Real-time card recommendations** — synergy score recomputed on every reward screen based on your current deck
- **Tier display** — S / A / B / C / D grade plus numeric score
- **Reason tags** — analysis based on roles needed by your deck (damage / defense / scaling, etc.)
- **Skip suggestion** — auto-suggest skip when all three cards are weak
- **Deck snapshots** — every reward screen saves a JSON snapshot of your deck state

### Supported characters

Silent / Ironclad / Defect / Necrobinder / Regent

---

## About the dashboard

This repo serves the **web dashboard** that pairs with the mod.

### Features

| Feature | Description |
|---|---|
| Card catalog | Browse axis tags, tier, and synergy roles for every card |
| Build synergy | Pick cards and see real-time recommendations |
| Run snapshots | View deck states saved during gameplay |
| Deck synergy analysis | Recommend cards based on a snapshot deck |

### Languages

The dashboard auto-detects your system language and supports **Korean / English / Chinese**. Use the **KO / EN / 中** buttons in the header to switch manually — your preference is remembered (localStorage).

### Usage

**During a game (live sync)**
1. Launch the game with the mod installed
2. Open `http://localhost:8765` in your browser
3. The dashboard auto-syncs every time a reward screen opens

**Without the game (catalog / past runs)**
1. Open the [dashboard](https://ing-gom.github.io/sts2-card-advisor/)
2. Use the sidebar "Deck snapshot → Choose file" to load a saved snapshot
   - Saved at: `%APPDATA%\Sts2CardAdvisor\run_snapshots\` (Windows)
   - Saved at: `~/Library/Application Support/Sts2CardAdvisor/run_snapshots/` (macOS)

---

## Deployment layout

```
ing-gom/sts2-card-advisor        ← this repo (public, dashboard HTML only)
ing-gom/sts2-card-advisor-dev    ← dev repo (private, full source)
```

---

## License

MIT
