# 手感回饋預算（hit-stop、震動、coyote time、輸入緩衝）

- 日期：2026-11-17
- 類型：方法庫
- 標籤：game feel、juice、hit-stop、screen shake、coyote time、input buffer、無障礙
- 主題卷：09
- 來源：Godot 論壇 game feel checklist https://forum.godotengine.org/t/game-feel-checklist-for-godot-4-hit-stop-trauma-shake-coyote-time-and-more/145340 ；https://kindatechnical.com/game-development/input-buffering-coyote-time-and-game-feel.html ；https://appscale.blog/en/blog/game-feel-juice-hitstop-screenshake-easing-2026
- 狀態：2026-11-17 查證。數字是經驗值，不是標準。

## 一句話摘要

回饋要照事件重要性分配：小事件 1–2 種回饋，大事件 5–8 種在 100ms 內一起發；每次都全開會讓人暈，也蓋掉真正重要的打擊。

## 核心內容

- Hit-stop：命中時凍結或減速約 2–6 幀。恢復計時器要用真實時間，不然時間比例 0 會卡死。
- Screen shake：用 trauma 值（0–1），震幅 = trauma²，隨時間衰減。依事件大小給 trauma。
- Coyote time：離開平台後約 0.1 秒內仍可跳。
- 輸入緩衝：落地前約 0.1 秒內按的跳也算數。
- 最便宜、效果最大：畫面震動、粒子、時機對的音效。
- 無障礙：提供「減少震動」開關，並尊重 prefers-reduced-motion。

## 可重複使用的規則或模板

| 事件等級 | 例子 | 回饋 |
|---|---|---|
| 小 | 撿東西、腳步 | 音效 + 小縮放 |
| 中 | 命中敵人 | 音效 + 粒子 + 敵人閃白 + 1–2 幀 hit-stop |
| 大 | 擊殺、連鎖、Boss 受傷 | 以上 + 震動 0.4 + 4 幀 hit-stop + 數字跳出 |
| 最大 | 通關、Boss 死 | 以上 + 慢動作 + 閃光 + 音樂變化 |

詳細作法另見已安裝的 game-feel skill；本卡只留分級原則。

## 什麼時候用（下次調用關鍵字）

手感、game feel、juice、hit-stop、畫面震動、coyote time、輸入緩衝、回饋分級
