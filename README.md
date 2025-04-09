# AI_co_lab

這是一個自動將文章發布到 Facebook 粉絲專頁的專案。

## 功能特色

- 自動監控 `articles` 資料夾的變更
- 自動發布最新的文章到 Facebook 粉絲專頁
- 支援手動觸發發文功能

## 設定步驟

### 1. Facebook 設定
1. 前往 [Facebook 開發者平台](https://developers.facebook.com/) 註冊
2. 建立新的應用程式（選擇 "Business" 類型）
3. 設定應用程式：
   - 新增 "Facebook Login" 產品
   - 設定 OAuth
4. 取得 Page Access Token：
   - 使用 [Graph API Explorer](https://developers.facebook.com/tools/explorer/)
   - 選擇應用程式和粉絲專頁
   - 請求權限：`pages_manage_posts`, `pages_read_engagement`

### 2. GitHub 設定
1. 在專案的 Settings > Secrets and variables > Actions 中新增：
   - `FB_PAGE_ID`：Facebook 粉絲專頁 ID
   - `FB_ACCESS_TOKEN`：Facebook Page Access Token

### 3. 使用方式
1. 在 `articles` 資料夾中新增 `.md` 格式的文章
2. 提交變更到 GitHub：
   ```bash
   git add articles/your-article.md
   git commit -m "新增文章"
   git push origin main
   ```
3. GitHub Actions 會自動執行發文流程

### 4. 手動觸發
1. 前往專案的 Actions 頁面
2. 選擇 "Post to Facebook Page" 工作流程
3. 點選 "Run workflow"

## 注意事項
- 確保文章內容符合 Facebook 社群規範
- 定期更新 Access Token
- 發文前檢查文章格式是否正確
