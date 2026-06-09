---
title: '小技・小ネタ'
description: 'HTML/CSS/JavaScriptやブラウザ周りの覚えておくと便利なテクニック、共有したい小ネタをまとめます。'
publishedAt: '2026-06-03T20:53:40+09:00'
---

## Webという言葉の表記

本サイトでは「Web」という表記で統一しています。

参考：「[Webという言葉の表記が揺れている](/articles/tech-blog/2026/06-01-web/)」


## CSS

### 1つのHTMLに施された200種類以上のスタイリング例

[CSS Zen Garden](https://www.csszengarden.com/)

2003年にDave Shea氏が立ち上げたデザイン投稿サイトです。同一のHTMLファイルに対してCSSのみを変更した例が200種類以上公開されており、HTMLとCSSの分離やWeb標準の考え方を広く普及させるきっかけのひとつとなりました。

### `rebeccapurple`という色名

```css
* {
  color: rebeccapurple;
}
```

CSSコミュニティで長年活躍されているEric Meyer氏のご息女、Rebecca Alison Meyerさんが6歳の誕生日に亡くなったことを受け、Rebeccaさんが好きだった紫色を彼女の名前で残そうという呼びかけが起こり、`rebeccapurple`が[CSS Color Module Level 4](https://www.w3.org/TR/css-color-4/#valdef-color-rebeccapurple)に追加されました[^1]。のちに[CSS-Nextコミュニティが公開したCSSのロゴ](https://github.com/CSS-Next/logo.css)にも、この`rebeccapurple`が採用されています。

[^1]: [rebeccapurple – Eric’s Archived Thoughts](https://meyerweb.com/eric/thoughts/2014/06/19/rebeccapurple/)（英語、2026年6月1日閲覧）


## JavaScript

### JavaScriptは`[ ] ( ) ! +`の6つの記号だけでコードが書ける

たとえば`!![]`は`true`になり、`+[]`は「0」、`+!+[]`は「1」になります。

```js
console.log(!![]);                       // > true
console.log(+[]);                        // > 0
console.log(+!+[]);                      // > 1
console.log((!![]+[])[+[]]);             // > t
console.log((!![]+[])[+!+[]]);           // > r
console.log((!![]+[])[!+[]+!+[]]);       // > u
console.log((!![]+[])[!+[]+!+[]+!+[]]);  // > e
```

文字列化した`"true"` `"false"` `"undefined"` `"[object Object]"`などからアルファベットを拾って`eval()`する、というテクニック（？）です[^2]。

[^2]: Martin Kleppe氏が2012年に作った[jsfuck.com](https://jsfuck.com/)で、任意のコードを6種類の記号にしたものが生成できる。（2026年6月1日閲覧）

```js:alert(1)を実行するコード
[][(![]+[])[+!+[]]+(!![]+[])[+[]]][([][(![]+[])[+!+[]]+(!![]+[])[+[]]]+[])[!+[]+!+[]+!+[]]+(!![]+[][(![]+[])[+!+[]]+(!![]+[])[+[]]])[+!+[]+[+[]]]+([][[]]+[])[+!+[]]+(![]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+[]]+(!![]+[])[+!+[]]+([][[]]+[])[+[]]+([][(![]+[])[+!+[]]+(!![]+[])[+[]]]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+[]]+(!![]+[][(![]+[])[+!+[]]+(!![]+[])[+[]]])[+!+[]+[+[]]]+(!![]+[])[+!+[]]]((!![]+[])[+!+[]]+(!![]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+[]]+([][[]]+[])[+[]]+(!![]+[])[+!+[]]+([][[]]+[])[+!+[]]+(+[![]]+[][(![]+[])[+!+[]]+(!![]+[])[+[]]])[+!+[]+[+!+[]]]+(!![]+[])[!+[]+!+[]+!+[]]+(+(!+[]+!+[]+!+[]+[+!+[]]))[(!![]+[])[+[]]+(!![]+[][(![]+[])[+!+[]]+(!![]+[])[+[]]])[+!+[]+[+[]]]+([]+[])[([][(![]+[])[+!+[]]+(!![]+[])[+[]]]+[])[!+[]+!+[]+!+[]]+(!![]+[][(![]+[])[+!+[]]+(!![]+[])[+[]]])[+!+[]+[+[]]]+([][[]]+[])[+!+[]]+(![]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+[]]+(!![]+[])[+!+[]]+([][[]]+[])[+[]]+([][(![]+[])[+!+[]]+(!![]+[])[+[]]]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+[]]+(!![]+[][(![]+[])[+!+[]]+(!![]+[])[+[]]])[+!+[]+[+[]]]+(!![]+[])[+!+[]]][([][[]]+[])[+!+[]]+(![]+[])[+!+[]]+((+[])[([][(![]+[])[+!+[]]+(!![]+[])[+[]]]+[])[!+[]+!+[]+!+[]]+(!![]+[][(![]+[])[+!+[]]+(!![]+[])[+[]]])[+!+[]+[+[]]]+([][[]]+[])[+!+[]]+(![]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+[]]+(!![]+[])[+!+[]]+([][[]]+[])[+[]]+([][(![]+[])[+!+[]]+(!![]+[])[+[]]]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+[]]+(!![]+[][(![]+[])[+!+[]]+(!![]+[])[+[]]])[+!+[]+[+[]]]+(!![]+[])[+!+[]]]+[])[+!+[]+[+!+[]]]+(!![]+[])[!+[]+!+[]+!+[]]]](!+[]+!+[]+!+[]+[!+[]+!+[]])+(![]+[])[+!+[]]+(![]+[])[!+[]+!+[]])()((![]+[])[+!+[]]+(![]+[])[!+[]+!+[]]+(!![]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+!+[]]+(!![]+[])[+[]]+([][(![]+[])[+!+[]]+(!![]+[])[+[]]]+[])[+!+[]+[+!+[]]]+[+!+[]]+([]+[]+[][(![]+[])[+!+[]]+(!![]+[])[+[]]])[+!+[]+[!+[]+!+[]]])
```


### JavaScriptコードそのものがアスキーアートになっている芸術がある

[aem1k - JS Hacks & Creativity](https://aem1k.com/)

実行すると地球が回り出す**Spin the globe**だけでも見てほしい[^3]。

[^3]: JSFuckの作者でもあるMartin Kleppe氏による作品群（2026年6月1日閲覧）


### `NaN`は`NaN`と等しくない

`NaN`は自分と比べても等しくない唯一の値です。`0/0`や`'hoge' * 2`など、異なる計算でも無効な結果はすべて`NaN`になります。それらを同じ値とみなさないようにするため、ECMAScript仕様（IEEE 754準拠）でこのように定められています[^4]。

[^4]: 6.1.6.1.13 Number::equal ( x, y ) [ECMAScript® 2027 Language Specification](https://tc39.es/ecma262/#sec-numeric-types-number-equal)（英語、2026年6月3日閲覧）

```js
console.log(null === null);           // > true
console.log(undefined === undefined); // > true
console.log(true === true);           // > true
console.log(1 === 1);                 // > true
console.log(Infinity === Infinity);   // > true
console.log(NaN === NaN);             // > false
```

ただし、後述のSameValueZero比較を使う`Array.prototype.includes()`や、SameValue比較を使う`Object.is()`であれば、`NaN`同士を等しいものとして扱えます。

```js
console.log([NaN].find(item => item === NaN)); // > undefined
console.log([NaN].some(item => item === NaN)); // > false
console.log([NaN].includes(NaN));              // > true
console.log(Object.is(NaN, NaN));              // > true
```

なお、ある値が`NaN`であるかを判定したいときは`Number.isNaN()`を使います。`globalThis.isNaN()`は引数を数値に変換してから判定するため、`isNaN('NaN')`が`true`になるなど直感的ではない結果が返ることがあります。

```js
// Not a Numberかどうかを確認してる
console.log(isNaN(1));            // > false
console.log(isNaN("NaN"));        // > true
console.log(isNaN(NaN));          // > true

// 値が NaN であるかを確認してる
console.log(Number.isNaN(1));     // > false
console.log(Number.isNaN("NaN")); // > false
console.log(Number.isNaN(NaN));   // > true
```

### JavaScriptには等価比較のアルゴリズムが4種類ある

抽象等価と厳密等価以外にも、`Array.prototype.includes()`や`Map`/`Set`のキー比較で使われる**SameValueZero**、`Object.is()`で使われる**SameValue**があります[^5]。

[^5]: [等価性の比較と同一性 - JavaScript | MDN](https://developer.mozilla.org/ja/docs/Web/JavaScript/Guide/Equality_comparisons_and_sameness)（2026年6月3日閲覧）

違いは`NaN`同士と`+0`/`-0`の扱いだけです。

| アルゴリズム | 使われる場所 | `NaN`と`NaN`の比較 | `+0`と`-0`の比較 |
|---|---|:-:|:-:|
| 抽象等価 (Loose Equality) | `==` | `false` | `true` |
| 厳密等価 (Strict Equality) | `===` | `false` | `true` |
| SameValueZero | `Array.prototype.includes()`、`Map`/`Set`のキー比較など | `true` | `true` |
| SameValue | `Object.is()` | `true` | `false` |

```js
console.log(NaN === NaN);          // > false
console.log(+0 === -0);            // > true

// SameValueZero
console.log([NaN].includes(NaN));  // > true
console.log([+0].includes(-0));    // > true

// SameValue
console.log(Object.is(NaN, NaN));  // > true
console.log(Object.is(+0, -0));    // > false
```

### `0.1 + 0.2`は`0.3`にならない

`0.1 + 0.2`の計算結果は`0.30000000000000004`になります。

```js
console.log(0.1 + 0.2);         // > 0.30000000000000004
console.log(0.1 + 0.2 === 0.3); // > false
```

十進の小数を正確に表せないために生じる誤差で、JavaScriptに限らず多くの言語で同じことが起こります[^6]。

[^6]: 各言語の結果は[0.30000000000000004.com](https://0.30000000000000004.com/)で確認できる。（英語、2026年6月3日閲覧）

### `document.all`はfalsy

`document.all`はすべての要素を含む`HTMLAllCollection`を返しますが、オブジェクトでありながら真偽値に変換すると`false`になる唯一の値です。型も`object`ではなく`undefined`です。

```js
console.log(Boolean(document.all));                     // > false
console.log(document.all instanceof HTMLAllCollection); // > true
console.log(typeof document.all);                       // > "undefined"
```

かつてInternet Explorerを判定するために`if (document.all)`のような分岐がよく書かれていました。こうした既存のコードがモダンブラウザで壊れないよう、<ruby>willful violation<rp>（</rp><rt>意図的な仕様違反</rt><rp>）</rp></ruby>として定められています[^7]。

[^7]: [typeof - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof#exceptional_behavior_of_document.all) - MDN Web Docs, Mozilla（英語、2026年6月3日閲覧）

### `undefined`と`NaN`、`Infinity`はリテラルではない

`true`や`null`などと異なり、`undefined`と`NaN`など一部の値は`window`に変数として用意されているだけ。

```js
console.log('undefined' in window, window.undefined); // > true, undefined
console.log('NaN' in window, window.NaN);             // > true, NaN
console.log('Infinity' in window, window.Infinity);   // > true, Infinity

console.log('null' in window, window.null);           // > false, undefined
console.log('true' in window, window.true);           // > false, undefined
```

かつて変数`undefined`は上書き可能だったため、`undefined`との比較は`typeof`を使うか、`undefined`を返す`void 0`と比較していました。

```js:hogeがundefinedであるかどうかを検証する例
if (typeof hoge === 'undefined') {}
if (hoge === void 0) {}
```

ローカルスコープでは、現代でも変数名として宣言できるので、ES3時代の雰囲気を味わうことができます。

```js:undefinedがundefinedではなくなる例
((undefined, NaN, Infinity) => {
  console.log(undefined, NaN, Infinity); // > 0, 1, 2
})(0, 1, 2);
```

```js:nullやtrueは予約語なのでSyntaxErrorになる
const undefined = true; // OK
const null = true;      // SyntaxError
const true = false;     // SyntaxError
```

### `id`属性をもつHTML要素はグローバル変数に公開される

とくに活用するタイミングはないですが、`id`属性を持つ要素が読み込まれるとグローバル変数として公開されます。たとえばスクリプト実行時点でDOMに`div#hoge`が存在すると、`window.hoge`は`HTMLDivElement`を返します。

```html
<script>
console.log(window.hoge);          // > undefined
console.log(window['my-element']); // > undefined
</script>

<div id="hoge"></div>
<div id="my-element"></div>

<script>
console.log(hoge);                  // > HTMLDivElement
console.log(window['my-element']);  // > HTMLDivElement
</script>
```

### 動画を2倍速以上で再生する裏技

倍速設定のUIがなくても早くできる。

```js
document.querySelector('video').playbackRate = 3
```

### 動画をピクチャーインピクチャー再生する裏技

PiPのUIがなくてもPiPできる。

```js
document.querySelector('video').requestPictureInPicture()
```
