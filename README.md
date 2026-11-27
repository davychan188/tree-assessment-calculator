# Tree Assessment Defect Calculator

瀏覽器端工具：上傳 Tree Assessment Schedule Excel，根據官方缺陷名單自動計算 **Form / Health / Structure**，以及 **Suitability for Transplanting Remarks** 代碼，並同原本評分對照。

開 [GitHub Pages](https://davychan188.github.io/tree-assessment-calculator/)，上傳或拖放 `.xlsx` / `.xls`。資料只在瀏覽器處理，不會上傳伺服器。

## 規則

- **Form / Health / Structure**：Remarks 逐項配對官方 190 項缺陷名單。該項若標示 P，對應評分便為 P；否則為 A。空 Remarks 時 Health / Structure 留空，Form 為 A。
- **Dead tree**：Form、Health、Structure 皆為 P。
- **Leucaena leucocephala**（銀合歡）：Form 及 Structure 為 P。
- **Suitability Remarks 代碼**
  - `a`：一律加上
  - `b`, `c`：高度達 3m，或 DBH 達 130mm（剛好 3m 或 130mm 亦加），或 Form / Health / Structure 任何一項為 P
  - `d`：DBH 大過 700mm
  - `e`：不自動加上
  - `f`：Form / Health / Structure 任何一項為 P
  - `g`：樹種為 *Leucaena leucocephala*
  - `h`：Remarks 含 slope / on slope
  - `i`：Remarks 含 hoarding / road / slope / Suppressed by adjacent tree / At drainage channel embankment / debris / fencing

修改 Remarks 後會即時重新計算。可匯出更新後的 Excel。未配對到官方名單的 Remarks 會以橙色標示，並集中列在「未在名單內」一頁（含棵數同 Tree No.）；匯出 Excel 亦有 Not in Defect List 工作表。

## 檔案格式

預設讀取名稱含 `Initial`、`Tree` 或 `Schedule` 的工作表，並按欄名識別 Tree No.、Scientific Name、Height、DBH、Form / Health / Structure、Suitability Remarks、Remarks 等（兼容前面有 Prohibited、TPRP/NEW 等額外欄的日程表）。
