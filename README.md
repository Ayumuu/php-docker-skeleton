# php-docker-skeleton

## 作業を行うコンテナ

本スケルトンでは、作業を行うコンテナを用意してあります。
composer等、開発時で必要なミドルウェアは、本番環境で使わない為、動作用と作業用をわけて開発を行います。

## アプリケーションのインストール

初期状態ではアプリケーションは入っていません、最新のLaravelを取得してアプリケーションを作成します。

コンテナに入って作業を行う場合は下記でsshします。
```docker-compose exec workspace sh```

コンテナに入ったら下記を実行してLaravelをインストールしましょう。
```composer create-project --prefer-dist laravel/laravel .```

localhostでアクセスできます。
```http://localhost/```
