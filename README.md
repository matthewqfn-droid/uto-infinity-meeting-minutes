# 優淼私董會會議紀錄技能

將會議錄音的文字轉錄、語音 App 摘要或筆記，整理成繁體中文總監會議紀錄，並沿用優淼私董會的固定議程與青綠色版面格式。

## 有甚麼用途

- 整理會議日期、時間、地點，以及與會者、列席者、缺席者與缺席原因。
- 按外務部、內務部、常務部的部門順序編排匯報，另列其他動議。
- 區分匯報、討論、建議與決議，整理「負責人／跟進內容／時間」表格。
- 將轉錄的矛盾日期、疑似錯誤人名等列為待核實，不自行猜測。
- 保留來源中的「金句精選」，轉為繁體中文並以獨立色塊卡片展示。
- 預設產出 PDF，包含會議資料表、章節色塊、活動分工表及頁碼；也可按要求改用 Word 等格式。

這個技能提供整理規則及版面規格，本身不會將錄音轉成文字。請先提供轉錄文檔或筆記；產出 PDF 或 Word 時，執行環境亦需具備相應的文件製作與渲染工具。

## 安裝

將這個儲存庫下載到個人 Codex 技能資料夾，並把資料夾命名為 `youmiao-meeting-minutes`。例如在 macOS 或 Linux 執行：

```bash
git clone https://github.com/matthewqfn-droid/uto-infinity-meeting-minutes.git ~/.codex/skills/youmiao-meeting-minutes
```

如果已自訂 `CODEX_HOME`，請放在該目錄的 `skills/youmiao-meeting-minutes/`。若目的資料夾已存在，先檢查現有技能，不要直接覆蓋。安裝後在新對話確認技能已出現在可用清單。

儲存庫名稱是 `uto-infinity-meeting-minutes`，技能的叫用名稱是 **`youmiao-meeting-minutes`**。

## 怎樣使用

在 Codex 附上轉錄文檔，並提供當次會議基本資料，輸入：

```text
請使用 $youmiao-meeting-minutes，將附件整理成優淼私董會總監會議紀錄。

日期：YYYY年MM月DD日
時間：開始時間至結束時間
地點：會議地點
與會者：名單
列席者：名單及身份備註
缺席者：名單及缺席原因

請以繁體中文生成 PDF，沿用色塊及表格格式，並加入原文的金句精選。
```

列席者指非強制性須參加總監會議的成員，並非一律指外部嘉賓。你提供的當次會議資料會優先於轉錄 App 的日期或名單。

需要修改現有紀錄時，可附上文件並輸入：

```text
請使用 $youmiao-meeting-minutes 修改這份會議紀錄，將以下資料更新，
保留原有繁體中文、色塊、表格及金句格式：
（列出需要修改的資料）
```

## 檔案內容

| 檔案 | 用途 |
| --- | --- |
| [SKILL.md](SKILL.md) | 資料整理規則、固定議程、出席分類及輸出要求 |
| [references/layout.md](references/layout.md) | 配色、字級、表格、頁面及金句卡片規格 |
| [agents/openai.yaml](agents/openai.yaml) | 技能顯示名稱及預設叫用提示 |

本儲存庫不包含實際會議紀錄或 PDF 範例。
