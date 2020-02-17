# practice-git-20200217

これは2020/02/17用のgit練習用のマスターリポジトリです。

## 事前準備

* 受講者側
  * GitHubアカウントの開設
  * gitのインストール
  * Visual Studio Codeのインストール
    * 拡張機能「Git Graph」のインストール
    * ※その他のgit用GUIツールを使用している場合は省略可

* 講師側
  * 勉強会用リポジトリの用意
    * 受講者側がpushできるよう設定変更
      * githubのリポジトリのページ -> Setteings -> Collaborators
        * 受講者のGitHubアカウントの追加

* GitHubのメール設定
  * [https://github.com/settings/emails](https://github.com/settings/emails)にアクセス
    * 「Keep my email addresses private」にチェックを入れる
    * 「99999999+xxxxxxxx@users.noreply.github.com」といった
      個人用のダミーメールアドレスが発行されているため、この文字列をコピーしておく
  * `git config user.email 99999999+xxxxxxxx@users.noreply.github.com`
    * メールアドレスの部分は先程コピーした個人のメールアドレスを使用

## 練習内容

* step1 リポジトリをクローン(clone)しよう
* step2 ブランチ(branch)を作成しよう
* step3 変更をコミット(commit)しよう
* step4 変更をプッシュ(push)しよう
* step5 他のブランチの取り込み=マージ(marge)しよう
* ※各stepにはより高度なAdvancedを追加しています
  * Advancedではコマンド操作のみで上記stepの手順を進めます

## コマンドサンプル

### ブランチ操作

* ブランチの確認
  * `git branch -a`
  * `-a`でリモートリポジトリのブランチも表示する

* ブランチの作成
  * `git checkout -b branch_name`

* ブランチの削除
  * `git branch -d branch_name`

* ブランチの切り替え
  * `git checkout master`
  * `git checkout branch_name`

* 追跡ブランチの更新
  * `git fetch --prune`
    * `--prune`でリモート上で削除されたブランチをローカル上でも削除する

### コミット操作

* コードのコミット
  * まずは作業ツリーからindexへの追加
    * `git add .`
      * `.`で全ファイル
  * コミットの登録(コメント必須)
    * `git commit -m 'add your comment'`

* コードのプル
  * `git pull`

### プッシュ操作

* コードのプッシュ
  * `git push origin master`
    * originの部分が対象のリモートリポジトリ名、masterの部分が対象のブランチ名
    * カレントブランチをpushする

* コードの強制プッシュ
  * `git push -f origin master`
  * push先の分岐以降のコミットは失われる

* リモートリポジトリの別ブランチにpush
  * `git push origin from-branch:to-branch`

### 設定操作

* user情報の確認
  * `git config user.name`
  * `git config user.email`

* user情報の更新
  * `git config user.name new_name`
  * `git config user.email new_email`

### その他の操作

* リモートリポジトリにコミットしたファイルを後から管理対象外にしたい場合
  * .gitignoreに管理対象のファイルを追加
  * 実ファイルを残したままgitの管理上から削除(--cachedオプション)
    * `git rm --cached FILE_TO_DELETE`
