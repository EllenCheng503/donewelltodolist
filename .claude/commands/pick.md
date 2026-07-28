---
description: 開工選題 — 產出下一篇貼文的候選題目（商業行銷觀察室）
---

依照 `ellen-tracker/` 這套系統，跑「開工選題」流程，產出下一篇的候選題目。

限定條件（可留空）：$ARGUMENTS

## 執行步驟

1. 讀 `ellen-tracker/threads_daily_tracker.json` 的 `account_summary`，
   確認目前最強訊號、最弱 pattern、走勢診斷。
2. 讀 `ellen-tracker/concept_library.md`：
   - 「已解釋過的概念」→ 短期內避開
   - 「解釋過但仍可延伸的概念」→ 優先素材
   - 「可串成下一篇的概念連結」→ 現成題目
3. 讀 `ellen-tracker/style_guide.md` 的 Topic Freshness Budget，
   確認各 semantic_cluster 的 fatigue risk。

## 產出：3 個候選題目

每個候選都要給：

- **題目**（含【】型標題草稿）
- **semantic_cluster** 與目前的 freshness / fatigue risk
- **content_type**（優先 `framework_method_explanation` — 目前唯一被驗證的高擴散類型）
- **建議 hook_type**（`conditional_provocation` 是目前最強模式）
- **建議 ending_type**
- **建議串長**（3-4 串）
- **topic tag 與 hashtag 建議**
- **為什麼現在寫這篇**：對應到哪個待補強訊號
- **重複風險**：跟哪幾篇既有貼文最接近，切角差在哪

## 選題偏好（依目前診斷）

1. **優先補行銷框架類**（marketing_framework_explainer 只發過 1 篇，卻是最強 share driver）
2. brand_observation 已有 2 篇，再寫要換結構：
   不要「品牌 X 在做 Y」，改成「為什麼 X 失敗了 Y」或「兩個品牌做同一件事為什麼結果不同」
3. 自介類已用完，不應再寫
4. Ellen 的親身案例是最未被使用的資產
   （汽車業、平台產業的異業合作實戰、名單引擎、ROAS 實戰數字），優先動用
5. 提及過去公司時用產業類別代替，不要寫公司名

## 收尾

最後直接問 Ellen 選哪一個，選定後可以接 `/draft` 起草。
