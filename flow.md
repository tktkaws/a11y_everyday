
■WCAG 2.2 Map 【和訳】
https://x.com/makoto_ueki/status/1841730312692171065
https://intopia.digital/wp-content/uploads/2024/05/Intopia_WCAGPoster_Japanese.pdf

■誰のためのアクセシビリティ？　障害のある人の経験と文化から考える
https://www.amazon.co.jp/%E8%AA%B0%E3%81%AE%E3%81%9F%E3%82%81%E3%81%AE%E3%82%A2%E3%82%AF%E3%82%BB%E3%82%B7%E3%83%93%E3%83%AA%E3%83%86%E3%82%A3%EF%BC%9F-%E9%9A%9C%E5%AE%B3%E3%81%AE%E3%81%82%E3%82%8B%E4%BA%BA%E3%81%AE%E7%B5%8C%E9%A8%93%E3%81%A8%E6%96%87%E5%8C%96%E3%81%8B%E3%82%89%E8%80%83%E3%81%88%E3%82%8B-%E7%94%B0%E4%B8%AD-%E3%81%BF%E3%82%86%E3%81%8D/dp/489815591X

視覚障害者が鑑賞するダンスの舞台の話が興味深かった
エイブリズム
エイブリズム（Ableism）とは、障害者に対する差別や社会的偏見を指す概念です。これは、能力のある人が優れているという考えに基づいており、障害を持つ人々を不当に扱うことを意味します

■アクセシビリティもくもく会を開催したい
オンライン
a11yのdiscordで開催させてもらえるとありがたい
心理的安全性を確保しつつ、技術的な正しさをどう提供できるかが問題？

会社のバックログにアクセシビリティの知見をためる
自分のnotionにまとめて公開できるものを公開する
ブログにもする

■読んだ本
困った見えにくい〜〜
色覚特性が異なる
性別人種の異なる6人のペルソナを立てて
それぞれの立場から困った状況とその解決方法を示してくれる
具体的な人物像があることで非常にわかりやすい

■アクセシブルなフォントサイズ
wcagには最低何PXという規定はない
ユーザーの見やすいサイズに変更可能であることが求められている
そのためには固定ではなくremでフォントサイズを指定する
vwやclampでレスポンシブに可変するのは楽だが、
フォントサイズを変更するという観点でいうと良くない
文字サイズを拡大したときに文字が認識できなくなるのもよくない
よくあるのがボタンのheightを固定のpxで指定してしまっているケース
拡大すると文字がはみ出て認識できない
letter-spacingとpaddingで調整するべし

■アクセシブルなフォントファミリー
UDフォント
IDフォントというのもある？


■ARIA Authoring Practices Guide (APG)
https://www.w3.org/WAI/ARIA/apg/

アクセシブルなコンポーネントの実装方法を紹介している
w3cが提供しているので安全安心


■アクセシビリティに取り組まないと、企業はどれくらい「損」をする？　試算する方法をご紹介
https://goodpatch.com/blog/2024-10-accessibility-cost

市場機会を逃すコスト
訴訟のコスト
問い合わせ対応のコスト
ブランドの評判とダメージに対応するコスト
後回し対応によるコスト

■スクリーンリーダーを使ってみた

■axe（自動チェックツールを使ってみた）

■アクセシビリティチェックを実際にどう行う？

■アクセシブルなフォーム
フォームのアクセシビリティを考える
https://azukiazusa.dev/blog/form-accessibility/

■アクセシビリティでキャリアを築きたい
副業
https://culumu.com/service/accessibility

■最速[要出典]アクセシビリティチェック
https://docs.google.com/presentation/d/16xM_XHva4h9JvF8Yfqdpxu2q2XjikQRgvHNDL0g4FFI/edit#slide=id.g2fbd433926a_0_0

具体的な方法が列挙されていてかなり参考になる
特にチェックシートの準備方法やチェックに役立つchrome拡張機能などの情報

■駒瑠市こまるしアクセシビリティ上の問題の体験サイト
https://a11yc.com/city-komaru/

＞アクセシビリティ上の問題を仕込んだサイトを生成します
＞勉強の教材、業務の資料としてお使いいただけます
＞用途にかかわらず無料でお使いいただけます

有限会社 時代工房が作成している
https://www.jidaikobo.com/

アクセシビリティの不具合について実際に公開されているサイトを使用して指摘するのは角が立つが、
架空の自治体サイトを生成してくれるのでとても便利


■SmartHR Design System　アクセシビリティ

https://smarthr.design/accessibility/

ウェブアクセシビリティ簡易チェックリスト
https://smarthr.design/accessibility/check-list/

ウェブアクセシビリティに関してよく取り上げられている事項について
分かりやすくまとまっている
最初期に読むテキストとしてよい




■ブログタイトル案
社内でWebアクセシビリティを布教させるには

■safariの困りごと
要件定義の段階では最新のsafariまで対応でよかったが、
先方のお偉いさんが古いiphoneを使っていたため数バージョン古いsafariに対応せざるをえなくなった。

■ヌーラボ アクセシビリティレポート #5
https://nulab.com/ja/blog/nulab/a11y-report-05/

■WCAG 2.2 達成基準 1.3.2 「意味のあるシーケンス」の検品について
https://www.mitsue.co.jp/knowledge/blog/qc/202501/29_1403.html

■アクセシビリティ推進の実情
https://docs.google.com/presentation/d/1fmhCK5WhphYockiFWYMetcMNbViyyGaadN0GF0JO2O4/edit#slide=id.g329093ae8b3_0_183

■ブランドを毀損しないためのウェブアクセシビリティ ~攻守でバランスよく実現するブランド価値~｜モリサワ　note編集部
https://note.morisawa.co.jp/n/n0259767b42c0

■みんコミュデザイン
https://www.dentsu.co.jp/news/item-cms/communication_design_guide.pdf
アクセシビリティだけではないDEIに関するコミュニケーションデザインのガイドライン

■ウェブアクセシビリティ改善での生成AI活用を模索する
https://zenn.dev/takanorip/articles/ad8437d4b5667e

生成AIは現時点では既存の手法を完全に代替することはできませんが、アクセシビリティ改善の相談相手として有用である可能性が高いです。今後、プロンプトの改善やモデルのアップデートにより、より精度の高い分析が期待されます