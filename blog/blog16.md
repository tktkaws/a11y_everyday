# font-sizeをvw単位で設定してあるサイトのアクセシビリティを向上する
font-sizeをvw単位で設定してあるサイトで1.4.4を達成するためにはどうするべきか？
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