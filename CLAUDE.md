# Yellowfir Group Limited — 黃杉集團 網站

## 專案概述

靜態 HTML 商業網站，雙語（中文 + 英文），展示黃杉集團的四大業務板塊。

## 技術棧

- 純 HTML + CSS（無框架、無 build 工具）
- 字體：Inter + PingFang SC + Microsoft YaHei
- 圖標：Font Awesome 6
- 圖片：GitHub (`xwindowscn/yellowfir`) 遠端載入 + 本地 PNG/JPG
- 配色：#0a1a1a (背景)、#00d084 (綠色強調)、#eef5f2 (文字)

## 網站架構

### 主要頁面
- `index.html` — 主頁（40K，當前維護版本）
- `REmodel.html` — 可再生能源財務模型（267K，獨立工具頁面）
- `REmodel.dev.html` — 模型開發版本

### 頁面區段（index.html）
1. Header（固定導航）
2. Hero（首屏橫幅）
3. About（公司簡介，雙語）
4. Business（四大業務：能源 / 投資 / 諮詢 / 移民）
5. Projects（項目展示）
6. CTA（行動呼籲）
7. Contact（聯繫方式）
8. Footer

### 四大業務板塊
- 綠色能源與基礎設施 (Green Energy)
- 跨境投資與戰略發展 (Cross-border Investment)
- 專業諮詢服務 (Professional Consulting)
- 移民與全球身分規劃 (Immigration & Global Identity)

## 開發規範

### 檔案管理
- 主維護檔案：`index.html`（其他 index 版本可清理）
- 模型檔案：`REmodel.html`（混淆後）、`REmodel.dev.html`（開發用）
- 圖片統一放在根目錄，命名為中文拼音

### HTML 規範
- `lang="zh-CN"`，雙語內容用 `.about-cn` / `.about-en` 結構
- 深色主題，綠色強調色 `#00d084`
- 行動端優先（`user-scalable=yes`、`-webkit-overflow-scrolling: touch`）

### CSS 規範
- 全內嵌在 `<style>` 標籤中（無外部 CSS 文件）
- CSS 變數用於主題色
- 使用 `rem` / `%` 響應式單位
- 動畫用 `@keyframes` + `will-change` 優化

### 圖片規範
- 本地圖片保持原始檔名（中文）
- 優先使用遠端 GitHub URL 載入（減少 repo 大小）
- 大圖（>500KB）建議壓縮或轉 WebP

## CLI 工具

- 本地預覽：`python3 -m http.server 8899`
- GitHub Pages 部署：推送到 `xwindowscn/yellowfir` 的 `main` 分支

## 常用斜線命令

- `/pitch-agent` — 投行 pitch
- `/market-researcher` — 行業研究
- `/earnings` — 財報分析
- `/comps` — 同業估值比較
