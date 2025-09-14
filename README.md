# Prompt 管理系統

這個專案用於管理和版本控制各種 AI Prompt 提示詞，方便團隊協作和維護。

## 資料夾結構

```
.
├── README.md                   # 專案說明和格式規範
├── PROMPT_TEMPLATE.md         # Prompt 模板檔案
├── n8n/                       # n8n 相關 Prompt
│   ├── Agent/                 # Agent 相關 Prompt
│   │   ├── example-agent.md   # 範例 Agent Prompt
│   │   └── ...
│   └── Workflow/              # 工作流程相關 Prompt
└── [其他工具資料夾]/
    └── ...
```

## Prompt 格式規範

每個 Prompt 檔案必須遵循以下格式：

### 檔案命名規則
- 使用小寫英文和連字符號：`example-agent.md`
- 檔案名稱要具有描述性
- 副檔名統一使用 `.md`

### 檔案內容格式

```yaml
---
author: [作者名稱]
version: [版本號，如 1.0.0]
language: [語言，如 中文/English]
description: [簡要描述 Prompt 的用途和特點]
tags: [標籤1, 標籤2, 標籤3]  # 可選
created_date: [創建日期，格式 YYYY-MM-DD]
updated_date: [最後更新日期，格式 YYYY-MM-DD]
---

# [Prompt 標題]

## 描述
詳細描述這個 Prompt 的用途、使用場景和預期效果。

## 使用方式
說明如何使用這個 Prompt，包括輸入參數、環境要求等。

## Prompt 內容

\```
[在這裡放置實際的 Prompt 內容]
\```

## 範例

### 輸入
\```
[範例輸入]
\```

### 預期輸出
\```
[範例輸出]
\```

## 更新記錄
- v1.0.0 (2024-01-01): 初始版本
- v1.1.0 (2024-01-15): 新增功能 X
```

## 版本管理規則

### 版本號格式
使用語義化版本號：`主版本號.次版本號.修訂號`

- **主版本號**：當進行不相容的 API 修改
- **次版本號**：當新增功能且向下相容
- **修訂號**：當修正錯誤且向下相容

### Git 提交規範
- `feat: 新增功能`
- `fix: 修正錯誤`
- `docs: 文檔更新`
- `style: 格式調整`
- `refactor: 重構`
- `test: 測試相關`

### 分支策略
- `main`: 主分支，穩定版本
- `develop`: 開發分支
- `feature/功能名稱`: 功能開發分支
- `hotfix/修正名稱`: 緊急修正分支

## 使用指南

1. **新增 Prompt**
   - 複製 `PROMPT_TEMPLATE.md` 作為模板
   - 填寫所有必要資訊
   - 放置到對應的資料夾中

2. **更新 Prompt**
   - 更新版本號
   - 修改 `updated_date`
   - 在更新記錄中加入變更說明

3. **標籤使用**
   - 使用有意義的標籤分類
   - 常見標籤：`assistant`, `chatbot`, `analysis`, `creative`, `technical`

## 貢獻指南

1. Fork 此專案
2. 建立功能分支
3. 提交您的變更
4. 發起 Pull Request

## 授權

此專案採用 MIT 授權條款。
