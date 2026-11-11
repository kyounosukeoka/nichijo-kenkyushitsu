# 日常研究室 Ver.3.0 — 冬の書斎（GitHub Pages版）

スマホ優先の観察記録Webアプリです。HTML/CSS/JavaScriptだけで動作します。

## GitHub Pagesで公開する
1. GitHubで新しいリポジトリを作成します。GitHub Freeでは通常、Pages公開に公開リポジトリを使います。
2. このフォルダ内のファイルとサブフォルダを、そのリポジトリのルートにアップロードします。`index.html` がルート直下にあることを確認してください。
3. リポジトリの Settings → Pages → Build and deployment → Source: Deploy from a branch を選択。
4. Branch: main、フォルダ: /(root) を選択して Save します。
5. 表示される公開URL（`https://ユーザー名.github.io/リポジトリ名/`）から開きます。

※ リポジトリを公開するとアプリのソースコードは誰でも閲覧できるため、パスワードや個人のJSONバックアップをリポジトリにコミットしないでください。

## ファイル構成
- index.html : HTML画面
- css/style.css : 冬の書斎のデザイン、ダイアログ、スマホ対応
- js/app.js : 観察・保存・疑問ツリー・写真描画・地図・JSONバックアップ
- assets/icon.svg : アンティーク手帳 × 羽ペン × 雪の結晶
- assets/icon-192.png, icon-512.png : ブラウザ／ホーム画面用アイコン
- manifest.webmanifest : Webアプリアイコン等の表示情報

## 新しい操作
- メニュー右端「＋ 観察」→「通常モード」または「今すぐ観察」
- 今すぐ観察：日時と仮タイトルを自動で作成し、「気づいたことを記録」をすぐに開きます。
- 「記録する」で観察内容を続けて記録できます（入力画面に留まります）。今すぐ観察で撮った最初の写真は自動で一覧のサムネイルになります。
- 「観察を終えて、名前を付ける」で観察タイトルと場所を後付けできます。
- 「設定」から「今すぐ観察」の自動位置情報取得のオン／オフを変更できます。
- 「気づいたことを記録」は写真添付が先頭です。
- クラウド同期はありません。保存はブラウザのIndexedDBのみです。
- 設定 → バックアップを書き出す／復元する でJSONを管理できます。

## 旧Netlify版から記録を移動する（重要）
1. 旧Netlify版の日常研究室の「設定」でJSONをエクスポートします。
2. 新GitHub Pages版の「設定」→ JSONバックアップ → JSONファイルを選択し「復元する」。
3. 観察件数・写真・メモなどが正しく引き継がれたか確かめます。

GitHub Pagesの公開URLとNetlifyの公開URLでは保存領域が異なり、データは自動で移動しません。
JSONファイルには写真・観察場所・位置情報が入る可能性があるので、GitHubリポジトリにアップロードしないでください。

## 注意事項
- GitHub Pagesはアプリファイルの公開先であり、記録のクラウド保存サービスではありません。
- IndexedDBはブラウザ・端末・サイト単位です。ブラウザを変更したりデータを削除したりすると記録が見えなくなる場合があります。定期的にJSONを保存してください。
- GitHub PagesはHTTPSで配信され、位置情報取得が利用可能ですが、ブラウザの権限と端末の設定が必要です。
- 地図表示はLeafletとOpenStreetMapをインターネット経由で読み込みます。オフライン表示は保証していません。
- 別端末間の自動同期はありません。

参考：GitHub Pages公式手順 https://docs.github.com/ja/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
