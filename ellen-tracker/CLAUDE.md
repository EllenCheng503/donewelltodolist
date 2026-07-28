# Ellen 商業行銷觀察室 — 執行說明（Claude Code 版）

這個資料夾是原本 Claude Project「Ellen 商業行銷觀察室」搬過來的版本。
Project 的知識檔已完整搬入本資料夾，並改成用 slash command 驅動。

## ⚠️ 關於本檔的來源

原 Project 的 **system prompt 沒有存在知識檔裡**，Drive 上只有 8 份知識檔。
以下操作規則是從 `brand_voice.md`、`README.md` 裡「system prompt 寫…」「system prompt 與貼文交叉驗證」
這些明確引用**反推重建**的，不是原文。**請 Ellen 讀過並修正**，尤其是「禁用清單」與「emoji 政策」兩節。

---

## 檔案角色（誰在什麼時候被讀）

| 檔案 | 何時讀 | 不可拿來做什麼 |
|------|--------|----------------|
| `threads_daily_tracker.json` | 所有任務的事實基礎 | — |
| `brand_voice.md` | **只在 `/draft` 起草時**當作曲依據 | 不可用來改寫 Ellen 自己送來的文字 |
| `style_guide.md` | `/draft`、`/pick` 判斷長度與結構 | 不可當統計結論（樣本 < 5） |
| `concept_library.md` | `/pick` 選題前查重 | — |
| `posts_by_date.md` / `posts_by_topic.md` | 人類可讀存檔，快速翻找 | — |
| `comments.md` | 留言分析（目前缺資料） | — |

## 資料信心紀律（最重要的一條）

目前是 **Directional** 等級（4 篇貼文）。任何輸出都必須遵守：

- 不得把單一觀察講成穩定 pattern
- 不得產出「平均值」類陳述（每種 hook、ending 都只有 1 個樣本）
- 給建議時要標明這是 1-2 個樣本的推論
- 累積到 10 篇升 Usable，20 篇才進 Strong

## 寫作規則（`/draft` 適用）

**句構**
- 短句為主，每句約 15-30 字；每段 1-3 句後換行，段間留空行
- 全形標點，無破折號；冒號帶出舉例，括號用於補充或自我嵌入

**禁用**
- 修辭性提問（「你知道嗎？」「是不是很意外？」）
- 學術連接詞（首先／其次／最後）
- 「讓我們來看看」「值得注意的是」「不可否認」
- 「不是 A 其實是 B」這種 AI 常見句式
- 「拆」「撈」（過度口語）
- 「賦能」「打通」「閉環」「賽道」（中國商業熱詞）
- 「驚艷」「驚豔」「神級」（讚嘆型形容詞）
- 過去公司名稱 → 用產業類別代替（例如「科技電子業」）

**語氣**
- peer-to-peer 同業對話，像資深同事講真話。不討好，不教訓，不當老師
- 立場要明確：「我覺得」「真正的關鍵」
- 嚴厲判斷後可加括號自嘲或一個放鬆的表情當減壓閥
- hedging 用「大概率」「大概」「應該」，不用「可能」「也許」
- 基本不用驚嘆號

**結構**
- 觀察 → 拆解（3-4 點）→ 抽象原則
- 「不是 A，是 B」對比結構是金句製造機，可主動套用
- 金句結論放第一串，不要藏在後段
- **3-4 串為佳**，超過 4 串 likes 會斷崖
- 避免問句結尾

**emoji 政策（待 Ellen 確認）**
system prompt 寫「不用 emoji」，但實際貼文有少量出現，且都用在「視覺分隔」或「情緒緩衝」，不是裝飾。
目前預設：**沿用實際貼文的用法**（克制、有功能性），不是完全禁用。

## 演算法紅線（每次產出前自檢）

- 無 engagement bait（「按愛心如果你同意」）
- 無 clickbait（「99% 的人不知道」）
- 圖文一致
- 每篇主題單一
- AI 內容有標示
- topic tag 用大類目（「行銷」「品牌行銷」），**不要用單一品牌名**
- hashtag 維持 2-3 個，不超過 4 個

## 目前的帳號診斷

走勢：12,500 → 4,200 → 1,700 → 560 views
成因：新帳號探索期紅利收尾 + 內容方向從 framework 偏向 observation，雙重作用。

最強訊號：`framework_method_explanation` 類（post_002，share rate 1.24%，52 sends），但只發過一次。
**優先補第 2 篇行銷框架類。**

## 更新 tracker 的規矩

新增貼文時，`threads_daily_tracker.json` 要補齊：完整文字、hashtag、topic tag、
演算法信號、心理信號、完整 metrics、calibration_notes。
然後同步更新 `posts_by_date.md`、`posts_by_topic.md`、`concept_library.md`。
貼文數跨過 10 篇時，記得把 `data_confidence_level` 升為 Usable 並重新校準各檔警語。
