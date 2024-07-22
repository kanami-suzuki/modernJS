### Viteとは
- 2020年にリリースされたフロントエンドのビルドツール
- Vue.jsの開発者であるEvan You氏が開発
- Vueだけでなく、React等様々な環境で利用可能な汎用的ツール
- フランス語で「速い」を意味する言葉で、その名の通り実行スピードが速いことが特徴

### Vite初期設定 
1. Viteを検索[https://ja.vitejs.dev/](https://ja.vitejs.dev/)
2. ページ内の「ガイド」をクリック
3. 「最初の Vite プロジェクトを生成する」の項目で、今回はnpmから制作する
4. npmのコマンドをコピー(npm create vite@latest)「npmで、viteを作成(create)するという意味」
5. ターミナルでViteを作成するディレクトリに移動し、コピーしたコマンドをペーストし、エンターキーを押す
6. viteの最新バージョンをインストールするかと聞かれるので、インストールする場合は「はい」を意味する「y」を入力してエンターキーを押す
7. プロジェクト名をどうするかを聞かれるので、変更しない場合はそのままエンターキーを押す(vite-projectになる)
8. フレームワークはどうするか聞かれるので、使用するフレームワークを矢印キーで選択し、エンターキーを押す
9. TypeScriptかJavaScriptかを聞かれるので使用する方を矢印キーで選択し、エンターキーを押す
10. 選択したフォルダ内にViteのプロジェクトが作成される
11. ターミナル上に表示される「Done. Now run:」以下のコマンドを実行する
12. 「cd vite-project」でvite-projectディレクトリに移動
13. vite-projectディレクトリで「npm install」コマンドを実行
14. vite-projectディレクトリの中に「node_modules」フォルダが作成される
  - Viteをインストールした段階で設定ファイルとして「package.json」ファイルが作成されている
  - 「npm install」コマンドを実行その「package.json」ファイルの中に記述されていることを読み込んでViteに関連するモジュールがインストールされる
  - 今後フレームワークやプラグインをインストールすると、「node_modules」フォルダにインストールしたものが追加されていく
15. 「npm run dev」コマンドを実行する。URLをブラウザで表示して「Hello Vite!」の画面が出てきたら環境構築は成功
  - 「package.json」ファイルのscriptプロパティのキー("dev"や"build"など)を「npm run ~」の~に入れることで、値の命令が実行される
  - 主に使用するのが「npm run dev」コマンドで、実行するとlocalhost(仮想サーバー)を立ち上げることができる(Live Serverのようなもの)
16. localhostを止めるときは「⌘ + C」で止まる

### モジュールをインストール
- JSの「Carouselライブラリ」をインストールする。Viteとnpmを使用すると、ライブラリを個々にダウンロードしなくてもnpmでインストールするだけで使用することが可能になる
1. ブラウザに表示した時に初期で記述されているViteの部分は不要なため、main.jsファイルの「import javascriptLogo」以下を削除する
2. スライダーライブラリの「[Splide](https://ja.splidejs.com/)」にアクセスする
3. 「はじめる」ボタンをクリック
4. NPMでのインストールをコピー
5. vite-projectディレクトリ上でコピーしてきたnpmをペーストし、Enterキーを押す
6. package.jsonにsplideの記述が追加される
7. node_modulesフォルダにもsplideフォルダが追加される
8. vite-projectディレクトリ直下のHTMLファイルにスライダーのHTMLを記述
9. main.jsに「Splideの適用」以下の「import文による導入」部分の記述をコピー&ペーストする
10. スタイルを当てるためにmain.jsの「new Splide」より上に「バンドラがCSSに対応している場合は〜」の下のimportをコピー＆ペーストする
11. 状況に応じでカスタマイズする

- sassをインストールする
1. sassの[npmインストールページ](https://www.npmjs.com/package/sass)にアクセスする
2. npmでのインストールをコピー
3. 「npm i sass」(iはinstallの略)コマンドを実行
4. vite-projectディレクトリの中にscssファイルを作成し、中身を記述
5. main.js内に「import './ファイル名.scss'」と記述
6. ブラウザに反映されれば成功

### package.json
- 設計図みたいなもの
- 他のエンジニアにコードを渡すとき、「node_modules」ディレクトリを渡すと膨大なデータ量になってしまう
- package.jsonのあるディレクトリで「npm install」コマンドを入力すれば、package.jsonに記述されているフレームワーク等を読み込んでインストールし、「node_modules」ディレクトリを作成してくれる
- そのため、他のエンジニアに共有するときはpackage.jsonファイルを渡してインストールしてもらう方が効率的
- また、「node_modules」ディレクトリがうまく動作しない時も一度「node_modules」フォルダを削除して、「npm install」コマンド実行し、再インストールすると解決することがある
- importやfrom等を使用すると、npmでインストールしたnode_modulesにあるファイルを読み込むことができる

### npmの検索
- npmモジュールとして公開されているライブラリは下記のサイトから全て検索できる
- [Build amazing things](https://www.npmjs.com/)