# 🚀 GitHub Repository Landing Page Generator

一個極簡、響應式的 GitHub 專案展示頁面生成器，只需修改幾行 JavaScript 配置，即可為任何 GitHub 專案建立專業的展示頁面。

**A minimal, responsive GitHub repository showcase page generator. Simply modify a few lines of JavaScript configuration to create a professional showcase page for any GitHub project.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

## ✨ 主要特色 (Key Features)

- 🎯 **專為 GitHub 專案設計** - 自動拉取專案資訊、星數、分支、Release 等
- 📱 **響應式設計** - 完美適配桌面、平板、手機各種設備
- ⚡ **極簡設置** - 僅需修改 2 行 JavaScript 配置即可使用
- 🌐 **雙語支持** - 內建中英文介面，適合國際化專案
- 🎨 **現代化 UI** - 深色主題、圓角設計、優雅的視覺效果
- 📊 **即時數據** - 自動顯示 GitHub 徽章和最新 Release 資訊
- 🚫 **零依賴** - 純 HTML/CSS/JavaScript，無需任何框架或建置工具

**English:**
- 🎯 **Designed for GitHub Projects** - Automatically fetches project info, stars, forks, releases
- 📱 **Responsive Design** - Perfect adaptation to desktop, tablet, and mobile devices
- ⚡ **Minimal Setup** - Only need to modify 2 lines of JavaScript configuration
- 🌐 **Bilingual Support** - Built-in Chinese/English interface for international projects
- 🎨 **Modern UI** - Dark theme, rounded design, elegant visual effects
- 📊 **Real-time Data** - Automatically displays GitHub badges and latest release info
- 🚫 **Zero Dependencies** - Pure HTML/CSS/JavaScript, no frameworks or build tools required

## 🚀 快速開始 (Quick Start)

### 方法一：直接使用 (Method 1: Direct Use)

1. **下載專案檔案**
   ```bash
   git clone https://github.com/QAQ-test/landpage.git
   cd landpage
   ```

2. **修改配置** (目前設定為 J-I-P/youtube_test)
   
   編輯 `landingpage.html` 第 105-106 行：
   ```javascript
   const REPO_OWNER = "你的GitHub用戶名";   // 例如 "facebook"
   const REPO_NAME  = "你的專案名稱";        // 例如 "react"
   ```

3. **本地預覽**
   
   直接用瀏覽器開啟 `landingpage.html` 文件即可預覽效果

4. **部署上線**
   
   將 `landingpage.html` 上傳到任何靜態網站託管服務即可

### 方法二：GitHub Pages (Method 2: GitHub Pages)

1. **Fork 或使用模板**
   
   Fork 這個專案或點擊 "Use this template" 按鈕

2. **修改配置**
   
   編輯 `landingpage.html` 中的 REPO_OWNER 和 REPO_NAME

3. **啟用 GitHub Pages**
   
   在專案設定中啟用 GitHub Pages，選擇 main 分支

4. **存取網站**
   
   網站將可在 `https://你的用戶名.github.io/landpage` 存取

## 📋 目前專案配置 (Current Configuration)

此範例專案目前配置為展示：
- **Repository**: `J-I-P/youtube_test`
- **功能展示**: 自動拉取該專案的 stars、forks、issues、license 等資訊
- **Release 資訊**: 顯示最新版本發佈資訊
- **Clone 指令**: 自動生成正確的 git clone 指令

## 📁 專案結構 (Project Structure)

```
landpage/
├── landingpage.html          # 主要的 Landing Page 檔案
├── README.md                 # 專案說明文件
└── .git/                     # Git 版本控制目錄
```

### 檔案說明 (File Description)

- **`landingpage.html`** - 包含完整的 HTML、CSS、JavaScript 的單一檔案
  - 響應式 CSS 樣式 (第 8-36 行)
  - 頁面結構和內容 (第 38-95 行)  
  - 自動化 JavaScript 邏輯 (第 97-150 行)

## 🛠️ 自定義指南 (Customization Guide)

### 基本配置 (Basic Configuration)

只需修改這兩個變數即可適用於任何 GitHub 專案：

```javascript
// 在 landingpage.html 的第 105-106 行
const REPO_OWNER = "你的用戶名";     // GitHub 用戶名或組織名
const REPO_NAME  = "你的專案名";     // GitHub 專案名稱
```

### 進階自定義 (Advanced Customization)

1. **修改頁面標題**
   ```html
   <title>你的專案名稱</title>  <!-- 第 6 行 -->
   ```

2. **調整主要色彩**
   ```css
   :root { 
     --bg:#0b1020;        /* 背景色 */
     --fg:#eaeef7;        /* 文字色 */
     --muted:#9aa3b2;     /* 次要文字色 */
     --card:#121832;      /* 卡片背景色 */
     --line:#27324e;      /* 邊框色 */
   }
   ```

3. **修改導航選單**
   ```html
   <nav>
     <a href="#quickstart">快速開始</a>
     <a href="#release">版本</a>
     <a href="#about">關於</a>
   </nav>
   ```

4. **調整快速開始說明**
   
   修改第 70-85 行的安裝步驟內容

## 📊 功能特色詳細說明 (Feature Details)

### 自動化資料拉取

- **GitHub API 整合**: 自動從 GitHub API 獲取專案資訊
- **即時徽章**: 使用 Shields.io 顯示 stars、forks、issues、license 徽章
- **Release 資訊**: 自動顯示最新版本的發佈日期和更新內容
- **錯誤處理**: 當 API 達到限額時會顯示友善的錯誤訊息

### 響應式設計細節

- **斷點設計**: 在 860px 以下自動切換為單欄布局
- **彈性網格**: 使用 CSS Grid 和 Flexbox 確保各種螢幕尺寸的最佳體驗
- **字體縮放**: 使用 `clamp()` 函數實現響應式字體大小

## 🎨 技術棧 (Tech Stack)

- **純前端技術**: HTML5 + CSS3 + Vanilla JavaScript
- **CSS 特性**: CSS Grid, Flexbox, CSS Variables, Responsive Design
- **JavaScript**: 現代 ES6+ 語法, Fetch API, Async/Await
- **外部服務**: GitHub API, Shields.io 徽章服務
- **部署**: 任何靜態網站託管服務 (GitHub Pages, Netlify, Vercel 等)

## 🌐 部署選項 (Deployment Options)

### GitHub Pages (推薦)

```bash
# 1. 推送代碼到 GitHub
git add .
git commit -m "Configure for my repository"
git push origin main

# 2. 在 GitHub 專案設定中啟用 Pages
# Settings → Pages → Source: Deploy from a branch → main
```

### Netlify

1. 將 `landingpage.html` 拖放到 [Netlify](https://app.netlify.com/drop)
2. 或連接 GitHub 專案進行自動部署

### Vercel

```bash
# 安裝 Vercel CLI
npm i -g vercel

# 部署
vercel --public
```

### 其他靜態託管

- **Surge.sh**: `surge landingpage.html`
- **Firebase Hosting**: 使用 Firebase CLI 部署
- **AWS S3**: 上傳到 S3 bucket 並啟用靜態網站託管

## 💡 使用場景 (Use Cases)

1. **開源專案展示** - 為你的 GitHub 開源專案建立專業的介紹頁面
2. **專案文檔首頁** - 作為專案文檔網站的首頁或入口頁面
3. **Portfolio 展示** - 在個人作品集中展示特定專案
4. **會議演示** - 在技術會議或展示中使用的專案介紹頁面
5. **README 補充** - 提供比 GitHub README 更豐富的視覺化展示

## 🔧 故障排除 (Troubleshooting)

### 常見問題

**Q: 為什麼徽章或 Release 資訊沒有顯示？**
- A: 可能是 GitHub API 達到限額，或專案設定為私有。公開專案通常沒有問題。

**Q: 如何處理私有專案？**
- A: 此工具主要為公開專案設計。私有專案需要 GitHub Token，但不建議在前端代碼中暴露。

**Q: 可以修改徽章的樣式嗎？**
- A: 可以修改 Shields.io URL 中的 `style` 參數，例如 `?style=for-the-badge`

**Q: 如何添加更多的自定義資訊？**
- A: 可以直接修改 HTML 內容，或在 JavaScript 中添加更多的 API 調用

## 📸 預覽截圖 (Preview)

目前專案配置為展示 `J-I-P/youtube_test` 專案：

```
🚀 J-I-P/youtube_test
   [Stars] [Forks] [Issues] [License] 徽章

   快速開始                    [🚀 產品預覽區域]
   ├─ git clone ...           [   使用圖示或   ]
   ├─ npm install             [   截圖展示     ]
   └─ npm run dev             [   產品效果     ]

   最新版本
   └─ 顯示最新 Release 資訊

   關於這個 Repo
   └─ 專案說明和特色介紹
```

## 🤝 貢獻指南 (Contributing)

歡迎貢獻改進這個 Landing Page 生成器！

### 如何貢獻

1. **Fork 專案** - 點擊右上角的 Fork 按鈕
2. **建立分支** - `git checkout -b feature/新功能名稱`
3. **提交更改** - `git commit -m '新增某某功能'`
4. **推送分支** - `git push origin feature/新功能名稱`
5. **建立 Pull Request** - 在 GitHub 上建立 PR

### 貢獻方向

- 🎨 **UI/UX 改進** - 更好的視覺設計或使用者體驗
- 🚀 **新功能** - 添加更多 GitHub API 整合功能
- 🌐 **多語言支持** - 添加更多語言版本
- 📱 **響應式改進** - 更好的行動裝置體驗
- 🔧 **程式碼最佳化** - 性能改進或程式碼品質提升

### 開發規範

- 保持 HTML 文件的單一檔案特性（易於使用）
- 確保向後相容性
- 添加適當的註釋
- 測試不同的 GitHub 專案配置

## 📄 授權條款 (License)

本專案採用 MIT 授權條款 - 詳見 [LICENSE](LICENSE) 檔案

## 📞 聯絡資訊 (Contact)

- **專案維護者**: Yi-Ping Jiang (J-I-P)
- **GitHub**: [@J-I-P](https://github.com/J-I-P)
- **專案連結**: [QAQ-test/landpage](https://github.com/QAQ-test/landpage)
- **範例展示**: 目前配置為 [J-I-P/youtube_test](https://github.com/J-I-P/youtube_test)

## 🙏 致謝 (Acknowledgments)

- GitHub API 提供豐富的專案資料
- Shields.io 提供美觀的徽章服務
- 所有為這個專案貢獻想法和代碼的開發者

## 🔄 更新日誌 (Changelog)

### v1.0.0 (2025-09-19)
- 🎉 初始版本發佈
- ✨ 基本的 GitHub 專案展示功能
- 📱 響應式設計實現
- 🌐 中英文雙語支持
- 📊 自動 GitHub API 整合
- 🎨 現代化深色主題設計

---

**⭐ 如果這個專案對你有幫助，請給它一個 star！**

**⭐ If this project helps you, please give it a star!**