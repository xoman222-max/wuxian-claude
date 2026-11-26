# OpenGame（nexu-io）：AI 代理遊戲工作室平台拆解

- 日期：2026-11-26
- 類型：工具＋方法庫
- 標籤：AI 遊戲生成、Claude Code、Codex、MCP、Three.js、HTML5 遊戲、遊玩測試、數值模擬、遙測、隱私
- 主題卷：09
- 來源：https://github.com/nexu-io/opengame （README、install.sh、.mcp.json、skills/、tracking/README.md 與 tracking/*.ts）
- 狀態：2026-11-26 查證。Apache-2.0，約 380 星，2026-11-25 才建立，更新很快。沒有安裝、沒有實際跑過。
- 決定：不安裝。理由見下方「為什麼不裝」。

## 一句話摘要

把 Claude Code、Codex 等程式代理變成「遊戲工作室」的開源平台：本機 Game Studio 網頁介面＋12 個 MCP 工具＋25 個可改的 HTML5／Three.js 遊戲範本；最值得學的是它的驗證流程，不是平台本身。

## 核心內容

- 組成：本機 Studio 介面、stdio MCP 伺服器（12 個 `openmotion_game_*` 工具）、6 個 skill（opengame 入口、openmotion-game 遊戲流程＋18 本參考手冊、design、media、video、openmotion）。
- 輸出：純 HTML5／Canvas 與內建 Three.js 的原始碼資料夾，附設計文件。微信、抖音、TikTok、itch.io 一鍵發佈還在路線圖，目前要手動包裝。
- 範本：README 列 25 個原創範本；標語裡的「100+ 爆款可改」和「Top 100 Profitable」是路線圖，還沒出。
- 安裝：install.sh 需要 git、Node 22.18+、npm、Codex CLI，淺層複製到 `~/.local/share/opengame` 後執行安裝腳本；手動方式是 `npm ci && npm run build:studio && npm start`。
- 金鑰：本機可零金鑰運作；可選自帶金鑰串接生圖（GPT Image、Nano Banana、FLUX 等）、音樂（ElevenLabs、Suno）、語音、影片（Wan、Seedance）。分享連結走 OpenDesign Cloud，另有付費方案。

## 為什麼不裝（2026-11-26 查證原始碼）

- **遙測預設開啟**：tracking/README.md 寫明「在所有環境和版本預設開啟」，送到 PostHog，綁定安裝 ID 與雜湊後的裝置 ID。
- **對話紀錄也會送**：Codex 呼叫它的 MCP 時，會把去敏後的使用者提問（上限 8,000 字）與助理回覆（上限 6,000 字）以 `$ai_generation` 事件送出。去敏會清掉 API 金鑰、Token、網址、Email、本機路徑，但內容本身仍會上傳。
- 關閉方式：環境變數 `OPENMOTION_TELEMETRY=0` 或 `DO_NOT_TRACK=1`（優先），或在 Studio 的「Privacy & data」關掉。
- 單獨的 openmotion-game skill 做遊戲時要呼叫它的 MCP 工具，沒有整套平台用不了；而本機已經有大量遊戲 skill。
- 專案才一天大，變動很快。

如果將來要試：先設 `DO_NOT_TRACK=1`，在獨立資料夾安裝，並讀過 `scripts/install-motion.command`。

## 可重複使用的技巧（值得學）

1. **規則與美術分離**：引擎邏輯放在確定性的 `logic.js`，美術與主題另外換皮。換主題不會改到玩法。
2. **validate 冒煙測試**：每個遊戲跑 50 個 tick 的自動測試，抓 NaN、例外、卡死。
3. **三檔數值模擬**：參考玩家、弱玩家、掛機三種行為，無頭跑關卡看是否過得了、會不會太快。
4. **手機尺寸無頭遊玩測試**：無頭 Chromium 用 390×844 實際玩一輪。
5. **自動拍封面與預告片**：腳本截圖＋FFmpeg 合成。
6. **每款遊戲固定四份文件**：`design/plan.md`（玩法）、`style.md`（美術風格）、`assets.csv`（素材清單）、`verification.md`（驗證紀錄）。

## 對照星詠契約（D:\claude\star-oath）

- 已做到：規則與畫面分離（tools/battle_core.js）、數值模擬（battle_sim.js，6 種隊伍）、無頭實機截圖（cdp_shot.js＋shot.html）、提示詞文件（prompts.md、icon_prompt.md）。
- 可以補：
  - 冒煙測試：每次改版後自動跑完 24 關＋14 位角色大招，檢查沒有 NaN、例外、卡死。
  - assets.csv：列出每張圖的用途、來源提示詞、尺寸，之後補圖或換風格比較好管。
  - 預告片：用 cdp_shot 逐格截圖＋FFmpeg 合成 15 秒宣傳影片，上架平台用得到。

## 什麼時候用（下次調用關鍵字）

OpenGame、opengame、OpenMotion、AI 遊戲工作室、AI 生成遊戲平台、遊戲 MCP、遊戲範本、遙測、DO_NOT_TRACK、冒煙測試、遊玩測試、預告片自動化
