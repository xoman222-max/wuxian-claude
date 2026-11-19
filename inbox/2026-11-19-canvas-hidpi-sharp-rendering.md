# Canvas／PixiJS 全螢幕不模糊：提高繪製解像度（RPG Maker MZ 實測）

- 日期：2026-11-19
- 類型：方法庫
- 標籤：canvas、PixiJS、devicePixelRatio、高解析度、Retina、模糊、RPG Maker MZ、ツクールMZ、效能、網頁遊戲
- 主題卷：09
- 來源：X 使用者 kotonoha*（@rahaandsary）2026-11-18 的 5 則串文（使用者貼上），https://x.com/rahaandsary/status/2122969085273362495
- 狀態：原作者在 M2 上實測；2026-11-19 套用到星詠契約的召喚畫布並驗證（375 寬、DPR 2 → 畫布 750×1624）。

## 一句話摘要

遊戲先畫在「遊戲解析度」的 canvas，再用 CSS 拉伸到螢幕，非整數倍（如 1280×720 → 1080p 的 1.5 倍）就會糊；解法是讓 canvas 的實際像素 = 顯示大小 × devicePixelRatio，遊戲內座標維持不變。

## 原理

- MZ（PixiJS）流程：在 1280×720 的 canvas 畫 → CSS 放大到視窗。1.5 倍會插值，字和像素都糊。
- 倍率 k = 拉伸倍率 × devicePixelRatio。
- PixiJS：`renderer.resolution = k; renderer.resize(w, h)` → canvas 實際尺寸變 k 倍，遊戲座標不變。MZ 會用 canvas.width 決定 CSS 尺寸，那裡要改成用邏輯尺寸。
- 文字的 Bitmap（2D canvas）同倍率：
  1. canvas 建成 寬×k、高×k
  2. `ctx.setTransform(k,0,0,k,0,0)`
  3. `new PIXI.BaseTexture(canvas, {resolution: k})`
  4. 讓 width／height 回傳邏輯尺寸，繪圖程式碼就不用改。

## 陷阱（原作者踩過的）

- `getImageData`／`putImageData` 不吃 transform → 那張圖要退回等倍處理。
- `shadowBlur` 不吃 transform → 要自己乘 k。
- `PIXI.Filter` 的 resolution 也要設成 k。
- 1.5 倍時奇數座標會落在半像素，又變糊 → 頂點要對齊到裝置像素（四捨五入）。

## 成本

- 成本跟像素數成正比，也就是 k²。M2 實測地圖一幀：1 倍 6.7ms → 1.5 倍 9.8ms → 2 倍 14.4ms → 3 倍 20.3ms。全螢幕濾鏡越多，差距越大。
- Retina 開發機上看不太出差別；Windows 的 1080p 螢幕效果最明顯。
- 建議做成「有上限」的選項。

## 純 2D canvas 範本（星詠契約版）

```js
const CVK = Math.min(devicePixelRatio || 1, 2);   // 上限 2，避免 3x 手機畫 9 倍像素
function sizeCv(){ cv.width = Math.round(cv.clientWidth*CVK); cv.height = Math.round(cv.clientHeight*CVK); }
// 所有線寬、半徑、shadowBlur 都 × CVK
ctx.shadowBlur = 40 * CVK;
window.addEventListener('resize', sizeCv);
```

## 套用紀錄

- 星詠契約（D:\claude\star-oath）：召喚演出的 #sumCanvas 原本已經乘 devicePixelRatio，但 shadowBlur 寫死 40（高解析螢幕上流星光暈變小），也沒有上限。已改成 CVK = min(DPR, 2)，shadowBlur 一起乘。其他畫面是 DOM／CSS 圖片，瀏覽器自己會用裝置解析度畫，不受影響。
- 灰燼燈籠（cinderfall）：像素遊戲刻意用 160×120 放大 + image-rendering: pixelated，不適用這招。

## 什麼時候用（下次調用關鍵字）

canvas 模糊、全螢幕模糊、devicePixelRatio、HiDPI、Retina、PixiJS resolution、RPG Maker MZ 模糊、ツクールMZ ぼやける、shadowBlur 高解析、canvas 效能
