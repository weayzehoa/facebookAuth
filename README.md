1. 安裝 Laravel 6.x LTS 及 Authentication
    composer create-project --prefer-dist laravel/laravel facebookAuth "6.*"
    composer require laravel/ui "^1.0" --dev
    php artisan ui vue --auth
    npm install && npm run dev
2. 安裝 laravel/socialite
    composer require laravel/socialite
3. 修改 config/app.php
4. 修改 config/services.php，加入 facebook
5. 建立 SocialAuthFacebookController 控制器
6. 修改 route/web.php
7. 建立 Model 及 修改相關檔案
    php artisan make:model SocialFacebookAccount -m
8. 修改 App/SocialFacebookAccount.php
9. 修改 create_social_facebook_accounts_table.php
10. 修改完成後執行 php artisan migrate:refresh 將資料庫建立起來。
11. 新增 app/Services 目錄及 SocialFacebookAccountService.php
12. 修改 login 視圖，新增一個按鈕
13. 到 https://developers.facebook.com/ 建立應用程式取得 APP_ID及 APP_SECRET，並修改 .env 檔案，新增 Facebook 相關設定
14. 完成，測試。
