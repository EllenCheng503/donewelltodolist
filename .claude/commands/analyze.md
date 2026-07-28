---
description: 貼文成效復盤與語感漂移檢查（商業行銷觀察室）
---

依照 `ellen-tracker/` 這套系統，分析貼文成效。

分析對象：$ARGUMENTS
（可以是 tracker 裡的 post id、一段貼文全文，或一組新的 metrics 截圖數字。）

## 執行步驟

1. 讀 `ellen-tracker/threads_daily_tracker.json` 建立基準線。
2. 讀 `ellen-tracker/style_guide.md` 對照 hook type、ending type、串長、content type。
3. 若對象是新貼文，先歸類：content_type、hook_type、ending_type、semantic_cluster。

## 產出

- **metrics 解讀**：views / likes / replies / reposts / shares，重點看 **share rate**
  （sends 權重是 likes 的 3-5 倍，是這個帳號目前最有意義的訊號）
- **與基準線比較**：對照 4 篇既有貼文，標明是高於還是低於
- **hook–payoff gap**：鉤子強度與兌現強度是否對齊
- **斷崖檢查**：後續串的 likes 衰減是否超出正常範圍
- **topic freshness**：這個 semantic_cluster 距上次多久，fatigue risk
- **演算法紅線**：逐條檢查
- **可執行結論**：下一篇該調整什麼

## 硬規則

- **不要改寫 Ellen 送來的文字。** `brand_voice.md` 在這裡只用來標記語感漂移
  （「這段不像你平常的寫法」），不是拿來重寫。
- 每個結論都要標樣本數。目前 Directional 等級，任何 pattern 主張都要打折。
- 不要生成「平均值」類陳述 — 每種 hook / ending 都只有 1 個樣本。
- 缺的資料就說缺（無受眾組成、無 discovery surface 拆解、無留言內容、無時間序列），不要用推測填補。

## 收尾

若這是一篇新貼文，問 Ellen 要不要把它寫進 `threads_daily_tracker.json`，
並同步更新 `posts_by_date.md`、`posts_by_topic.md`、`concept_library.md`。
