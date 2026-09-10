---
title: 📄displayプロパティでアニメーション
---

displayプロパティは離散値なので普通はアニメーションできない。

```css
.element {
  transition: opacity 1s;
}

.element.hidden {
  opacity: 0;
  display: none;
}
```

上のようにしてhiddenクラスをトグルしてもアニメーションしない。  

しかし以下のようにするとアニメーションする。

```css
.element {
  transition: opacity 1s, display 1s allow-discrete;

  @starting-style {
    opacity: 0;
  }
}

.element.hidden {
  opacity: 0;
  display: none;
}
```

表示から非表示のアニメーションは `transition` でdisplayに対して設定している `allow-discrete` が影響する。  
これは離散値のアニメーションが有効になる設定。  
`display: none` と `content-visibility: hidden` だけ特別で、アニメーションが終わってから非表示になる。  
それ以外のプロパティは50%アニメーションしてから切り替わる。

非表示から表示のアニメーションは `@starting-style` が影響する。  
これはレンダリングされた瞬間の設定。  
したがって `display: none` が外れた瞬間は `opacity: 0` から始まる。

参考

- [transition-behavior - CSS: カスケーディングスタイルシート | MDN](https://developer.mozilla.org/ja/docs/Web/CSS/transition-behavior)
- [@starting-style - CSS: カスケーディングスタイルシート | MDN](https://developer.mozilla.org/ja/docs/Web/CSS/@starting-style)
