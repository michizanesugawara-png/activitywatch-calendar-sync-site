ActivityWatch Calendar Sync | Google OAuth向け公開ページ
====================================================

ファイル構成
  index.html             ホームページ
  privacy.html           プライバシーポリシー
  terms.html             利用規約
  assets/styles.css      デザイン
  assets/icon.svg        サイトアイコン（OAuthアプリのロゴとしてアップロードしない）
  .nojekyll              GitHub Pages用

GitHub Pagesでの無料公開手順（既存のGitHubユーザー名: michizanesugawara-png）
1. https://github.com/new にアクセス
2. Repository name を「activitywatch-calendar-sync-site」にして、Publicを選び作成
3. リポジトリ画面 > Add file > Upload files で本ZIP内のファイルをアップロード
   注意：assetsフォルダも含めること。HTMLファイルを単にクリックしてページ公開しただけではありません。
4. Settings > Pages > Build and deployment > Source を Deploy from a branch
5. Branch を main、Folder を /(root)に設定し、Save
6. 公開先（予定）:
   https://michizanesugawara-png.github.io/activitywatch-calendar-sync-site/
   https://michizanesugawara-png.github.io/activitywatch-calendar-sync-site/privacy.html
   https://michizanesugawara-png.github.io/activitywatch-calendar-sync-site/terms.html
7. 実際にページが公開され、プライベートウィンドウでも閲覧できることを確認

Google Search Console所有権確認の候補手順
1. https://search.google.com/search-console を開く
2. URLプレフィックスとして公開したサイトURLを登録
3. 「HTMLファイルをアップロード」からgooglexxxxxxxx.htmlを取得
4. そのファイルを、公開サイトのリポジトリのルートにアップロード
5. 公開URLで検証ファイルが見えることを確認してSearch Console側で確認

Google Auth Platformのブランディング入力
アプリ名: ActivityWatch Calendar Sync
ホームページURL: 上記ホームページの実際に公開できたURL
プライバシーポリシーURL: 上記privacy.htmlの実際に公開できたURL
利用規約URL: 上記terms.htmlの実際に公開できたURL
ユーザーサポートメール: nikonikokoshii@gmail.com
承認済みドメイン: Google Cloud側に要求される登録可能なドメイン

★重要な制限★
GitHub Pagesの*.github.ioは共有ホスティングドメインです。
Google公式は、自分が所有権検証できない共有ドメインをOAuth本番アプリの
ホームページとして使うことを推奨していません。
この無料サイトはGoogle側で拒否される場合があります。
Search ConsoleのURLプレフィックス確認に成功しても、OAuth側の承認が保証されるわけではありません。
もし拒否された場合は、独自ドメインを取得してDNSレベルで所有権を検証し、
同じサイトファイルを独自ドメインでホストしてください。

★公開前の確認★
・サポート用メールアドレスnikonikokoshii@gmail.comがprivacy.htmlとterms.htmlで公開されます。
・ドキュメントの記述は今回のローカルGoogle Calendar -> ActivityWatch同期ツール
  （google_calendar_to_aw.py v2）の挙動に合わせて作っています。ツールを改変するなら文章も修正。
・credentials.json、token-google-calendar.json、ActivityWatchのバックアップ等は
  絶対に公開リポジトリへアップロードしないでください。
・Google OAuthの認証ファイルやトークンをこのサイトへ配置する必要はありません。
・GitHub Pagesのサイト公開はこのZIPの作成だけでは完了していません。
・Googleの個人利用・非公開審査の例外と、公開ステータスを本番に切り替える際の
  入力要件は別です。Googleの設定・判定結果に従ってください。

作成日: 2026-11-01
