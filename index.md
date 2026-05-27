---
title: 'WikiʻoleWeb'
description: 'WikiʻoleWeb（ウィキオレウェブ）は、日常的なメモ書きやツールの使い方など、雑多な個人的知識を書き留めておくWikiっぽいなにかです。'
publishedAt: '2026-05-06T16:33:29+09:00'
---

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

- 内容の正確性は保証されません。
- サイト内検索はGoogle検索を利用しています。
- サイト内ツールへのバナー画像は生成AIによって作成しています。
