# ゴミ箱App

## 設計書

https://docs.google.com/spreadsheets/d/1VFd2y1Y8dnjgAvS_c9fTA69DEW1dZkMF2lo1asfQVk4/edit#gid=0

## 環境構築

* Clone & Sail Up

```
$ git clone git@github.com:kbanchi-spartacamp/garbage-can-app.git
$ cd garbage-can-app
$ git switch develop
$ docker run --rm \
  -v $(pwd):/opt \
  -w /opt \
  laravelsail/php80-composer:latest \
  bash -c "composer install"
$ cp .env.example .env
$ sail up -d
$ sail artisan key:generate
$ sail artisan migrate:fresh --seed
```

* GCPのcredential

credential.jsonをengineer-connect-app/配下に配置してください
