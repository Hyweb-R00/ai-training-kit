# AI workflow 與 SDD 內訓材料包

更新：2026-11-23。以下是延伸閱讀與工具候選，功能與安裝方式請以各專案文件為準；選擇符合自己工作的工具即可。第三方專案在安裝前先看權限、資料處理方式與授權。

## SDD 開發流程

| 工具 | 是什麼 |
|---|---|
| [GitHub Spec Kit](https://github.com/github/spec-kit) | 以規格、計畫、任務串起開發的工具包。 |
| [OpenSpec](https://github.com/Fission-AI/OpenSpec) | 用 change 與規格管理需求變更的工具。 |
| [Matt Pocock Skills](https://github.com/mattpocock/skills) | 各種可供參考的 agent skills。 |
| [Superpowers](https://github.com/obra/superpowers) | 以 skills 組合開發與驗證流程。 |
| [Everything Claude Code](https://github.com/affaan-m/ECC) | agents、skills 與 hooks 的整合參考。 |
| [Addy Osmani Agent Skills](https://github.com/addyosmani/agent-skills) | 軟體工程領域的 skills 範例。 |

## Skills

| 名稱 | 用途 |
|---|---|
| [Anthropic Skills](https://github.com/anthropics/skills) | Anthropic 公開的 skill 範例，內含許多 skills 可參考。 |
| [`/grill-me`](https://github.com/mattpocock/skills/tree/main/skills/productivity/grill-me) | 針對你的計畫或設計不斷追問，逐一釐清決策，直到雙方理解一致再動手。 |
| [`/handoff`](https://github.com/mattpocock/skills/tree/main/skills/productivity/handoff) | 把目前的對話壓縮成交接文件，讓另一個 agent 接著做。 |
| [`/superpowers:brainstorming`](https://github.com/obra/superpowers/tree/main/skills/brainstorming) | 動手前先把需求問清楚、提出做法再定設計。 |
| [Ponytail](https://github.com/DietrichGebert/ponytail) | 引導程式開發 agent 先理解需求、查找既有能力，再選擇簡單的解法，避免過度設計。 |
| [Caveman](https://github.com/JuliusBrussee/caveman) | 以精簡表達減少部分輸出。 |
| [RTK](https://github.com/rtk-ai/rtk) | 精簡部分開發工具輸出的 CLI 工具。 |
| [I Have ADHD](https://github.com/ayghri/i-have-adhd) | 讓回答聚焦下一步、分步驟，並標出目前進度。 |
| [NVIDIA SkillSpector](https://github.com/NVIDIA/skillspector) | 安裝 skill 前先掃描，偵測漏洞、惡意模式與安全風險的開源工具。 |
| [NVIDIA SkillEvaluator](https://github.com/NVIDIA/SkillEvaluator) | 評估 skill 是否真的提升 agent 表現：靜態檢查，加上有／無該 skill 的實際任務對照執行。 |

## Graph tools

| 名稱 | 用途 |
|---|---|
| [Understand Anything](https://github.com/Egonex-AI/Understand-Anything) | 將程式內容整理成交互式知識圖，協助探索結構與關聯。 |
| [Graphify](https://github.com/Graphify-Labs/graphify) | 將程式與文件整理為可查詢的圖譜。 |
| [CodeGraph](https://github.com/colbymchenry/codegraph) | 分析程式符號與呼叫等關聯。 |
| [GitNexus](https://github.com/abhigyanpatwari/GitNexus) | 從函式連結整理出較大的應用流程，可用來查變更影響。 |
| [Codebase Memory MCP](https://github.com/DeusData/codebase-memory-mcp) | 在本機保存可搜尋的程式關係圖，透過 MCP 提供給 agent 查詢。 |
| [Code Review Graph](https://github.com/tirth8205/code-review-graph) | 函式關係圖，另附變更 review 與測試建議。 |

## AGENTS.md 範例：借鏡與入口地圖

| 參考 | 借鏡的做法 |
|---|---|
| Boris Cherny | 從團隊實際遇到的錯誤，持續更新專案指示。[分享轉載](https://site.twstalker.com/dvdsgl/status/2007211258219770308) |
| Karpathy 風格 | 先釐清假設、保持簡單、聚焦修改，並以可觀察結果驗證。[社群整理](https://github.com/multica-ai/andrej-karpathy-skills) |
| Matt Pocock | 把入口文件當地圖，指向任務所需的詳細文件。[AGENTS.md 範例](https://github.com/mattpocock/skills/blob/main/AGENTS.md) |


## Mods（Claude Code 擴充）

| 名稱 | 用途 |
|---|---|
| [個資防護盾 pii-shield](https://github.com/Jiang-Yude/pii-shield) | AI 讀資料之前，先在本機把名單上的人名與身分證號、手機、Email 換成代號；不連網。 |
| [Blast Radius](https://github.com/anthropics/claude-code-playground/tree/main/claude-code/mods/blast-radius) | 危險指令（`rm -rf`、`git reset --hard`、force push 等）執行前先暫停，列出影響範圍，由你決定繼續或取消。 |
| [Flightdeck](https://github.com/scasella/claude-flightdeck) | 即時儀表板：看模型、context 用量、費用、權限檢查與 subagent 進度。只觀察，不改任何呼叫。 |
