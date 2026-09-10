---
title: 📄ビューポート外の要素をレンダリングしない
---

```css
.element {
  content-visibility: auto;
  contain-intrinsic-size: auto 100px;
}
```

`content-visibility: auto` によってビューポート外の要素がレンダリングされなくなり初期表示時のパフォーマンスが良くなる。  
`contain-intrinsic-size: auto 100px` はレンダリングされていないときの大きさの設定。一度もレンダリングされていないときは100pxとなり、一度レンダリングされたら実際の大きさになる。

参考

- [content-visibility - CSS: カスケーディングスタイルシート | MDN](https://developer.mozilla.org/ja/docs/Web/CSS/content-visibility)
- [contain-intrinsic-size - CSS: カスケーディングスタイルシート | MDN](https://developer.mozilla.org/ja/docs/Web/CSS/contain-intrinsic-size)
