# Tree Assessment Defect Calculator

瀏覽器端工具：上傳 Tree Assessment Schedule Excel，根據官方缺陷名單自動計算 **Form / Health / Structure**，以及 **Suitability for Transplanting Remarks** 代碼，並同原本評分對照。

開 [GitHub Pages](https://davychan188.github.io/tree-assessment-calculator/)，上傳或拖放 `.xlsx` / `.xls`。資料只在瀏覽器處理，不會上傳伺服器。

## 規則

- **Form / Health / Structure**：Remarks 逐項配對官方 161 項缺陷名單。該項若標示 P，對應評分便為 P；否則為 A。空 Remarks 時 Health / Structure 留空，Form 為 A。
- **Dead tree**：Form、Health、Structure 皆為 P。
- **Leucaena leucocephala**（銀合歡）：Form 及 Structure 為 P。
- **Suitability Remarks 代碼**
  - `a`：一律加上
  - `b`, `c`：高度大過 5m，而且 DBH 大過 200mm（剛好 5m 或 200mm 不加）
  - `d`：DBH 大過 700mm
  - `e`：不自動加上
  - `f`：Form / Health / Structure 任何一項為 P
  - `g`：樹種為 *Leucaena leucocephala*
  - `h`：Remarks 含 slope / on slope
  - `i`：Remarks 含 hoarding / road / slope

修改 Remarks 後會即時重新計算。可匯出更新後的 Excel。未配對到官方名單的 Remarks 會以橙色標示。

## 檔案格式

預設讀取名稱含 `Initial`、`Tree` 或 `Schedule` 的工作表，欄位順序與常見 Tree Assessment Schedule 相同（Tree No.、Scientific Name、Height、DBH、Form / Health / Structure、Suitability Remarks、Remarks 等）。
