# CLAUDE.md

此檔案為 Claude Code (claude.ai/code) 在此程式碼倉庫中工作時提供指導。

## 專案概述

這是一個 GitHub Pages 倉庫 (`eddietcg.github.io`)，用於託管靜態 HTML 檔案。這是一個簡單的靜態網站，具有基本的 HTML 頁面和 iframe 嵌入功能。

## 開發指令

### 套件管理

```bash
# 安裝相依性
pnpm install

# 執行 Husky hooks 設定
pnpm run prepare
```

### 程式碼品質

```bash
# 格式化程式碼（pre-commit 時自動執行）
pnpm exec prettier --write "*.{js,jsx,ts,tsx,vue,css,scss,md,html,json}"

# 執行 lint-staged（pre-commit hook 使用）
pnpm exec lint-staged
```

## 架構與結構

### 核心檔案

- `index.html` - 主要登陸頁面（簡單測試頁面）
- `download2.html` - 嵌入 iframe 的頁面，載入 `https://eddieyang.github.io/download.html`
- `package.json` - 專案配置，包含 Prettier 和 Husky 設定

### 開發流程

- **Pre-commit hooks**：Husky 在提交前自動執行 `lint-staged`
- **程式碼格式化**：Prettier 格式化 HTML、CSS、JS、MD 和 JSON 檔案
- **套件管理器**：使用 `pnpm`（由 `pnpm-lock.yaml` 可知）

### 程式碼品質設定

專案使用完整的程式碼品質管線：

- **Husky** 用於 Git hooks 管理
- **lint-staged** 在暫存檔案上執行工具
- **Prettier** 自動格式化所有常見檔案類型

## 開發注意事項

- 這是用於 GitHub Pages 託管的靜態網站倉庫
- 所有格式化都透過 pre-commit hooks 自動處理
- 網站結構簡單，包含基本 HTML 頁面和 iframe 功能
