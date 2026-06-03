---
title: 'Markdownプレビュー'
description: 'このページはMarkdownの各種要素がどう表示されるかを目視で確認するためのものです。本番ビルドには含まれません。'
publishedAt: '2026-05-23T00:00:00+09:00'
sortIndex: 10
---

## 段落とインライン

通常の段落と**太字**、*斜体*、~~取り消し線~~、`インラインコード`、[通常リンク](https://example.com/)を含む文章です。日本語とEnglishが混ざる場合のアキ感も確認できます。

### 改行スパン（2スペース改行）

1行目  
2行目（直前の行末に2スペースが入っており、`<span class="block">`で包まれる想定）

### 会話風（`——`始まり）

——これは`talking`拡張で描画される会話風の段落です。

## 見出し

### h3見出し

#### h4見出し

##### h5見出し

###### h6見出し

## リスト

### 順序なし

- 項目A
- 項目B
  - ネストB-1
  - ネストB-2
    - さらにネスト
- 項目C

### 順序付き

1. ステップ1
2. ステップ2
   1. サブステップ2-1
   2. サブステップ2-2
3. ステップ3

<!-- ### 画像差分ビューア（リストに画像2件）

- ![比較画像1：Before](https://placehold.co/600x400/png?text=Before&size=600x400)
- ![比較画像2：After](https://placehold.co/600x400/png?text=After&size=600x400) -->

### Amazonアソシエイトリスト

- [Amazon商品サンプル1](https://amzn.to/preview-sample-1)
- [Amazon商品サンプル2](https://amzn.to/preview-sample-2)

## 引用

### 通常の引用

> シンプルな引用ブロックのサンプル。複数行にわたる場合の体裁もここで確認できます。
>
> 引用内の改段落。

### 出典つき引用

> 名前のついた色は、長い時間をかけて文化として定着していくものだと言える。
>
> 出典：[サンプル出典タイトル - example.com](https://example.com/sample)

## コードブロック

### インラインコード

地のテキストに`const x = 42;`のように埋め込み。

### 言語のみ

```ts
const greet = (name: string): string => `Hello, ${name}`;
```

### 言語＋タイトル

```ts:挨拶を返す関数
const greet = (name: string): string => `Hello, ${name}`;
```

### シェル（`$`プレフィックス）

```sh
$ git status
$ git commit -m "Add preview page"
$ git push
```

### Diff

```diff
- const oldValue = 1;
+ const newValue = 2;
  const unchanged = 0;
```

### 日本語訳（`japanize`）

```japanize
Markdown is a lightweight markup language for creating formatted text.
```

<!-- ### プラットフォーム指定（`macOS向け：`/`Windows向け：`）

```sh:macOS向け：Homebrewのインストール
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

```pwsh:Windows向け：wingetでGitをインストール
winget install --id Git.Git -e
``` -->

## キーボードショートカット（kbd）

シンボル付きキー: `Command` + `Shift` + `K`

シンボル付き各種: `Cmd` `Ctrl` `Option` `Return` `Enter` `Tab` `Escape` `Esc` `Delete` `Space`

テキストのみのキー: `Alt` + `F4`、`PrintScreen`、`A` `Z` `0` `9` `-` `[` `;`

## テーブル

### 標準テーブル（align指定あり）

| 名前  | 説明             | 数量 |
| :---- | :--------------- | ---: |
| help  | サイトの使い方   |    1 |
| life  | 生活メモ         |    4 |
| setup | キッティング手順 |    2 |

### 行ヘッダ（先頭セルが`^`始まり）

| カテゴリ      | 例                       |
| :------------ | :----------------------- |
| ^フルーツ     | りんご、ばなな、もも     |
| ^野菜         | にんじん、たまねぎ、なす |

### 手順テーブル（`of-steps`が付くケース）

| 手順 | 内容                   |
| :--: | :--------------------- |
|  1   | サーバーを準備する     |
|  2   | 設定ファイルを編集する |
|  3   | サービスを起動する     |

### キャプション付きテーブル

主要キャラクター一覧：

| 名前  | 役割       |
| :---- | :--------- |
| Alice | 探検家     |
| Bob   | エンジニア |

<!-- ## カスタムブロック

:::note
注釈ブロック（`:::note`）です。補足情報を書きます。
:::

:::alert
警告ブロック（`:::alert`）です。リスクの高い操作などに使います。
:::

:::warn
注意点ブロック（`:::warn`）です。
:::

:::tip
ヒントブロック（`:::tip`）です。
:::

:::info
情報ブロック（`:::info`）です。
:::

:::memo
メモブロック（`:::memo`）です。
::: -->

## 外部埋め込みリンク
<!-- 
### YouTube（`youtu.be`）

[YouTube動画タイトル](https://youtu.be/preview-test-id)

### CodePen（`codepen.io`）

[CodePenのデモ](https://codepen.io/hiroya_uga/pen/preview-test-id) -->

### Amazonリンク単独（`amzn.to`）

[Amazon商品ページ](https://amzn.to/preview-single)

<!-- ## 画像

### サイズ指定なし

![代替テキストのサンプル](https://placehold.co/400x300/png?text=NoSize)

### サイズ指定あり（`?size=WxH`）

![代替テキストのサンプル](https://placehold.co/800x450/png?text=Sized&size=800x450) -->

## 区切り線

---

## 脚注

本文中に脚注[^1]を付けられます。複数の脚注[^2]も使えます。

[^1]: 最初の脚注の本文。
[^2]: 2番目の脚注の本文。

## 定義リスト

Markdown
: 軽量マークアップ言語

Frontmatter
: ファイル先頭のメタ情報ブロック
