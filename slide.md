class: center, middle
background-image: url(background-image.jpg)

## 最近デザインやCSSで得た知見

### by @y_temp4

---

## 概要

- CSSとかフロントのデザインで得た知見をまとめた（まとめてない）
- 雑に見て、知ってなかったら「ふ〜ん」と思ってくれると便利

---

## 1. 色

- [Open Color](https://yeun.github.io/open-color/) を使っている
- なんかいい感じの色として使っている

<a href="https://gyazo.com/ec31dfee741a1a927e721b3f84dd602c"><img src="https://i.gyazo.com/ec31dfee741a1a927e721b3f84dd602c.png" alt="https://gyazo.com/ec31dfee741a1a927e721b3f84dd602c" width="500" style="width: 100%"/></a>

---

## 2. 要素から外れた文字を「...」で省略（2行）

あああああ<br>
ああああ...


↑ みたいなのを想定

```css
.hoge {
  -webkit-line-clamp: 2;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
}
```

---

## 3. 改行しない

```css
p {
  white-space: nowrap;
}
```

---

## 4. ローディングモーション

- [NProgress](http://ricostacruz.com/nprogress/)

[![https://gyazo.com/0b61ed5ae42b3c3c404dee3e99a5e167](https://i.gyazo.com/0b61ed5ae42b3c3c404dee3e99a5e167.gif)](https://gyazo.com/0b61ed5ae42b3c3c404dee3e99a5e167)

---

## 5. いい感じのデザインにするための知見

1. まずはグレースケールでつくる
2. 余白をとる
3. いい感じのサイトを真似る（参考：[medium.com](https://medium.com/)）

---
class: center, middle

# おわり

---
class: center, middle

## 参考：このスライドのスタイル

---

```CSS
body {
  font-family: sans-serif;
}
.remark-slide-content {
  background: #f8f9fa;
  background-size: cover;
  color: #495057;
}
.remark-slide-number {
  color: #5c7cfa;
  opacity: 1;
}
h1, h2 {
  background: #4263eb;
  margin: -.5em -2em 1em -2em;
  padding: .5em 1em;
  color: #f8f9fa;
}
a {
  color: #1862ab;
}
li {
  font-size: 1.5em;
}
.remark-code, .remark-inline-code {
  font-family: Consolas, 'Courier New', Courier, Monaco, monospace;
}
```
---

## 参考：このスライドのスタイル

- 色はさっき紹介した[Open Color](https://yeun.github.io/open-color/)
- 画像は[STOCK UP](https://www.sitebuilderreport.com/stock-up#q=splash)から入手
- 見出しを見やすくした
- コードハイライトは`monokai-sublime`

```js
var slideshow = remark.create({
  sourceUrl: 'slide.md',
  highlightStyle: 'monokai-sublime',
})
```
