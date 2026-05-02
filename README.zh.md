# STS2 卡牌顾问 仪表板

为 **Slay the Spire 2** 提供实时卡牌推荐与牌组联动分析的仪表板。

> 语言: [English](README.md) · [한국어](README.ko.md) · **中文**

🎮 **模组下载**: [Nexus Mods](https://www.nexusmods.com/slaythespire2/mods/627)
📊 **仪表板**: [ing-gom.github.io/sts2-card-advisor](https://ing-gom.github.io/sts2-card-advisor/)

---

## 模组简介

一款 Slay the Spire 2 模组,在奖励界面为每张卡牌叠加显示 **等级、联动分数与推荐原因**。

### 主要功能

- **实时卡牌推荐** — 每个奖励界面基于当前牌组重新计算联动分数
- **等级显示** — S / A / B / C / D 等级及数值分数
- **推荐原因标签** — 基于牌组所需角色(伤害/防御/成长等)的分析
- **跳过建议** — 三张牌都偏弱时自动建议跳过
- **牌组快照** — 每个奖励界面将牌组状态保存为 JSON

### 支持角色

沉默 / 钢铁 / 空灵 / 死灵缚物 / 摄政

---

## 仪表板简介

本仓库托管与模组配套的 **网页仪表板**。

### 功能

| 功能 | 说明 |
|---|---|
| 卡牌目录 | 浏览全卡的轴标签、等级与联动角色 |
| 构筑联动 | 选定卡牌后实时计算推荐卡 |
| 战局快照 | 查看游戏中保存的牌组状态 |
| 牌组联动分析 | 基于快照牌组推荐卡牌 |

### 语言

仪表板会自动识别系统语言,支持 **韩文 / 英文 / 中文**。点击页眉右侧的 **KO / EN / 中** 按钮可手动切换,所选语言会被记住(localStorage)。

### 使用方法

**游戏运行中(实时同步)**
1. 安装模组后启动游戏
2. 浏览器打开 `http://localhost:8765`
3. 每次打开奖励界面时自动同步快照

**无游戏(目录 / 历史战局)**
1. 打开 [仪表板](https://ing-gom.github.io/sts2-card-advisor/)
2. 侧栏 "牌组快照 → 选择文件" 加载已保存的快照
   - 保存路径: `%APPDATA%\Sts2CardAdvisor\run_snapshots\` (Windows)
   - 保存路径: `~/Library/Application Support/Sts2CardAdvisor/run_snapshots/` (macOS)

---

## 部署结构

```
ing-gom/sts2-card-advisor        ← 本仓库(公开,仅含仪表板 HTML)
ing-gom/sts2-card-advisor-dev    ← 开发仓库(私有,完整源码)
```

---

## License

MIT
