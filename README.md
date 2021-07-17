# Git practice

## git lol

gitの履歴をみやすくする
```
git config --global alias.lol "log --graph --decorate --pretty=oneline --all --abbrev-commit"
```

## プル

``git pull``を使わない

```
git switch main
git fetch
// 差分を確認
git diff HEAD origin/main
// ファイル単位
git diff HEAD origin/main README.md
// マージ
git merge origin/main
```

## コンフリクト

リポジトリをクローンする(repo-a)
コンフリクトテスト用にリポジトリをクローンする(repo-b)
repo-aとrepo-bで同じファイルを変更する

mergeを解消したら
```
git add <conflict解消したファイル>
git commit
```

HEADの変更を受け入れる
```
git checkout --ours [ファイル名]
```
マージするブランチを受け入れる
```
git checkout --theirs [ファイル名]
```


## リモートブランチ
https://git-scm.com/book/ja/v2/Git-%E3%81%AE%E3%83%96%E3%83%A9%E3%83%B3%E3%83%81%E6%A9%9F%E8%83%BD-%E3%83%AA%E3%83%A2%E3%83%BC%E3%83%88%E3%83%96%E3%83%A9%E3%83%B3%E3%83%81

追跡ブランチ(remote-tracking branches)

ローカルに作られている
git branch -a というコマンドを打ったときに表示される
remotes/origin/master
git fetchしたときに更新される
git checkout -b [branch] [remotename]/[branch] を実行すると作成される
- ローカルブランチが存在せず、リモートが1つだけのとき、自動的に追跡ブランチを作成する
```
git checkout serverfix
```
- どのブランチを追跡しているかを調べる
```
git branch -vv
```

上流ブランチ(upstream branch)
コマンドの引数を省略したときにデフォルトととして対象となるブランチ
追跡ブランチが追跡するブランチ

