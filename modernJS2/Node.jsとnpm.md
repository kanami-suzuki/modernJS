### Node.js
- JavaScriptをサーバーサイドで実行するためのツール

### npm　
- モジュールを管理するためのツール

### Homebrew
- MacまたはLinuxのパッケージマネージャー
- Homebrewを使うことによってPythonやNode.jsといったパッケージ等がインストールできる

### nvm
- Node Version Manager(ノード・バージョン管理ツール)の意味
- 一つのシステム内に複数のバージョンのNode.jsをインストールでき、必要に応じてバージョンを切り替えて使用することができる
- Node.jsはたくさんのバージョンがリリースされているため、nvmで管理することでNode.jsのバージョン管理が簡単になる

- インストール後、必要な工程
  - ホームディレクトリに.nvmというディレクトリが存在しなければ作成する
  - 「open ~/」コマンドでホームディレクトリを開いて確認
  - なければ「mkdir ~/.nvm」コマンドで作成
  - 同じく「zshrc」ファイルがあるかを確認し、なければ「touch ~/.zshrc」コマンドで作成
  - ファイル作成後.zshrcファイル内に「Add the following to your shell〜」の下の「export〜# This loads nvm bash_completion」をファイル内にペースト
  - 「nvm -v」コマンドでバージョンを確認
    - 「command not found: nvm」が出てくる場合
    - まず「source ~/.nvm/nvm.sh」と入力して再度バージョン確認
    - 「nvm:854: no such file or directory: /Users/suin/.nvm/nvm-exec」が出てくるようであればリンクを作り直す
      1. mkdir -p ~/.nvm
      2. cd ~/.nvm
      3. ln -s $(brew --prefix nvm)/nvm.sh
      4. ln -s $(brew --prefix nvm)/nvm.sh
    - 上記コマンド後は.nvmの中にいるのでcdコマンドで戻る
    - 再度「source ~/.nvm/nvm.sh」と入力
    - 多分うまくいくはず