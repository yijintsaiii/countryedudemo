# GitHub 部署指南

## 📦 部署步驟

### 1. 初始化 Git 倉庫（如果還沒有）

```bash
cd /Users/cai_yijin/Desktop/countryedudemo
git init
git add .
git commit -m "Initial commit: 鄉育教育系統 MVP 版本"
```

### 2. 在 GitHub 創建新倉庫

1. 登入 GitHub
2. 點擊右上角 "+" → "New repository"
3. 填寫倉庫名稱（建議：`countryedudemo` 或 `xiangyu-education-system`）
4. 選擇 Public（公開）或 Private（私有）
5. **不要**勾選 "Initialize this repository with a README"（因為我們已經有 README.md）
6. 點擊 "Create repository"

### 3. 連接本地倉庫到 GitHub

```bash
# 添加遠程倉庫（將 YOUR_USERNAME 和 REPO_NAME 替換為實際值）
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git

# 推送到 GitHub
git branch -M main
git push -u origin main
```

### 4. 啟用 GitHub Pages

1. 進入 GitHub 倉庫頁面
2. 點擊 "Settings"（設置）
3. 在左側選單找到 "Pages"
4. 在 "Source" 下選擇：
   - Branch: `main`
   - Folder: `/ (root)`
5. 點擊 "Save"
6. 等待幾分鐘，GitHub 會生成你的網站連結：
   `https://YOUR_USERNAME.github.io/REPO_NAME/`

## ✅ 部署前檢查清單

- [x] 所有文件已提交到 Git
- [x] README.md 已創建並包含專案說明
- [x] .gitignore 已創建
- [x] 無敏感信息（API keys、密碼等）
- [x] CDN 資源連結正確
- [x] 所有功能在本地測試正常

## 🔍 測試部署

部署完成後，請測試以下功能：

1. **首頁載入**：確認所有 CDN 資源正確載入
2. **模組切換**：測試三個主要模組的切換
3. **角色切換**：測試導師/學生視角切換
4. **互動功能**：測試按鈕點擊、表單提交等
5. **響應式設計**：在不同設備尺寸下測試

## 🐛 常見問題

### 問題 1：GitHub Pages 顯示 404

**解決方案**：
- 確認倉庫設置中的 Pages 源已正確設置為 `main` 分支和 `/ (root)`
- 確認 `index.html` 在倉庫根目錄
- 等待 5-10 分鐘讓 GitHub 完成部署

### 問題 2：CDN 資源無法載入

**解決方案**：
- 檢查瀏覽器控制台是否有 CORS 錯誤
- 確認 CDN 連結在 HTML 中正確
- 某些地區可能需要使用代理或 VPN

### 問題 3：Emoji 顯示異常

**解決方案**：
- 確認 HTML 的 `<meta charset="UTF-8" />` 已設置
- 某些舊版瀏覽器可能不支持部分 emoji

## 📝 後續優化建議

1. **性能優化**：
   - 考慮使用 GitHub Actions 自動部署
   - 添加 Service Worker 實現離線功能

2. **SEO 優化**：
   - 添加 `<meta>` 標籤描述
   - 添加 Open Graph 標籤用於社交媒體分享

3. **分析工具**：
   - 可選：添加 Google Analytics 或其他分析工具

4. **自定義域名**：
   - 如需使用自定義域名，可在 GitHub Pages 設置中配置

## 🔗 有用的連結

- [GitHub Pages 文檔](https://docs.github.com/en/pages)
- [Git 基礎命令](https://git-scm.com/docs)
- [Vue 3 文檔](https://vuejs.org/)
- [Tailwind CSS 文檔](https://tailwindcss.com/docs)

---

**祝部署順利！** 🚀
