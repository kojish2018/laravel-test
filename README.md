# ASAS バックオフィス

## Clone後、最初にすること
```
# cp -p src/.env.example src/.env
# docker compose build
# docker compose up -d
# docker compose exec php bash
$ npm install && npm update
$ composer install
$ npm run dev
$ php artisan migrate
```

## ブラウザで動作確認
https://localhost:60444/

---

## 開発関連ヘルプ
### Laravel8.x
https://readouble.com/laravel/8.x/ja/

### アイコンを探す
https://blade-ui-kit.com/blade-icons?set=8#search

### CSS関連ドキュメント
https://tailwindcss.jp/docs/utility-first  
https://www.creative-tim.com/learning-lab/tailwind-starter-kit/documentation/css/alerts

---

## プロジェクトの作成
_以下はプロジェクト作成時のみ実行する_  
別プロジェクトから dockerディレクトリ と docker-compose.yml をコピー  
Docker関連のファイルを修正  
Dockerを起動  
```
$ docker compose up -d
```
phpのコンテナに入る
```
$ docker compose exec php bash
```
Laravelプロジェクトを作成
```
# composer create-project "laravel/laravel=8.*" asas_pos_manager
```
PHP, Laravelのバージョン確認
```
# php -v
# php artisan --version
```
ファイルを移動
```
# mv asas_pos_manager/* .
# mv asas_pos_manager/.[^\.]* .
# rm -Rf asas_pos_manager/
```



## 参考記事 laravel-test
https://reffect.co.jp/laravel/env-file-basic-understanding

https://readouble.com/laravel/8.x/ja/configuration.html


# laravel-test 学習メモ
.envの変更を反映させるために
> php artisan config:clear
を実行

