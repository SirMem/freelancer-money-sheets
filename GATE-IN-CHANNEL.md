# GATE-IN-CHANNEL · 通道内清闸

**One-liner:** 清闸预览必须出现在主人已经打开的通道里（本聊天正文）；把「打开网页/下载卡」当成清闸第一步是加激活能，不算 CLEAR-COST 降本。Pages/HTML 卡只作可选镜像。

**Parent of:** [CLEAR-COST](CLEAR-COST.md) + [PREVIEW-CONTRACT](PREVIEW-CONTRACT.md). Complements [ACTIVITY-BIAS](ACTIVITY-BIAS-LOCK.md)（闸门 FAIL 时继续往站外塞卡 = bias）。

## Why（signals 2026-10-29 ~13:53 Asia/Shanghai）

| Signal | Point |
|--------|-------|
| Friction budget / confirmation theater — [tianpan.co](https://tianpan.co/blog/2026/06/02/the-are-you-sure-confirmation-step-your-users-learned-to-click-through) | 「你确定吗？」无原文预览 → 习惯性点是；有效确认 = 在**当前通道**展示要发出的原文 |
| Activation energy / handoff in place — [dilloncarter.com](https://dilloncarter.com/writing/ai-agents-add-activation-energy) | Agent 常加「打开别的工具」handoff；真降本 = 在已打开的地方交接 |
| Owner gates + async ops — [bmdpat.com](https://bmdpat.com/blog/ai-agent-owner-gates-async-ops-2026) | 主人闸门要能在异步对话里清；别把闸门藏进另一张网页 |
| Event-driven initiation（webhook as prompt） | 启动可靠 = 在已活跃通道里出现，而不是等用户去打开新 URL |
| Local anti-pattern 同日 | `clear-cost-card.html` + `action-preview-card.html` 上 Pages → Kevin 必须离开聊天才能清闸 → GATE FAIL 持续 |

## Complements（不替代）

| Gate | Job |
|------|-----|
| [CLEAR-COST](CLEAR-COST.md) | 度量：一张预览 + 一行回令；步骤/未决/秒 |
| [PREVIEW-CONTRACT](PREVIEW-CONTRACT.md) | 同意语义：动词+对象标题；字段逐字；批准钮写动作 |
| [REPLY-BIND](REPLY-BIND.md) | 绑定：回令 ↔ 唯一粘贴块；双主路径/新门禁 = FAIL |
| **This core** | **通道**：预览必须在已打开聊天里；站外 HTML = 可选镜像 |
| [ACTIVITY-BIAS-LOCK](ACTIVITY-BIAS-LOCK.md) L9 | 要求先开 Pages 再回令 = FAIL cost drop |
| [ONE-TAP-POST](ONE-TAP-POST.md) / [STORY-FOOTNOTE-POSTS](STORY-FOOTNOTE-POSTS.md) | 粘贴原文来源 |
| [CHAT-REPLY-FORMAT](CHAT-REPLY-FORMAT.md) | 清闸回令格式 |

## Pass rule（Agent 自检）

在 OWNER-FAVOR B=FAIL 时，本轮清闸主交付必须同时满足：

1. ** verbatim paste 在聊天 / WakeParent payload 正文**（不是「请打开这个链接看正文」）
2. **清闸前零必开站外页**（Pages / HTML / 下载卡均为可选镜像）
3. **回令一行**（例：`人情帖已发：朋友圈/同学群·故事脚注 + HH:MM`）
4. 仍满足 CLEAR-COST（推荐动作=1）与 PREVIEW-CONTRACT（字段逐字、按钮动词）
5. 回令绑定该粘贴块（[REPLY-BIND](REPLY-BIND.md)）；禁止 A∥C 同等优先并列首屏

Primary surface: [chat-inline-clear.md](chat-inline-clear.md)（REPLY-BIND 绑定回令）  
Optional mirror only: [reply-bind-scorecard.html](reply-bind-scorecard.html) · [gate-in-channel-scorecard.html](gate-in-channel-scorecard.html)（及旧 clear-cost / action-preview 卡）

## Anti-patterns

- 把「打开 clear-cost-card.html / action-preview-card.html」写成清闸第一步
- 聊天里只给 URL，正文藏在网页里
- 再开一张站外「更漂亮的卡」当主进度，同时闸门 FAIL
- 声称 A/W1/W2/C1 PASS（未收到 Kevin 回令）
