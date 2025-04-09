# Facebook 發文設定指南

## 取得 Access Token

1. 前往 [Facebook 開發者平台](https://developers.facebook.com/)
2. 建立新的應用程式
   - 選擇 "Business" 類型
   - 填寫應用程式基本資訊

3. 設定應用程式
   - 新增 "Facebook Login" 產品
   - 在設定中啟用 OAuth 功能

4. 取得 Page Access Token
   - 前往 [Graph API Explorer](https://developers.facebook.com/tools/explorer/)
   - 選擇你的應用程式
   - 選擇要發文的粉絲專頁
   - 勾選必要權限：
     - pages_manage_posts
     - pages_read_engagement
   - 點擊「產生存取權杖」

5. 設定 GitHub Secrets
   - 前往專案的 Settings > Secrets and variables > Actions
   - 建立新的 secret：FB_ACCESS_TOKEN
   - 將取得的 Access Token 填入值中

## 注意事項
- Access Token 請務必保密，不要提交到程式碼中
- 建議定期更新 Access Token
- 如果遇到權限問題，請確認粉絲專頁的管理員權限是否正確
