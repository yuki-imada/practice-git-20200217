# step1 リポジトリをクローン(clone)しよう

* やりたいこと
  * GitHub上にあるリモートリポジトリから、自身の端末にローカルリポジトリを作成する

## 前提

* クローン元となるリモートリポジトリ
  * https://github.com/yuki-imada/practice-git-yyyymmdd.git
  * yyyymmddは都度変わるため適宜変更すること
* クローン先のフォルダ
  * 任意
  * 例：`C:\Users\USER_NAME\git\practice-git-yyyymmdd`

## 手順

1. github作業用フォルダの作成
    * 手順省略

1. リポジトリのクローン - clone
    * コマンドプロンプトを起動し、クローン先のフォルダに移動
    * `git clone https://github.com/yuki-imada/practice-git-yyyymmdd.git`
      * usernameとpasswordを聞かれるので入力

1. フォルダ配下にファイルが追加されていることを確認する

## memo

* 通常のOSS開発などの場合は対象のリポジトリをまずforkし、forkした自身のリモートリポジトリをcloneするのが手順として一般的
* 今回は手順簡略化のためにリポジトリのオーナー(yuki-imada)からメンバー権限を与えられているため、他人のリモートリポジトリでもcloneできる
* publicとprivateについて
  * githubでは作成するリモートリポジトリをpublicとprivateの2種類から選べる
    * publicリポジトリはGitHub上で公開され、誰でも参照やforkができる
    * privateリポジトリは公開されず、自分と承認された人以外はリポジトリを参照できない
  * 今回のハンズオンのようにpublicリポジトリにメンバーを追加するのは無料だが、privateリポジトリにメンバーを追加したい場合は、有料プランに入る必要がある
