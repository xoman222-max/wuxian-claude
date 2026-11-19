# GPT 生同風格圖示與 UI 套件流程（星詠契約實作）

- 日期：2026-11-19
- 類型：方法庫＋專案
- 標籤：遊戲圖示、UI 套件、ChatGPT 生圖、透明背景、切圖、border-image、9-slice、抽卡遊戲、星詠契約
- 主題卷：09
- 來源：本次在星詠契約（D:\claude\star-oath）實作；檔案：tools/icon_prompt.md、tools/slice_icons.py、tools/slice_parts.py、tools/shot.html
- 狀態：已實作並在瀏覽器驗證（圖片全部載入、375 寬無溢出）。

## 一句話摘要

一張圖裡一次生整組圖示或 UI 部件（風格才會一致），要求「fully TRANSPARENT background」拿到真透明 PNG，再用腳本切開，用 CSS border-image 套進遊戲。

## 流程

1. 盤點遊戲要哪些圖示：搜程式碼裡當圖示用的符號（◆ ✦ ✧ ★）和線條 SVG。
2. 寫固定風格前綴：主題、材質（glossy jewel-like、gold filigree）、外框、光源、「32 px 也看得懂」、no text；色碼直接取遊戲 CSS 變數。之後補圖一字不改，只換清單。
3. 一次生一張：
   - 圖示：Square 1:1，4×4 共 16 個，每格置中、留白、不互相碰到 → 1254×1254。
   - UI 部件：按鈕（金／深色）、四角金飾面板、緞帶標題、資源膠囊、圓形按鈕底座、分隔線。
   - 卡框：Wide 16:9，三個 2:3 框（SSR／SR／R），要求框內也透明 → 1672×941。
4. 下載：ChatGPT 分頁中用 `<a href=blob download>` 存到下載資料夾，再用 take1.py 搬進 art/raw。
5. 切圖：
   - 圖示：等分 4×4 格 → 依透明度裁邊 → 補成正方形 → 128×128（slice_icons.py）。
   - UI 部件：1/4 縮圖上找透明度連通塊，依列排序（slice_parts.py）。
   - 卡框靠太近時：淡光暈會連在一起，改用「不透明度 > 128 的像素最少的直欄」當切線。
6. 套進遊戲（CSS）：
   - 按鈕：`border-image: url(btn.png) 70 90 fill / 50% 30px stretch`，兩端星飾不變形。
   - 面板：`border:14px solid transparent; border-image: url(panel.png) 70 / 22px` 不加 fill，保留原本半透明背景（`background-clip: padding-box`）。
   - 彈窗標題：緞帶當 h2 背景，`width: max-content`。
   - 卡框：`.cc::after` 疊框圖，`inset` 往外推 5–9%（SSR 頂部皇冠要多推），`.cc` 改 `overflow: visible`。
   - 貨幣：符號換成 `<i class="ci gem">`，背景圖 contain；`textContent` 寫入的地方改 `innerHTML`。
7. 驗證：fetch 每張圖確認 200、檢查所有 img 有 naturalWidth、檢查元素沒有超出 app 寬度。

## 陷阱

- ChatGPT 偶爾顯示「帳戶已變更，請重新傳送」，或模式掉回 Instant；送出前確認、出錯就重送。
- Chrome 無頭截圖在 Windows 最小視窗寬約 500px，手機寬度要用 iframe 375px 包起來截。
- 無頭截圖的 virtual-time-budget 太短時，圖片會顯示成破圖，不代表檔案壞掉。
- 第一批圖滿意後，存起來當之後補圖的風格參考。

## 什麼時候用（下次調用關鍵字）

遊戲圖示、同風格圖示、UI 套件、按鈕圖、面板框、卡框、稀有度框、border-image、9-slice、GPT 生圖示、切圖腳本、星詠契約
