# font-sizeをvw単位で設定してあるサイトのアクセシビリティを向上する

## 序章
font-sizeをvw単位で設定してあるサイトで1.4.4を達成するためにはどうするべきか？
初めて担当したアクセシビリティ案件で遭遇したのが本件。
sp版ではfont-sizeをvw単位で設定してあるため、達成基準 1.4.4が不適合となっていた。
414px幅のカンプで16pxをvwに変換して font-size: 3.8vw;と設定してあった。
単純にremに変換しても414px幅の基準で変換すれば767付近では文字が小さすぎて余白がありすぎる状態に。
767付近に合わせれば逆にスマホでは大きすぎる状態に。
どうやって解決すればよいのか。


## wcag
達成基準 1.4.4 テキストのサイズ変更

https://waic.jp/translations/WCAG21/#resize-text

達成基準 1.4.4: テキストのサイズ変更を理解する

https://waic.jp/translations/WCAG21/Understanding/resize-text.html

## 問題点
chromeではフォントサイズを絶対指定するとテキストのみの拡大ができない
→そのため相対指定する必要がある

vwでフォントサイズを指定すると同様にテキストのみの拡大ができない

## 対処方法
### 方法01　相対指定のみで指定　小さい方に合わせる
### 方法02　相対指定のみで指定　大きい方に合わせる
### 方法03　細かくメディアクエリを設定して基準のフォントサイズを変更する
### 方法04 clampで指定 tan~~
qiitaの記事

## お手本

https://recruit.smarthr.co.jp/
```
html {
    font-size: 62.5%;
}

// 1440pxで24px
.lead[data-astro-cid-kbwy6dry] {
    font-size: var(--fz-lv3);
}

--fz-lv3: clamp(2* var(--rem), .376vw + 1.859* var(--rem), 2.4* var(--rem));

--rem: calc(1rem* max(1440, var(--window-width)) / 1440);

--window-width: tan(atan2(var(--100vw), 1px));

@property
--100vw {
    syntax: "<length>";
    initial-value: 0;
    inherits: false;
}

```
smarthrの採用サイト
aaa1yでおなじみ、トルクさんが制作


## その他の事例
デジタル庁
コンテンツ幅もrem指定のため文字サイズの拡大で拡がる

## 参考情報
https://zenn.dev/ixkaito/articles/fluid-typography

https://shibajuku.net/font-size-still-relative/

https://qiita.com/kskwtnk/items/67b8d85253ada19ed6c5

https://dev.to/janeori/css-type-casting-to-numeric-tanatan2-scalars-582j


## 記事の要約

https://dev.to/janeori/css-type-casting-to-numeric-tanatan2-scalars-582j

この記事では、CSSで単位付きの値を数値に変換する革新的な手法として、tan(atan2())関数の組み合わせを利用する方法を解説しています。現在のCSS仕様ではcalc(100vw / 1px)のような単位同士の除算が正式にサポートされていませんが、三角関数を活用することでこの制限を回避できます

### 技術的な背景
atan2(y, x)関数は座標から角度を計算し、tan()関数でその角度から元の比率（y/x）を取得します。数学的にはtan(atan2(y, x))がy/xと等しくなる性質を利用して、単位付きの値を単位なしの数値に変換します。

### ブラウザ対応状況（2025年1月現在）
ブラウザ	動作状況	備考
Chrome	部分対応	混合単位で不正確な値
Firefox	条件付き	同単位のみ有効
Safari	非対応	calc()内でラップ必要

現在の制限としてブラウザ実装の不完全さが指摘されていますが、@propertyルールと組み合わせることでChromeでは実用的な結果が得られます12。今後のブラウザ更新でより安定した動作が期待される手法です。