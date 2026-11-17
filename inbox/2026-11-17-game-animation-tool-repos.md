# 遊戲、動畫、音效工具與 Skills repo 清單（2026-11 收）

- 日期：2026-11-17
- 類型：工具
- 標籤：GitHub、Agent Skills、遊戲開發、Blender、Three.js、動畫庫、音效、像素
- 主題卷：09
- 來源：使用者提供的連結；README 於 2026-11-17 讀過
- 狀態：星數、版本、功能使用前重新查證

## 一句話摘要

一批給 AI 代理用的遊戲與動畫工具：四個已裝成本機 Skill，其餘先記在這裡。

## 核心內容

### 已安裝到本機 Claude Code（2026-11-17，安裝結果見當次對話）
- `achimala/dream-loop`：先用生圖「夢」出目標截圖 → 照著做 → 另一個 AI 評審比對實機截圖與目標 → 迴圈。需要生圖能力和視覺輸入。
- `EL4CTEO/blender-skills`：28 個 Blender 技能（建模、UV、貼圖、烘焙、綁骨、動畫、布料、毛髮、匯出到 Unity/Unreal/Godot/Roblox、資產 QA）。需 Blender 5.2 LTS 以上。MIT。
- `MengTo/Skills`：共 183 個技能。只裝了遊戲相關的部分；其餘（web-design 92、3d 16、illustration 14、codex 20、media 7、workflow 4、ui 3）沒裝，要用時再從 repo 取。
- `remotion-dev/skills`：Remotion 官方技能，用 React 程式做影片。安裝指令 `npx skills add remotion-dev/skills`。

### 沒裝，先記著
- `WhiteTowerAI/ohmygame`（https://ohmygame.ai）：開源的 AI 做遊戲桌面工作室。代理寫設計文件、做素材、寫程式、自己試玩、發布成連結。可接 Claude Code、Codex、OpenCode 或 40 多家模型，也能反過來透過 MCP 被代理使用。內建 Godot、Unity、Unreal、Blender、Aseprite、Tiled、微信與抖音小遊戲外掛。Apache-2.0，beta。沒裝的原因：Windows 版尚未簽章，要使用者自己決定是否安裝。
- `Leonxlnx/earshot`：給代理「耳朵」。描述聲音、比對描述、找長錄音裡最好的片段、判斷真錄音或合成、影片聲畫同步時間軸、對照專業發布影片打分；還有 252 個用程式合成的音效庫（`earshot sfx`、`earshot kit`，不用模型）。CLI、Python API、MCP。安裝：`uv tool install "earshot[mcp] @ git+https://github.com/Leonxlnx/earshot"`，需 uv 和 ffmpeg，模型約 1.1 GB。沒裝的原因：本機沒有 uv，且下載量大。
- `ma1902056219-coder/openpixel`：31 個瀏覽器即時繪製的像素實驗（夜池、磁流體、星系相撞、斷冠騎士首領戰、千里江山等），每件一個目錄，附可改的 `source.js`，無需建置。MIT。可當像素特效和小玩法的參考源碼。線上：https://ma1902056219-coder.github.io/openpixel/
- Fil：https://fil.design（HTML 動態設計場景；MengTo 的 `url-to-motion-design` 技能用它）
- ThreeUI：https://threeui.com（3D UI 庫）

### 動畫與 3D 函式庫（需要時才裝進專案）
| 用途 | 庫 |
|---|---|
| AI 做影片的官方技能 | remotion-dev/skills |
| 圖解動畫 | motion-canvas/motion-canvas |
| 畫面切換動效 | motiondivision/motion |
| 數值平滑變動 | franciscop/ola |
| 時間線、錯峰動效 | juliangarnier/anime |
| 公式與圖形動畫 | ManimCommunity/manim |
| 緩動與補間 | jeremyckahn/shifty |
| 2D 向量動畫 | jonobr1/two.js |
| 輕量向量動畫播放 | airbnb/lottie-web |
| 順序動畫 | CreateJS/TweenJS |
| 用 HTML 做 3D 場景 | lume/lume |
| GIF 匯出 | mattdesl/gifenc |
| 可觸摸互動畫布 | konvajs/konva |
| 綁定與角色動畫 | blender/blender |
| 3D 場景 | mrdoob/three.js |
| 遊戲動畫 | godotengine/godot |
| 3D 渲染與動畫 | BabylonJS/Babylon.js |
| 粒子 | drawcall/Proton |

## 可重複使用的規則或模板

- 想讓畫面變好看：用 dream-loop 的做法，先生目標圖，再讓獨立評審比對截圖。
- 遊戲缺音效：先看 earshot 的 `sfx` 音效庫（不用模型）。
- 要像素特效的寫法：先翻 openpixel 對應作品的 `source.js`。

## 什麼時候用（下次調用關鍵字）

dream-loop、blender skills、MengTo Skills、remotion、ohmygame、earshot、音效、openpixel、像素實驗、Fil、ThreeUI、動畫庫、anime.js、manim、lottie、gifenc、Proton
