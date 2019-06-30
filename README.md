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

ただし、Laravel 5.5 以降では上記だけではエラーになるので以下のように`vendor`配のコードの修正を行う。
[Laravel の Scaffold のインストール問題](https://qiita.com/masahirok_jp/items/f4efcf9f8b518c2be7b0)

さらに以下の対応も必要だった。
[Laravel 5.7 の scaffold でハマった](https://qiita.com/take8/items/9fe3442be55f0de5d76e)

```sh
php artisan make:scaffold Task -v --schema="title:string,body:text"
```
