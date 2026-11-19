# Tessera-small：瀏覽器本機生成 16×16 像素圖示（Slack Moji）

- 日期：2026-11-19
- 類型：工具
- 標籤：像素美術、AI 生圖、16x16、sprite、emoji、WebGPU、ONNX、本機推論、Hugging Face
- 主題卷：09
- 來源：示範 https://huggingface.co/spaces/cfahlgren1/slack-moji （使用者分享的 t.co 短網址轉址到這裡）；ONNX 模型 https://huggingface.co/cfahlgren1/tessera-small-onnx ；原始模型 https://huggingface.co/thejagstudio/tessera-small
- 狀態：2026-11-19 查證（讀 README 和模型卡，沒有實際跑過）。
- 授權：**CC BY-NC 4.0，不可商用**，要標註原作者 Jagrat Patel（TheJagStudio）。CLIP 文字編碼器是 OpenAI 的，MIT。

## 一句話摘要

輸入幾個字，在瀏覽器裡用 WebGPU 生成 4 張 16×16 像素圖示，不經過伺服器；模型約 115 MB，第一次載入後會快取。

## 核心內容

- 輸出：16×16，從 512 色調色盤取色，有透明背景；每次 4 張變化，可放大成 128×128 PNG 顯示。
- 模型：去雜訊模型 `tessera_w8.onnx`（51 MB，int8）＋ CLIP ViT-B/32 文字編碼器 `clip_text_w8.onnx`（64 MB）。16 步取樣器已移植成 JavaScript。
- 速度（模型卡說法）：瀏覽器 WebGPU 約 1 秒 4 張；Python CPU（onnxruntime）約 2.5 秒 4 張。
- 示範專案：Svelte + Vite，Hugging Face 靜態 Space，透過 onnxruntime-web 從模型 repo 載入，不打包在專案裡。

## 可重複使用的用法

- 瀏覽器：從模型 repo 複製 `web/tessera.js` → `Tessera.load()` → `generate("prompt")`。
- Python：`python/tessera_onnx.py`，CPU 就能跑。
- 適合：遊戲原型的道具、圖示、表情符號佔位圖；在遊戲裡讓玩家打字即時生成小圖示（例如自訂旗幟、寵物）。
- 不適合：要上架、販售或拿去領獎金的作品（例如 make.fun 參賽作），因為授權不可商用。商用請改用自己畫的、pixelbolt-pixel-art 或 agent-sprite-forge。
- 16×16 太小，做不了角色動畫；需要多姿勢精靈圖請用 sprite-gen 或 video2dsprite（見 2026-11-18 遊戲 AI Skill 地圖）。

## 什麼時候用（下次調用關鍵字）

Tessera、Slack Moji、16x16 像素圖、AI 生成 emoji、瀏覽器本機生圖、WebGPU 生圖、ONNX、像素圖示產生器、不可商用模型
