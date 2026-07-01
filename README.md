# ✍️ pdf-sign

在瀏覽器中手寫或上傳簽名，拖曳放到 PDF 上，下載簽名完成的檔案。純前端執行，檔案不離開你的電腦。

Draw or upload a signature, drag it onto your PDF, and download the signed file — entirely in your browser.

---

## 這是什麼？/ What is it?

簽合約、報價單、確認單時，常常需要印出來簽名再掃描回去，或用其他工具東拼西湊。pdf-sign 讓你直接在網頁上完成整個流程：手寫簽名、拖到 PDF 上對的位置、微調大小，然後下載。

Signing contracts, quotes, or confirmations often means printing, signing, and scanning — or juggling multiple tools. pdf-sign lets you do it all in one page: draw a signature, drag it onto the right spot in your PDF, resize it, and download.

---

## 功能 / Features

### ✏️ 兩種簽名來源 / Two signature sources

- **手寫** — 在畫布上直接寫，可調整筆色與粗細
- **上傳** — 匯入既有的簽名圖片（建議透明背景 PNG）

- **Draw** — write directly on canvas, adjustable pen color & width
- **Upload** — import an existing signature image (transparent PNG recommended)

### 🖐 拖曳放置 / Drag to place

簽名預覽圖可以直接拖到 PDF 上任意位置放開即完成放置，不用點按鈕、不用猜座標。

Drag the signature preview straight onto the PDF — drop it where you want, no buttons, no guessing coordinates.

### 🎯 放置後可調整 / Adjustable after placement

- 拖動微調位置 / Drag to reposition
- 右下角把手縮放（維持比例）/ Resize handle (aspect-ratio locked)
- 一鍵刪除 / One-click delete

### 🪟 透明背景 / Transparent background

簽名不會有白色色塊蓋住 PDF 內容 — 手寫畫布本身透明，貼上 PDF 時用 `multiply` 混合模式，只留筆跡。

No white box covering your document — the canvas is transparent, and placement uses `multiply` blend mode so only the ink shows.

### 💾 記住簽名 / Remember signature

簽名可以「記住」在瀏覽器本機（localStorage），下次開啟直接載入，不用重畫。也可以另存成 PNG 圖檔下載到電腦。

Signatures can be "remembered" locally (localStorage) for instant reload next time — or downloaded as a standalone PNG file.

### 📄 多頁 PDF 支援 / Multi-page support

上一頁 / 下一頁切換，每頁可以放置各自的簽名。

Navigate pages and place different signatures on each.

---

## 使用方式 / How to use

1. 開啟網頁，上傳 PDF（點擊或拖曳）
   Open the page, upload a PDF (click or drag)
2. 手寫簽名，或切換到「上傳」匯入圖片
   Draw a signature, or switch to "Upload" tab
3. 拖曳簽名預覽圖到 PDF 上想要的位置
   Drag the signature preview onto the PDF
4. 需要的話拖動、縮放調整位置與大小
   Reposition or resize as needed
5. 下載簽名完成的 PDF
   Download the signed PDF

---

## 隱私 / Privacy

所有處理都在你的瀏覽器本機完成，PDF 與簽名都不會上傳到任何伺服器。

All processing happens locally in your browser. Neither the PDF nor the signature is ever uploaded anywhere.

- 無後端、無資料庫、無追蹤 / No backend, no database, no tracking
- 「記住簽名」只存在你自己的瀏覽器 localStorage / "Remember signature" only uses your own browser's localStorage
- 原始碼公開，歡迎審查 / Source fully open, audit freely

---

## 技術棧 / Tech stack

純前端，單一 HTML 檔案，零框架。

Pure frontend, single HTML file, zero framework.

| 函式庫 / Library | 用途 / Purpose |
|---|---|
| PDF.js | PDF 渲染與預覽 / PDF rendering & preview |
| pdf-lib | PDF 輸出、嵌入簽名圖片 / PDF output, image embedding |
| Signature Pad | 手寫簽名擷取 / Signature capture |

---

## 開發路線圖 / Roadmap

| 狀態 | 功能 / Feature |
|---|---|
| ✅ | 手寫簽名（透明背景）/ Draw signature (transparent) |
| ✅ | 上傳簽名圖片 / Upload signature image |
| ✅ | 拖曳放置到 PDF / Drag-to-place on PDF |
| ✅ | 放置後拖動 / 縮放 / Reposition & resize after placement |
| ✅ | 記住簽名（localStorage）/ Remember signature |
| ✅ | 另存簽名為 PNG / Export signature as PNG |
| ✅ | 多頁 PDF 導覽 / Multi-page navigation |
| ⬜ | 多組簽名管理（命名、切換）/ Named signature presets |
| ⬜ | 加入日期戳章 / Date stamp insertion |
| ⬜ | 行動裝置觸控優化 / Mobile touch refinements |

---

## License

MIT
