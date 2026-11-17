# 落沙像素模擬（Noita 技術）

- 日期：2026-11-17
- 類型：方法庫
- 標籤：程序模擬、cellular automata、falling sand、Noita、像素物理、效能
- 主題卷：09
- 來源：GDC 2019 Petri Purho〈Exploring the Tech and Design of Noita〉https://gdcvault.com/play/1025695/Exploring-the-Tech-and-Design （影片 https://www.youtube.com/watch?v=prXuyMCgbTc ，多執行緒段落約 9:20）；80.lv 報導 https://80.lv/articles/noita-a-game-based-on-falling-sand-simulation/ ；參考實作 https://github.com/MathExpert/GodotSand 、https://github.com/BradFitz66/BeefSand
- 狀態：2026-11-17 查證（二手報導，未看完原片）。

## 一句話摘要

每個像素是一種材料（沙、水、油、火、石），每格依簡單規則跟鄰居交換位置；靠分塊、只更新有變動的區域、棋盤式分批更新，才撐得起大世界。

## 核心內容

- 規則範例：沙往下，下方被擋就往左下／右下；水同上再加左右流；火會點燃可燃鄰格並隨機熄滅；氣體往上。
- 更新順序：由下往上掃，否則同一格一幀會掉好幾格。左右掃描方向每幀交替，避免往一側偏。
- 分塊（chunk）：世界切成 64×64 之類的塊，各塊記錄「髒矩形」，沒變動的塊整個跳過。
- 多執行緒：棋盤式分四批更新，相鄰的塊不同時跑，執行緒不會互搶像素。
- 剛體：會被破壞的物件用剛體物理，每個像素記住相對碰撞盒的座標，旋轉時不丟像素。

## 可重複使用的規則或模板

1. 網頁小遊戲：用 Uint8Array 存材料 ID，ImageData 直接寫顏色，320×180 解析度放大顯示就夠快。
2. 材料用表驅動：{密度, 可燃, 液體, 顏色變化}。新材料只加一列。
3. 每幀只處理髒矩形；靜止的沙堆不花 CPU。
4. 先做 4 種材料（沙、水、石、火）確認好玩，再加。
5. 玩法鉤子：玩家的能力是「放一種材料」或「把某種材料變成另一種」，跟化學引擎卡可直接合用。

## 什麼時候用（下次調用關鍵字）

落沙、falling sand、Noita、像素模擬、cellular automata、可破壞地形、粉末遊戲
