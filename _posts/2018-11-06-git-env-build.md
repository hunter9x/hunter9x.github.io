---
type: post
title: 俺派git環境構築
---

## チーム開発環境の模索

自分がやりやすいものを設計してみる

### やること

* git運用のルール
* CI設定
* deployフロー

### やらないこと

* 開発環境構築
* 言語の書き方解説

### 前提

* PHPプロジェクト
* 2人チーム開発
* gitlab使用

## git運用ルール作成

### Branch

* github flow採用
  * testもdeployも対象はmasterだけ -> わかりやすい
  * 開発/検証/本番は一律masterで確認する
  * チームは２人しかないため開発ブランチはそこまで派生しない
* 命名規則
  * `feature/` : 定番の機能ブランチ
  * `hotfix/` : バグ修正や微修正など
    * [ここ](https://udacity.github.io/git-styleguide/)が参考になりそう

### Commit message
