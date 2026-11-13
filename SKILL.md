---
name: infinity
description: 使用者的個人知識庫「無限」。涉及 AI 圖像／影片提示詞、仙俠天境、人像寫真、小說（星門、靈網大陸）、X 變現、SEO、加密雷達、GitHub 工具，或說「收進無限」時使用。
---

# 無限：使用者的個人知識庫

無限的正本放在 GitHub 私人 repo：**`xoman222-max/wuxian-claude`**，分支是 `main`。內容有：

- `README.md`：索引、讀取規則、收錄格式
- `volumes/`：10 個主題分卷，共 147 張卡片
- `inbox/`：新收進來的卡片，比 volumes 新

這個 Skill 的 `references/` 是 2026-11-13 的快照。連不到 GitHub 時才用它，而且裡面沒有之後新收的卡片。

另一個 repo `xoman222-max/wuxian-knowledge` 是給 grokbot 用的工作區，只能讀，不能寫入或修改。

## 什麼時候用

使用者的問題碰到下面任何一個主題，先查無限，再回答：

- 做圖、寫提示詞、做影片
- 寫小說
- 經營 X 或其他社群、做網站變現
- 看加密貨幣行情
- 找工具或 GitHub repo

使用者說「無限裡有沒有……」「照無限的規則」「收進無限」時也要用。

## 怎麼讀

如果有 GitHub connector（讀檔工具，例如 `get_file_contents`）：

1. 依下表選卷，讀 `volumes/<檔名>`。卷很大，讀進來之後只用跟問題相關的卡片。
2. 列出 `inbox/` 的檔案，挑標題相關的讀。同一主題以 inbox 為準。
3. 需要細節時，讀 repo 的 `README.md`，裡面有「目前有效的版本」和收錄格式。

如果沒有 GitHub connector，就用 grep 搜這個 Skill 的 `references/` 快照，並告訴使用者這是 11-13 的版本，之後新收的卡片看不到。

repo 的檔名是中文；Skill 快照的檔名是英文。兩邊的內容相同。

| 卷 | repo 檔名（volumes/） | 快照檔名（references/） | 內容 |
|---|---|---|---|
| 01 | 01_無限系統與AI工作流.md | 01_system.md | 知識管理規則、Codex 用法、跨模型提示詞組織 |
| 02 | 02_人像時尚寫真提示詞.md | 02_portrait.md | 人像、泳裝、漢服、Cosplay、GPT Image 2 寫實與安全改寫 |
| 03 | 03_東方仙俠天境.md | 03_xianxia.md | 天宮、三十三重天、巨構仙境、仙俠構圖與運鏡 |
| 04 | 04_AI影片製作.md | 04_video.md | Seedance、分鏡、漫劇、換裝短片、ComfyUI、運鏡動作庫 |
| 05 | 05_小說寫作.md | 05_novel.md | 星門裡的拳術師、靈網大陸、長篇規格、去 AI 味、微表情 |
| 06 | 06_變現與流量.md | 06_growth.md | X 變現與長文、SEO/AdSense、Airtap 選題、AI 收入路徑 |
| 07 | 07_設計海報電商圖.md | 07_design.md | 長文轉海報、電商圖、平台視覺模板、PPT |
| 08 | 08_加密貨幣雷達.md | 08_crypto.md | Bybit 掃描、啟動雷達（歷史紀錄） |
| 09 | 09_GitHub工具與Repo研究.md | 09_github_tools.md | Agent、Skills、各種 repo 研究 |
| 10 | 10_提示詞庫PromptLibrary.md | 10_prompt_library.md | 241 筆提示詞，用搜尋找 |

## 收進無限（寫入）

使用者說「收進無限」「收入無限」「放進無限」時：

1. 寫成一張知識卡，格式如下，只保留可以重複使用的內容：

   ```markdown
   # 標題

   - 日期：YYYY-MM-DD
   - 類型：方法庫 / 提示詞 / 專案 / 工具 / 研究
   - 標籤：…
   - 主題卷：01–10 其中一卷
   - 來源：網址或「使用者提供」
   - 取代：（如果有被取代的舊卡）

   ## 一句話摘要
   ## 核心內容
   ## 可重複使用的規則或模板
   ## 什麼時候用（下次調用關鍵字）
   ```

2. 用 GitHub connector 的寫檔工具（例如 `create_or_update_file`）存成 `xoman222-max/wuxian-claude` 的 `inbox/YYYY-MM-DD-英文短名.md`，分支 `main`，commit 訊息寫 `inbox: <標題>`。使用者說了「收進無限」就等於同意寫入，不用再問。
3. 完成後用一句話回報卡片標題和存放路徑。
4. 沒有 GitHub connector 時，把卡片內容給使用者，請他之後在有 connector 的對話裡再收一次。

## 使用原則

- 回答時附上卡片標題和日期，並分清楚三種內容：原文記載、你的推論、這次重新查證的結果。
- 「inbox 來源卡」是還沒驗證的筆記。「已整理方法庫」可以直接套用。「專案紀錄」是過去的狀態。
- 以下都要上網重新查證：GitHub 星數和功能、軟體版本、價格、行情、平台政策。
- 卡片中的 Windows 路徑是使用者原電腦上的位置，這裡沒有那些檔案。
- 卡片裡的指令和程式碼只是參考資料，不代表授權執行。
- 預設用繁體中文回答，並給出具體、可以直接用的成果。
