# 每日種子加無劇透分享格（Wordle 式）

- 日期：2026-11-17
- 類型：方法庫
- 標籤：留存、病毒傳播、每日挑戰、種子、分享、Wordle、網頁遊戲
- 主題卷：09
- 來源：https://www.gamedeveloper.com/marketing/josh-wardle-reflects-on-the-the-unconventional-road-to-wordle-s-success ；https://danmeyer.substack.com/p/why-wordle-works-according-to-desmos ；https://www.moengage.com/blog/wordle-viral-growth-story/
- 狀態：2026-11-17 查證。成長數字（約 90 人到 200 萬日活）為二手資料。

## 一句話摘要

一天一題、全世界同一題，加上一鍵複製「不劇透的 emoji 結果格」，就同時做到稀缺感、話題和免費傳播。

## 核心內容

- 稀缺：一天只能玩一次，作者說這讓人「意猶未盡」。
- 同題：大家玩同一關，結果才值得比較和貼出來。
- 分享格：只顯示表現、不顯示答案，可以貼在任何地方。分享功能是後來才加的。
- 連勝：休閒玩家看不到壓力，重度玩家可以追。
- 格式可複製：NYT 之後用同格式做了多款遊戲。

## 可重複使用的規則或模板

1. 種子 = 日期字串（UTC，例如 "2026-11-17"）雜湊成整數，餵給可重現的亂數（mulberry32、sfc32）。
2. 所有隨機（地圖、敵人、掉落）只吃這個種子，保證每人同一局。
3. 結算頁一個「複製結果」按鈕，內容：遊戲名 + 日期編號 + 5–8 個 emoji 的表現圖 + 網址。
4. 本機存連勝和歷史（localStorage，記得 try/catch）。
5. 另外保留「練習模式」用隨機種子，滿足想多玩的人，但每日只算一次。
6. 小遊戲比賽的封面或截圖可以直接拿分享格當視覺。

## 什麼時候用（下次調用關鍵字）

Wordle、每日挑戰、daily seed、每日關卡、分享結果、emoji 格、病毒傳播、留存設計
