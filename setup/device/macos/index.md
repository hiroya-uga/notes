---
title: 'macOSのキッティング'
description: 'macOSでWeb制作をするためのPCキッティング手順です。'
publishedAt: '2026-05-23T00:00:00+09:00'
---

## 1. GUIで行う作業

### 1-1. システム設定

![システム設定のキャプチャ](./preference.webp?size=1280x892)

| 画面遷移 | 変更内容と手順 | 備考 |
| :- | :- | :- |
| アクセシビリティ → ディスプレイ → ポインタ | 「カーソルのサイズ」を少し上げる |  |
| ディスプレイ | 「スペースを拡大」 | メモリが8GBなどの機種では負荷が増すため非推奨 |
| メニューバー | 「Bluetooth」「バッテリー」「集中モード」の表示設定を「使用中に表示」から「常に表示」に変更 |  |
| メニューバー → バッテリーオプション | 「割合(%)を表示」を有効化 |  |
| 外観 | 「スクロールバーの表示」を「常に表示」 |  |
| キーボード → テキスト入力 → 入力ソース → 編集 | 「文頭を自動的に大文字にする」を無効化、「スペースバーを2回押してピリオドを入力」を無効化 |  |
| キーボード → テキスト入力 → 入力ソース → 編集 → 日本語 | 「ライブ変換」を無効化、「Windows風のキー操作」を**有効化** |  |
| キーボード → キーボードショートカット → キーボード | 「次のウインドウを操作対象にする」を`option` + `Tab`に変更 | デフォルトは`option` + `@` |

### 1-2. アプリケーションごとの設定

| 対象アプリ | 変更内容と手順 | 備考 |
| :- | :- | :- |
| Finder | `Command` + `Shift` + `.`で隠しファイルを表示する | |
| Safari | 設定（`Command` + `,`）→ 「詳細」タブ → 「Tab キーを押したときに Web ページ上の各項目を強調表示」にチェック | デフォルトではフォーム要素以外がTab移動の対象外 |
| Safari | 設定（`Command` + `,`）→ 「詳細」タブ → 「Web デベロッパ用の機能を表示」にチェック | |

## 2. CLIで行う作業

### 2-1. Homebrewのインストール

https://brew.sh

### 2-2. setupリポジトリで一括セットアップ

[hiroya-uga/setup](https://github.com/hiroya-uga/setup)をクローンして`install.sh`を実行する。

```sh
git clone https://github.com/hiroya-uga/setup.git
cd setup
zsh ./install.sh
```

### 2-3. Gitの識別情報を設定

`~/.gitconfig.local`にユーザー名とメールアドレスを設定する。

```sh
git config -f ~/.gitconfig.local user.name "name"
git config -f ~/.gitconfig.local user.email "email"
```
