# Git / GitHub について

## Git とは?

| Git（ギット）は、プログラムのソースコードなどの変更履歴を記録・追跡するための分散型バージョン管理システムである\[Wikipedia](https://ja.m.wikipedia.org/wiki/Git)より

主にプログラミングなどのソースコードを管理するもの。

## GitHub とは?

Git を GUI で操作できるようにしたもの

## Git の使い方

|command|説明|
|-------|---|
|config|Git の設定関連をするコマンド。`git config` で一覧が見れたり、後に続けて設定項目も打つことで設定できる。一番最初にやらないと使えない。|
|init|フォルダを git フォルダとして初期化するためのコマンド|
|…|…|
|push|git 上のリモートリポジトリにアップする時のコマンド|

## GitHub の使い方

### アカウント作成の流れ

1. メアド登録
1. パスワード
1. 色々

### プルリクエストの送る流れ

```mermaid
graph LR

  cloneorfork-->branch
  branch-->add
  add-->commit
  commit-->push
  push-->commit
  push-->pullrequest
  pullrequest-->review
  review-->recommit
  recommit-->review
  review-->merge

```
