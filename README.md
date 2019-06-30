# Laravel memo

## Environment

Laravel 5.7.\*

## How to create

バージョンを指定してプロジェクトを生成

```sh
composer create-project "laravel/laravel=5.7.*" bookapp
```

???: 学習動画と異なり、 application key が表示されなかった。バージョンアップで動作が変わったのかも。  
--> `.env`に書いてあるものがそれっぽい  
参考: 最後の方に以下のようなコマンド実行が書いてあった。

```sh
> Illuminate\Foundation\ComposerScripts::postAutoloadDump
> @php artisan package:discover --ansi
> @php artisan key:generate --ansi
```

```sh
# バージョンを確認
php artisan -V
> Laravel Framework 5.7.28
```

## Scaffold を使う

```sh
composer require 'laralib/l5scaffold' --dev
```
