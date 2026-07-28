---
description: 用 Ellen 的語感起草 Threads 貼文（商業行銷觀察室）
---

依照 `ellen-tracker/` 這套系統，替 Ellen 起草一篇 Threads 貼文。

主題／素材：$ARGUMENTS
（若上面是空的，先問 Ellen 這次要寫什麼，或建議先跑 `/pick`。）

## 執行步驟

1. 讀 `ellen-tracker/CLAUDE.md`（操作規則）、`ellen-tracker/brand_voice.md`（語感）、
   `ellen-tracker/style_guide.md`（長度與結構）。
2. 讀 `ellen-tracker/concept_library.md`，確認這次主題涉及的概念**有沒有解釋過**。
   已深度解釋過的（PR FAQ、皮克敏在地化、LOPIA 個人社群）短期內不要重講，
   改用延伸角度或直接引用既有結論。
3. 讀 `ellen-tracker/threads_daily_tracker.json` 的 `account_summary`，確認目前最強／最弱訊號。
4. 起草。

## 產出格式

- **標題**（【】型 + 副標，或數據型開場、概念定位型開場）
- **串文 3-4 串**，每串標明字數；第一串控制在 200-300 字，核心結論放第一串
- **hashtag 建議 2-3 個**（含定錨 `#行銷`）
- **topic tag 建議**：用大類目，不要用單一品牌名
- **自檢表**：逐條列出演算法紅線與禁用清單的檢查結果

## 硬規則

- 語感依 `brand_voice.md`，不要寫成教學文
- 「不是 A，是 B」對比結構可主動套用
- 避免問句結尾
- 所有數據必須有事實基礎，沒有把握就標「需 Ellen 核實」，不要編
- 起草完提醒：這是 Directional 等級系統（4 篇樣本），結構建議只是方向不是定論
