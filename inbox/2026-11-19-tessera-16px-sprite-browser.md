# Tessera-small：瀏覽器本機生成 16×16 像素圖示（Slack Moji）

- 日期：2026-11-19
- 類型：工具＋研究
- 標籤：像素美術、AI 生圖、16x16、sprite、emoji、WebGPU、ONNX、本機推論、離散擴散、Hugging Face
- 主題卷：09
- 來源：示範 https://huggingface.co/spaces/cfahlgren1/slack-moji （使用者分享的 t.co 短網址轉址到這裡）；ONNX 模型 https://huggingface.co/cfahlgren1/tessera-small-onnx ；原始模型 https://huggingface.co/thejagstudio/tessera-small ；原作程式碼在 Space thejagstudio/tessera-pixel-studio
- 狀態：2026-11-19 查證（讀 README 和模型卡，沒有實際跑過）。
- 授權：**權重 CC BY-NC 4.0，不可商用**，要標註原作者 Jagrat Patel（TheJagStudio）。CLIP 文字編碼器是 OpenAI 的，MIT。程式碼沒有另外標授權。

## 一句話摘要

輸入幾個字，在瀏覽器裡用 WebGPU 生成 4 張 16×16 像素圖示，不經過伺服器；模型約 115 MB，第一次載入後會快取。

## 核心內容

- 輸出：16×16，從 512 色調色盤取色，有透明背景；每次 4 張變化，可放大成 128×128 PNG 顯示。
- 模型檔：去雜訊模型 `tessera_w8.onnx`（51 MB，int8）＋ CLIP ViT-B/32 文字編碼器 `clip_text_w8.onnx`（64 MB）。16 步取樣器已移植成 JavaScript。
- 速度（模型卡說法）：瀏覽器 WebGPU 約 1 秒 4 張；Python CPU（onnxruntime）約 2.5 秒 4 張。
- 示範專案：Svelte + Vite，Hugging Face 靜態 Space，透過 onnxruntime-web 從模型 repo 載入，不打包在專案裡。

## 技術拆解（原作模型卡）

- 方法：**遮罩式離散擴散（absorbing state）**。不是 UNet、DiT、VAE，也不是逐格自回歸。畫布從全部 [MASK] 開始，雙向 transformer 每步依信心度平行揭開一批格子。
- 表示：每個像素是一個 token，16×16 = 256 個 token。調色盤 512 色由 OKLab 色彩空間、依出現頻率加權的 k-means 得出（ΔE 0.010）；token 0 是透明，另有 [MASK] token。所以輸出天生是乾淨像素，不會有模糊邊緣。
- 架構：文字與像素合併的 transformer，沙漏形 2 + 8 + 2 個 block，中段 2×2 patch 合併；寬 512、8 頭、4 個 register；QK-RMSNorm、2D 軸向 RoPE、Conv-SwiGLU、adaLN-single、self-conditioning。共 4760 萬參數。
- 條件：凍結的 CLIP 文字塔，24 個 token；訓練時做 CFG dropout，推論 cfg_scale = 3.0。
- 訓練目標：cosine 遮罩排程、塊狀遮罩（blob mask）、感知標籤平滑。
- 取樣：依信心度平行揭開 + CFG + Gumbel 退火選擇 + 空間 NMS；16 步；支援 inpainting（局部重畫）。
- 訓練：資料 Pixel Art Atlas 1.4M（Angais，約 140 萬張精靈圖，授權未寫明）；82,342 步 × 每步 512 張 ≈ 30 個 epoch；單張 RTX PRO 6000 Blackwell 約 5.5 小時；Muon（隱藏層矩陣）+ AdamW、Warmup-Stable-Decay 學習率、EMA 0.9995、bf16、torch.compile。

## 自製路線（2026-11-19 評估）

- 技術本身不受保護；但不能拿 Tessera 權重微調，否則仍受不可商用限制。
- 要商用，訓練資料必須乾淨：CC0（Kenney、OpenGameArt CC0）、自己畫的，或可商用的生圖服務產出。
- 使用者電腦沒有 NVIDIA 顯卡，本機不能訓練；要訓練就租雲端 GPU，數小時。
- 更務實的順序：
  1. 用 GPT 或 Gemini 生圖產出整張圖示表，再用腳本切格、去背、縮成 16 或 32 像素、量化到遊戲調色盤。
  2. 或寫程序式圖示產生器（形狀模板 + 隨機變化 + 調色盤 + 自動描邊陰影）。
  3. 累積幾千張自己的圖後，再考慮照本卡架構訓練小模型。
- 注意：OpenAI 條款禁止用輸出去開發「與 OpenAI 競爭」的模型。用 GPT 圖當自製模型的訓練資料屬於灰色地帶，要訓練前先查最新條款。

## 可重複使用的用法

- 瀏覽器：從模型 repo 複製 `web/tessera.js` → `Tessera.load()` → `generate("prompt")`。
- Python：`python/tessera_onnx.py`，CPU 就能跑。
- 適合：原型的道具、圖示、表情符號佔位圖；讓玩家打字即時生成小圖示。
- 不適合：要上架、販售或領獎金的作品（例如 make.fun 參賽作）。
- 16×16 太小，做不了角色動畫；多姿勢精靈圖請用 sprite-gen 或 video2dsprite（見 2026-11-18 遊戲 AI Skill 地圖）。

## 什麼時候用（下次調用關鍵字）

Tessera、Slack Moji、16x16 像素圖、AI 生成 emoji、瀏覽器本機生圖、WebGPU 生圖、ONNX、離散擴散、masked diffusion、像素圖示產生器、自己訓練像素模型、不可商用模型
