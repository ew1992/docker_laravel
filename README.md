# docker_laravel

# 環境

* PHP 7.4-fpm-buster
* mysql 8.0
* Laravel: 8.0

# 環境構築

1.ソースコードを任意のディレクトリにクローン

```bash
$ git clone git@github.com:ew1992/docker-laravel.git
$ cd docker-laravel
```

2.環境変数を設定し(.envを修正し)、コンテナをビルド

```bash
$ cp .env.sample .env
$ docker-compose up -d --build
```

3.Laravelインストール  
  
.envファイルを作成し、DB関連の環境変数を設定(docker-laravelディレクトリで作成した.envの内容と一致させる)

```bash
$ cd src
$ cp .env.sample .env
$ docker-compose exec app bash
$ php artisan key:generate
$ composer install
$ php artisan key:generate
```