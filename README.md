# Docker + Seleniumのテスト

Docker と Selenium を使って少し手軽にスクレイピングするサンプル。

## 1. 準備

必要なライブラリをインストール

### Poetryを使っている場合

``` shell
$ poetry install
```

### Pipを使う場合

``` shell
$ pip install -r requirements.txt
```

## 2. docker-compose.yml の準備

自分の使っているMacのCPUに応じて docker-compose.yml を準備する。

### Intel Macの場合

``` shell
$ cp docker-compose.yml.intel docker-compose.yml
```

### M1 Macの場合

``` shell
$ cp docker-compose.yml.apple_silicon docker-compose.yml
```

## 3. DockerでSeleniumを起動

``` shell
$ docker compose up -d
```

## 4. プログラムを実行

``` shell
$ poetry run python test.py
```

## 5. 実行が終わったら Selenium を終了

``` shell
$ docker compose down
```

いじょ。
