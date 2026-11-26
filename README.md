# AIOT-DIC4 — DietSense IEEE Conference Paper & OpenSpec Revision

本儲存庫收錄 **DietSense** 研究計畫之 IEEE 會議論文（初稿 Draft V1 與 OpenSpec 驅動修訂稿 Draft V2）、OpenSpec 規格與變更紀錄，以及完整驗證報告。

## 研究摘要

飲食自我監測是行為性體重管理介入中的重要工具，但既有系統性回顧顯示，各研究之依從性指標與使用成效仍具高度異質性。在台灣日常飲食情境中，餐點常以混合料理、地方俗稱與模糊份量描述，例如「一碗加蛋牛肉麵，湯喝一半」，使傳統資料庫手動搜尋流程容易面臨搜尋負擔、配方錯配與假精確估算等問題。本研究提出 **DietSense**，一個面向繁體中文台灣飲食情境之對話式領域 AI Agent 研究計畫，探討如何將大型語言模型（LLM）之自然語言理解與工具編排能力，與版本化營養資料檢索及確定性數值計算加以隔離與整合。系統規劃採八模組概念架構並設置明確信任邊界：使用者輸入與檢索文本皆視為不可信資料，營養候選自 USDA FoodData Central 及經版本與授權查核之台灣食品成分與在地食譜資料檢索，再由 Analytics Engine 執行確定性公式計算熱量與巨量營養素，且嚴格區分未知值（`null`）與零值，絕不以零補值。當食物身份、烹調方式或份量克數不足時，系統以非阻塞狀態機進行有限次澄清，或優雅降級為部分估算、具證據上下界之合理估算範圍（不宣稱為統計信賴區間）或純文字紀錄；安全護欄則將回應限制於一般資訊輔助，排除醫療診斷與處方。研究規劃建置 500 筆分層標註之繁體中文台灣餐點資料集與四層參照標籤，與固定版本人工搜尋基線比較估算誤差、來源追溯率、任務時間、完成率與澄清負擔，另規劃 20 名成人、7 日之可行性研究與 SUS 評估。本階段屬研究提案，尚未實作系統或執行實驗，所有效能門檻均屬待驗證之候選目標。

## Repository Structure

```text
AIOT-DIC4/
├── README.md
├── paper/
│   ├── before/          # Draft V1 (Initial IEEEtran paper + BibTeX + compiled PDF)
│   └── after/           # Draft V2 (OpenSpec-refined IEEEtran paper + BibTeX + compiled PDF)
├── openspec/
│   ├── specs/           # Core OpenSpec paper specification
│   └── changes/         # refine-ieee-paper change artifacts (proposal, design, tasks, specs)
└── verification.md      # LaTeX compilation, OpenSpec validation, MCP status, and V1→V2 diff report
```
