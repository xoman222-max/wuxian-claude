# Game UI Database：遊戲介面截圖資料庫與抽卡 UI 參考路線

- 日期：2026-11-19
- 類型：工具＋方法庫
- 標籤：遊戲 UI、UX、參考資料、抽卡、gacha、HUD、選單、介面設計
- 主題卷：09
- 來源：https://www.gameuidatabase.com/ （作者 Edd Coates）
- 狀態：2026-11-19 在瀏覽器查看首頁與分類選單。一般網頁抓取會被擋（403），瀏覽器可正常瀏覽；本次深入分類頁的導覽被瀏覽器政策擋下，沒看到抽卡分類內的遊戲清單。
- 授權：截圖是各遊戲公司的作品，只能當參考，不能直接拿來用在自己的遊戲或宣傳。

## 一句話摘要

收錄約 2,001 款遊戲、79,925 張介面截圖和影片的資料庫，依「畫面類型」細分上百類，可以直接找到「抽卡揭曉」「每日獎勵」「商店確認購買」這類畫面的業界做法。

## 核心內容

- 規模（2026-11-19）：2,001 款遊戲、79,925 張截圖，每天更新一款；部分遊戲有影片。
- 附帶：作者的《The Game UI Bible》預購中；同作者的 PadCrafter 2.0（手把按鍵配置圖工具）。
- 用法：首頁 → Browse Screen Categories，用網址參數 `index.php?scrn=<編號>` 篩畫面類型；`set=1` 看截圖、`set=0` 看遊戲、`vid=1` 只看影片。

### 與抽卡遊戲相關的分類編號

| 需求 | 分類 | scrn |
|---|---|---|
| 抽卡總覽 | All Gachas, Crates & Boosters | 125 |
| 卡池選擇與付費 | Purchase & Selection | 177 |
| 抽卡揭曉演出 | Reveal | 178 |
| 抽到的獎勵總表 | Prizes & Rewards | 179 |
| 簽到、每日獎勵 | Daily and Timed Rewards | 124 |
| 獎勵階梯、通行證 | Rewards Ladder／All Season Pass & Events | 123／175 |
| 商城、禮包、貨幣商店 | Premium Store／Offers & Bundles／Currency Store | 121／126／122 |
| 任務、成就 | Missions and Quests／Challenges & Achievements | 81／82 |
| 圖鑑 | Collectables Menu／Gallery Menu／Gallery & Concept Viewer | 94／129／127 |
| 角色介紹、角色選擇 | Character Intro／Character Select | 105／41 |
| 升級、突破 | All Upgrading & Ranking Up／Inspect & Confirm | 73／97 |
| 彈窗 | All Modals & Popups／Item Get | 902／33 |
| 新功能解鎖 | Progress/Feature Unlocked | 101 |
| 新手引導 | Guided Tutorial | 152 |
| 公告、通知 | Updates, News & Notifications | 102 |
| 手機操作 | Mobile Controls | 147 |

## 可重複使用的規則

1. 做任何新畫面前，先在對應分類看 5 到 10 款同類遊戲，記下共通的資訊層級（什麼最大、什麼放角落），不要抄外觀。
2. 抽卡畫面重點檢查清單（從分類結構推導）：卡池選擇、單抽／十連價格、保底進度、機率說明入口、揭曉演出、獎勵總表、重複轉換說明。
3. 每日獎勵：連續天數格、今天高亮、已領打勾、第 7 天大獎特別放大。
4. 商店：價格用貨幣圖示＋數字；確認購買彈窗要重述「花多少、得到什麼」。
5. 截圖只當參考，不能放進遊戲、宣傳圖或訓練資料。

## 套用到星詠契約（2026-11-19）

已有：召喚頁（雙卡池、單抽／十連、保底、機率說明、召喚紀錄）、揭曉演出、結果總表、簽到 7 天、任務、圖鑑、星塵商店、派遣。
對照分類後的待補項目：
- 卡池選擇（177）：卡池剩餘時間倒數、UP 角色縮圖列。
- 獎勵階梯（123）：累計召喚次數獎勵。
- 新功能解鎖（101）：例如第一次解鎖派遣時的提示彈窗。
- 新手引導（152）：第一次進入時，帶玩家完成第一次召喚。
- 公告（102）：活動公告頁。
- 角色詳情（105）：技能、好感度劇情、語音列表。

## 什麼時候用（下次調用關鍵字）

Game UI Database、遊戲 UI 參考、介面設計參考、抽卡 UI、gacha UI、每日獎勵介面、商店介面、彈窗設計、HUD 參考、Edd Coates
