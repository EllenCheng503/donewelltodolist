# Ellen 商業行銷觀察室 — Tracker System

> 基於 AK-Threads-Booster 框架建立的個人化內容決策系統。
> 資料來源：@ellen_bizmarketinglab 的 4 篇貼文截圖
> 建立日期：2026-05-07
> 信心等級：Directional（< 5 篇貼文，所有觀察為一次性）

---

## 檔案結構

```
ellen-tracker/
├── README.md                    ← 本檔，整套系統的說明
├── threads_daily_tracker.json   ← 核心數據庫，4 篇貼文完整解析
├── style_guide.md               ← Ellen 的寫作風格量化分析
├── brand_voice.md               ← Ellen 的語感深度分析（語氣、句構、招牌動作）
├── concept_library.md           ← 已解釋過的概念清單，避免重複
├── posts_by_date.md             ← 依日期排序的可讀存檔
├── posts_by_topic.md            ← 依主題分群的索引
└── comments.md                  ← 留言記錄（目前資料有限）
```

---

## 每個檔案的用途

### `threads_daily_tracker.json`
這是整個系統的**核心**。所有後續的選題、分析、預測、復盤都基於這份檔案。
每篇貼文都記錄了：
- 完整文字、hashtag、topic tag
- 演算法信號（discovery surface、topic graph、freshness、originality risk）
- 心理信號（hook payoff gap、share motive split、retellability）
- 完整 metrics（views、likes、replies、reposts、shares）
- 校正筆記（calibration_notes）

### `style_guide.md`
**量化**的風格觀察：字數、串文長度、hook type、ending pattern 各自的表現。
用途：未來起草時知道 Ellen 過去什麼長度、什麼結構表現好。

### `brand_voice.md`
**質化**的語感分析：句構偏好、語氣切換、情感表達、招牌動作。
用途：起草時用來模仿 Ellen 的口吻。**不是**用來在 analyze 時改寫 Ellen 自己的文字。

### `concept_library.md`
追蹤已經向受眾解釋過哪些概念。
用途：避免下次又重新解釋一次 PR FAQ；同時提示哪些概念還沒展開可發展。

### `posts_by_date.md` / `posts_by_topic.md`
人類可讀的存檔，方便 Ellen 自己快速翻找。

### `comments.md`
留言記錄。**目前缺資料，待補**。

---

## 目前的核心觀察（來自 4 篇貼文）

### 一句話結論
> Ellen 帳號目前最強的擴散方向是「**可立即套用的行銷框架**」（post_002 share rate 1.24%），但只發過一次。後續三篇都偏「品牌觀察」，share signal 弱很多。

### 走勢診斷
12,500 → 4,200 → 1,700 → 560 views

不是內容變差，是「新帳號探索期紅利收尾 + 內容方向從 framework 偏向 observation」雙重作用。

### 待補強的訊號
1. **Marketing framework 類型**目前只有 1 篇，建議補第 2 篇
2. **串文長度**控制在 3-4 串（目前出現過 5 串、9 串，後段斷崖）
3. **Topic tag 選擇**：避免用單一品牌名（LOPIA、皮克敏），優先用「行銷」「品牌行銷」這類大類目
4. **第一串就要把核心結論說完**：post_002 的 124 likes 集中在 part 1 是因為核心反直覺斷言放在第一句；其他篇結論都藏在後段

### 演算法紅線檢查（截至目前）
- 沒有 engagement bait（無「按愛心如果你同意」）✓
- 沒有 clickbait（無「99% 的人不知道」）✓
- 沒有圖文不一致（4 篇都是純文字）✓
- 沒朊主題混雜（每篇主題都單一）✓
- 沒有 AI 內容未標示問題 ✓

---

## 下一步建議

### 立即可做
1. 直接基於這份 tracker 走「開工選題」流程，產出下一篇候選題目
2. Ellen 讀過 `brand_voice.md` 後修正 AI 從外部觀察可能誤判的部分

### 中期累積
1. 累積到 10 篇後，data confidence 升級為 Usable
2. 屆時可以做 hook × topic × ending 的 cross analysis
3. 建議至少每篇都把第一小時、24 小時、72 小時的 metrics 記錄一次（手動截圖即可）

### 想完整自動化
1. 申請 Meta Threads Developer API token（步驟在 AK-Threads-Booster 的 setup skill 內有完整指南）
2. 用 `fetch_threads.py` 自動更新 tracker
3. 不過目前的手動版本已經夠用，這是長期項目

---

## 信心等級警語

**這份 tracker 目前是 Directional 等級（< 5 篇貼文）。**

意思是：
- 觀察是真的觀察，但每個結論都來自 1-2 個樣本
- 不能把任何單一觀察當成穩定 pattern
- 任何「Ellen 應該這樣寫」的建議都要打折看，因為樣本還小
- 累積到 20 篇後才能進入「Strong」等級的判斷

但即使在 Directional 等級，**有 tracker 比沒有 tracker 強很多**。至少每次發文不是從零開始猜。
