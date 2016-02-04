# concrete5 Coding Guideline (5.7.x)

Switch branch for different language and versions.

- コーディングガイドライン (5.7.x 以降)
- concrete5.7.5.6 対応
- 更新 2016/2/4
- Authored by Katz Ueno (コンクリートファイブジャパン株式会社)
- GitHub: https://github.com/katzueno/concrete5-Coding-Guideline


<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a>

Pull requests are welcomed!
ガイドラインの誤字・脱字の修正、編集の提案などプルリクエストをお待ちしております。

## Translations / 翻訳

言語 | URL
----|----
English (英語) | https://github.com/katzueno/concrete5-Coding-Guideline/tree/english
Japanese (日本語) | https://github.com/katzueno/concrete5-Coding-Guideline/tree/japanese




# 本コーディングガイドラインについて

## 趣旨

HTML+CSS+JS の知識を持ったエンジニアが、クライアントワークで concrete5 のオリジナルテーマを作成する際、元となるコーディングを作成することが一般的です。そのコーディングを concrete5 の親和性を高めるためのコーディングガイドラインです。

concrete5 はフロントのページ上で編集可能な CMS です。

それは、編集ができるような管理系のインタフェースが、表のページにも出力されます。そうすると、自作 concrete5 テーマと、concrete5 の編集管理をするインターフェースがコンフリクトを起こさないようにする必要があります。

このコーディングガイドラインは、コンクリートアイブジャパン株式会社が、自身が行っている受託案件のために、パートナー企業にお見せしているコーディングガイドラインを一般公開しているものです。コンクリートファイブジャパン株式会社では、企業・団体様の concrete5 サイト制作や制作会社様のプロジェクトのサポートを行っています。


## ターゲット＆想定シーン

このコーディングガイドラインは下記の方をターゲットにしています。

- HTML + CSS + JS の知識がある
- concrete5 の基本的な知識がある
- お客様が希望するオリジナルデザインをベースに concrete5 テーマの作成をする
- デザインは PSD や AI で提供され、コーディングを行う

またデザインの時点でも、コーダーの方が逐一、コーディングが可能かどうかの確認もされることをおすすめします。

## ライセンス

このコーディングガイドラインは クリエイティブ・コモンズ 表示 4.0 国際 ライセンスの下に提供されています。

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a>

このガイドラインを使用することにより、いかなる損害が発生したとしても、コンクリートファイブジャパン株式会社は責任を負わないことを同意したとみなします。


## お断り

このガイドラインは、あくまでも指針として提供しているものです。月日の変化により、コーディングのベストな方法は常に変わり続けます。

このガイドラインのご利用されることにより、いかなる損害が発生したとしても、コンクリートファイブジャパン株式会社、および他の作者は一切の責任を負いません。


## クレジット

- Katz Ueno (concrete5 Japan, Inc) - http://concrete5.co.jp
- Remo Laubacher (Ortic Solutions GmbH) - http://www.ortic.com



# 本プロジェクトの仕様 (例)

プロジェクトのコーディングの基本的な仕様を記入する例を書いておきます。

## 基本仕様 (例)

項目 | 内容
----|----
テーマハンドル | ***
使用フレームワーク | Bootstrap / Foundation / 960Grid / オリジナル


## 使用ライブラリとバージョン (例)

プロジェクトで使用するライブラリとバージョンを記入してください

使用ライブラリ | バージョン
---- | ---
Bootstrap | 3.1.1
jQuery | 1.11.1
Bxslider | TBA


## ページテンプレートリスト (例)

Body Wrapper Class で出力を変更したいときに対応表として利用してください

名前 | ハンドル
--- | ---
p0_0 総合トップ | p0_0_top
p0_1 事業部トップ | p0_0_top_dept
p1_0 汎用 | default
p2_0 製品トップ | p2_0_product_top
p2_1 製品一覧 | p2_1_product_index
p2_2 製品詳細 | p2_1_product_detail

* 半角英大文字、半角英小文字、半角数字とアンダースコア(_)のみが使用可能です。
* アンダースコアー(_) は、Body Wrapper Class として出力されるときに、 **ハイフン(-) に自動変換** されます

## ページタイプリスト (例)

Body Wrapper Class で出力を変更したいときに対応表として利用してください

名前 | ハンドル | 使用ページテンプレート
--- | --- | ---
pt0_0 総合トップ | pt0_0_top | p0_0_top
pt0_1_1 ○事業部トップ | pt0_0_1_top_XX_dept | p0_0_top_dept
pt0_1_2 ○事業部トップ | pt0_0_2_top_XX_dept | p0_0_top_dept
pt0_1_3 ○事業部トップ | pt0_0_3_top_XX_dept | p0_0_top_dept
pt1_0_1 汎用一覧 | default_index | default
pt1_0_2 汎用詳細 | default_page | default
pt2_0 ライブラリトップ | pt2_0_product_top | p2_0_product_top
pt2_1_1 製品一覧 XXX | pt2_1_1_product_index_XXX | p2_1_product_index
pt2_1_2 製品一覧 XXX | pt2_1_2_product_index_XXX | p2_1_product_index
pt2_1_3 製品一覧 XXX | pt2_1_3_product_index_XXX | p2_1_product_index
pt2_2_1 製品詳細 XXX | pt2_1_1_product_index_XXX | p2_1_product_detail
pt2_2_2 製品詳細 XXX | pt2_1_2_product_index_XXX | p2_1_product_detail
pt2_2_3 製品詳細 XXX | pt2_1_3_product_index_XXX | p2_1_product_detail


* 半角英大文字、半角英小文字、半角数字とアンダースコア(_)のみが使用可能です。
* アンダースコアー(_) は、Body Wrapper Class として出力されるときに、 **ハイフン(-) に自動変換** されます


# 基本規則

- 文字コードは UTF-8 を使用
- 改行コードは LF (UNIX互換) を使用


# ファイルやアセットの保存場所

concrete5 では、テーマ関連のファイルを下記フォルダに保存しています。

バージョン | 保存先
--- | ---
concrete5.6.x | /themes/XXX/
concrete5.7.x | /application/themes/XXX

* XXX はテーマの識別ハンドル
* 半角英小文字と数字のみにしてくだい。英語大文字は使えません。
* 上記保存場所は自作テーマを保存する先です。パッケージ化をする場合は、「packages/XXX/themes/XXX/」以下となります。


## テーマ埋め込みのCSS, JS, 画像ファイルの保存場所

コーディングを行う時点で、テーマに埋め込む CSS や JS 画像ファイルは

- /application/themes/XXX/css/
- /application/themes/XXX/js/
- /application/themes/XXX/images/

や

- /application/themes/XXX/assets/css/
- /application/themes/XXX/assets/js/
- /application/themes/XXX/assets/images/

などとまとめられることを推奨します。（assets フォルダにまとめる後者をより推奨します。）


## HTML コーディング

HTML コーディングもモックアップなどは

- /application/themes/XXX/html/

配下に設置し、同じ、css, js, 画像ファイルを読み込むように設定するとデバッグが用意になります。


# ライブラリについて

各バージョンのconcrete5 に同梱しているライブラリです。
同じライブラリを使用する場合は下記のバージョンを使用してください。

**特に jQuery は concrete5 と密接に関わり合っているので、競合する JavaScript を利用する際は、最新の注意を払ってください。**

ライブラリ名 |c5.6.3.3| c5.7.3.1 | c5.7.5.2 | c5.7.5.3 | c5.7.5.6
----- | ---- | ----- | ----- | ----- | -----
ace | N/A | 1.1.8 | 1.2.0 | 1.2.2 | 1.2.2
backbone | TBA | TBA | TBA | TBA | 1.1.2
backstretch | TBA | 2.0.4 | 2.0.4 | 2.0.4 | 2.0.4
bootstrap | 2.0.3 | 3.1.1 | 3.1.1 | 3.1.1 | 3.1.1
dropzone | N/A | 4.0.1 | 4.1.0 | 4.2.0 | 4.2.0
dynatree | N/A | 1.2.6 | 1.2.8 | 1.2.8 | 1.2.4
font-awesome | N/A  | TBA  | 4.2.0 | 4.2.0 | 4.2.0
html5shiv | N/A  | N/A | 3.7.2 | 3.7.2 | 3.7.2
respond | N/A  | N/A | 1.4.2 | 1.4.2 | 1.4.2
jquery | 1.7.2 | 1.11.1 | 1.11.3 | 1.11.3 | 1.11.3
jquery/awesome-rating | N/A | TBA  | 0.1.1 | 0.1.1 | 0.1.1
jquery/cookie |  N/A | 1.4.1 | 1.4.1 | 1.4.1 | 1.4.1
jquery/fileupload |  N/A | TBA | 5.39.0 | 5.39.0 | 5.39.0
jquery/form |  N/A | TBA | 2.87 | 2.87 | 2.87
jquery/live-update |  N/A | TBA | TBA | TBA | TBA
jquery/magnetic-pop-up |  N/A | TBA | TBA | 1.0.0 | 1.0.0
jquery/mousewheel |  N/A | TBA | TBA | 3.1.12 | 3.1.12
jquery/pep |  N/A | TBA | TBA | TBA | TBA
jquery/placeholder |  N/A | TBA | TBA | 2.0.8 | 2.0.8
jquery/textcounter |  N/A | N/A | N/A | N/A | 0.3.4
jquery/tristate |  N/A | TBA | TBA | TBA | TBA 
jquery/touch-punch | N/A | TBA | 0.2.3 | 0.2.3 | 0.2.3
jquery/ui | TBA | 1.10.3 | 1.11.4 | 1.11.4 | 1.11.4
jquery/visualize | N/A | TBA | TBA | TBA | TBA
kinetic | N/A | TBA | 4.7.2 | 4.7.2 | 4.7.2
Modernizr | N/A | TBA  | 2.8.3 | 2.8.3 | 2.8.3
packery | N/A | TBA | TBA | 1.0.2 | 1.0.2
picturefill | N/A | TBA | 2.3.1 | 2.3.1 | 2.3.1
redactor | N/A | TBA | 10.2.1 | 10.2.1 | 10.2.1
select2 | N/A | TBA | 3.5.1 | 3.5.1 | 3.5.1
spectrum | N/A | TBA | TBA | 1.3.4 | 1.3.4
swfobject | N/A | TBA | TBA | TBA | 2.1
TinyMCE | 3.5.11 | N/A | N/A | N/A | N/A
underscore | N/A | TBA | 1.6.0 | 1.6.0 | 1.6.0

- N/A: そのバージョンの concrete5 パッケージに入っていないライブラリ
- TBA: バージョン番号を調査中、もしくは不明

これらのライブラリをテーマで使用したり、使用しない場合 concrete5 の実装時に設定する必要があります。設定は下記のドキュメントを参考にしてください。

- [コアのJavascriptとCSSをテーマで使用する](http://concrete5-japan.org/help/5-7/developer/designing-for-concrete5/advanced-css-and-javascript-usage/requiring-core-javascript-or-css-in-a-theme/)
- [コアのJavascriptやCSSをテーマから上書きする](http://concrete5-japan.org/help/5-7/developer/designing-for-concrete5/advanced-css-and-javascript-usage/overriding-or-providing-core-javascript-or-css-in-a-theme/)
- [elementalのpage_theme.php](http://acliss.secret.jp/private-blog/acliss-blog/2015/12/12/elemental%E3%81%AEpage_theme/)


# CSS/JS フレームワーク

レスポンシブデザインなどを行う場合 concrete5 では下記のフレームワークに対応しています。

- Bootstrap
- Foundation
- 960Grid

どのフレームワークを決めかねている場合は Bootstrap をお使いください。concrete5.7.x のブロックは、Bootstrap を中心に作られている場合があるため、concrete5 側での修正工数が少なくなるので、Bootstrap がおすすめです。

ただ concrete5 のバージョンによって concrete5 で使用している Bootstrap のバージョンが変わってくるので、ご注意ください。

Foundation をお使いの場合は UI の部分のハックが多少必要ですが、Bootstrap のバージョンには依存されません。


# CSS 関連事項

## 禁止 & 注意事項

### body タグ禁止事項

#### body に ID や class を付けない (必須)

ページのデザインを変えるために Body タグに ID や class をつけることはしないでください。

#### body に Position を設定しない (必須)

Body には Position を設定しないでください。

#### Body には背景の設定をしない (推奨)

背景の設定は避けてください。
下記の Body Wrapper クラスで背景を指定するようにしてください。


## ccm- クラスを使わない (必須)

ccm-page というクラスを除いて ccm-* というクラスは使用しないでください。これらは concrete5 が管理画面などのインターフェース用に使用しています。


## Body Wrapper クラス (必須)

concrete5.7.x では、下記の CSS クラスが組み込まれた `<div>` タグを `<body>` の開始直後と `</body>` 閉じタグの直前に挿入します。

- ccm-page
- page-template-XXX (XXX はページテンプレートのハンドル)
- page-type-XXX (XXX はページタイプのハンドル)

入れ子での CSS スタイルの適応を行う場合は、上記 class を活用できます。

高度な表現を行わない場合は、「page-template-XXX」や「page-type-XXX」のクラスは無視してコーディングを行ってください。

* ページテンプレートとページタイプのハンドルは半角英大文字、半角英小文字、半角数字とアンダースコア(_)のみが使用可能です。
* アンダースコアー(_) は、Body Wrapper Class として出力されるときに、 **ハイフン(-) に自動変換** されます
* ページタイプは「指定なし」が可能なため、page-type-XXX が出力されないパターンも想定可能です。


## HTML 要素や Bootstrap の基本 CSS に直接 CSS スタイルを割り当てない

concrete5 では、同じページ内に管理画面用のタグも出力します。

そのために、 a input タグや、Bootstrap の .btn や .btn-success などの class スタイルを .ccm-page を親要素を指定せずに宣言しないでください。

また、既存の HTML+CSS を concrete5 に移行する場合、LESS を使って .ccm-page の子要素としてまとめる方法もあります。

悪い例: 下記のような CSS を宣言しない

```
/* concrete5 の管理画面でも影響する HTML 要素 */
a { /* いろいろな CSS  */ }
input { /* いろいろな CSS  */ }

/* concrete5 の管理画面でも影響する Bootstrap のクラス */
.btn { /* いろいろな CSS  */ }
```

良い例1 : 下記のように .ccm-page の下に CSS を宣言する

```
/* Page Wrapper の中だけに影響する HTML 要素 */

.ccm-page a { /* いろいろな CSS  */ }
.ccm-page input { /* いろいろな CSS  */ }

/* Page Wrapper の中だけに影響する Bootstrap のクラス */

.ccm-page .btn { /* いろいろな CSS  */ }

```

良い例2 : LESS を使ってシンプルに実装する

```
/* Page Wrapper の中 に宣言する */

.ccm-page {

    a { /* いろいろな CSS  */ }
    input { /* いろいろな CSS  */ }
    
    .btn { /* いろいろな CSS  */ }

}

```

## Z-index について (必須)

Z-index は 1000 未満にしてください。

* concrete5.6.x は 5 未満


## ファイルのアップロード場所に依存しない (必須)

編集者が自由に画像をアップロードして使うような画像の場合、ファイルのアップロード位置に依存したコーディングは行わないでください。

- ユーザーが編集するブロック内部の画像はファイルマネーはーがランダムに生成したフォルダ内に格納されます。
- マイスオーバーで画像ファイル名の末尾に「_over」を付与する Javascript などは動作しません (* テーマ内にハードコーディングする場合を除きます)

## ブロックに ID を指定しない (強く推奨)

ブロックに ID を指定して表示するようなコーディングは避けてください。

## meta title, description, keywords, OGP タグ は不要 (推奨)

concrete5 側で挿入するため、不要です。


# コーディング必須事項

## ページ上に表示されるすべての表示パターンを網羅してください。

- 仕様書、デザインデータを元に、必要な表示パターンすべてをコーディングしてください。
- 例：画像の左寄せ、中寄せ、右寄せなどの複数パターンが想定される場合はそのすべてのパターンのコーディングを行ってください。

## トルツメの対応

- 要素が未入力の場合、トルツメにすることによって表示が崩れるようにしないでください。
- 例：ページリストのサムネイル画像がない場合、ページタイトルの表示部分が崩れないようにする。

## 繰り返し表示予定の箇所の対応

- 同じ要素を繰り返し出力する箇所では、要素の増減により、表示崩れなどが発生しないようにしてください。
- グリッド表示を行う場合、横1列、縦1列ごとに div で囲むような入れ子処理はせずに、そのブロック全体で div を囲むようにしてください。
- 必ず繰り返した状態でコーディングしてください
- 必要であれば、要素が全くない状態を考慮してください。場合によっては別のコーディングを出力する必要がある場合があります。カスタマイズで対応できるので、事前に concrete5 実装者と可能かどうか相談してください。
    - 例：0個の時、トルツメにするのか別の表示にするのか
    - 例：1個のとき、 スライドショーで自動再生をするが、画像が1個しかないとき自動再生があるため同じ画像でエフェクトが繰り返されてしまう場合の対処

## 繰り返し要素の高さなどのサイズの考慮

- グリットデザインなど縦の位置を他の要素と合わせないといけない場合は、できれば JS などで縦の高さを調整するように設定してください。
- 不可能であれば横1列ごとに1つのブロックを追加するように対処するので運用を検討してください。
- 例：グリット表示のページリストで、サムネイル画像、日付、ページタイトルの3要素が横に並んでいる場合、ページタイトルの長さによって高さが変わって、縦の長さが不揃いになり表示崩れが起きてしまう。。


## テキストの増減への対応

入力文字数が増減することを想定して、表示崩れが起きないようにしてください。

- 例：画像の回り込みの増減で、少ない時に clearfix がないため、次の要素とかぶる
- 例：ページリストで、サムネイル画像、日付、ページタイトルの3要素が横に並んでいる場合、ページタイトルが2行になる時に、表示崩れが起きてしまう。

## ページ上部FIXメニューや、アンカーリンクの編集モード時の配慮

concrete5 では、編集権限があるユーザーが concrete5 サイトに入ると、上部に 49px の編集バーを表示します。この時、ページ内アンカーリンクや、グローバルナビゲーションメニュー等を上部に固定して表示している場合、 **編集バーの後ろに隠れてしまう** 場合があります。

その場合は concrete5 実装時、編集バーを表示している時だけ特別に編集バーの後ろに隠れてしまう要素をなくすよう、特別な設定を header 部分に記述する準備をしてください。

例
```
<?php $cp = new Permissions($c); if($cp->canViewToolbar()){?>
    <style media="screen">
        .header {top:48px;}
        /* 他 CSS ファイル */
    </style>

    <script type="text/javascript">
        /* スムーススクロールの追加設定など */
    </script>
    
<?php } ?>
```


# コーディング奨励事項

## ブロックのコーディングが、ブロック単位でデザインが再現し、できるだけ汎用的になるようにしてください

- ブロックはエリアに自由に配置できます (上級権限モードなどで制限は可能)
- そのエリアだけにしか使えないようにするなど、ブロック外の class から継承するようなことは避けてください。(ただし、ヘッダー、フッターなど背景色が違う場合などの特定の場合を除く)

## BEM (Block Elements Modifier)

ページの枠をコーディングする際、BEM のコンセプトに基づいてコーディングをされることを推奨します。

参考記事
https://app.codegrid.net/entry/bem-basic-1


## LESS の使用

concrete5.7.x では、LESS のコンパイラーを内蔵しています。
HTMLコーディングを確認する際は、コンパイルが必要ですが、concrete5 ではコンパイルが必要ありません。

CSS プリプロセッサーを使用する際は LESS を採用されることをおすすめしますが、必須ではありません。

# 各ブロックのコーディング仕様

## 記事ブロック

記事ブロックは Redactor という JS ライブラリを使用して、下記記事ブロックサンプルのコードを出力するようにできています。 class や ID なしの HTML タグが出力されるため、きちんと CSS を出力するために、下記の2パターンで対応して頂く必要があります。

### デフォルト

囲む div など何もなしで挿入されます。
その場合は、エリアの前後に class を囲むなどして、CSS の適用がきちんとされるよう調整することをおすすめします。

### 推奨：

記事ブロックは一つのブロック全体を `<div class="wysiwyg"></div>` で囲むようにして中身のタグはなにも class を指定しないようにしてください。この場合、記事ブロックのオーバーライドのカスタマイズが必要になります。

どうしても任意の class やID の指定が必要な場合や `<span>` を間に挟まないといけないような場合は、更新者が HTML のコードを直接変更してでクラスをつけるリテラシーがある場合や、一定の法則があれば JS で対応するようにしてください。

下記が、記事ブロックから排出した HTML コーディングのサンプルです。
下記のコードを参考に CSS の調整をしてください。もしくは、実際に concrete5 サイト上で、記事ブロックを作成し、考えられるパターンのコーディングを作成し、コーダーに渡してください。


```html
<div class="wysiwig"> <!-- この div タグは concrete5 標準ではありませんがコンクリートファイブジャパンが推奨する方法です。記事ブロックをオーバーライドする必要があります。-->
    <p>P</p>

    <h1>H1</h1>

    <blockquote>
        Blockquote
    </blockquote>

    <p><strong>Strong</strong></p>

    <p><em>Italic</em></p>

    <p><u>Underscore</u></p>

    <p><del>Strikethrough</del></p>

    <p>UL&nbsp;List</p>

    <ul>
        <li>UL List</li>

        <li>UL List</li>

        <li>UL List</li>
    </ul>

    <p>OL List</p>

    <ol>
        <li>OL List</li>

        <li>OL List</li>

        <li>OL List</li>
    </ol>

    <p>No&nbsp;Indent</p>

    <p style="margin-left: 20px;">1 Indent</p>

    <p style="margin-left: 40px;">2 Indent</p>

    <p>Image</p>

    <p><img src="/index.php/download_file/view_inline/1"></p>

    <p>Align Left</p>

    <p>Align Right</p>

    <p>Table</p>

    <table>
        <thead>
            <tr>
                <td>Head</td>

                <td>Head</td>

                <td>Head</td>
            </tr>
        </thead>

        <tbody>
            <tr>
                <td>1</td>

                <td>2</td>

                <td>3</td>
            </tr>

            <tr>
                <td><p>セルの中に複数行のテキストを入れると</p>
                <p>このように p タグが入ります。</p></td>

                <td><p>セルの中に複数行のテキストを入れると</p>
                <p>このように p タグが入ります。</p></td>

                <td><p>セルの中に複数行のテキストを入れると</p>
                <p>このように p タグが入ります。</p></td>
            </tr>
        </tbody>
    </table>

    <p><a href="/index.php?cID=1" data-concrete5-link-type="ajax">Internal Link</a></p>

    <p><a href="/index.php/download_file/view/1" data-concrete5-link-type="image" data-concrete5-link-launch="lightbox-image">Light box Link - Image</a></p>

    <p><a href="/index.php?cID=1" data-concrete5-link-type="ajax" data-concrete5-link-launch="lightbox-image">Light box Link - AJAX</a></p>

    <p><a href="/index.php/download_file/view/1" data-concrete5-link-type="image">File Download Link</a></p>

    <p>Align Text to the Left</p>

    <p style="text-align: center;">Center text</p>

    <p style="text-align: right;">Align text to the right</p>

    <p style="text-align: justify;">Justify Text</p>
    <hr>

    <p><span style="color: rgb(192, 80, 77);">Font color</span></p>
</div>
<!-- この div タグは concrete5 標準ではありませんがコンクリートファイブジャパンが推奨する方法です。記事ブロックをオーバーライドする必要があります。-->
```

## HTMLブロック

### デフォルトでの使用

HTML ブロックはデフォルトでは

`<div id="HTMLBlockXXX" class="HTMLBlock">`

という、ブロックの識別数字がついた ID と HTMLBlock という Class を div で囲って表示します。

### 推奨方法

HTML ブロックは、そのまま生のコードを出力したい場合が多いため、
HTML ブロックのデフォルトの view をオーバーライドして、1個1個の HTML ブロックに div が囲まれないようにするのも良いです。

## オートナビ

ul li で構成するナビゲーションブロックです。

- 階層で分けることが可能
- グローバルナビなどで使用
- メガメニュー表示なども追加カスタマイズで可能
- パンくずの表示も可能

ul のレベルに応じて、div や span などを新たに囲むことも可能です。
ただし、閉じタグなどのパターンを考えるときに複雑になりかねないので、ul li のみで構成できるように極力努力してください。。

## ページリスト

表示できる要素

- ページタイトル
- 日付
- サムネイル画像
- その他任意のページ属性
    - トピックラベル
    - 選択肢など

ブロック全体を大きく div で囲み、ひとつのページ情報に対して一つの繰り返し要素としてコーディングする。


### ページ送りのコーディングについて

ページ送りについては、特定のコーディングで対応することが必要。
ただしカスタマイズにより自由度の高いページ送りのコーディングが可能です。

#### デフォルトで出力されるページネーションのサンプルについて

下記サンプルコードです。 ul li を使用します。

```html
<div class="ccm-pagination-wrapper">
    <ul class="pagination">
        <li class="prev disabled"><span>&larr; 前へ</span></li>
        <li class="active"><span>1 <span class="sr-only">（このページ）</span></span></li>
        <li><a href="#">2</a></li>
        <li><a href="#">3</a></li>
        <li><a href="#">4</a></li>
        <li><a href="#">5</a></li>
        <li><a href="#">6</a></li>
        <li><a href="#">7</a></li>
        <li class="disabled"><span>&hellip;</span></li>
        <li><a href="#">23</a></li>
        <li class="next"><a href="#">次へ &rarr;</a></li>
    </ul>
</div>
```

Boostrap 3 ベースでの出力サンプルです。

##### 1. div wrapper

`<div class="ccm-pagination-wrapper">` で囲ってください。

##### 2. ul

`<ul class="pagination">` で囲ってください。

##### 3. 「前へ」

前へリンクは

`<li class="prev disabled"><span>&larr; 前へ</span></li>`

- 「prev」クラスが付きます
- リンクがないときは「disable」クラスが付きます。(表示しないという設定の場合は CSS で調整ください)
- 「`<span></span>`」が付きます。
- 「`&larr; 前へ`」の部分は変更可能です

##### 4. ページ番号部分部分：基本形

`<li><a href="#">7</a></li>`

- list タグ
- a リンク
- ページ番号数字

です


##### 5. ページ番号部分部分：そのページの場合

基本形

`<li class="active"><span>○○ <span class="sr-only">（このページ）</span></span></li>`

- list タグに active というクラスが付きます
- span タグを間にはさみます
- 「`<span class="sr-only">（このページ）</span>`」はデフォルトの表記です。現ページであることを示すための任意コーディングを挿入できます。なにもなしでも可能です。

##### 6. ページ番号部分部分：省略しているところ


`<li class="disabled"><span>&hellip;</span></li>`

- li タグで disabled クラスがあります
- `<span>&hellip;</span>` で「・・・」を表示しています


##### 7. 「次へ」

`<li class="next"><a href="#">次へ &rarr;</a></li>`

- list タグ
- next クラスが付きます
- リンクがないときは disabled などクラスをつけます。(表示しないという設定の場合は CSS で調整ください)
- 「`次へ &rarr;`」がデフォルトですが、変更が可能です。

#### CSS ファイルについて

ページリストブロックは、ページネーションが追加されると自動的に下記のファイルを読み込みます。

/concrete/css/frontend/pagination.css

しかし、自分でページネーションの CSS を作成したい場合は、concrete5 実装時に下記のいずれかの方法で解除してください。

**1. page_theme.php で読み込まないように設定する**

例

```
<?php
public function registerAssets() {
    $this->providesAsset('css', 'core/frontend/pagination');
}
```

page_theme.php の registerAssets() に上記の1行を追加するとOKです。

**2. /concrete/css/frontend/pagination.css を上書きする**

`/application/css/frontend/pagination.css` という CSS ファイルを作成し、
ページネーション関連の CSS はそちらに記入するようにすることが可能です。

**3. /concrete/blocks/page_list/controller.php を上書きする**

あまりおすすめしませんが、上記ファイルを /application/blocks/page_list/controller.php にコピーし、

`$this->requireAsset('css', 'core/frontend/pagination');`

という行を削除かコメントアウトしてください。

#### ページネーションの出力自体をカスタマイズする方法

ページネーションの出力コーディングを変更したい場合は、下記を参照してください。

 - [ページリストブロックのページ送りのカスタマイズ](http://concrete5-japan.org/help/5-7/recipes/customize-pagination/)



## イメージスライダー

表示できる要素

- 画像
- タイトル
- WYSIWYG (記事ブロック)
- リンク

ページリストブロックのコーディング方法と基本的に同じ。
JS ライブラリを使う場合は、concrete5 標準JSライブラリとコンフリクトを起こさないようにする。

ブロック内でサムネイル画像一覧を表示し、画像のページ送りなどを行う場合は、ブロック側ではサムネイル画像を全部表示し、画像送り部分は JS で処理する。(例: http://memocarilog.info/memocarilog-demo/galleriffic-demo/ )

## 画像ブロック

デフォルトでは下記のようなコードが出力されます。

```html
<picture>
    <!--[if IE 9]><video style='display: none;'><![endif]--><!--[if IE 9]></video><![endif]-->
    <img src="/index.php/download_file/view_inline/1" alt="#" class="ccm-image-block img-responsive bID-XXXX">
</picture>
```

* 'bID-XXXX' のところはブロックIDが入ります。


## FAQ ブロック

要素(作成中)

- ナビゲーションリンクテキスト
- タイトル(テキストのみ)
- WYSIWYG (記事ブロックと同じ)

## ページタイトルブロック

作成中

## 属性ブロック

作成中

## YouTube ブロック

作成中

## Google Map ブロック

作成中
