# step2 ブランチ(branch)を作成しよう

* やりたいこと
  * ローカルリポジトリに自分の作業用のブランチを作成する
  * ブランチを切り替えると作業ツリーの内容が変わることを確認する

## 手順

1. ブランチの作成
    * GitGraph上のmasterタグの付いたコミットを右クリックし、「Create Branch...」を選択
    * nameにブランチ名を入力
      * 例：feature-imada
    * Check out にチェックを入れる
    * 「Create Branch」を選択
    * ブランチが作成される
    * ※「master」タグ自体を右クリックするとブランチに対する操作と扱われ、「Create Branch...」の選択肢が出ない、注意

1. ブランチの確認
    * GitGraph上に先程作成した名前のブランチが生成されていることを確認する
    * ※もしされていない場合はGitGraphのタブ内右上のrefreshを押す

1. ブランチの切り替え
    * src/index.htmlを開く
    * 9行目に`<p>これはmasterブランチです。</p>`とあることを確認する
    * GitGraph上のdevelopタグをダブルクリックし、developブランチをcheckoutする
    * 9行目が`<p>これはdevelopブランチです。</p>`に変わっていること確認する

## memo

* ブランチを切り替える行為であるcheck outは、コミット前の変更がある場合はできない
  * その場合は全ての変更をコミットするか、stashコマンドによる一時退避を行う
  * stashについてはstepXXを参照(T.B.D)

## Advanced

* 上記作業をコマンドライン上で行う

  * ブランチの確認
    * `git branch -a`
      * `-a`オプションでリモートリポジトリ上のブランチ(追跡ブランチ)も表示される
      * ※fetchしてからでなければリモートリポジトリの最新の状態ではない点に注意

  * ブランチの作成
    * `git checkout -b branch_name`

  * ブランチの切り替え
    * `git checkout develop`
    * `git checkout branch_name`

  * ブランチの削除
    * `git branch -d branch_name`
