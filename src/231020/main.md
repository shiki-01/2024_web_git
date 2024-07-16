# Git / GitHub について

## Git とは?

> Git（ギット）は、プログラムのソースコードなどの変更履歴を記録・追跡するための分散型バージョン管理システムである
> 
> [*Wikipedia*](https://ja.m.wikipedia.org/wiki/Git) *より*

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

### Git のインストール方法

1. [git の公式サイト](https://gitforwindows.org/) にアクセスする
1. ダウンロードする
1. `config` あたりの設定をする

## GitHub の使い方

### アカウント作成の流れ

1. メアド登録
1. パスワード
1. 色々

### プルリクエストの流れ

**そもそもプルリクとは？**\
プルリク | プルリクエスト | PR とは、Git においてなんたらの意味を持つものである。こうたらしてからああたらすることでこんなことができる。

#### フローチャート
```mermaid
---
title: Pull Request
---
graph LR

  subgraph Eddit
    direction LR
      push-->commit
      commit-->push
  end

  subgraph PullRequest
    direction LR
      review-->ReCommit
      ReCommit-->review
  end

  CloneOrFork-->Branch
  Branch-->Add
  Add-->Eddit
  Eddit-->PullRequest
  PullRequest-->Merge

```
#### ユースケース

```mermaid
sequenceDiagram
    participant プログラマ
    participant Github
    participant レビューア
    participant GithubAction

    プログラマ->>Github: pull-requestを作成
    Github->>レビューア: pull-requestを通知
    レビューア->>Github: コメントを投稿
    Github->>プログラマ: コメントを通知
    プログラマ->>Github: 修正コードをpush
    Github->>レビューア: 修正内容を通知
    レビューア->>Github: pull-requestをマージ
    Github->>GithubAction: ビルド・テスト・デプロイを実行
```

## その他

### コンフリクトが起きた場合

**コンフリクトとは？**\
コンフリクトとは…

### GitHub Copilot とは

### 便利な使い方

### OSS について
