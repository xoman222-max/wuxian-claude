# 無限｜GitHub工具與Repo研究

範圍：各種 GitHub repo／工具研究筆記

排序：先放已整理的方法庫（libraries/projects），其餘 inbox 卡片由新到舊。同主題有多個版本時，以較新的為準。

## 本卷目錄

- 2026-08-12｜TapXWorld ChinaTextbook 中國教材 PDF 資源庫
- 2026-08-01｜Mr-funny / hbg-gemini-flow-suite
- 2026-06-27｜EverMind-AI EverOS
- 2026-06-15｜GitHub AI Resource Map
- 2026-06-14｜yaojingang/yao-open-prompts
- 2026-06-01｜notebooklm-py repo intake
- 2026-05-23｜AI 相關 GitHub 資源索引：提示詞、副業、字幕翻譯、中文 LLM、Repo AI 讀懂
- 2026-05-23｜GitHub 非程序員挖寶方法與資源路徑索引
- 2026-05-23｜PicList：雲端儲存與圖床管理工具
- 2026-05-22｜huangserva/3DCellForge：AI 圖生 3D 互動工作台
- 2026-05-22｜LingyiChen-AI/boris-prompts：AI Agent 任務 Prompt 壓縮與改寫 Skill
- 2026-05-21｜msitarzewski/agency-agents 筆記
- 2026-05-21｜多 Agent 團隊復刻 3D 細胞教學 Demo 工作流
- 2026-05-14｜2026-05-14 LearningCell Research Note
- 2026-05-12｜2026-05-12 GenericAgent Research Note
- 2026-05-12｜2026-05-12 OpenCLI Research Note


---

## TapXWorld ChinaTextbook 中國教材 PDF 資源庫

- 原路徑：`inbox/2026-08-12-tapxworld-chinatextbook.md`
- 日期：2026-08-12（依檔名）
- 類型：inbox 來源卡（未驗證）

# TapXWorld ChinaTextbook 中國教材 PDF 資源庫

Source: https://github.com/TapXWorld/ChinaTextbook
Verified: 2026-08-12
Snapshot commit: `5a80345f2043ba6f8db8d7be9cf3db82725ff1f7`（2025-10-18）
Type: repo_tool
Tags: 無限, ChinaTextbook, 中國教材, PDF教材, 小學, 初中, 高中, 大學, 人教版, 五四學制, 數學, 教材索引, 著作權
Tool Potential: high
Prompt Library Impact: no
Use When: 需要查找中國小學、初中、高中、五四學制或大學教材 PDF，做個人學習、教材摘要、章節定位、題目解析、課程規劃，或判斷教材再利用邊界時。

## 一句話摘要

大型中國教材 PDF 聚合倉庫，技術上可供個人查閱、選書、下載與文本分析；但倉庫沒有授權條款，教材本身通常仍受出版社與作者權利保護，不應把「GitHub 公開」理解為可自由重製、再發布、商用或訓練模型。

## 核心內容

- 倉庫：`TapXWorld/ChinaTextbook`，公開、未封存，預設分支 `master`。
- GitHub API 快照：倉庫 size 約 `43,543,927 KiB`，約 41.5 GiB；不適合為一般查詢完整 clone。
- 根目錄包含：`小学`、`小学（五•四学制）`、`初中`、`初中（五•四学制）`、`高中`、`大学`、數學習題資源與 README。
- 小學可見學科包含語文、數學、英語、科學、道德與法治、音樂、美術、體育與健康等；大學目錄明確包含高等數學、線性代數、離散數學、概率論。
- README 提供小學至高中人教版數學及大學數學的快速連結。
- PDF 超過 GitHub 單檔限制時可能拆為 `.pdf.1`、`.pdf.2` 等；README 指向 `ChinaTextbook-tools` 的合併工具。執行第三方 EXE 前應另行檢查來源與雜湊；也可用可信的位元組合併方式還原。
- 倉庫 API 回報 `license: null`，根目錄未見 LICENSE；README 說「開源」與教育公益目的，但沒有授予可重製、改作、再散布或商用的明確法律許可。

## 這裡面的書可以怎麼用

### 通常可採低風險方式使用

- 個人閱讀、學習、研究與欣賞。
- 針對一本書或一章做搜尋、摘要、重點整理、題目講解、讀書計畫或知識卡。
- 為介紹、評論或說明問題而適量引用，標明教材、出版社、版次、章節／頁碼與來源。
- 在學校課堂或科研的合理範圍內少量複製或使用，但不出版發行；實際情境仍須符合適用法律和機構規定。
- 只把書名、版本、科目、年級、路徑、章節索引與摘要收進無限，不保存整本 PDF。

### 不應預設有權進行

- 把整庫或整本教材重新上傳到自己的網站、雲端、App、付費會員庫或公開分享包。
- 大量複製教材正文、插圖、題目或答案，製作高度替代原書的衍生內容。
- 刪除出版社、作者、版權頁或水印後再發布。
- 把 PDF 當作已獲授權的商業 AI 訓練集、微調集、RAG 公開知識庫或可轉售素材。
- 以倉庫 README 的「開源」字樣取代逐本教材的權利查核；倉庫維護者未必是每本教材的權利人。

## 可重複使用的規則

1. 先選學段、科目、出版社、版次和冊別，再抓單本或單章；不要為一次查詢 clone 約 41.5 GiB 全庫。
2. 優先從出版社、國家中小學智慧教育平台或教育主管機關取得仍在線的官方版本；本倉庫適合作為索引與備援來源。
3. 下載前檢查是完整 `.pdf` 還是拆分檔 `.pdf.N`，並驗證合併後 PDF 可開啟、頁數合理。
4. 分析時保留來源鏈：repo URL、commit、相對路徑、出版社、版次、冊別、頁碼、存取日期。
5. 對外內容以摘要、解題與評論為主，引用保持必要且適量；避免輸出可替代整本教材的內容。
6. 商用、公開發布、模型訓練或大規模資料庫用途，必須另查每本書的權利人與授權；無授權即不做。

## 可轉成工具/詞庫的部分

- 教材目錄索引器：解析 Git tree，建立 `學段 / 學科 / 出版社 / 年級 / 冊別 / 路徑 / 大小` 清單。
- 單本擷取器：只下載指定教材或指定 `.pdf.N` 分片，避免完整 clone。
- PDF 合併與校驗器：依序合併分片，檢查 PDF header、頁數、雜湊與檔名。
- 教材 RAG：限本地、私人、按需索引，並保留出處；對外部署前先取得內容授權。
- 章節學習器：產生章節摘要、觀念卡、練習題解說與複習計畫，不複製整章原文。

## 對目前專案的用法

- 無限只保存本知識卡與來源路由，不複製 PDF 本體。
- 後續可說：「用 ChinaTextbook 找人教版七年級數學上冊」「把指定教材做章節索引」「用這一章出複習計畫」。
- 若要製作圖書號影片、課程網站或公開教材工具，先把用途分成私人學習、課堂使用、公開免費、商業發布或模型訓練，再依風險決定是否需要正式授權。

## 工具判斷

- 能不能本地使用：可以；建議 sparse checkout、GitHub API 或單檔 raw 下載，避免完整 clone。
- 是否需要帳號/API/付費：公開瀏覽與單檔下載通常不需帳號；大量 API 呼叫可能受速率限制。
- 是否適合接入目前網站：適合做「教材索引與跳轉」或私人分析工具；不適合未授權鏡像整本教材。
- 是否適合做成 Codex skill：若未來反覆需要，可做成「教材定位與章節學習」Skill，內建來源追蹤、單檔下載、分片合併和著作權護欄。
- 風險或限制：無倉庫授權、教材權利分散、版本可能過時、資料量巨大、部分 PDF 拆分、第三方合併 EXE 需安全審查。

## 依據與判斷邊界

- GitHub 官方說明：公開倉庫若沒有 license，預設著作權法仍適用；GitHub 使用者可查看與 fork，不等於取得廣泛重製、散布或改作權。
- 《中華人民共和國著作權法》第二十四條容許個人學習／研究／欣賞，以及課堂教學或科研中的合理、少量使用，但要求不影響作品正常使用、不不合理損害權利人利益；課堂／科研例外不得出版發行。
- 出版社或官方平台「免費提供下載／使用」仍不當然轉移著作權。具體跨境、商業、訓練或公開發布計畫應另做逐本授權查核；本卡不是法律意見。

## 下次調用關鍵字

`ChinaTextbook`, `TapXWorld`, `中國教材 PDF`, `人教版教材`, `小學課本`, `初中課本`, `高中課本`, `大學數學`, `五四學制`, `教材下載`, `教材分片合併`, `教材著作權`, `教材可以用嗎`, `無限教材庫`。


---

## Mr-funny / hbg-gemini-flow-suite

- 原路徑：`inbox/2026-08-01-mr-funny-hbg-gemini-flow-suite.md`
- 日期：2026-08-01
- 類型：inbox 來源卡（未驗證）

# Mr-funny / hbg-gemini-flow-suite

Source: https://github.com/Mr-funny/hbg-gemini-flow-suite
Date: 2026-08-01
Type: repo_tool
Tags: Google Flow, Veo, Gemini Web, AI video, browser automation, Docker, CLI, text-to-video, image-to-video, first-last-frame
Tool Potential: high
Prompt Library Impact: no
Local Status: 尚未安裝，尚未以本機 Google 帳號實測

## 一句話結論

這是一套非官方的 Docker + CLI 封裝，透過本機瀏覽器登入與網頁自動化呼叫 Gemini Web、Google Flow / Veo；能讓已有 Flow 權限的帳號以命令列生成與下載影片，但不會替帳號開通訂閱、地區、模型或額度權限。

## 能做什麼

- Flow / Veo 文生影片（t2v）。
- 首幀或首尾幀影片、參考圖影片（實際可用項目以帳號當下的 Flow UI 為準）。
- Flow 圖片文生圖、圖生圖。
- Gemini Web 圖片與影片生成。
- 統一下載到 `outputs/`，並產生 `result.json`。
- 適合由 Codex 或批次工作流呼叫，不必每次手動操作 Flow 網頁。

## 使用前提

- Windows 建議使用 Docker Desktop + Compose v2，另需 Chrome / Chromium。
- 網路必須能正常存取 Gemini 與 Flow。
- Google 帳號仍須符合 Flow 的年齡、地區、方案、模型權限及 AI credits 限制。
- 台灣列在 Google Flow 官方支援地區中，但功能仍可能依方案與帳號逐步開放。
- Gemini 與 Flow 需要分別執行一次本機瀏覽器授權：`./suite auth gemini`、`./suite auth flow`。
- 登入資料會匯入 Docker named volume `gemini-flow-suite-data`；不要分享該 volume、Chrome Profile 或 Cookie。

## 重要限制

- 不是 Google 官方 API，也不是免資格、免訂閱或免額度的替代入口。
- 依賴 Google Flow 網頁 UI 與上游 `gflow-cli`；Google 改版後可能立即失效，需要更新 selector 或版本。
- 倉庫 README 自述於 2026-07-24 驗證 Flow Veo 3.1 Lite、Nano Banana 2 與首尾幀入口，但「曾驗證」不代表持續相容。
- 專案很新：查閱時 GitHub 顯示僅 2 commits、1 star、0 forks，應視為需要審慎試用的早期工具。
- Flow 官方頁面與 Help 對免費／訂閱資格的文字可能不同步；實際可用模型、credit 成本與功能以登入後的 Flow UI 為準。

## 安全與部署建議

- 第一次部署前先更換 `.env` 的 `NOVNC_PASSWORD`，noVNC 僅綁定 `127.0.0.1`，不要暴露到公網。
- 不把 Cookie、Chrome Profile、Google 帳號資料或 Docker volume 上傳、打印或提交到 Git。
- 建議先將 `REMOVE_VISIBLE_WATERMARKS=false`、`KEEP_ORIGINALS=true`；原始 `.env.example` 的預設值相反。
- Google 官方指出 Veo / Imagen 輸出含 SynthID，部分方案影片另有可見標記。發布時應保留必要的 AI 披露並遵守平台與 Google 條款。
- 正式使用前先審查 Dockerfile、第三方 binary、AGPL-3.0 與 third-party notices，再用低權限測試帳號、小額 credits 做一次端到端測試。

## 最小驗證流程（未執行）

1. 檢查 Docker Desktop、Compose v2、Chrome 與磁碟空間。
2. clone 到 `D:\codex\projects\hbg-gemini-flow-suite`。
3. 複製 `.env.example` 為 `.env`，設新密碼並採用上述安全設定。
4. 執行 build/up/status；由使用者親自在本機瀏覽器完成 Gemini 與 Flow 登入。
5. 先跑一個 4 秒、低成本的 Flow t2v 測試，確認 credits、下載、`result.json`、輸出路徑與原始檔都正常。
6. 驗證成功後再接 Codex、自動批次、首尾幀或參考圖工作流。

## 未來何時取用

當使用者要把 Flow / Veo 影片生成接到 Codex、CLI、Docker、批次生成、首尾幀轉場或自動下載流程時，先讀此卡；若要安裝，重新查 GitHub 最新 commit、issue、上游版本與 Google Flow 當日資格後再執行。

## 查證來源

- Repository README and configuration, checked 2026-08-01: https://github.com/Mr-funny/hbg-gemini-flow-suite
- Google Flow Help, checked 2026-08-01: https://support.google.com/flow/answer/16353333
- Supported regions, checked 2026-08-01: https://support.google.com/flow/answer/16353544
- Models and features, checked 2026-08-01: https://support.google.com/flow/answer/16352836


---

## EverMind-AI EverOS

- 原路徑：`inbox/2026-06-27-evermind-ai-everos.md`
- 日期：2026-06-27
- 類型：inbox 來源卡（未驗證）

# EverMind-AI EverOS

Source: https://github.com/EverMind-AI/EverOS
Date: 2026-06-27
Type: repo_tool
Tags: EverOS, EverMind, agent memory, long-term memory, Markdown source of truth, SQLite, LanceDB, FastAPI, OME, cascade daemon, Codex memory, 無限
Tool Potential: high
Prompt Library Impact: no

## 一句話摘要

EverOS 是一個 Python + FastAPI 的本地優先 AI agent 長期記憶層，把 Markdown 當唯一真實來源，再用 SQLite 與 LanceDB 做狀態、索引、向量/BM25 檢索，概念上非常接近無限可以演化的方向。

## 核心內容

- GitHub repo 描述：一個可攜式 memory layer，面向 AI agents；local-first、Markdown-native、user-owned，跨 apps/tools/workflows 自我演化。
- README 重點：對話、檔案、agent trajectories 都保存成可讀、可編輯、可 Git 版本化的 Markdown；SQLite/LanceDB 是可重建索引。
- 儲存架構：Markdown + YAML frontmatter 是 source of truth；SQLite 負責系統狀態、audit log、cascade queue、OME 狀態；LanceDB 負責 vector + BM25 + scalar retrieval。
- 記憶類型：user episodes/profile/atomic facts/foresights、agent cases/skills、shared knowledge documents/topics。
- 寫入流程：`POST /api/v1/memory/add` 累積 session messages；`POST /api/v1/memory/flush` 強制抽取；episode markdown 同步寫入，索引與 profile/skills 等由 cascade/OME 非同步補齊。
- 使用門檻：Python 3.12+；demo 不需 API key；實際 server flow 需要 LLM/multimodal 與 embedding/rerank provider key，預設提到 OpenRouter + DeepInfra，也支援 OpenAI-compatible endpoint。
- 安裝入口：`pip install everos` 或 `uv pip install everos`；`everos init`；`everos server start`；健康檢查 `GET /health`。
- 截至 2026-06-27 檢查：GitHub API 顯示 repo 9239 stars、796 forks、open issues 35、default branch `main`、latest push `2026-06-27T02:16:27Z`；`pyproject.toml` 顯示 package `everos` version `1.1.0`，license Apache-2.0，requires Python >=3.12。

## 可重複使用的規則

- 記憶系統要把人可讀、可編輯、可備份的檔案當真實來源；向量庫與資料庫應該是派生索引，可刪除重建。
- 長期記憶不要只存聊天紀錄；要區分 user memory、agent memory、project/app/session scope、knowledge wiki。
- 寫入與檢索要接受 eventual consistency：先確保 Markdown durable，再讓索引追上。
- 對 Codex 類工具，agent cases/skills 比單純 facts 更有用，因為它能記住「怎麼做過一件事」。
- 搜尋最好混合：向量語意 + BM25 + scalar filters，而不是只有 embedding retrieval。

## 可轉成工具/詞庫的部分

- 無限可借用的架構：`inbox/` 與 `libraries/` 繼續作 Markdown source of truth，另加 SQLite/LanceDB 派生索引與 watcher。
- 可做本地 bridge：把 Codex session 摘要寫成 episode markdown，再用 EverOS 或類 EverOS 索引提供跨專案搜尋。
- 可做 Codex skill：`everos-memory-sync`，負責把聊天決策、repo 卡、prompt 卡同步進 EverOS/無限。
- 可做 prompt-library 輔助：把「提示詞使用案例、失敗修復、成功圖像 prompt」當 agent/user episodes 存，之後以語意搜尋找相似案例。

## 對目前專案的用法

- 對無限有直接參考價值：無限目前是輕量 Markdown + catalog + search script；EverOS 提供一個更完整的 memory runtime 藍圖。
- 最有用的不是直接整套替換無限，而是採納三件事：Markdown source-of-truth、可重建索引、agent skill/case 形式的經驗沉澱。
- 短期可以先不導入 EverOS server，因為無限目前足夠輕；等 memory palace 搜尋量、跨專案記憶量變大，再評估用 EverOS 或仿 EverOS 的 SQLite/LanceDB index。

## 工具判斷

- 能不能本地使用：可以。Python package/CLI/server 形式，預設 root `~/.everos`，可用 `--root` 或 env 調整。
- 是否需要帳號/API/付費：demo 不需要；真實抽取/檢索 flow 需要 LLM、embedding、rerank provider key，成本取決於供應商。
- 是否適合接入目前網站：中高。適合接 prompt-library / Codex 工作流的後端記憶搜尋，但不應先替換現有 JSON/Markdown 儲存。
- 是否適合做成 Codex skill：高。可以做成「同步本次工作摘要到 EverOS/無限」「查詢跨專案記憶」「把 agent cases 轉技能草稿」。
- 風險或限制：需要常駐 FastAPI server；Python 3.12+；索引是 eventual consistency；真實效果依賴 LLM/embedding/rerank 品質；導入會增加維護面。

## 下次調用關鍵字

EverOS, EverMind, agent memory, long-term memory, Markdown memory, Markdown source of truth, SQLite LanceDB, OME, cascade daemon, AI agent 長期記憶, 無限升級, Codex memory, agent cases, agent skills, memory runtime


---

## GitHub AI Resource Map

- 原路徑：`inbox/2026-06-15-github-ai-resource-map.md`
- 日期：2026-06-15
- 類型：inbox 來源卡（未驗證）

---
type: index
topic: github-ai-resource-map
created: 2026-06-15
source: GitHub API repository search + known high-utility AI repos
secondary_tags:
  - repo_tool
  - artificial_intelligence
  - llm
  - rag
  - ai_agent
  - image_generation
  - ai_video
  - tts
  - computer_vision
  - local_ai
---

# GitHub AI Resource Map

Source: GitHub repository search, sampled 2026-06-15  
Date: 2026-06-15  
Type: index  
Tags: GitHub AI, LLM, RAG, agent, image generation, video generation, TTS, computer vision, local AI, prompt engineering  
Tool Potential: high  
Prompt Library Impact: yes, selected prompt/template repos only

## 一句話摘要

GitHub 上「所有 AI repo」數量太大，不適合全量塞進無限。本卡作為可擴充的 AI repo 地圖：先收高星、實用、可被本地工具借鑑的 AI 專案，之後再按任務擴充。

## 收錄原則

- 不下載整個 repo。
- 不把所有 README 全文塞進無限。
- 優先記錄：用途、分類、能做什麼本地工具、是否適合 CPU/本機、是否可作為 UI/架構參考。
- 對 prompt 類 repo 只標記可匯入方向，不直接污染原圖片提示詞庫。

## LLM / Local Runtime / Model Serving

- https://github.com/ollama/ollama  
  Local LLM runtime. 適合本地模型、角色聊天、工具接 Ollama API。

- https://github.com/open-webui/open-webui  
  User-friendly AI interface. 適合參考本地 AI 聊天 UI、模型管理、Ollama 前端。

- https://github.com/huggingface/transformers  
  Text/vision/audio/multimodal model framework. 適合模型載入與推理參考。

- https://github.com/ggerganov/llama.cpp  
  CPU/GPU-friendly local inference. 適合低成本本地 LLM、GGUF、量化模型方向。

- https://github.com/vllm-project/vllm  
  High-throughput LLM serving. 適合之後有 GPU/server 時做推理服務。

- https://github.com/mudler/LocalAI  
  OpenAI-compatible local AI engine for LLM/vision/voice/image/video. 適合 local-first API gateway。

- https://github.com/unslothai/unsloth  
  Local/open model training and finetune tooling. 適合未來微調/LoRA 學習。

## RAG / Knowledge Base / Workflow

- https://github.com/langchain-ai/langchain  
  Agent/RAG engineering framework. 適合工具串接、RAG pipeline、agent orchestration。

- https://github.com/run-llama/llama_index  
  Data framework for LLM apps. 適合知識庫、文件索引、查詢。

- https://github.com/langgenius/dify  
  Production-ready agentic workflow platform. 適合本地工具 workflow/UI 架構參考。

- https://github.com/infiniflow/ragflow  
  RAG engine with document parsing and agent capabilities. 適合 PDF/image/document knowledge base。

- https://github.com/FlowiseAI/Flowise  
  Visual AI agent builder. 適合低代碼工作流、節點式工具設計參考。

- https://github.com/Shubhamsaboo/awesome-llm-apps  
  Runnable AI Agent/RAG app examples. 適合作為應用點子庫。

## AI Agents / Coding Agents / Memory

- https://github.com/Significant-Gravitas/AutoGPT  
  Autonomous agent platform. 適合 agent 任務規劃概念參考。

- https://github.com/OpenHands/OpenHands  
  AI-driven development environment. 適合 coding agent、dev workflow 參考。

- https://github.com/NousResearch/hermes-agent  
  Agent-focused project. 適合 agent memory/skill 概念觀察。

- https://github.com/thedotmack/claude-mem  
  Persistent context/memory for coding agents. 適合無限/跨 session memory 設計參考。

- https://github.com/zhayujie/CowAgent  
  Multi-channel AI assistant/agent harness. 適合微信/多渠道助理架構參考。

- https://github.com/HKUDS/nanobot  
  Lightweight AI agent for tools/chats/workflows. 適合輕量 agent 設計。

## Prompt / Prompt Engineering

- https://github.com/f/prompts.chat  
  Awesome ChatGPT Prompts / self-host prompt collection. 適合提示詞知識庫、Prompt Library 匯入來源。

- https://github.com/dair-ai/Prompt-Engineering-Guide  
  Prompt/context/RAG/agent guide. 適合提示詞工具、教學內容、提示詞品質檢查。

- https://github.com/yaojingang/yao-open-prompts  
  中文提示詞合集。已另收無限卡：`2026-06-14-yaojingang-yao-open-prompts.md`。

## Image Generation / Image Editing

- https://github.com/Comfy-Org/ComfyUI  
  Node-based diffusion GUI/API/backend. 適合圖片工作流、節點 UI、AIGC pipeline 參考。

- https://github.com/AUTOMATIC1111/stable-diffusion-webui  
  Stable Diffusion WebUI. 適合本地圖片生成工具參考。

- https://github.com/huggingface/diffusers  
  Diffusion models for image/video/audio in PyTorch. 適合模型 pipeline 參考。

- https://github.com/invoke-ai/InvokeAI  
  Creative engine/WebUI for Stable Diffusion. 適合專業創作 UI 參考。

- https://github.com/Sanster/IOPaint  
  AI inpainting/object removal tool. 適合圖片修復、物件移除、本地圖片工具。

- https://github.com/upscayl/upscayl  
  AI image upscaler. 已有 Upscayl release note 收錄，可用於圖片放大工具。

## AI Video / Shorts / Creative Media

- https://github.com/AIDC-AI/Pixelle-Video  
  Topic/script/media/TTS/BGM/composition automated short video pipeline.

- https://github.com/harry0703/MoneyPrinterTurbo  
  One-click short-video generation workflow. 適合 AI Shorts Factory 參考。

- https://github.com/SamurAIGPT/AI-Youtube-Shorts-Generator  
  Long video to 9:16 shorts with highlight detection/cropping.

- https://github.com/zhouxiaoka/autoclip  
  AI-powered video clipping/highlight generation.

- https://github.com/rushindrasinha/youtube-shorts-pipeline  
  News -> script -> visuals -> voiceover -> captions -> upload.

- https://github.com/alecm20/story-flicks  
  AI story short video generator.

- https://github.com/xuanyustudio/LocalMiniDrama  
  Local AI short drama/storyboard/video workflow.

- https://github.com/YouMind-OpenLab/awesome-seedance-2-prompts  
  Seedance video prompt collection. 適合影片提示詞庫參考。

## Voice / TTS / Voice Clone

- https://github.com/RVC-Boss/GPT-SoVITS  
  Few-shot voice cloning/TTS. 適合配音工具研究。

- https://github.com/coqui-ai/TTS  
  Deep learning TTS toolkit.

- https://github.com/2noise/ChatTTS  
  Dialogue-oriented TTS model.

- https://github.com/myshell-ai/OpenVoice  
  Instant voice cloning.

- https://github.com/OpenBMB/VoxCPM  
  Multilingual TTS / voice generation.

- https://github.com/FunAudioLLM/CosyVoice  
  Multilingual voice generation/inference/training.

## Computer Vision / OCR / Image Understanding

- https://github.com/opencv/opencv  
  General computer vision library.

- https://github.com/ultralytics/ultralytics  
  YOLO object detection/segmentation/tracking. 適合圖片辨識、服裝/物件檢測方向。

- https://github.com/google-ai-edge/mediapipe  
  Live media ML pipeline. 適合姿態、臉部、手部偵測。

- https://github.com/roboflow/supervision  
  Reusable computer vision utilities.

- https://github.com/PaddlePaddle/PaddleOCR  
  OCR/document image to structured data. 適合圖片牆 metadata、文件辨識、掃描圖整理。

## Learning / Reference / Course

- https://github.com/rasbt/LLMs-from-scratch  
  Learn LLM implementation from scratch.

- https://github.com/jingyaogong/minimind  
  Tiny LLM training from scratch, Chinese-friendly.

- https://github.com/d2l-ai/d2l-zh  
  動手學深度學習中文教材。

- https://github.com/microsoft/AI-For-Beginners  
  AI beginner curriculum.

- https://github.com/ashishpatel26/500-AI-Machine-learning-Deep-learning-Computer-vision-NLP-Projects-with-code  
  AI/ML/CV/NLP project idea list.

## 對本地專案的建議用法

- `prompt-memory-lab`: 匯入 prompt 類 repo metadata，不要混入圖片生成提示詞主庫。
- `image-wall-browser`: 可接 PaddleOCR / YOLO / MediaPipe 做圖片自動標籤、人物/服裝/場景分類。
- `image-puzzle-game`: 可參考 Open Design/agent UI 方向做成完整 tool/game site。
- `clothing-extractor`: 優先看 YOLO/MediaPipe/SAM/roboflow supervision，而不是完整 AIGC repo。
- `AI Shorts Factory`: 優先參考 MoneyPrinterTurbo、Pixelle-Video、AI-Youtube-Shorts-Generator、youtube-shorts-pipeline。
- `local model chat`: 優先 Ollama + Open WebUI + LocalAI。

## 後續擴充規則

如果使用者再說「搜尋 GitHub AI」：

1. 先判斷類別：LLM / RAG / agent / image / video / voice / CV / prompt / UI。
2. 用 GitHub API 或網頁搜尋補該類別 top repo。
3. 只把可重用摘要加入本卡或另開 repo card。
4. 不全量複製 README，不下載大型模型或圖片/影片。

## GitHub Search Queries Used

- `topic:artificial-intelligence stars:>1000`
- `topic:llm stars:>1000`
- `topic:rag stars:>500`
- `topic:ai-agent stars:>500`
- `topic:stable-diffusion stars:>500`
- `topic:text-to-speech stars:>500`
- `topic:computer-vision stars:>1000`
- `topic:ai-video stars:>100`


---

## yaojingang/yao-open-prompts

- 原路徑：`inbox/2026-06-14-yaojingang-yao-open-prompts.md`
- 日期：2026-06-14
- 類型：inbox 來源卡（未驗證）

---
type: repo_tool
topic: yao-open-prompts
created: 2026-06-14
source: https://github.com/yaojingang/yao-open-prompts
license: CC BY 4.0 for prompt content; MIT possible for future scripts per repo README
secondary_tags:
  - prompt_asset
  - chinese_prompts
  - ai_content
  - ai_marketing
  - ai_methods
  - short_video
---

# yaojingang/yao-open-prompts

Source: https://github.com/yaojingang/yao-open-prompts  
Date: 2026-06-14  
Type: repo_tool  
Tags: 中文提示詞庫, AI方法, AI工作, AI學習, AI內容, AI行銷, GEO, 短視頻, 小紅書, 公众号, 元提示詞  
Tool Potential: high  
Prompt Library Impact: yes

## 一句話摘要

`yaojingang/yao-open-prompts` 是《姚金剛提示詞合集》的開源版，整理出 117 個中文提示詞文件，適合當作本地提示詞知識庫、提示詞生成器、內容工具、短視頻文案工具、GEO/SEO 行銷工具的種子資料。

## 核心內容

- Repo 有中文與英文提示詞鏡像，中文主體在 `prompts/`，英文版在 `prompts-en/`。
- 提示詞按場景分類，而不是混在單一大檔案。
- 每個提示詞文件使用 frontmatter，包含 title、category、subcategory、source_section、author、version、created、status、tags。
- 正文保留可複製的 Prompt，教程、截圖、附件和 HTML 殘留被移出主提示詞正文。
- 全量索引在 `CATALOG.md`，網頁導航在 GitHub Pages。

## 分類統計

- AI方法：8，含元提示詞、反編譯、網頁逆向、提示詞工程。
- AI工作：10，含合同、客服、產品原型、PPT、網頁、銷售等。
- AI學習：11，含費曼學習、康奈爾筆記、SQ3R、記憶術、習慣養成。
- AI生活：2，健康、親子歌曲。
- AI教育：4，兒童互動學習與小遊戲。
- AI內容：50，含寫作、標題、短視頻、內容運營、AI繪畫、PPT、公众号、小紅書。
- AI編程：1，架構設計。
- AI行銷：28，含 GEO 內容生成、信源建設、數據監測、增長診斷、合規風險。
- AI思考：3，批判思維、記憶宮殿、標題思考。

## 對本地工具的價值

- 可接進 `prompt-memory-lab` 當外部知識儲備，但不要整包混入圖片提示詞庫。
- 適合建立「中文任務提示詞模板庫」：寫作、行銷、短視頻、PPT、網頁、學習助教。
- 適合拆成 RAG/搜尋索引：使用 title、category、subcategory、tags 做檢索，再只取最相關模板。
- 可作為「提示詞變體生成器」的結構參考：分類、frontmatter、狀態、版本、目錄生成腳本。
- 可補強無限的短視頻與內容運營模板，特別是短視頻鉤子、口播文案、爆款拆解、小紅書標題、視頻號運營。

## 值得優先吸收的方向

- 元提示詞：RTF/meta prompt 系列，可用來提升本地提示詞生成器的架構感。
- 反編譯：文章、圖片、視頻、網頁反向拆解，可用來做「分析參考 → 生成新提示詞」。
- 短視頻內容：鉤子開場、口播爆款、7秒起號、抖音爆款策劃、視頻號運營。
- 圖文與平台內容：小紅書標題、小紅書圖文、公众号 HTML、標題優化。
- GEO/AI行銷：內容工廠、AI友好內容、Schema.org、信源建設、增長診斷。
- 學習與記憶：費曼提問、記憶宮殿、關鍵詞學習，可用來優化無限本身的整理流程。

## 收錄策略

不要直接把全部 117 個提示詞寫入 `prompt-library`，避免污染原本以圖片提示詞為主的個人詞庫。

建議分三層處理：

1. `repo knowledge card`：本卡，記錄來源、用途、分類和後續方向。
2. `external prompt index`：未來可建立獨立索引，保留 repo URL、檔案路徑、標籤、摘要。
3. `selected imports`：只把符合需求的模板抽到工具中，例如短視頻、元提示詞、GEO、圖文內容。

## 可做成的工具

- 中文 AI 提示詞搜尋器：輸入任務，回傳最相關模板與改寫版。
- 短視頻腳本助手：套用鉤子、口播、爆款拆解、平台運營模板。
- GEO 內容生成器：用 GEO/SEO 模板生成文章、信源計畫、Schema.org 建議。
- 參考反編譯工具：貼文章、圖片描述、短視頻截圖，先拆結構再產生新提示詞。
- 提示詞品質檢查器：用 repo 的 frontmatter 與版本規範檢查本地提示詞是否完整。

## 後續行動

- 若要接進 `prompt-memory-lab`，先只匯入 metadata 與摘要，不直接混進圖片提示詞生成。
- 若要做 AI 短片工具，優先取 `AI內容` 中的短視頻、口播、爆款、平台運營模板。
- 若要優化無限，優先取 `AI思考/記憶宮殿` 和 `AI學習/記憶術` 類模板作為整理策略參考。

## 來源

- GitHub repo: https://github.com/yaojingang/yao-open-prompts
- README: https://raw.githubusercontent.com/yaojingang/yao-open-prompts/main/README.md
- Catalog: https://raw.githubusercontent.com/yaojingang/yao-open-prompts/main/CATALOG.md


---

## notebooklm-py repo intake

- 原路徑：`inbox/2026-06-01-notebooklm-py-repo.md`
- 日期：2026-06-01
- 類型：inbox 來源卡（未驗證）

# notebooklm-py repo intake

Source: https://github.com/teng-lin/notebooklm-py
Date: 2026-06-01
Type: Unofficial NotebookLM Python API / CLI / Agent Skill
Tags: NotebookLM, Python API, CLI, Codex Skill, research automation, audio overview, slide deck, quiz, flashcards, mind map, source ingestion

## What It Is

`teng-lin/notebooklm-py` is an unofficial Python API, CLI, and agent skill for Google NotebookLM.

It gives programmatic access to NotebookLM workflows, including notebook/source management, chat over sources, research automation, artifact generation, downloads, exports, and agent integration for tools like Claude Code, Codex, and OpenClaw.

Important: it uses undocumented Google APIs. Treat it as useful for prototypes, personal workflows, and research automation, not as a guaranteed stable production dependency unless the risk is accepted.

## Why It Matters

This can turn NotebookLM from a manual web tool into an automated research/content pipeline.

Useful for:

- bulk importing sources into NotebookLM;
- asking questions over a notebook from scripts or agents;
- generating Audio Overviews / podcast-style summaries;
- generating video overviews, slide decks, quizzes, flashcards, infographics, reports, data tables, and mind maps;
- downloading artifacts locally as MP3, MP4, PDF, PNG, CSV, JSON, Markdown, or PPTX depending on artifact type;
- exporting outputs to Google Docs/Sheets;
- batch downloading content that the NotebookLM UI does not expose conveniently;
- letting Codex/agents operate NotebookLM through a skill-like workflow.

## Main Capabilities

### Notebook and Source Management

- Create, list, rename, and delete notebooks.
- Add sources from URLs, YouTube, files, Google Drive, pasted text, and other supported document/media types.
- Refresh sources.
- Retrieve source guide/full text when available.

### Chat and Research

- Ask questions against notebook sources.
- Access conversation history.
- Use custom personas.
- Run web/Drive research modes with optional auto-import.

### Artifact Generation

- Audio Overview with multiple formats, lengths, and language options.
- Video Overview and cinematic-video style output.
- Slide decks, including editable PPTX/PDF-style exports depending on command.
- Infographics.
- Quizzes and flashcards, exportable to structured formats.
- Reports / study guides / blog-post-like outputs.
- Data tables as CSV.
- Mind maps as JSON.

### Features Beyond NotebookLM Web UI

- Batch artifact downloads.
- Quiz/flashcard export to JSON/Markdown/HTML.
- Mind map JSON extraction.
- Data table CSV export.
- Slide deck PPTX download / slide revision.
- Report template customization.
- Save chats to notes.
- Programmatic sharing and permission management.
- Multi-account profiles.
- Browser cookie import from an existing logged-in browser session.

## Installation Notes

Quick CLI / agent setup:

```powershell
pip install "notebooklm-py[browser]"
playwright install chromium
notebooklm login
notebooklm auth check --test --json
```

Lightweight library-only setup:

```powershell
pip install notebooklm-py
```

Agent skill install options:

```powershell
notebooklm skill install
```

or:

```powershell
npx skills add teng-lin/notebooklm-py
```

The project docs say `notebooklm skill install` writes skill files for Claude / `.agents`; the repo also includes `AGENTS.md` guidance for Codex-like agents.

## Basic CLI Workflow

```powershell
notebooklm login
notebooklm create "My Research"
notebooklm use <notebook_id>
notebooklm source add "https://example.com/article"
notebooklm source add ".\paper.pdf"
notebooklm ask "What are the key themes?"
notebooklm generate audio "make it engaging" --wait
notebooklm generate quiz --difficulty hard
notebooklm generate mind-map
notebooklm download audio ".\podcast.mp3"
notebooklm download quiz --format markdown ".\quiz.md"
notebooklm download mind-map ".\mindmap.json"
```

## Basic Python Pattern

```python
import asyncio
from notebooklm import NotebookLMClient

async def main():
    async with NotebookLMClient.from_storage() as client:
        nb = await client.notebooks.create("Research")
        await client.sources.add_url(nb.id, "https://example.com", wait=True)
        result = await client.chat.ask(nb.id, "Summarize this")
        print(result.answer)

asyncio.run(main())
```

## Auth and Config Caveats

- Authentication is cookie-based.
- Interactive login stores `storage_state.json`, typically under a NotebookLM profile directory.
- Headless/CI usage usually requires moving a pre-authenticated `storage_state.json` or setting `NOTEBOOKLM_AUTH_JSON`.
- Browser cookie reuse can be more convenient, but optional cookie extraction dependencies may have Python-version build issues.
- Always verify auth with `notebooklm auth check --test --json`, not only a local parse check.

## Risk Notes

- Unofficial library; not affiliated with Google.
- Uses undocumented internal RPC APIs.
- Google can change endpoints without notice.
- Rate limits may apply; heavy automated usage may be throttled.
- Avoid relying on it for mission-critical production workflows without fallback.
- Treat Google auth state / cookies as sensitive credentials.

## How To Use In Our Workflow

Potential use cases for our local system:

1. **無限 intake assistant**
   - Use NotebookLM as a temporary research notebook for large PDFs/articles/repos.
   - Ask NotebookLM for grounded summaries, then save durable distilled cards into `D:\codex\memory-palace\inbox`.

2. **Prompt/course material processing**
   - Upload long prompt articles, GitHub READMEs, PDFs, and ask for structured SOPs.
   - Export quiz/flashcard/mind-map artifacts for learning or content packaging.

3. **X / blog article prep**
   - Feed source materials into NotebookLM.
   - Generate study guide / briefing / mind map.
   - Then use our `x-longform-writing-sop.md` to turn the distilled material into an X article.

4. **Audio/podcast summarization**
   - Generate NotebookLM Audio Overviews from collected sources.
   - Download MP3 for review, content repurposing, or internal study.

5. **Codex automation**
   - If installed locally and authenticated, Codex can call `notebooklm` CLI for create/source/ask/generate/download flows.
   - Best suited to user-approved workflows because it touches Google account data.

## Search Keywords

NotebookLM API, notebooklm-py, Google NotebookLM automation, audio overview generator, AI podcast, source ingestion, research assistant, mind map export, quiz export, flashcards, slide deck, Codex skill, Claude skill, unofficial Google API.

## GitHub update check - 2026-06-10


- Repo: `teng-lin/notebooklm-py`
  - Card date: `2026-06-01`
  - Default branch: `main`
  - HEAD: `20ad2c0732da`
  - Latest commit: `2026-06-09T19:54:27Z` - arch(rpc): narrow single-level positional gate to name[int] + migrate…
  - Commit URL: https://github.com/teng-lin/notebooklm-py/commit/20ad2c0732da223e01dabe2f590c0bdc149c3f80


---

## AI 相關 GitHub 資源索引：提示詞、副業、字幕翻譯、中文 LLM、Repo AI 讀懂

- 原路徑：`inbox/2026-05-23-ai-github-resources-from-github-goldmine.md`
- 日期：2026-05-23
- 類型：inbox 來源卡（未驗證）

# AI 相關 GitHub 資源索引：提示詞、副業、字幕翻譯、中文 LLM、Repo AI 讀懂

Source: user pasted GitHub goldmine article; web-verified selected AI-related resources on 2026-05-23
Date: 2026-05-23
Type: repo_tool
Tags: GitHub, AI resources, prompts, Claude, ChatGPT, video subtitle, AI side hustle, Chinese LLM, DeepWiki, repo reading
Tool Potential: high
Prompt Library Impact: yes

## 一句話摘要

這是一組從 GitHub 挖寶文章中抽出的 AI 相關資源，分成提示詞合集、AI 副業、AI 字幕/翻譯工具、中文大模型索引與 AI 讀懂 repo 工具，可作為無限的 AI 資源種子庫。

## 核心內容

### 1. AI 提示詞與模型使用指南

| 資源 | URL | 核心用途 | 無限用途 |
|---|---|---|---|
| `langgptai/wonderful-prompts` | https://github.com/langgptai/wonderful-prompts | 中文 prompt 精選、ChatGPT 使用指南、提升可玩性與可用性 | 可抽提示詞分類、提示詞模板、中文 prompt 寫法 |
| `langgptai/awesome-claude-prompts` | https://github.com/langgptai/awesome-claude-prompts | Claude prompt collection，含 Claude Code、PDF 摘要、GitHub Project、商業/行銷 prompt 等 | 可抽 Claude 專用 prompt、長上下文任務模板、商業 prompt |
| `wikieden/Awesome-ChatGPT-Prompts-CN` | https://github.com/wikieden/Awesome-ChatGPT-Prompts-CN | 中文 ChatGPT prompts 與調教指南 | 可做中文 prompt 教學和工具範例來源 |
| `tsaol/awesome-claude` | https://github.com/tsaol/awesome-claude | Claude prompts、中文調教指南、提示詞指南、學習指南 | 可補 Claude 生態索引 |

### 2. AI 副業與商業化資源

| 資源 | URL | 核心用途 | 無限用途 |
|---|---|---|---|
| `bleedline/aimoneyhunter` | https://github.com/bleedline/aimoneyhunter | AI 副業賺錢大集合，教如何利用 AI 做副業項目 | 可納入 X 長文、工具站選題、副業工具研究 |

### 3. AI 字幕、翻譯、配音與視頻本地化工具

| 資源 | URL | 核心用途 | 無限用途 |
|---|---|---|---|
| `WEIFENG2333/VideoCaptioner` | https://github.com/WEIFENG2333/VideoCaptioner | 卡卡字幕助手，基於 LLM 的字幕生成、斷句、校正、翻譯、字幕視頻合成；Wiki 說 Windows 有打包版，支援本地/線上 ASR、LLM API、Whisper/fasterWhisper | 可作為字幕工具候選；可研究接本地短影音流程 |
| `chenyme/Chenyme-AAVT` | https://github.com/chenyme/Chenyme-AAVT | 全自動音視頻翻譯：Whisper 識別、AI 大模型翻譯字幕、合併字幕視頻，也提到圖文博客、字幕翻譯、聲音模擬等 | 可作為視頻翻譯/字幕工具候選 |
| `agan-j/xiaoniu` | https://github.com/agan-j/xiaoniu | 小牛視頻翻譯，支援本地視頻翻譯、字幕翻譯、YouTube 下載，多角色識別、自動/克隆配音、音畫字幕嘴型同步等 | 可作為視頻出海、短劇配音翻譯工具候選 |

### 4. 中文 LLM 與模型/資料/框架索引

| 資源 | URL | 核心用途 | 無限用途 |
|---|---|---|---|
| `AiHubCN/Awesome-Chinese-LLM` | https://github.com/AiHubCN/Awesome-Chinese-LLM | 中文 LLM 大合集，整理文本/多模態模型、垂直領域微調、應用、資料集、訓練微調框架、推理部署框架、評測、教程等 | 查中文開源模型、私有化部署、垂直微調與本地模型路線 |

### 5. AI 讀懂 GitHub Repo

| 資源 | URL | 核心用途 | 無限用途 |
|---|---|---|---|
| DeepWiki by Cognition | https://cognition.ai/blog/deepwiki | 官方說法：把任意 repo URL 裡的 `github.com` 換成 `deepwiki.com`，可查看 AI 生成的 repo docs | 可做工具「DeepWiki URL 轉換器」和 repo 讀懂流程 |
| DeepWiki site | https://deepwiki.org/ | DeepWiki 搜尋/瀏覽入口，展示大量 GitHub repo 的 AI docs | 可作為查 repo 的輔助入口 |

## 可重複使用的規則

- AI prompt 類 repo 不要全量複製進 prompt-library；先按用途抽象成模板、標籤、欄位和可點選例子。
- 字幕/視頻翻譯工具要先判斷四件事：Windows 是否有打包版、是否需要 GPU、是否需要 LLM API、是否能直接處理 YouTube 或本地視頻。
- 中文 LLM 索引型 repo 適合當「路由表」，不要直接當教程；使用時應按目標查子項，例如本地部署、推理框架、垂直微調、中文多模態。
- DeepWiki 適合非程序員快速讀 repo：先轉 URL，再問「這是什麼」「怎麼安裝」「是否適合 Windows」「核心功能在哪」「有沒有 API key 需求」。
- 收 GitHub AI 資源時，統一記錄：repo path、URL、用途、是否本地可跑、是否需要 API/付費、是否適合網站工具、是否適合 Codex skill、最新驗證日期。

## 可轉成工具/詞庫的部分

- 「AI Repo 評估器」：輸入 GitHub URL，輸出用途、安裝難度、依賴、API key、Windows 友好度、是否適合接網站。
- 「DeepWiki URL 轉換器」：把 `https://github.com/owner/repo` 轉為 `https://deepwiki.com/owner/repo`。
- 「AI 提示詞資源導入器」：輸入 prompt repo，抽標題、用途、模板、變數欄位，先進待審區，不直接污染正式詞庫。
- 「字幕工具比較表」：VideoCaptioner、Chenyme-AAVT、xiaoniu 比較 Windows 支援、字幕翻譯、配音、YouTube 下載、API 需求、GPU 需求。

## 對目前專案的用法

- prompt-library 可以新增「GitHub AI 資源」小工具，保存和評估 AI repo。
- 網站工具可以加「DeepWiki 轉換」和「AI Repo 讀懂提示詞」。
- X 長文可用這張卡寫一篇「非程序員如何用 GitHub 找 AI 工具」。
- 本地工作流可以優先試 VideoCaptioner 或 xiaoniu，服務短影音字幕、翻譯和跨平台內容。

## 工具判斷

- 能不能本地使用：
  - Prompt 類 repo：可直接閱讀使用。
  - VideoCaptioner：Wiki 顯示 Windows 有打包可執行版本，也可源碼/Docker 運行。
  - Chenyme-AAVT：開源自動音視頻翻譯項目，需依 README 配環境。
  - xiaoniu：開源視頻翻譯工具，需依 repo 說明評估安裝。
  - Awesome-Chinese-LLM：資源索引，不是單一工具。
  - DeepWiki：線上服務，主要處理公開 repo。
- 是否需要帳號/API/付費：
  - GitHub 閱讀免費。
  - 字幕翻譯工具若使用高品質 LLM，通常需要 OpenAI 兼容 API 或本地模型。
  - DeepWiki 公共 repo 可直接用，但具體限制需以官網當前政策為準。
- 是否適合接入目前網站：
  - 適合接「資源索引」「repo 評估」「DeepWiki 轉換」。
  - 不建議直接把整個字幕工具接到 prompt-library；可另做本地工具或教程頁。
- 是否適合做成 Codex skill：
  - 適合。可做 `github-ai-resource-review`、`repo-to-deepwiki`、`subtitle-tool-evaluator`、`prompt-repo-intake`。
- 風險或限制：
  - GitHub repo 可能停止維護、換 license、安裝失敗。
  - 字幕工具涉及 API key、視頻下載、平台條款與版權風險。
  - 自動翻譯字幕可能有幻覺、術語錯誤、時間軸偏移，需要人工校對。

## 下次調用關鍵字

AI GitHub 資源, prompt repo, Claude prompts, ChatGPT prompts, AI 副業, VideoCaptioner, Chenyme-AAVT, 小牛視頻翻譯, Awesome Chinese LLM, DeepWiki, repo 讀懂, GitHub AI 工具

## 詞庫增量

- 可新增標籤：
  - GitHub AI
  - Claude prompt
  - ChatGPT prompt
  - AI 副業
  - 字幕翻譯
  - 中文 LLM
  - Repo 讀懂
  - DeepWiki
- 可新增模板：
  - `請分析這個 GitHub repo：{url}。用非程序員能懂的方式說明用途、安裝方式、API 需求、Windows 是否可用、適合我拿來做什麼。`
  - `請把這個 prompt repo 裡的提示詞按用途分類：寫作、行銷、程式、學習、商業、圖片、影片，並提取可複用模板。`
  - `請比較這三個字幕工具：{repo1}、{repo2}、{repo3}，從 Windows 友好度、GPU/API 需求、翻譯品質、批次處理、配音能力排序。`
- 可新增安全替換詞：
  - 無
- 可新增負面詞：
  - 無
- 可新增救場詞：
  - `如果安裝失敗，先檢查 Python/Node/ffmpeg/模型/API key/系統路徑。`
  - `如果 repo 太複雜，先用 DeepWiki 讀架構，再回到 README 跑最小示例。`
- 可新增範例方向：
  - GitHub repo 評估器
  - DeepWiki 轉換器
  - AI prompt repo 吸收器
  - AI 字幕工具比較器


---

## GitHub 非程序員挖寶方法與資源路徑索引

- 原路徑：`inbox/2026-05-23-github-nonprogrammer-goldmine-resource-index.md`
- 日期：2026-05-23
- 類型：inbox 來源卡（未驗證）

# GitHub 非程序員挖寶方法與資源路徑索引

Source: user pasted article "AI时代，GitHub是金矿，会用的月入10万"
Date: 2026-05-23
Type: business_growth
Tags: GitHub, non-programmer, open source, resource index, GitHub Pages, DeepWiki, AI tools, student pack, indie hacker
Tool Potential: high
Prompt Library Impact: no

## 一句話摘要

GitHub 對非程序員也可以是公開工作台、免費知識庫、興趣雷達和副業資源池；核心能力是讀 README、Star 倉庫、Follow 真人、用 AI 幫忙理解和運行開源工具。

## 核心內容

- GitHub 不只是程式碼倉庫，而是全球公開工作現場：README、教程、清單、模板、工具、issue 討論與提交紀錄都能提供高密度資訊。
- 非程序員的三個基本動作：讀 README、Star 倉庫、Follow 人。
- 搜尋 `awesome + 領域` 是找精華清單的最快方式，尤其適合學習資料、AI prompts、設計、法律、效率工具、獨立開發、副業工具。
- 進階玩法是「看人」：從好項目的作者頁面看 Star、Follow、貢獻和互動，建立不靠演算法的高品質資訊流。
- GitHub Pages 可用來搭個人網站、履歷、作品集、博客和數字身份。
- Git/GitHub 可當作文字、研究、設計、小說和內容專案的版本管理工具。
- GitHub Student Developer Pack 對學生是高價值福利，常見項目包括 JetBrains、GitHub Copilot、域名、雲服務額度等。
- AI 時代降低了 GitHub 使用門檻：可把 repo 丟給 Claude、Cursor、Claude Code 等工具，要求逐步教安裝、跑起來、解釋報錯。
- DeepWiki 用法：把公共 GitHub repo URL 中的 `github.com` 換成 `deepwiki.com`，查看自動生成的 Wiki 並提問。

## 文中 GitHub 路徑索引

> 狀態：以下路徑為來源文章提供，已收錄為可查索引，未在本次逐一驗證最新 Star、維護狀態或可用性。

### 學習資料類

| 路徑 | URL | 文章用途摘要 |
|---|---|---|
| `0voice/Awesome-CS-OpenCourse` | https://github.com/0voice/Awesome-CS-OpenCourse | 全球頂尖高校計算機公開課清單 |
| `EbookFoundation/free-programming-books` | https://github.com/EbookFoundation/free-programming-books | 多語言免費程式書籍與學習資源 |
| `KnowNo/books-2` | https://github.com/KnowNo/books-2 | 個人電子書庫，涵蓋心理、歷史、經濟等 |
| `csr632/awesome-learning-resources` | https://github.com/csr632/awesome-learning-resources | 學習資料與入門順序整理 |

### AI 提示詞與使用指南

| 路徑 | URL | 文章用途摘要 |
|---|---|---|
| `langgptai/wonderful-prompts` | https://github.com/langgptai/wonderful-prompts | 中文高品質 prompts 精選 |
| `langgptai/awesome-claude-prompts` | https://github.com/langgptai/awesome-claude-prompts | Claude 提示詞合集 |
| `wikieden/Awesome-ChatGPT-Prompts-CN` | https://github.com/wikieden/Awesome-ChatGPT-Prompts-CN | 中文 ChatGPT 調教指南 |
| `tsaol/awesome-claude` | https://github.com/tsaol/awesome-claude | Claude prompts、中文調教與學習指南 |

### 入門級有趣項目與中文 GitHub 雜誌

| 路徑 | URL | 文章用途摘要 |
|---|---|---|
| `521xueweihan/HelloGitHub` | https://github.com/521xueweihan/HelloGitHub | 中文圈入門友好的 GitHub 月刊 |
| `GitHubDaily/GitHubDaily` | https://github.com/GitHubDaily/GitHubDaily | 日更推薦流行、有趣項目 |
| `GrowingGit/GitHub-Chinese-Top-Charts` | https://github.com/GrowingGit/GitHub-Chinese-Top-Charts | GitHub 中文排行榜 |

### 行業專屬資源

| 路徑 | URL | 文章用途摘要 |
|---|---|---|
| `jobbole/awesome-design-cn` | https://github.com/jobbole/awesome-design-cn | 設計師資源大全 |
| `pengxiao-song/awesome-chinese-legal-resources` | https://github.com/pengxiao-song/awesome-chinese-legal-resources | 中文法律資源、法規、數據集 |
| `ivmm/Student-resources` | https://github.com/ivmm/Student-resources | 學生與教職工優惠資源 |

### 獨立開發者與副業資源

| 路徑 | URL | 文章用途摘要 |
|---|---|---|
| `zhugezifang/indie-hackers-guide` | https://github.com/zhugezifang/indie-hackers-guide | 獨立開發者國內外推廣渠道 |
| `loonggg/DevMoneySharing` | https://github.com/loonggg/DevMoneySharing | 獨立開發者賺錢經驗與項目列表 |
| `bleedline/aimoneyhunter` | https://github.com/bleedline/aimoneyhunter | AI 副業賺錢集合 |

### AI 工具與可運行開源神器

| 路徑 | URL | 文章用途摘要 |
|---|---|---|
| `WEIFENG2333/VideoCaptioner` | https://github.com/WEIFENG2333/VideoCaptioner | 視頻字幕生成與翻譯工具 |
| `chenyme/Chenyme-AAVT` | https://github.com/chenyme/Chenyme-AAVT | AI 音視頻字幕/翻譯相關工具 |
| `agan-j/xiaoniu` | https://github.com/agan-j/xiaoniu | 視頻字幕或翻譯相關工具 |
| `AiHubCN/Awesome-Chinese-LLM` | https://github.com/AiHubCN/Awesome-Chinese-LLM | 中文開源大模型大全 |

### 搜尋關鍵字而非固定 repo

| 關鍵字 | 用途 |
|---|---|
| `awesome-productivity` | 效率工具精華清單 |
| `awesome-mac` | macOS 工具與資源 |
| `awesome-windows` | Windows 工具與資源 |
| `awesome-design` / `awesome-design-cn` | 設計資源 |
| `awesome + 你的行業` | 找行業精華清單 |

## 可重複使用的規則

- 先搜尋 `awesome + 領域`，再看 README 的結構、更新頻率、Star、issue 和最近提交。
- 不只看項目，也要看作者：從好項目作者的 Star 和 Follow 反向挖同領域資源。
- 對非程序員，GitHub 操作優先順序是：註冊帳號 -> Star 5 個倉庫 -> Follow 3 個人 -> 用 DeepWiki 或 AI 讀懂一個 repo -> 嘗試跑一個工具。
- 看到開源工具時，把 repo URL 丟給 AI，要求：說明用途、列安裝步驟、判斷依賴、解釋錯誤、給非程序員操作清單。
- 將 GitHub Pages 視為免費個人網站/作品集/履歷的靜態托管方案。
- 將 GitHub 當數字履歷：個人 README、awesome 清單、作品集 Pages、持續 Star/整理資源。

## 可轉成工具/詞庫的部分

- 可做「GitHub 挖寶導航器」：輸入領域，輸出 awesome 搜尋詞、推薦 repo、DeepWiki 轉換 URL、閱讀順序。
- 可做「Repo 非程序員評估器」：輸入 repo URL，輸出用途、適合誰、是否能本地跑、需要什麼依賴、是否適合做副業或網站工具。
- 可做「GitHub 資源收藏表」：按分類保存 repo path、URL、用途、是否驗證、Star、最後更新、是否已試用。
- 可做「DeepWiki 快捷轉換器」：將 `https://github.com/owner/repo` 轉成 `https://deepwiki.com/owner/repo`。

## 對目前專案的用法

- prompt-library 網站可新增一個輔助工具：「GitHub Repo 讀懂器 / 非程序員挖寶器」，幫用戶把 repo 轉成摘要、安裝指令與用途。
- 無限可把這份表當作「GitHub 資源種子庫」，之後再逐一查最新狀態、篩出可接入網站或可做 Codex skill 的工具。
- X 長文寫作可用這篇作為「AI 時代普通人如何使用 GitHub」主題範本：先改認知，再給分類資源，再給今天能做的 5 步。

## 工具判斷

- 能不能本地使用：部分 repo 可本地跑，部分只是資源清單；需逐一確認。
- 是否需要帳號/API/付費：GitHub 瀏覽免費；GitHub Pages 免費；Student Pack 需學生身份；部分工具可能需模型 API 或本地環境。
- 是否適合接入目前網站：適合做成 repo 評估、DeepWiki 轉換、awesome 搜尋、資源收藏工具。
- 是否適合做成 Codex skill：適合。可做「GitHub 挖寶」「Repo 閱讀」「README 摘要」「開源工具安裝引導」skill。
- 風險或限制：來源文章中的 repo 未逐一驗證；部分 repo 可能失效、停止維護、安裝困難或與 Windows 不兼容。使用前需看 license、README、最近更新和 issue。

## 下次調用關鍵字

GitHub 挖寶, 非程序員 GitHub, awesome 清單, GitHub 資源路徑, DeepWiki, GitHub Pages, Student Developer Pack, AI 副業 repo, 開源工具, Repo 評估器, GitHub 金礦


---

## PicList：雲端儲存與圖床管理工具

- 原路徑：`inbox/2026-05-23-piclist-repo.md`
- 日期：2026-05-23
- 類型：inbox 來源卡（未驗證）

# PicList：雲端儲存與圖床管理工具

Source: https://github.com/Kuingsmile/PicList
Official site: https://piclist.cn/
Date: 2026-05-23
Type: repo_tool
Tags: PicList, PicGo, image hosting, cloud storage, image upload, WebDAV, S3, GitHub image host, Typora, Obsidian, Docker, image management
Tool Potential: high
Prompt Library Impact: no

## 一句話摘要

PicList 是基於 PicGo 深度二次開發的圖床與雲端儲存管理工具，適合把本地圖片上傳到 GitHub、S3、WebDAV、OSS、COS、本地資料夾等圖床/儲存平台，並支援圖片壓縮、水印、轉檔、相冊管理與命令列/伺服器模式。

## 核心內容

- PicList 官方定位是「強大的雲儲存與圖床管理工具」，基於 PicGo，保留 PicGo 功能並兼容大多數 PicGo 插件。
- 內建/擴展平台包含 WebDAV、本地圖床、SFTP、AList、SM.MS、GitHub、Imgur、騰訊 COS、阿里雲 OSS、又拍雲、七牛雲、S3 API 兼容平台、蘭空圖床等。
- 相冊支援同步雲端刪除文件，可做圖片列表、搜索、預覽、批量 URL 修改、排序與雲端文件管理。
- 內建圖片處理：水印、壓縮、縮放、旋轉、格式轉換、高級重命名。
- 支援 Typora、Obsidian、VSCode 等寫作/筆記流程：Typora 可設為 PicGo(app)，Obsidian 可用 Image auto upload Plugin 接 `http://127.0.0.1:36677/upload`。
- PicList-Core 是核心庫，基於 PicGo-Core 修改，支援 CLI、圖片處理、`picgo-server` 上傳服務。
- 可用 Docker 啟動上傳服務，常見端口 `36677`，需掛載 `.piclist` 配置目錄並設定 key。
- 支援 Windows Winget、Scoop、macOS Homebrew、直接下載 release。
- 官方網站英文頁也強調：兼容 PicGo 插件與生態、雲存儲管理、圖片預處理、腳本/主題等擴展能力。

## 可重複使用的規則

- 若需要「圖片上傳 + 可公開訪問 URL + Markdown/提示詞案例引用」，PicList 可作為本地圖片上傳層。
- 若使用 Obsidian/Typora 寫文章，PicList 可自動把粘貼圖片上傳圖床並回填 URL，適合 X 長文、微信文章、博客和提示詞案例文檔。
- 若要保留控制權，優先選 WebDAV/S3/本地文件夾/AList 這類自己可控儲存；GitHub 圖床要注意平台使用政策與倉庫容量。
- 若要給本地工具接上傳，可走 `picgo-server` 本地 HTTP 服務，而不是手工操作 GUI。
- 圖片涉及私密素材時，不要上傳到公開 GitHub 或不可信圖床；用本地資料夾、私有 WebDAV、私有 S3 儲存較穩。

## 可轉成工具/詞庫的部分

- 可做「圖片上傳管線」：生成圖 -> PicList 上傳 -> 回填 URL -> 存到 prompt-library。
- 可做「圖床設定檢查器」：檢查 PicList 支援的儲存類型、API key、bucket、域名、是否可刪除。
- 可做「文章圖片工作流」：把本地圖片批量上傳後產生 Markdown 圖片引用。
- 可做「prompt-library 圖片外鏈化」：把本地例圖同步到自有圖床，便於網站部署到 Cloudflare Pages 時引用。

## 對目前專案的用法

- prompt-library 目前圖片存在本機 `data/images`，若以後要公開網站，PicList 可幫你把範例圖片上傳到自有圖床，解決 Cloudflare Pages 不能讀本機 `D:\` 圖片的問題。
- X 封面圖、AI 圖片提示詞案例、角色卡圖片可以先在本地管理，確定要發布時再用 PicList 上傳並產生外鏈。
- 若做「提示詞詞庫公開版」，可用 PicList 管理圖片 CDN/圖床來源，但要避免把私人或未公開素材同步出去。
- 可和 Obsidian/Markdown 寫作結合：文章中的圖片由 PicList 自動上傳，無限只保存 URL、標籤和摘要，不直接保存圖片。

## 工具判斷

- 能不能本地使用：
  - 能。GitHub README 提供 Windows Winget/Scoop、macOS Homebrew、直接下載、Docker、源碼開發等方式。
- 是否需要帳號/API/付費：
  - PicList 本身 MIT 開源免費。
  - 實際使用的儲存平台可能需要帳號/API key/雲服務費，例如 OSS、COS、S3、WebDAV、GitHub token 等。
- 是否適合接入目前網站：
  - 適合做圖片上傳/外鏈管理層，尤其是公開網站需要圖片 URL 時。
  - 不建議直接把整個 GUI 嵌入網站；更適合透過 PicList-Core 或本地 `picgo-server` API 串接。
- 是否適合做成 Codex skill：
  - 適合。可做 `piclist-upload` skill：把指定本地圖片上傳、取得 URL、更新 prompt-library 或 Markdown。
- 風險或限制：
  - 使用 GitHub 當大量圖床可能有政策/容量/流量風險。
  - 雲端同步刪除要小心，誤刪可能影響已發布文章圖片。
  - 私密圖片不可傳到公開圖床。
  - 若接本地服務，需保護上傳 key，避免 36677 端口被他人濫用。

## 下次調用關鍵字

PicList, PicGo, 圖床, 圖片上傳, 圖片外鏈, prompt-library 公開圖片, Cloudflare Pages 圖片, WebDAV 圖床, S3 圖床, GitHub 圖床, Obsidian 圖片上傳, Typora 圖片上傳, picgo-server, PicList-Core

## GitHub update check - 2026-06-10


- Repo: `Kuingsmile/PicList`
  - Card date: `2026-05-23`
  - Default branch: `dev`
  - HEAD: `13f4c49ab04a`
  - Latest commit: `2026-06-08T09:31:02Z` - :sparkles: Feature(custom): add support for ULID in advanced rename
  - Commit URL: https://github.com/Kuingsmile/PicList/commit/13f4c49ab04af365b05faec957d7aa45543cdcdb


---

## huangserva/3DCellForge：AI 圖生 3D 互動工作台

- 原路徑：`inbox/2026-05-22-3dcellforge-repo.md`
- 日期：2026-05-22
- 類型：inbox 來源卡（未驗證）

# huangserva/3DCellForge：AI 圖生 3D 互動工作台

Source: https://github.com/huangserva/3DCellForge
Date: 2026-05-22
Type: repo_tool
Tags: 3D, image-to-3D, GLB, React, Three.js, React Three Fiber, Tripo, Fal.ai, Hunyuan3D, Hyper3D, 3D展示, 工作台
Tool Potential: high
Prompt Library Impact: medium

## 一句話摘要

`3DCellForge` 是一個 React + Three.js 的 AI 圖生 3D / GLB 檢查 / 展示工作台，可把上傳參考圖或 GLB 放進三欄式 WebGL 介面中生成、檢查、展示、截圖與匯出。

## 核心內容

Repo README 將它定位為 **AI-powered interactive 3D model generation, inspection, and presentation studio**。

主要能力：

- React Three Fiber 互動式 3D 模型 viewer。
- 三欄工作台：左側模型庫，中間 WebGL 舞台，右側資產/生成工具。
- 支援旋轉、縮放、隔離部件、檢查細節、匯出目前場景。
- 物件感知 inspector，可推斷類別、來源、provider 狀態、材質焦點、demo value、tags。
- 生成 GLB 品質分數：檔案大小、三角面數、貼圖數、demo readiness。
- Demo Mode：隱藏側欄，使用物件感知 cinematic camera path，適合截圖/錄影。
- 模型庫 drawer：縮圖、provider 狀態、task id、GLB URL、比較、刪除。
- 生成/匯入模型透過 IndexedDB/localStorage 在刷新後恢復。
- 支援 Hyper3D、Tripo、Fal.ai、Hunyuan3D、JS Depth、Local GLB。
- API key 保存在 Node backend `.env.local`，不暴露到前端。

技術棧：

- React
- Vite
- Three.js
- React Three Fiber
- Drei
- Framer Motion
- Node backend
- optional Tripo / Fal.ai / Hunyuan3D / Hyper3D Rodin providers

## 可重複使用的規則

1. 圖生 3D 不只需要生成模型，還需要「檢查、展示、比較、保存、錄屏」的完整工作台。
2. 3D provider API key 應留在 server-side，不要進前端 bundle。
3. 成功生成/匯入的 GLB 要本地 cache，避免 provider 臨時 URL 失效。
4. Demo Mode 很重要：生成工具不只要能做，也要能乾淨地展示成果。
5. 3D 模型需要品質卡：檔案大小、三角面數、貼圖數、展示可用度。
6. 對使用者來說，左側資產庫 + 中央舞台 + 右側工具面板，是比單頁 upload 更實用的 UI。

## 可轉成工具/詞庫的部分

可轉成：

- `AI 3D 資產工作台`：圖片/GLB 上傳、模型庫、3D 預覽、截圖、demo mode。
- `圖生 3D Prompt 產生器`：先分析圖片用途，再產出給 Tripo/Fal/Hunyuan 的更穩定 prompt。
- `GLB 品質檢查器`：檢查檔案大小、面數、貼圖、是否適合網頁展示。
- `3D Demo 封面/短片工作流`：用 demo mode 截圖或錄屏，變成 X 文章素材。

可新增到提示詞詞庫的概念：

- 圖生 3D 參考圖 prompt
- model demo readiness
- GLB asset inspection
- object-aware cinematic camera path
- productized model library

## 對目前專案的用法

目前不建議直接把它整個接進 AI Creator Toolkit，因為它是一個完整 3D 工作台，體量比現有工具頁大很多。

更實際的用法：

- 參考它的 UI：模型庫 / 舞台 / 工具面板三欄布局。
- 參考它的圖生 3D provider abstraction。
- 之後如果要做「AI 影片故事版 → 3D 資產」或「圖生 3D 工具頁」，可用它當藍本。
- 可與之前收的 3D 細胞 demo / Tripo3D 工作流合併成一條「AI 圖片 → 3D 模型 → 展示」資料線。

## 工具判斷

- 能不能本地使用：
  - 可以。README 提供 `npm install`、`npm run dev`，後端用 `npm run dev:api`。

- 是否需要帳號/API/付費：
  - 基本 GLB 匯入/展示不一定需要。
  - 圖生 3D provider 需要對應 API key：`TRIPO_API_KEY`、`FAL_API_KEY`、`RODIN_API_KEY`、`OPENAI_API_KEY` 等。
  - Hunyuan3D 可走本地 API server。

- 是否適合接入目前網站：
  - 短期不適合整包接入。
  - 適合拆概念：3D 資產庫、GLB viewer、模型 demo mode、圖生 3D prompt。

- 是否適合做成 Codex skill：
  - 適合做「3D 資產工作流」skill：生成圖片、送 provider、下載/整理 GLB、檢查品質、產出展示頁。

- 風險或限制：
  - 3D provider 成本與 API key 管理要注意。
  - GLB 品質差異大，不能保證每張圖都可生成可展示模型。
  - 若接網站，需要處理檔案上傳、安全、儲存、使用者配額。

## 下次調用關鍵字

- 3DCellForge
- 3D Model Studio
- 圖生 3D 工作台
- GLB 檢查
- React Three Fiber
- Tripo
- Fal.ai
- Hunyuan3D
- Hyper3D Rodin
- 3D 資產展示

## 詞庫增量

- 可新增標籤：
  - 圖生3D
  - GLB
  - 3D工作台
  - React Three Fiber
  - Tripo
  - Fal.ai
  - Hunyuan3D
  - Hyper3D
  - 模型檢查
  - Demo Mode

- 可新增模板：
  - 圖片生成後轉 3D 資產流程卡。
  - `image-to-3D prompt + GLB quality check + demo screenshot` 工作流。

- 可新增救場詞：
  - clean silhouette
  - single isolated subject
  - no text labels
  - clear object boundary
  - material separation
  - front / side / three-quarter reference


---

## LingyiChen-AI/boris-prompts：AI Agent 任務 Prompt 壓縮與改寫 Skill

- 原路徑：`inbox/2026-05-22-boris-prompts-repo.md`
- 日期：2026-05-22
- 類型：inbox 來源卡（未驗證）

# LingyiChen-AI/boris-prompts：AI Agent 任務 Prompt 壓縮與改寫 Skill

Source: https://github.com/LingyiChen-AI/boris-prompts
Date: 2026-05-22
Type: repo_tool
Tags: prompt engineering, Claude Code, ChatGPT, Cursor, AI agent, Codex skill, task prompt, prompt compression, BORIS, software development
Tool Potential: high
Prompt Library Impact: medium

## 一句話摘要

`boris-prompts` 是一套給 AI coding agent / AI assistant 用的 Prompt 優化 skill，核心是把冗長、模糊、像人話的需求，壓縮成更短、更精準、更適合 AI agent 執行的任務 prompt。

## 核心內容

Repo README 將 BORIS Prompts 定位為「the advanced AI prompt optimizer that transforms messy, verbose prompts into precise, actionable instructions for AI coding assistants and chatbots」。

它的目標使用場景：

- Claude Code
- ChatGPT
- Cursor
- Windsurf
- Bolt.new
- Cline
- v0
- Grok
- 通用 AI assistant / chatbot

核心能力：

- 把長而散的需求壓縮成可執行 prompt。
- 清除多餘文字，但保留真正重要的上下文。
- 針對 coding assistant 和 general AI assistant 都可用。
- 支援清晰任務描述、步驟、約束、預期輸出。
- Repo 中提供 Claude Code skill 結構，主要檔案是 `skills/boris-prompts/SKILL.md`。

README 強調的效果：

- 減少 token 浪費。
- 降低 AI 理解偏差。
- 提升 task completion success rate。
- 讓 prompt 從「我想要很多東西」變成「AI 可以直接做的任務」。

## 可重複使用的規則

1. 好的 agent prompt 要短，但不能少關鍵上下文。
2. 先把需求拆成：目標、上下文、限制、步驟、輸出格式。
3. 刪掉情緒化、重複、無行動價值的文字。
4. 對 coding task，要明確寫：
   - 要改什麼
   - 哪些檔案/範圍
   - 不要改什麼
   - 如何驗證
   - 最終回報格式
5. 對一般聊天/寫作任務，要明確寫：
   - 受眾
   - 語氣
   - 長度
   - 格式
   - 禁止事項
6. prompt 壓縮不是刪越多越好，而是讓每句話都有任務價值。
7. 對 AI agent 來說，最重要的是「可執行」，不是「寫得像完整文章」。

## 可轉成工具/詞庫的部分

可轉成：

- `AI 任務 Prompt 壓縮器`
- `Codex 任務提示詞優化器`
- `網站工具需求改寫器`
- `Claude/Codex/Cursor 任務模板生成器`
- `長需求 → 可執行任務清單`

可新增模板：

```text
目標：
上下文：
限制：
需要修改/生成：
不要做：
驗證方式：
輸出格式：
```

適合用在使用者常見情境：

- 「幫我做網站功能」前，先壓成明確開發任務。
- 「收進無限」前，先抽出知識卡重點。
- 「寫小說」前，先抽成章節規則、字數、檢查項。
- 「生成圖片」前，先抽主體、場景、風格、鏡頭、負面約束。

## 對目前專案的用法

這個 repo 對目前工作流很有用，但不用整包照搬。更適合抽成兩個方向：

1. 做成本地 Codex skill：`任務Prompt優化`
   - 當使用者貼很長需求時，先幫忙濃縮成可執行版本。
   - 特別適合網站開發、小說規則、提示詞工具、無限吸收。

2. 放進 AI Creator Toolkit：
   - 做一個公開工具：`AI 任務提示詞整理器`
   - 使用者輸入很亂的需求，輸出清晰 prompt 給 ChatGPT / Claude / Codex / Cursor。

它和目前的 `無限吸收` 有互補：

- `boris-prompts`：把任務 prompt 寫清楚。
- `無限吸收`：把資料吸收成知識卡。

它和 `角色設計` 也互補：

- `boris-prompts`：先把自然語言需求整理成清楚欄位。
- `角色設計`：再把欄位翻成圖像生成提示詞。

## 工具判斷

- 能不能本地使用：
  - 可以。Repo 提供 Claude Code skill 結構，可作為 Codex skill 參考。

- 是否需要帳號/API/付費：
  - 不需要特定 API。它本質是 prompt/skill 文件。

- 是否適合接入目前網站：
  - 適合做成一個工具頁：`AI 任務 Prompt 壓縮器`。
  - 也適合加到現有 `AI Prompt 出片率檢查器` 或 `Prompt 結構拆解` 的文字任務模式。

- 是否適合做成 Codex skill：
  - 很適合。可建立一個本地 skill，當使用者需求很長、很亂、含多個目標時，先輸出「清理後任務 prompt」再執行。

- 風險或限制：
  - 過度壓縮可能刪掉使用者真正想保留的語氣或背景。
  - 對創作類任務，不應把所有情緒與風格都壓掉。
  - 需要保留使用者硬規則，例如字數、輸出路徑、不能改舊檔、不能生成某類內容。

## 下次調用關鍵字

- boris-prompts
- BORIS
- prompt optimizer
- 任務 prompt 壓縮
- Codex 任務提示詞
- Claude Code skill
- 長需求整理
- 可執行 prompt
- AI 任務整理器

## 詞庫增量

- 可新增標籤：
  - 任務prompt
  - prompt壓縮
  - agent prompt
  - Codex
  - Claude Code
  - Cursor
  - 需求整理
  - 可執行任務

- 可新增模板：
  - `目標 / 上下文 / 限制 / 要做 / 不要做 / 驗證 / 輸出格式`
  - `messy request → actionable agent prompt`
  - `長需求 → 任務清單`

- 可新增安全替換詞：
  - 無特定安全詞。本 repo 重點是 task prompt 工程。

- 可新增負面詞：
  - vague instruction
  - unclear scope
  - missing output format
  - no verification step
  - excessive context
  - conflicting requirements

- 可新增救場詞：
  - clarify goal
  - preserve hard constraints
  - remove low-signal text
  - define output format
  - specify validation
  - separate must-have and optional


---

## msitarzewski/agency-agents 筆記

- 原路徑：`inbox/2026-05-21-agency-agents-repo.md`
- 日期：2026-05-21
- 類型：inbox 來源卡（未驗證）

# msitarzewski/agency-agents 筆記

Date: 2026-05-21
Source: https://github.com/msitarzewski/agency-agents
License: MIT
Tags: AI agents, Claude Code, Cursor, Gemini CLI, GitHub Copilot, subagents, agent personalities, workflow templates, AI agency

## 核心定位

`msitarzewski/agency-agents` 是一套「AI agency」角色庫。它不是單純 prompt 集，而是把不同專業職能做成可安裝、可引用、可改寫的 agent Markdown 檔。每個 agent 都包含身份、個性、任務邊界、流程、交付物和成功指標。

作者把它定位成：一組專業 AI 團隊成員，例如前端工程師、後端架構師、成長行銷、Reddit 社群、UI 設計、證據收集、Reality Checker 等。

## 主要特色

- 專業分工：每個 agent 聚焦一個領域，而不是泛用「你是一位專家」。
- 有人格與語氣：agent 有自己的行為風格、偏好和溝通方式。
- 交付導向：要求產出實際結果，如代碼、審查、報告、策略、文件。
- 有工作流程：每個 agent 有 step-by-step process。
- 有成功指標：用可衡量標準判斷是否完成。
- 可移植：能轉成多種工具格式。

## 分類

README 中列出大量 division，包括：

- Engineering：Frontend Developer、Backend Architect、AI Engineer、DevOps、Security Engineer、Code Reviewer、SRE、Database Optimizer、Technical Writer 等。
- Design：UI Designer、UX Researcher、Brand Guardian、Visual Storyteller、Whimsy Injector、Image Prompt Engineer、Inclusive Visuals Specialist。
- Paid Media：PPC、Search Query、Tracking、Ad Creative、Paid Social 等。
- Sales：Outbound、Discovery、Deal Strategist、Sales Engineer、Proposal、Pipeline 等。
- Marketing：Growth Hacker、Content Creator、Twitter/X、TikTok、Instagram、Reddit、SEO、Bilibili、小紅書、抖音、微博、私域、跨境電商等。
- Product：Sprint Prioritizer、Trend Researcher、Feedback Synthesizer、Behavioral Nudge Engine、Product Manager。
- Project Management：Studio Producer、Project Shepherd、Experiment Tracker、Senior PM、Jira Workflow Steward。
- Testing：Evidence Collector、Reality Checker、Test Results Analyzer、Performance Benchmarker、API Tester、Accessibility Auditor。
- Support：Support Responder、Analytics Reporter、Finance Tracker、Infrastructure Maintainer、Legal Compliance Checker、Executive Summary Generator。
- Game Development：Game Designer、Level Designer、Narrative Designer、Unity、Unreal、Godot、Blender、Roblox 等。
- Academic：Anthropologist、Geographer、Historian、Narratologist、Psychologist。
- Specialized / Integrations / Finance 等其他大量角色。

## 安裝與支援工具

README 說明原生支援 Claude Code，也提供轉換與安裝腳本給多工具使用。

典型用法：

```bash
./scripts/install.sh --tool claude-code
./scripts/convert.sh
./scripts/install.sh
```

支援工具包括：

- Claude Code：複製 `.md` agents 到 `~/.claude/agents/`
- GitHub Copilot：複製到 GitHub/Copilot agent 目錄
- Antigravity / Gemini：轉成 `SKILL.md`
- Gemini CLI：轉成 extension + skills
- OpenCode：轉成 `.opencode/agents/`
- Cursor：轉成 `.mdc` rules
- Aider：整合成 `CONVENTIONS.md`
- Windsurf：整合成 `.windsurfrules`
- OpenClaw：轉成 `SOUL.md` + `AGENTS.md` + `IDENTITY.md`
- Qwen Code：轉成 SubAgent
- Kimi Code：轉成 YAML agent spec

## Agent 模板結構

新增 agent 時建議包含：

- Frontmatter：name、description、color
- Identity & Memory
- Core Mission
- Critical Rules
- Technical Deliverables with examples
- Workflow Process
- Success Metrics

這對自建工具助手、網站內角色助手、Prompt 生成器、AI 工作流頁很有參考價值。

## 可借鑑到本地專案的點

1. 網站工具助手可改成「角色職能分工」
   - 例如：Prompt Engineer、Prompt Score Checker、Character Card Builder、Storyboard Planner、Feedback Synthesizer。

2. AI 角色工作台可以新增「agent 卡模板」
   - 不只做 SillyTavern 角色卡，也能做工作型 agent 卡：身份、任務、規則、流程、輸出格式、成功指標。

3. 提示詞詞庫可以加分類
   - 圖像 prompt、影片 prompt、X 內容、角色卡、世界書、工具站 SEO、廣告文案。

4. 回饋表單可用 Feedback Synthesizer 思路
   - 收集使用者回饋後，整理成問題分類、優先級、新工具需求。

5. 對 Codex skills 有啟發
   - repo 的 agent 結構可轉譯成 Codex skill 或本機「角色設計」類似的專門工作流。

## 對使用者的實際價值

這個 repo 適合拿來參考「如何設計專業代理角色」，不是直接拿來讓網站變強。真正有用的是抽取它的 agent 設計格式，做成你自己的：

- AI 創作者工具箱助手
- Prompt 出片率教練
- 角色卡生成 agent
- X 內容策略 agent
- 工具站 SEO / AdSense 準備 agent
- 使用者回饋整理 agent

## GitHub update check - 2026-06-10


- Repo: `msitarzewski/agency-agents`
  - Card date: `2026-05-21`
  - Default branch: `main`
  - HEAD: `a077c9ac0be3`
  - Latest commit: `2026-06-07T20:42:10Z` - feat: add GIS division with 13 specialized agents across 4 tiers (#572)
  - Commit URL: https://github.com/msitarzewski/agency-agents/commit/a077c9ac0be381ec15e7dcbb690f641d6091a5db


---

## 多 Agent 團隊復刻 3D 細胞教學 Demo 工作流

- 原路徑：`inbox/2026-05-21-agent-team-3d-cell-demo-workflow.md`
- 日期：2026-05-21
- 類型：inbox 來源卡（未驗證）

# 多 Agent 團隊復刻 3D 細胞教學 Demo 工作流

Source: user-provided longform note; verified repo: https://github.com/limin112/cell; product site: https://www.helio.im/
Date: 2026-05-21
Type: tool_idea
Tags: 多Agent, Helio, AI-native workforce, 3D細胞, GPT Image 2, Tripo3D, 教育Demo, PM工作流, AI監工
Tool Potential: high
Prompt Library Impact: yes

## 一句話摘要

這篇的核心不是 3D 細胞本身，而是用 HR/PM/內容工程師/全棧工程師組成多 Agent 團隊，把人類角色縮到「定需求、授權、生成關鍵圖、跑圖生 3D、收包」。

## 核心內容

目標產品是一個給小學/初中生用的互動式 3D 細胞教學站：

- 中央可旋轉、可剖切的風格化 3D 細胞。
- 旁邊放真實顯微鏡照片。
- 側邊用白話中文講解。
- 覆蓋植物細胞、動物細胞、神經元、白細胞、肌肉細胞等。
- 包含多個細胞器與 3D/2D 教學資產。

經 GitHub README 驗證，`limin112/cell` repo 名為 **Cell Architecture Studio**，描述為互動式 3D 細胞生物學探索器，面向中國小學/初中學生；技術棧包含 React 18、TypeScript、Vite、react-three-fiber、drei、three.js、Tailwind CSS；README 也說明 3D 資產流程是 GPT Image 2 生成關鍵幀，再丟 Tripo3D image-to-3D 導出 GLB。

## 多 Agent 工作流

1. 先讓 HR 招人
   - 全棧搭建網站。
   - 內容專家兼提示詞工程師，拆解細胞結構並產出圖片提示詞。
   - PM，負責拉通、對齊、拆任務、看進度。

2. 給 PM 授權
   - 所有任務寫進 task list。
   - 使用者只看進度，不逐項審批。
   - PM 負責判斷何時升級、何時自己決策。

3. 人類只做 AI 團隊當下不方便做的外部工具步驟
   - 用 GPT Image 2 生成細胞關鍵幀圖。
   - 用 Tripo3D image-to-3D 生成 GLB / 分享連結。

4. 等 PM 通報完成
   - 不審 PR、不看 commit、不插手工程細節。
   - 等 task completed 後讓團隊打包下載。

核心口訣：

```text
小白復刻 = 花錢招最牛逼的人/AI，自己當甩手掌櫃。
```

更抽象的流程：

```text
需求 + 截圖 + 參考案例
→ HR 建團隊
→ PM 拆 task 並獲得授權
→ 各 Agent 自主完成內容/工程/測試
→ 人類補外部不可自動化步驟
→ PM 收斂與交付
```

## 可重複使用的規則

1. 多 Agent 任務不要只叫「幫我做」，要先定角色：HR、PM、工程、內容、設計、測試。
2. PM 必須能決策，不能只是傳話筒；否則所有阻塞都會回到使用者身上。
3. Task list 是多 Agent 協作的核心可視化層，比單純聊天更容易控進度。
4. 人類要主動標出「我自己做」和「AI 團隊做」的邊界。
5. 外部工具步驟如果暫時不能自動化，就變成人類介入點，例如 GPT Image 2 生圖、Tripo3D 圖生模型。
6. 給內容工程師參考截圖/風格錨，比只給一句需求更穩。
7. 先做可跑 demo，再補完整資產與細節。
8. 多 Agent 工作流的價值在於 AI-in-loop：用 AI 監工 AI，而不是人逐條監工 AI。

## 3D 細胞圖像風格錨

可復用 Style Anchor：

```text
Vibrant semi-realistic scientific illustration, painterly textures, bold volumetric 3D-sculpted forms, rich polychromatic palette, at least 4 distinct saturated hues per subject, plump readable organelles, contemporary children's science picture book, soft even studio lighting, warm off-white paper-textured background, single isolated subject, no text, no labels, no arrows, no scale bar.
```

中文摘要：

```text
鮮明半寫實科學插畫，繪畫質感，所有結構都是厚實立體雕塑感，不要扁平線稿；多彩高飽和配色，每個細胞器都飽滿、易讀、像兒童科普圖鑑；柔和無方向棚拍光，暖白紙張背景，單一主體，無文字、無標籤、無箭頭、無比例尺。
```

適合資產：

- `plant-cell`
- `animal-cell`
- `neuron`
- `white-blood-cell`
- `epithelial-cell`
- `bacterial-cell`
- `muscle-cell`
- `nucleus`
- `mitochondrion`
- `cell-membrane`
- `endoplasmic-reticulum`
- `golgi-apparatus`
- `lysosome`

## 可轉成工具/詞庫的部分

可做成以下工具或模板：

- `多 Agent 專案啟動器`：輸入目標、受眾、參考圖、自己要保留的任務，自動生成 HR 招人 prompt、PM 授權令、task list。
- `AI Demo 復刻工作流生成器`：針對教學 demo、工具站、3D/互動展示，自動拆角色與步驟。
- `GPT Image 2 科學插畫資產生成器`：用 Style Anchor 生成統一風格的生物、器官、零件、圖示。
- `圖生 3D 資產管線卡`：記錄「圖片 prompt → 生成圖 → Tripo3D → GLB 命名 → public/models」。
- `PM 授權提示詞模板`：強調不逐項審批、所有工作進 task list、PM 主動升級阻塞。

## 對目前專案的用法

對使用者目前最有用的是把這套方法放進 Codex/Helio 類工作流，而不是照抄 3D 細胞：

- 做網站新工具時，可先用「HR 招人 + PM 授權 + task list」拆工作。
- 做提示詞詞庫新功能時，可讓「內容工程師」負責詞庫/文案，「全棧」負責頁面，「PM」負責驗收。
- 做圖片/3D/影片 demo 時，保留外部生成工具作為人類介入點，其他讓 Agent 團隊處理。
- 可參考 `limin112/cell` 的資料夾結構：`src/data` 放 schema 與文案，`public/models` 放 GLB，`artifacts` 放 prompts 與來源。

## 工具判斷

- 能不能本地使用：
  - `limin112/cell` repo 可本地跑，README 顯示使用 `npm ci`、`npm run dev`、`npm run build`、`npm run typecheck`。
  - Helio 是外部 AI-native team workspace，需上網站使用。

- 是否需要帳號/API/付費：
  - Helio 可能需要帳號與額度；原文提到公測期有免費額度，但這屬於時間敏感資訊，需使用前再確認。
  - GPT Image 2 與 Tripo3D 依各自平台方案使用。

- 是否適合接入目前網站：
  - 不適合直接接 Helio 到網站；比較適合把它的工作流抽象成網站工具或 Codex skill。
  - 3D 細胞 repo 可作為互動式教育 demo 參考，不是 AI Creator Toolkit 的直接功能。

- 是否適合做成 Codex skill：
  - 適合。可做 `多Agent專案啟動` skill，輸出角色配置、PM 授權令、task list、外部工具步驟與驗收清單。

- 風險或限制：
  - 多 Agent 容易產生表面完成但細節未驗證，需保留最後驗收。
  - 外部工具生圖/圖生 3D 可能需要人工挑圖與品質控制。
  - 科學教育內容需要基本正確性審查，不應只靠視覺好看。
  - 顯微鏡參考照片有授權問題；`limin112/cell` README 指出 `artifacts/cell-studio/lm-refs/` 下照片不在 MIT license 範圍內，需按各自 attribution 使用。

## 下次調用關鍵字

- 多 Agent 團隊
- Helio
- AI-native workforce
- AI in loop
- PM 授權令
- HR 招人 prompt
- 3D 細胞 demo
- GPT Image 2 科學插畫
- Tripo3D
- Cell Architecture Studio

## 詞庫增量

- 可新增標籤：
  - 科學插畫
  - 3D細胞
  - 教育Demo
  - 生物教學
  - volumetric
  - 兒童科普
  - GPT Image 2
  - Tripo3D
  - GLB
  - 多Agent

- 可新增模板：
  - `Style Anchor v2` 科學插畫風格錨。
  - 細胞/細胞器資產命名模板：`{asset-id}.png`、`{asset-id}.glb`。
  - 多 Agent HR 招人 prompt。
  - PM 授權令 prompt。

- 可新增安全替換詞：
  - 無特定安全詞；本篇主要是教育與工作流。

- 可新增負面詞：
  - no text
  - no labels
  - no arrows
  - no scale bar
  - not flat drawing
  - not thin line art
  - not monochromatic
  - no delicate wisps

- 可新增救場詞：
  - bold volumetric 3D-sculpted forms
  - plump readable organelles
  - at least 4 distinct saturated hues
  - soft even studio lighting
  - warm off-white paper-textured background
  - subject fills 80-85% of frame
  - three-quarter cross-section cutaway

- 可新增範例方向：
  - 兒童科普圖鑑風細胞插畫
  - 3D 雕塑感細胞器資產
  - 植物細胞剖切圖
  - 神經元橫向圖
  - 白細胞彩色顆粒剖面
  - 骨骼肌纖維條紋剖面


---

## 2026-05-14 LearningCell Research Note

- 原路徑：`inbox/2026-05-14-learningcell-research-note.md`
- 日期：2026-05-14（依檔名）
- 類型：inbox 來源卡（未驗證）

# 2026-05-14 LearningCell Research Note

Source:
- GitHub: https://github.com/GordenSun/LearningCell
- Accessed: 2026-05-14.

What it is:
- `LearningCell` is a Chinese classroom-oriented interactive 3D biology teaching web app.
- It displays five real-scale cell / molecular `.glb` models:
  - plant cell,
  - animal cell,
  - white blood cell,
  - neuron,
  - DNA double helix.

Tech stack:
- Vite + React 19 + TypeScript.
- three.js / `@react-three/fiber` / `@react-three/drei`.
- `DRACOLoader` with local wasm decoders, so Draco decoding works offline without hitting `gstatic`.
- Custom streaming loader using `fetch + ReadableStream` to report real download progress.

Useful repo ideas:
- Treat it as a polished 3D model viewer scaffold.
- Good patterns to borrow:
  - sidebar model selector,
  - 3D viewer canvas,
  - info panel per model,
  - `.glb` model organization under `public/models`,
  - local Draco decoder under `public/draco`,
  - real loading progress and percentage,
  - background preloading after the first model loads,
  - `force-cache` browser caching for `.glb`,
  - GitHub Pages deploy workflow.

Local dev from README:
```bash
cd app
npm install
npm run dev
```

Build:
```bash
cd app
npm run build
npm run preview
```

Directory shape:
```text
.
├── .github/workflows/deploy.yml
├── README.md
├── app/
│   ├── public/
│   │   ├── draco/
│   │   ├── images/
│   │   └── models/
│   ├── src/
│   │   ├── components/
│   │   ├── data/models.ts
│   │   ├── hooks/useModel.ts
│   │   ├── lib/modelLoader.ts
│   │   ├── App.tsx
│   │   └── ...
│   └── package.json
```

Applicability to 3D Hanfu:
- Useful for viewing/showcasing 3D Hanfu models, not for creating garment geometry from scratch.
- It can provide the web shell for:
  - rotating/zooming a Hanfu model,
  - switching styles,
  - loading `.glb` variants,
  - showing material/style notes,
  - previewing fabric/embroidery themes,
  - comparing multiple outfits.
- It does not solve:
  - human body rigging,
  - garment simulation,
  - cloth physics,
  - automatic image-to-3D,
  - accurate Tang/Song/Ming garment pattern construction.

Recommended 3D Hanfu workflow inspired by LearningCell:
1. Asset source:
   - make or obtain `.glb` character/garment models,
   - use Blender / Marvelous Designer / CLO / Meshy / Tripo / Rodin / Hunyuan3D-style tools as upstream model generators,
   - export optimized `.glb`.
2. Optimization:
   - reduce polygon count,
   - bake textures,
   - compress textures,
   - Draco-compress geometry,
   - keep variants ideally under 10-30 MB each.
3. Viewer:
   - clone LearningCell-like architecture,
   - replace biology data with Hanfu style data,
   - put models in `public/models/hanfu`,
   - put thumbnails in `public/images/hanfu`,
   - use side navigation for style variants.
4. Controls:
   - orbit/zoom/pan,
   - reset view,
   - lighting presets,
   - background presets,
   - material notes,
   - optional texture/color selector.
5. Content model:
   - title,
   - dynasty/style,
   - silhouette,
   - collar,
   - sleeves,
   - skirt/pao structure,
   - fabric,
   - embroidery,
   - accessories,
   - model path,
   - thumbnail path.

Suggested MVP:
- Build `D:\codex\projects\hanfu-3d-viewer`.
- Start with placeholder `.glb` models if no Hanfu assets exist yet.
- Implement:
  - one full-screen 3D viewer,
  - left style selector,
  - right description panel,
  - progress bar,
  - model preloading,
  - lighting/background presets.
- Once real Hanfu `.glb` exists, swap it in.

Risk assessment:
- Low risk for a 3D viewer.
- Medium/high risk for real 3D Hanfu asset creation because garment quality depends on source models, cloth topology, texture detail, and rigging.
- Best first deliverable is not "AI generates perfect 3D Hanfu"; it is "a reusable 3D Hanfu model browser/viewer with a clean asset pipeline."

Tags: learningcell, threejs, react-three-fiber, vite, glb, draco, 3d-viewer, hanfu, asset-pipeline


---

## 2026-05-12 GenericAgent Research Note

- 原路徑：`inbox/2026-05-12-genericagent-research-note.md`
- 日期：2026-05-12（依檔名）
- 類型：inbox 來源卡（未驗證）

# 2026-05-12 GenericAgent Research Note

Source:
- GitHub: https://github.com/lsdefine/GenericAgent
- Accessed: 2026-05-12

What it is:
- GenericAgent is a minimal self-evolving autonomous agent framework.
- Repo claims the core is about 3K lines, with a roughly 100-line agent loop.
- Goal: give an LLM system-level control over a local computer using a small atomic toolset plus layered memory.

Why it matters:
- Its key idea matches the user's "無限" direction: do not preload every skill; let the agent solve tasks and crystallize successful paths into reusable skills.
- Could inspire local Codex workflows:
  - better task archive memory,
  - reusable SOP/Skill growth,
  - Telegram bot frontend,
  - lightweight local agent experiments,
  - lower-token workflow routing.

Core philosophy:
- Do not prebuild all capabilities.
- Let each solved task become a reusable skill.
- Over time, build a personal skill tree from real work.

Important features from README:
- Self-evolving:
  - Each task execution can be summarized into a reusable Skill.
  - Future similar tasks can recall the Skill directly.
- Minimal architecture:
  - about 3K lines of core code.
  - agent loop is about 100 lines.
- Strong execution:
  - Can use a real browser and preserve login sessions.
  - Covers browser, terminal, filesystem, keyboard/mouse, screen vision, and mobile devices via ADB.
- Model compatibility:
  - Supports models such as Claude, Gemini, Kimi, MiniMax.
- Token efficiency:
  - Designed to run with under 30K context by using layered memory and dense recall.

Self-evolution mechanism:
```text
[New Task]
  -> [Autonomous Exploration: install deps, write scripts, debug, verify]
  -> [Crystallize Execution Path into Skill]
  -> [Write to Memory Layer]
  -> [Direct Recall on Next Similar Task]
```

Layered memory model:
- L0 Meta Rules:
  - core behavior rules and constraints.
- L1 Insight Index:
  - compact routing/recall index.
- L2 Global Facts:
  - stable long-term facts.
- L3 Task Skills / SOPs:
  - reusable task workflows.
- L4 Session Archive:
  - distilled finished-session records for long-horizon recall.

Minimal toolset concept:
- Atomic tools listed in README include:
  - `code_run`: execute code.
  - `file_read`: read files.
  - `file_write`: write files.
  - `file_patch`: patch/modify files.
  - `web_scan`: perceive web content.
  - `web_execute_js`: control browser behavior.
  - `ask_user`: human confirmation.
- Also has memory management tools:
  - `update_working_checkpoint`
  - `start_long_term_update`

Quick start from README:
```bash
git clone https://github.com/lsdefine/GenericAgent.git
cd GenericAgent
pip install requests streamlit pywebview
pip install requests textual
cp mykey_template.py mykey.py
# edit mykey.py with LLM API key
python launch.pyw
```

uv route:
```bash
git clone https://github.com/lsdefine/GenericAgent.git
cd GenericAgent
uv venv
uv pip install -e ".[ui]"
cp mykey_template.py mykey.py
python launch.pyw
```

Frontends:
- Default desktop UI:
  - `python launch.pyw`
- Terminal UI:
  - `python frontends/tuiapp.py`
- Qt desktop app:
  - `python frontends/qtapp.py`
- Streamlit UI:
  - `streamlit run frontends/stapp2.py`
- Telegram bot:
  - configure in `mykey.py`:
```python
tg_bot_token = 'YOUR_BOT_TOKEN'
tg_allowed_users = [YOUR_USER_ID]
```
  - run:
```bash
python frontends/tgapp.py
```

Common chat commands:
- `/new`: start fresh conversation and clear current context.
- `/continue`: list recoverable conversation snapshots.
- `/continue N`: restore the Nth recoverable conversation.

Potential use for our setup:
- Study the memory layering and Skill crystallization approach for `D:\codex\memory-palace`.
- Compare with current Codex workflows:
  - Codex App already has skills/plugins/MCP and local tool control.
  - GenericAgent may be useful as an experimental standalone local agent, especially for Telegram/IM frontend and persistent task skills.
- Its Telegram frontend could be conceptually useful, but our current route is Composio Telegram MCP plus local TG inbox tool.
- The "solve once -> save SOP -> recall later" pattern should be copied into our durable memory habits.

Cautions:
- It grants broad local computer control, so run only in a trusted environment.
- Do not store API keys/tokens in memory.
- Before using its Telegram bot, whitelist allowed users.
- Treat web automation and account/session use carefully.

Tags: genericagent, agent-framework, self-evolving-agent, skill-tree, memory, telegram, browser-automation, local-agent

## GitHub update check - 2026-06-10


- Repo: `lsdefine/GenericAgent`
  - Card date: `2026-05-12`
  - Default branch: `main`
  - HEAD: `3284222725c9`
  - Latest commit: `2026-06-10T03:14:31Z` - memory: subagent.md 更新fork/cwd共享约定
  - Commit URL: https://github.com/lsdefine/GenericAgent/commit/3284222725c9ea7fedae12b63fc90c1aba43cea5


---

## 2026-05-12 OpenCLI Research Note

- 原路徑：`inbox/2026-05-12-opencli-research-note.md`
- 日期：2026-05-12（依檔名）
- 類型：inbox 來源卡（未驗證）

# 2026-05-12 OpenCLI Research Note

Source:
- `https://github.com/jackwener/OpenCLI`
- Checked 2026-05-12.

What it is:
- OpenCLI by `jackwener`.
- GitHub repo: `jackwener/OpenCLI`.
- Description: "Make Any Website & Tool Your CLI" / universal CLI hub and AI-native runtime.
- Purpose: turn websites, browser sessions, Electron apps, and local tools into deterministic command-line interfaces for humans and AI agents.

Useful positioning:
- OpenCLI is not a Telegram MCP by itself.
- It is a CLI/browser automation layer that can expose websites, logged-in Chrome sessions, Electron apps, and local binaries to agents.
- It can be useful as a fallback or parallel route when a direct MCP tool is not available.

Core capabilities:
- Use built-in adapters for sites such as Bilibili, Zhihu, Xiaohongshu, Reddit, HackerNews, Twitter/X, etc.
- Let AI agents operate websites through logged-in Chrome via `opencli browser` primitives.
- Create reusable website adapters using the `opencli-adapter-author` skill.
- Wrap local binaries like `gh`, `docker`, `tg-cli`, `discord-cli`, `wx-cli`, and custom tools.
- Control Electron apps such as Cursor, Codex, ChatGPT, Notion, etc. through CDP-backed integrations.
- Reuses Chrome/Chromium logged-in state; credentials remain in the browser.
- Deterministic CLI output, pipeable/scriptable, no LLM runtime cost.

Install / setup:
- Requires Node.js `>= 21`.
- Install:
  - `npm install -g @jackwener/opencli`
- Install Browser Bridge extension:
  - Chrome Web Store is recommended, or manual install from GitHub releases.
- Verify:
  - `opencli doctor`
- Browser profile helpers:
  - `opencli profile list`
  - `opencli profile rename <contextId> work`
  - `opencli profile use work`
  - `opencli --profile work browser state`

AI-agent skills:
- Install all OpenCLI skills:
  - `npx skills add jackwener/opencli`
- Or install specific skills:
  - `npx skills add jackwener/opencli --skill opencli-adapter-author`
  - `npx skills add jackwener/opencli --skill opencli-autofix`
  - `npx skills add jackwener/opencli --skill opencli-browser`
  - `npx skills add jackwener/opencli --skill opencli-usage`
  - `npx skills add jackwener/opencli --skill smart-search`

Potential Telegram relevance:
- OpenCLI can wrap local binaries, including `tg-cli`.
- Possible route:
  - install/configure a Telegram CLI locally,
  - register it with OpenCLI,
  - call it from Codex through shell/OpenCLI.
- This is different from Composio Telegram MCP:
  - Composio MCP gives direct tool-style access if connected in Codex.
  - OpenCLI gives browser/local-CLI automation and can be useful when direct MCP is unavailable.

Suggested use for this workspace:
- Prefer Composio Telegram MCP for direct Telegram send/read if available in Codex tools.
- Use OpenCLI as a general automation bridge for:
  - websites that require logged-in Chrome,
  - X/Twitter/Xiaohongshu style sites,
  - local CLI wrappers,
  - possible Telegram CLI fallback,
  - Electron app control.

Tags: opencli, cli-automation, browser-automation, telegram-fallback, tg-cli, codex, ai-agent, chrome-session, electron-apps, x-twitter

## GitHub update check - 2026-06-10


- Repo: `jackwener/OpenCLI`
  - Card date: `2026-05-12`
  - Default branch: `main`
  - HEAD: `678d0086d860`
  - Latest commit: `2026-06-06T15:54:06Z` - feat(auth): add refresh maintenance command (#1881)
  - Commit URL: https://github.com/jackwener/OpenCLI/commit/678d0086d860b77305501a6c2c9a25d6b022fb54
