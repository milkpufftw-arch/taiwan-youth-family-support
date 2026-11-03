# 逆境少年家庭支持服務 Skill
版本 1.1.0｜已整合失蹤兒少案家服務指引

以臺灣繁體中文協助逆境少年及家庭支持服務紀錄、初步評估、家庭服務計畫、文字潤飾與督導建議。已讀取使用者提供的失蹤兒少案家服務指引文字擷取內容，整合評估、服務項目及內附空白表單結構；原 GPT 完整設定及其餘獨立附件尚未取得。

## 使用
將本儲存庫根目錄作為完整 Skill 資料夾，保留 SKILL.md、references、assets 的相對位置。交由支援 Agent Skills 的宿主載入；單純把儲存庫放在GitHub不代表已安裝到ChatGPT。
Codex本機可將整個資料夾置於其技能探索目錄（例如 ~/.agents/skills/taiwan-youth-family-support）；依實際宿主設定確認載入。根目錄不另包雙層資料夾。官方規範參考：https://learn.chatgpt.com/docs/build-skills 。

輸入前先去識別化；指定任務並提供實際筆記。缺漏填 OOO，正式系統欄位須核對版本。
- 「依以下去識別化筆記，產出六大段落訪視紀錄：……」
- 「只撰寫服務評估與下次會談目標：……」
- 「僅潤飾以下段落，不新增事實：……」

## 六大功能
服務摘要、內容摘要、目標達成性、服務評估、下次會談目標、社工督導建議。另支援初步評估、家庭服務計畫、潤飾及分段產生。

## 檔案
- [SKILL.md](SKILL.md)：觸發情境、路由與核心流程。
- [系統欄位](references/01-system-fields.md)：暫行欄位、版本界線及計入限制。
- [目標評估](references/02-goals-and-assessment.md)：需求連貫、證據及APGAR。
- [介入策略](references/03-intervention-strategies.md)：已做與擬議策略。
- [品質倫理](references/04-quality-and-ethics.md)：事實、隱私及安全通報。
- [來源登錄](references/05-source-register.md)：已讀、未取得及補件程序。
- [訪視範本](assets/visit-record-template.md)、[服務計畫](assets/service-plan-template.md)、[初步評估](assets/initial-assessment-template.md)：去識別化暫行空白範本。
- [驗收案例](tests/acceptance-cases.md)：模型功能測試案例及執行狀態。

## 驗證與限制
建立時已做靜態驗證：YAML、UTF-8、Markdown結構、相對路徑、必要檔案、核心限制及常見個資格式掃描。這些檢查不能證明沒有所有識別風險，也不能代替模型功能測試。
九項模型功能案例已建立，尚未在獨立模型或目標宿主執行，不宣稱通過。由承辦社工及督導檢核產出，不自動登錄、施測、通報或診斷。

## 維護與Plugin準備
已取得一份指引，且內含初評、服務紀錄、計畫、執行摘要及結轉案空白表單；其餘獨立文件待補或確認是否重複，現行版本仍需專業核對，詳來源登錄。不得公開任何原案、真實個案編號或填寫後表單。
已具備可封裝的Skill內容及相對資源，不需MCP；尚未建立Plugin manifest、安裝分享設定或完成宿主測試。本版不是已發布的Plugin。
