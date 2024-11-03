# README
## Overview
- Golang でCLIツールを作成する際にベースとなるリポジトリ

## First Step
- このリポジトリ内の sample-cli-app を任意のプロジェクト名に置換する

## How to Develop
- WinodwsやLinuxなど任意のディレクトリでこのリポジトリをcloneする
- VSCode で cloneしたローカルリポジトリを開く
- .devcontainer 配下のファイルを利用して開発コンテナを開く

## How to Build
- VSCodeで .devcontainer 配下のファイルを利用して開発コンテナを開く
- 起動したコンテナ上のbashで以下のビルドコマンドを実行する

```bash
# Linux向けビルド
go build -o sample-cli-app main.go
# Winodws向けビルド
GOOS=windows GOARCH=amd64 go build -o sample-cli-app.exe main.go
```

## How to Test
- VSCode で このリポジトリを開く
- .devcontainer 配下のファイルを利用して開発コンテナを開く
- 起動したコンテナ上のbashで以下のテストコマンドを実行する
- 現在のディレクトリとサブディレクトリのパッケージをテスト対象とする
- -v: テスト結果を詳細に出力する
- -cover: テストのカバレッジを出力する

```bash
go test -v -cover ./...
```
