# Git practice

## コンフリクト

リポジトリをクローンする(repo-a)
コンフリクトテスト用にリポジトリをクローンする(repo-b)
repo-aとrepo-bで同じファイルを変更する

mergeを解消したら
```
git add <conflict解消したファイル>
git commit
```

リモートブランチ
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
