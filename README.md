# satellite-scheduling-research

衛星排程相關技術的深度研究彙整。以 [NotebookLM](https://notebooklm.google.com) 的 **Deep Research** 功能對 6 個關鍵主題做深度研究,產出繁體中文報告並轉為 PDF,另附一份跨主題的「衛星排程技術總覽」合併報告。

> 本 repo 由 Claude Code 協助產製(專案代號 ClaudeEP04)。

---

## 📑 研究報告(`research-reports/`)

每份報告都同時提供 `.md`(原始)與 `.pdf`(成品,繁體中文)。

| # | 主題 | 說明 | 深度研究來源數 | 檔案 |
|---|------|------|:---:|------|
| 00 | **衛星排程技術總覽** | 以端到端排程鏈彙整下列 6 份研究並加上交叉洞察 | — | [md](research-reports/00_satellite-scheduling-overview.md) · [pdf](research-reports/00_satellite-scheduling-overview.pdf) |
| 01 | **AstroBus NEO** | Airbus 敏捷衛星平台產品線與 CO3D 任務 | 60 | [md](research-reports/01_AstroBus-NEO.md) · [pdf](research-reports/01_AstroBus-NEO.pdf) |
| 02 | **Google OR-Tools CP-SAT** | 約束規劃求解器,地面批次排程最佳化 | 92 | [md](research-reports/02_OR-Tools-CP-SAT.md) · [pdf](research-reports/02_OR-Tools-CP-SAT.pdf) |
| 03 | **GSaaS** | Ground Station as a Service,地面段與下傳排程 | 91 | [md](research-reports/03_GSaaS.md) · [pdf](research-reports/03_GSaaS.pdf) |
| 04 | **ECSS 自主等級 E1–E4** | ECSS-E-ST-70-11C 太空航段自主等級 | 79 | [md](research-reports/04_ECSS-autonomy-E1-E4.md) · [pdf](research-reports/04_ECSS-autonomy-E1-E4.pdf) |
| 05 | **CASPER / ASPEN** | NASA JPL 星上連續規劃與迭代修復排程系統 | 60 | [md](research-reports/05_CASPER-ASPEN.md) · [pdf](research-reports/05_CASPER-ASPEN.pdf) |
| 06 | **Pléiades Neo** | Airbus 超高解析度地球觀測星座與分鐘級任務指派 | 80 | [md](research-reports/06_Pleiades-Neo.md) · [pdf](research-reports/06_Pleiades-Neo.pdf) |

### 六個主題如何構成一條排程鏈

| 排程鏈層級 | 對應主題 |
|---|---|
| 被排程的資產 | AstroBus NEO(01)、Pléiades Neo(06) |
| 最佳化引擎(地面批次) | OR-Tools CP-SAT(02) |
| 最佳化引擎(星上連續) | CASPER / ASPEN(05) |
| 自主權責框架 | ECSS 自主等級 E1–E4(04) |
| 地面段執行與下傳 | GSaaS(03) |

完整的交叉分析與操作啟示見 [00 總覽報告](research-reports/00_satellite-scheduling-overview.pdf)。

### 產製方法

1. NotebookLM Deep Research(**deep 模式**,網路來源)對每個關鍵字做深度研究。
2. 匯入排名最前的來源後,由 NotebookLM Studio 產生 **Briefing Doc**(繁體中文)。
3. 下載為 Markdown,以 Chrome headless 套繁中字型排版轉為 PDF。
4. 00 總覽報告為 6 份研究的人工綜合彙整(排程鏈框架與交叉洞察為分析觀點)。

> ⚠️ 各單一主題內容僅根據其深度研究之來源文本;報告標題為 NotebookLM 自動命名,部分主題聚焦在子題(如 02 偏 JSSP 基準測試、04 併入模型驅動開發)。

---

## 🧪 其他檔案

| 檔案 | 說明 |
|---|---|
| [gemini-test.html](gemini-test.html) | Gemini 免費 API 測試頁;金鑰只在瀏覽器輸入,不寫入原始碼 |
| [us-market-20260717.html](us-market-20260717.html) | 2026/07/17 美股收盤資訊圖表(獨立版) |
| [us-market-artifact.html](us-market-artifact.html) | 上者的 Artifact 發布版 |

---

## 授權與免責

- 研究報告內容取自各主題之公開網路來源,僅供技術研究參考。
- 美股資訊圖表為市場資訊整理,非投資建議。
