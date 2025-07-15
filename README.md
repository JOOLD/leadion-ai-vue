# 🚀 LeadIO Vue3 - SEO 分析平台

## 📋 項目概述

LeadIO 是一個使用 **Vue3 + Clerk + n8n** 建構的現代化 SEO 分析平台，提供企業級的認證系統和強大的分析功能。

### ✨ 主要特色

- 🎯 **Vue3 + TypeScript** - 現代化前端框架
- 🔐 **Clerk 認證** - 企業級認證服務，支援多種登入方式
- 🎨 **Element Plus** - 美觀且功能豐富的 UI 組件庫
- 🔧 **n8n 整合** - 無程式碼後端處理流程
- 📱 **響應式設計** - 完美適配桌面和行動裝置
- 🌙 **深色模式** - 支援深色/淺色主題切換
- ⚡ **效能優化** - Vite 構建工具，極速開發體驗

---

## 🛠️ 技術棧

| 分類 | 技術 | 版本 |
|------|------|------|
| **前端框架** | Vue 3 | ^3.4.21 |
| **開發語言** | TypeScript | ^5.4.5 |
| **認證服務** | Clerk | ^0.3.8 |
| **UI 框架** | Element Plus | ^2.6.3 |
| **狀態管理** | Pinia | ^2.1.7 |
| **路由管理** | Vue Router | ^4.3.0 |
| **HTTP 客戶端** | Axios | ^1.6.8 |
| **構建工具** | Vite | ^5.2.10 |
| **後端處理** | n8n | - |

---

## 🚀 快速開始

### 環境要求

- Node.js >= 18.0.0
- npm >= 8.0.0

### 1. 安裝依賴

\`\`\`bash
# 複製項目
git clone <your-repo-url>
cd leadio-vue3

# 安裝依賴
npm install
\`\`\`

### 2. 設定環境變數

\`\`\`bash
# 複製環境變數範例檔案
cp .env.example .env

# 編輯 .env 檔案，填入以下配置：
\`\`\`

\`\`\`env
# Clerk 認證配置
VITE_CLERK_PUBLISHABLE_KEY=pk_test_your_clerk_key_here

# n8n 後端配置
VITE_N8N_BASE_URL=https://your-n8n-instance.zeabur.app
VITE_N8N_WEBHOOK_URL=https://your-n8n-instance.zeabur.app/webhook

# 應用配置
VITE_APP_NAME=LeadIO
VITE_APP_VERSION=1.0.0
\`\`\`

### 3. 啟動開發伺服器

\`\`\`bash
npm run dev
\`\`\`

應用程式將在 [http://localhost:3000](http://localhost:3000) 運行。

---

## 📁 項目結構

\`\`\`
leadio-vue3/
├── src/
│   ├── components/          # 可重用組件
│   │   ├── AppNavbar.vue    # 導航欄
│   │   ├── AppNotifications.vue # 通知系統
│   │   └── StatCard.vue     # 統計卡片
│   ├── views/               # 頁面組件
│   │   ├── HomeView.vue     # 首頁
│   │   ├── SignInView.vue   # 登入頁
│   │   ├── SignUpView.vue   # 註冊頁
│   │   ├── DashboardView.vue # 儀表板
│   │   ├── AnalysisView.vue # 分析工具
│   │   ├── ReportsView.vue  # 報告中心
│   │   ├── HistoryView.vue  # 歷史記錄
│   │   └── NotFoundView.vue # 404 頁面
│   ├── stores/              # Pinia 狀態管理
│   │   └── notification.ts  # 通知狀態
│   ├── services/            # 服務層
│   │   └── api.ts          # API 服務
│   ├── router/              # 路由配置
│   │   └── index.ts        # 路由定義
│   ├── config/              # 配置檔案
│   │   └── index.ts        # 應用配置
│   ├── App.vue             # 根組件
│   └── main.ts             # 應用入口
├── public/                  # 靜態資源
├── package.json            # 依賴和腳本
├── vite.config.ts          # Vite 配置
├── tsconfig.json           # TypeScript 配置
└── README.md               # 項目說明
\`\`\`

---

## 🔧 Clerk 認證設定

### 1. 註冊 Clerk 帳號

1. 前往 [clerk.com](https://clerk.com)
2. 建立免費帳號
3. 建立新應用程式

### 2. 設定認證選項

在 Clerk Dashboard 中：

**認證方式：**
- ✅ Email/Password
- ✅ Google OAuth
- ✅ GitHub OAuth

**重定向 URL：**
- Sign-in URL: \`http://localhost:3000/sign-in\`
- After sign-in: \`http://localhost:3000/dashboard\`

### 3. 取得 API 金鑰

在 **API Keys** 頁面複製 **Publishable Key**，並填入 \`.env\` 檔案。

---

## 🌐 n8n 後端整合

### 必要的 n8n Workflows

1. **表單處理** (\`/analysis/submit\`)
2. **狀態查詢** (\`/analysis/status/:id\`)
3. **報告獲取** (\`/analysis/report/:id\`)
4. **歷史記錄** (\`/analysis/history\`)
5. **健康檢查** (\`/health\`)

### 設定步驟

1. 確認你的 n8n 實例正常運行
2. 建立對應的 workflows
3. 在 \`.env\` 中設定正確的 n8n 網址

---

## 📦 可用腳本

\`\`\`bash
# 開發模式
npm run dev

# 生產構建
npm run build

# 預覽生產版本
npm run preview

# 類型檢查
npm run typecheck
\`\`\`

---

## 🚀 部署

### 部署到 Zeabur（推薦）

1. **準備部署**
   \`\`\`bash
   npm run build
   \`\`\`

2. **設定 Zeabur**
   - 前往 [zeabur.com](https://zeabur.com)
   - 建立新專案
   - 連接 Git 倉庫
   - 選擇 Vue.js 模板

3. **設定環境變數**
   在 Zeabur Dashboard 中設定生產環境變數

4. **更新 Clerk 設定**
   在 Clerk Dashboard 中更新生產域名和重定向 URL

### 部署到 Vercel

\`\`\`bash
# 安裝 Vercel CLI
npm i -g vercel

# 部署
vercel
\`\`\`

---

## 🎯 功能特色

### 🔐 完整認證系統
- Clerk 企業級認證
- 多種登入方式（Email、Google、GitHub）
- 自動路由保護
- 用戶狀態管理

### 🎨 現代化 UI
- Element Plus 組件庫
- 響應式設計
- 深色/淺色模式
- 優雅的動畫效果

### ⚡ 效能優化
- Vite 極速構建
- 路由懶加載
- 組件自動導入
- Tree-shaking 優化

### 🔧 開發體驗
- TypeScript 類型安全
- ESLint 程式碼規範
- 自動導入 API
- 完整的錯誤處理

---

## 🤝 貢獻指南

1. Fork 本倉庫
2. 建立功能分支 (\`git checkout -b feature/AmazingFeature\`)
3. 提交更改 (\`git commit -m 'Add some AmazingFeature'\`)
4. 推送到分支 (\`git push origin feature/AmazingFeature\`)
5. 開啟 Pull Request

---

## 📄 授權協議

本項目使用 MIT 授權協議。詳見 [LICENSE](LICENSE) 檔案。

---

## 📞 技術支援

如果您在使用過程中遇到問題：

1. 檢查 [完整設定指南](./🚀%20Vue3%20+%20Clerk%20完整設定指南.md)
2. 查看瀏覽器開發者工具的錯誤訊息
3. 確認所有環境變數設定正確
4. 檢查 n8n 服務狀態

---

## 🎉 致謝

感謝以下開源項目：

- [Vue.js](https://vuejs.org/) - 漸進式 JavaScript 框架
- [Clerk](https://clerk.com/) - 現代化認證平台
- [Element Plus](https://element-plus.org/) - Vue 3 UI 組件庫
- [Vite](https://vitejs.dev/) - 下一代前端工具
- [n8n](https://n8n.io/) - 工作流程自動化工具

**使用 Vue3 + Clerk，讓您的 SEO 分析平台更上一層樓！** 🚀 