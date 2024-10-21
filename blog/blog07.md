# 業務歴1年目のコーダーがアクセシビリティ案件にアサインされた話

## 前段

転職する前にwebアプリケーションアクセシビリティを読んでいた
Webアクセシビリティへの興味を軽くアピールしていた
社内にWebアクセシビリティに明るい人がいなかった
十分な時間を取ることができたので調べながら実装するチャンスを得ることができた

## 案件の概要

全国的な金融機関のコーポレートサイト
jis規格＊＊＊に適合するサイトに改修する案件

最初はチェックも依頼されていたが知見がないのでお断り
別会社のチェック結果を元にwcag2.2の適合を目指して改修していく

手探りの見積もり
見積もりの結果、600項目の中でサイト全体の表示に関わる400項目を優先的に改修することに

## 苦労
ハック的なマークアップが多用されていた
アコーディオンの実装でチェックボックスにチェックがされるとその隣の要素の高さが変わる、というハック的な手法でアコーディオンが実装されていた

sp版のフォントサイズがvwのみで実装されていた
420pxのカンプの数値を元にvwで実装
それをremに変換
750あたりでだいぶレイアウトが変なことになる


■altテキスト
リストや地図を含む画像　テキストにするのはしんどいが
AIの力でなんとかなったかも
perplexityを使用
ソフトバンク・ワイモバイルユーザーは月額30ドルの有料プランを1年間無料で使用できる
既にwebで公開されている画像だったため、perplexityに画像を渡しても問題ないと判断
かなりの精度で言語化してくれる
それを元に
URL
を参考に体裁を整える

テーブルを画像で置いている箇所も多数あったためテーブルでマークアップ




WCAGのルールの解釈に悩む
こう書いてるということはこれでいいはず、みたいな状況

診断結果に実装のヒントが記載されていて助かった
が、そのヒントにピンとこない部分も散見されたので困ることもあった