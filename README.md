# 🚀 LeadIO Vue3 - SEO 分析平台

## 📋 項目概述

LeadIO 是一個使用 **Vue3 + Clerk + n8n** 建構的現代化 SEO 分析平台，提供企業級的認證系統和強大的分析功能。

### ✨ 主要特色

- 🎯 **Vue3 + TypeScript** - 現代化前端框架
- 🔐 **Clerk 認證** - 企業級認證服務，支援多種登入方式
- 🎨 **LiblibAI 風格設計** - 現代化工作流程管理介面
- 🔧 **n8n 整合** - 無程式碼後端處理流程
- 📱 **響應式設計** - 完美適配桌面和行動裝置
- 🌙 **深色模式** - 支援深色/淺色主題切換
- ⚡ **效能優化** - Vite 構建工具，極速開發體驗
- 📊 **實時工作流執行** - 完整的執行歷史追蹤

---

## 🛠️ 技術棧

| 分類 | 技術 | 版本 |
|------|------|------|
| **前端框架** | Vue 3 | ^3.4.21 |
| **開發語言** | TypeScript | ^5.4.5 |
| **認證服務** | Clerk | ^0.3.8 |
| **狀態管理** | Pinia | ^2.1.7 |
| **路由管理** | Vue Router | ^4.3.0 |
| **構建工具** | Vite | ^5.2.10 |
| **後端處理** | n8n | - |
| **部署平台** | Zeabur | - |

---

## 🚀 快速開始

### 環境要求

- Node.js >= 18.0.0
- npm >= 8.0.0

### 1. 安裝依賴

```bash
# 複製項目
git clone https://github.com/river-chang-adbest/n8n-seo.git
cd n8n-seo

# 安裝依賴
npm install
```

### 2. 設定環境變數

```bash
# 複製環境變數範例檔案
cp .env.example .env
```

```env
# Clerk 認證配置
VITE_CLERK_PUBLISHABLE_KEY=pk_test_your_clerk_key_here

# n8n 後端配置
VITE_N8N_BASE_URL=https://your-n8n-instance.zeabur.app
```

### 3. 啟動開發伺服器

```bash
npm run dev
```

應用程式將在 [http://localhost:3000](http://localhost:3000) 運行。

---

## 🎯 功能特色

### 🔐 完整認證系統
- Clerk 企業級認證
- 多種登入方式（Email、Google、GitHub）
- 自動路由保護
- 用戶狀態管理

### 🎨 現代化 Dashboard
- LiblibAI 風格的工作流程管理
- 左側執行歷史側邊欄
- 分類過濾功能
- 工作流卡片網格布局
- 實時狀態更新

### 🔧 n8n 整合
- SEO 關鍵字分析器
- 表單資料正確傳送
- 執行狀態追蹤
- 完成通知系統

### ⚡ 效能優化
- Vite 極速構建
- 路由懶加載
- 組件自動導入
- Tree-shaking 優化

---

## 📦 可用腳本

```bash
# 開發模式
npm run dev

# 生產構建
npm run build

# 預覽生產版本
npm run preview

# 類型檢查
npm run typecheck
```

---

## 🚀 部署到 Zeabur

1. **推送代碼到 GitHub**
2. **前往 [zeabur.com](https://zeabur.com)**
3. **建立新專案**
4. **連接 Git 倉庫**
5. **選擇 Vue.js 模板**
6. **設定環境變數**

---

## 📄 授權協議

本項目使用 MIT 授權協議。

---

**使用 Vue3 + n8n，打造智能 SEO 分析平台！** 🚀