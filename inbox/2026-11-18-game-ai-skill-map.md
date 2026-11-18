# 遊戲 AI Skill 與 repo 地圖（含已安裝對照）

- 日期：2026-11-18
- 類型：工具
- 標籤：Claude Code、Agent Skills、遊戲開發、three.js、Blender、精靈圖、3D 動畫、效能、Agent-Reach
- 主題卷：09
- 來源：使用者提供的兩份清單；2026-11-18 用 GitHub API 逐一查證存在與星數
- 狀態：27 個 repo 都還在。星數是 2026-11-18 的數字，會變。
- 相關：2026-11-17-game-animation-tool-repos（3D 動作工具）

## 一句話摘要

遊戲 AI 工具鏈（素材 → 玩法 → 介面 → 手感 → 測試 → 效能 → 聯機）大多已被本機裝的 skill 覆蓋；2026-11-18 只補裝了 game-perf 和 game-design-theory，其他留作參考。

## 這次安裝的（本機 ~/.claude/skills）

| Skill | 來源 | 用途 | 備註 |
|---|---|---|---|
| game-perf | gykim80/andrew_game_perf（12★），commit d0976ee | 掃出 10 種掉幀寫法並修正：迴圈裡的 .find()、每幀 new 物件、Three.js 沒 dispose、沒用物件池、可變時間步長物理等 | 只裝 SKILL.md，references 指向 GitHub |
| game-design-theory | pluginagentmarketplace/custom-plugin-game-developer（53★），commit aa7edfe | MDA、心流、Bartle 玩家類型、獎勵排程、「無聊／挫折／單一最佳解」的排錯表 | 內容偏入門教科書，附帶的 script 和 guide 只是空殼，沒裝 |

## 已經有同類 skill，不用裝

| 清單項目 | 星數 | 本機已有的對應 |
|---|---|---|
| gamedev-skills/awesome-gamedev-agent-skills（game-feel 等 79 個 skill） | 9.3k | game-feel、game-ui-ux、godot、web-engines 等，很可能就是這套 |
| MengTo/Skills（戰鬥動畫、怪物系統、關卡、遊玩測試） | 7.7k | game-dev-combat-animation、build-game-monster-system、author-game-levels、test-playable-web-games |
| majidmanzarpour/threejs-game-skills（threejs-game-director） | 2.8k | optimize-threejs-games、ship-web-games、build-mobile-threejs-games 等 |
| EL4CTEO/blender-skills（Blender 5.3，28 個） | 2.0k | 本機約 28 個 blender-* skill |
| aldegad/sprite-gen（同角色多姿勢精靈圖） | 4.1k | agent-sprite-forge（generate2dsprite、video2dsprite）、pixelbolt |
| github/awesome-copilot 的 game-engine | 41k（整個 repo） | web-engines 系列 |
| omer-metin/skills-for-antigravity 的 game-ui-design | 216 | game-ui-ux |
| openai/skills 的 develop-web-game（歷史 commit 0ed635a） | 28.8k（整個 repo） | test-playable-web-games ＋ 瀏覽器面板。「4/23 從 curated 移除」未查證 |

## 留作參考，現在不裝

### 引擎與大型框架（目前做網頁小遊戲，用不上）
- Jeffallan/claude-skills（12.4k）：其中 game-developer 偏 Unity／Unreal。
- Unity-Technologies/skills（1.3k）：Unity 官方 skill，建專案、建置、套件管理。
- OpenDCAI/GameFactory-3A（1.3k）：需求 → 圖、3D、動作、音效 → UE5／Unity／Godot／three.js 程式碼。很重。
- scenario-labs/skills（3.9k）：透過 Scenario MCP 生圖、影片、3D，另有操作 Blender、Maya、ZBrush、Unreal、Unity 的專家團隊。需要 Scenario 帳號。
- higgsfield-ai/skills（2.0k）：higgsfield-websites 生素材並搭建、部署網頁遊戲；舊的 higgsfield-game-generation 已併入。需要 Higgsfield 帳號。

### 企劃與流程
- eremes81/game-design-ai-practice（117）：24 年資歷企劃寫的書（韓文原稿，CC BY-NC-SA 4.0），戰鬥、數值、關卡章節可挑讀。是書不是 skill。
- dudwns0921/claude-gamedev-kit（10★，78 個未解 issue）：說一句話就產出規格、設計、建置，附儀表板。很新、不成熟。

### 網頁 3D 與範例
- viettranx/3dviz-pro-max（1.4k）：一行想法 → 可走動的 Three.js／Blender 場景，223 個配方。
- lovisdotio/video-to-game（631）：遊玩影片 → 分析影格 → 瀏覽器遊戲。需要 fal API 金鑰（付費）。
- achrefelouafi/LinearAbiltyCastingThreeJS（1.2k）：手寫 shader 的 MOBA 式技能施放沙盒，學特效程式碼用。
- boona13/mykonos-island-voxels（1.1k）：14×14 等距方塊島嶼建造，原生 ES modules、手機可用。參考建造系統。

### 2D 像素
- handsupmin/mono-pix（161）：把 AI 假像素圖修成真像素格。瀏覽器免費工具，不用安裝。

### 3D 動作與動畫（另見 2026-11-17-game-animation-tool-repos）
- MaxLiu22/Motion2MixamoRig（2.0k）：影片或照片的人體動作 → Mixamo 角色，有 Blender 外掛版。
- Friedrich-M/UniMate（2.7k，SIGGRAPH Asia 2026）：一行文字驅動不同骨架（人、四足、鳥、蛇），可放自己的 GLB／FBX。
- alchaincyf/3d-vibe-coding-handbook（316）：中文 386 頁手冊，圖生 3D → 減面 → 綁骨 → 動畫，有依症狀分類的索引。

### 聯機
- rivet-dev/skills（53）：multiplayer-game 只在歷史 commit ba5d3db，主分支已移除；依賴要自己核對。

### 讓代理讀社群平台
- Panniantong/Agent-Reach（112.8k）：一個 CLI 讓代理搜尋和讀取 X、Reddit、YouTube 字幕、B 站、小紅書、V2EX、雪球、GitHub。只讀不發文。
  - 風險：要登入的平台會把你 Chrome 裡該網站的登入複製到它的專用瀏覽器，作者建議用小號。會裝 uv 和多個上游工具到 ~/.agent-reach/。
  - PyPI 上同名的 agent-reach 不是本專案，只能用 GitHub 的 install.md 安裝。
  - 2026-11-18 決定先不裝；需要抓社群內容收進無限時再評估。

## 可重複使用的規則

1. 看到新的 skill 清單，先對照本機已裝的，重疊就不裝。
2. 安裝前完整讀過 SKILL.md；用 commit 固定版本下載，並比對雜湊。
3. 會複製登入、裝背景瀏覽器、要付費 API 金鑰的工具，先收進無限，不主動安裝。
4. 歷史 commit 版、被移除的 skill，除非真的需要，否則不用。

## 什麼時候用（下次調用關鍵字）

遊戲 skill、game skills、Claude Code 遊戲開發、three.js skill、Blender skill、精靈圖 skill、掉幀、效能、game-perf、遊戲設計理論、Agent-Reach、讀小紅書、讀推特、多人聯機 skill
