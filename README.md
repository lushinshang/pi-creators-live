# 寫出不爛的程式碼：Pi 兩位創作者談「放手」的界線

Matt Pocock 在 2026-11-17 的直播裡，請開源 coding agent Pi 的兩位創作者 Mario Zechner 與 Armin Ronacher 談了約 46 分鐘：模型變強之後，哪些事能交給 agent，哪些仍得自己讀。本導讀依對談順序整理，講者的話標示說話者（只在能靠內容確認時才標），並把講者的說法與官方資料對照。另附全文繁體中文譯文與中英雙語字幕播放器。

## 200字介紹

Pi 是開源的 coding agent，兩位創作者 Mario 與 Armin 上 Matt Pocock 的直播，談他們自己怎麼用 agent 寫程式。Armin 說 Opus 5.5 之後，有些有參考測試的任務能長時間無人看管地跑，但不一定能轉成日常的 Pi 工作；Mario 說系統設計與 API 設計沒有大躍升，核心程式碼他仍讀完整個 diff，並認為整個產業在「逃避理解」。對談也談到驗證與 CI 綠燈不等於安全感、用不同模型家族做對抗式審查、系統設計靠迭代，以及黑燈工廠（dark factory）目前沒有人提出做成的例子。導讀逐段附可點擊的時間連結，另有講者說法與官方資料的對照表。本文由 AI 模型製作，字幕為機器字幕，講者辨識只確認了約六成句數。

## 檔案

| 檔案 | 說明 |
|---|---|
| `index.html` | 深度導讀網頁，單檔可直接開啟；Mermaid 圖表由 CDN 載入 |
| `pi-creators-live.md` | 導讀 Markdown 正式稿 |
| `translation-zh.html` | 全文繁體中文譯文（非官方，AI 翻譯，不標示說話者） |
| `player.html` | 中英雙語字幕播放器（YouTube 內嵌，字幕隨播放同步） |
| `images/` | 封面（本機為 16:9、9:16 PNG，發布版為 WebP）與分享圖 `og-hero.jpg`（1200×630） |
| `share_post.md` | 社群分享文 |
| `qa/`、`research/` | 驗收截圖、查證與審稿紀錄、建置腳本，僅留本機 |

## 原始資料

- 類型：影片（直播）
- 名稱：LIVE: Writing code that doesn't suck with the creators of Pi（Matt Pocock 頻道，約 46 分鐘，2026-11-17）
- 網址：https://www.youtube.com/watch?v=ZBTegd8DUZM
- 字幕：使用者提供的字幕檔（`transcription/LIVE_ Writing code that doesn't suck with the creators of Pi.srt`，機器自動字幕，來源軌未標示；824 個 cue，整理成 563 句）。原檔未修改，工作用副本在 `research/`。

## 重要來源

- 第一手與官方（2026-11-18 讀取）：[earendil-works/pi](https://github.com/earendil-works/pi)（MIT、`gh api` 計數）、[CONTRIBUTING.md](https://github.com/earendil-works/pi/blob/main/CONTRIBUTING.md)、[Earendil 官網](https://earendil.com)、[Armin 的文章](https://lucumr.pocoo.org/2026/1/27/earendil/)、[Mario 加入 Earendil](https://lucumr.pocoo.org/2026/4/8/mario-and-earendil/)、[AI Engineer Code Summit 議程](https://www.ai.engineer/code/2026/schedule)、[Anthropic：Opus 5.5](https://www.anthropic.com/news/claude-opus-5-5)、[Claude Fable 5.2](https://www.anthropic.com/news/claude-fable-and-mythos-5-2)、[Rocq 9.0.0](https://rocq-prover.org/releases/9.0.0)、[Sentry 新聞稿](https://sentry.io/about/press-releases/sentry-raises-40m-series-c-to-reinvent-application-performance-monitoring/)、[Meta 大當機說明](https://engineering.fb.com/2021/10/05/networking-traffic/outage-details/)。
- 二手：[Forklog（GPT-6 Astra）](https://forklog.com/en/news/openai-opens-limited-access-to-gpt-6-astra)；OpenAI 官方頁讀取被擋。

## 重要限制

- 字幕是機器自動字幕，未逐句對照原音；中文譯文已依官方資料校正專名，英文字幕保留原樣。
- 講者辨識只確認了 341／563 句（約六成句數，以 cue 起訖時間加總約 56%），其餘寫「來賓」或不標；換人判斷（agy，4 個半窗口逾時）與影格只當線索，沒有逐句聽音訊。
- 講者自述的軼事與數字（例如「啟動時間減少 100%」、每天 40–50 個 issue、「12 個月」）多半查無一手或與官方資料有落差，對照表逐項列出。
- 封面為 AI 生圖，圖內不含文字與真人臉；影片本身沒有逐格檢視。
- 本導讀的研究、翻譯、撰稿、查證與審稿皆由 AI 模型完成（agy gemini-3.8-flash-high 初譯，Claude Sonnet／Opus 撰稿與審稿），沒有人工逐句校稿。

## 狀態

已發布（2026-11-18）。

- 網頁：https://lushinshang.github.io/pi-creators-live/
- Repo：https://github.com/lushinshang/pi-creators-live（公開，Pages 用 `main` 分支根目錄）
- 公開內容只有 `index.html`、`translation-zh.html`、`player.html`、`pi-creators-live.md`、`README.md`、`share_post.md`、`images/`；`qa/` 與 `research/` 不公開。
- 發布版的圖片改為 WebP；`index.html` 以 `PUBLISH_BASE` 重建，`og:image` 為絕對網址。
- `transcription/` 內的原始字幕檔未修改。
