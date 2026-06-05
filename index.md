---
title: 'WikiʻoleWeb'
description: 'WikiʻoleWeb（ウィキオレウェブ）は、日常的なメモ書きやツールの使い方など、雑多な個人的知識を書き留めておくWikiっぽいなにかです。'
publishedAt: '2026-05-06T16:33:29+09:00'
---

## 豆知識

「Wiki」はハワイ語で「速い」を意味し、1995年に公開されたWikiWikiWebが、現在の「Wiki」という言葉の起源だそうです。

そのWikiに、ハワイ語の否定語「ʻole」を加えて、このメモ書き領域を「Wikiではない」を意味する「WikiʻoleWeb」と命名しました。

ちなみに「ʻ」はアポストロフィではなく、**ʻokina（オキナ）** と呼ばれる文字（子音）です。

```js:オキナ（U+02BB）とシングルクオートの表記揺れ
const inputs = [
  "Wiki'oleWeb",   // U+0027 APOSTROPHE
  "Wiki'oleWeb",   // U+2018 LEFT SINGLE QUOTATION MARK
  "Wiki'oleWeb",   // U+2019 RIGHT SINGLE QUOTATION MARK
  "WikiʼoleWeb",   // U+02BC MODIFIER LETTER APOSTROPHE
  "Wiki`oleWeb",   // U+0060 GRAVE ACCENT
  "Wiki´oleWeb",   // U+00B4 ACUTE ACCENT
  "Wiki′oleWeb",   // U+2032 PRIME
  "WikiʻoleWeb",   // U+02BB MODIFIER LETTER TURNED COMMA (ʻokina)
];

const result = inputs.filter(item => item.includes("\u02BB"));

console.log(result); // > ["WikiʻoleWeb"]
```

## ご利用にあたって

- 内容の正確性は保証されません。一部わかりづらいジョークが含まれる場合があります。
- サイト内検索はGoogle検索を利用しています。
- サイト内ツールへのバナー画像は生成AIによって作成しています。
