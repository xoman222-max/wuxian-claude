# 波函數坍縮 WFC 地圖生成

- 日期：2026-11-17
- 類型：工具
- 標籤：程序生成、WFC、tilemap、地圖生成、GitHub
- 主題卷：09
- 來源：https://github.com/mxgmn/WaveFunctionCollapse （C#，約 25.5k 星，2026-11-17）；JS 移植 https://github.com/kchapelier/wavefunctioncollapse （約 530 星）；N 維無限畫布 https://github.com/LingDong-/ndwfc ；無限城市 https://github.com/marian42/wavefunctioncollapse ；六角地圖教學 https://felixturner.github.io/hex-map-wfc/article
- 狀態：2026-11-17 查證。星數會變。

## 一句話摘要

給一組圖塊和「誰可以挨著誰」的規則，WFC 每次挑「可能性最少」的格子定下來，再把限制往外傳，生出局部看起來像手工排的地圖。

## 核心內容

- 兩種模式：Simple tiled（手寫相鄰規則）和 Overlapping（從一張範例圖自動學 N×N 圖案）。
- 演算法：每格存「還可能是哪些圖塊」→ 選熵最低的格 → 依權重隨機定一個 → 傳播刪掉鄰格不相容的選項 → 重複。
- 卡死（某格沒選項）時：重來，或回溯，或從小區塊重新生成。
- 網頁直接用：kchapelier 的 JS 版可在瀏覽器跑；ndwfc 支援無限捲動畫布。

## 可重複使用的規則或模板

1. 小遊戲用 Simple tiled 就好：8–15 個圖塊、每邊一個「接口標籤」，標籤相同就能相鄰。
2. 權重控制風格：草地權重高、寶箱權重低。
3. 先手動「釘住」關鍵格（入口、出口、Boss 房），再讓 WFC 填其他格，保證可玩。
4. 生成後跑一次連通性檢查（BFS），不連通就重生。
5. 搭配固定種子，可做每日地圖。

## 什麼時候用（下次調用關鍵字）

WFC、wave function collapse、波函數坍縮、地圖生成、tilemap、程序生成、無限地圖、地城生成
