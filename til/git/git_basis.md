# Github
Githubはプログラムのコードやデザインのデータを保存、共有するためのサービス

## GitとGithubの違い
**Git**はプログラムなどを記述したソースファイルを管理するための「分散型バージョン管理システム」です
ソースコードの更新履歴を時系列にそって記憶することが出来、誤ってファイルを上書きしてしまった際にバージョンを戻したり、
チーム開発をスムーズに行うことを可能にします

対して、**Github**はGitの仕組みを利用した**プログラムのコードやデザインのデータを保存、公開するためのWebサービス**である

Githubでは`ローカルリポジトリ`で作業を行い、`リモートリポジトリ`で管理する
GitHubを使った開発は、ローカルでファイルを作成・更新し、リモートリポジトリにアップデートする、という流れ

## 用語集
### ローカルリポジトリ
自分のパソコン上に存在する、データの保管場所
### リモートリポジトリ
Githubのサーバー上に存在するデータの保管場所
### コミット
作成したファイルや更新情報をローカルリポジトリに登録する操作のこと
```git commit -m "メッセージ"```
### プッシュ
ローカルリポジトリで更新したファイルを、リモートリポジトリにアップロードする操作のこと
ファイル更新時にプッシュすると、ローカルリポジトリにコミットされた変更が GitHubのリモートリポジトリに送信される
### ブランチ
1つのプロジェクトを分岐させ、チーム内の機能追加、バグ修正など、ファイルやディレクトリの変更・更新を**同時進行**できるようにした機能
### masterブランチ
リポジトリに最初のコミットを行う際に作成されるブランチ
### マージ
マージとは、あるブランチで行った変更・更新の記録を別のブランチに適用すること
例えばバグ修正したブランチの記録を、機能追加を行ったブランチに適用することが可能

ブランチで行った作業内容をmasterにマージすることで、複数の更新情報をプロジェクトに反映できます。
### クローン
GitHubのローカルリポジトリで作業を行っているとき、このローカルリポジトリ自体をローカルマシン上にコピーして配置することが可能です。この操作をクローンと呼びます。
### プルリクエスト
ローカルリポジトリにおける変更をほかの開発者に通知する操作
### インデックス
ファイルの保管場所にコミットするためのファイルを登録すること

##　コマンド
### 初期化
ローカルリポジトリを作成する
`git init`
### 記録
変更内容をステージに上げ、リポジトリに反映する
`git add .`
`git commit -m "commit message"`

## 状況確認
`git diff`
`git diff -stage`
`git status`

## 履歴の確認
`git log`

## もとに戻す
`git restore file_name`
`git restore -stage file_name`


## Flow
1. github上でリモートリポジトリを作成
2. パスをコピーして、`git clone`
3. `git init`でローカルリポジトリを作成
4. `git add [filename]`でステージング
5. `git remote add [path]`
6. `git checkout -b [repository name]`でブランチの作成と移動
7. `git commit -m "commit message"` でコミット
8. `git push [repository name] [branch name]`でプッシュ
9. `git checkout main`でmainブランチに移動
10. `git checkout -D [branch name]`でブランチを削除
