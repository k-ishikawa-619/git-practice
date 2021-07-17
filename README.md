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

リモート追跡ブランチ(remote-tracking branches)
git branch -a というコマンドを打ったときに表示される
remotes/origin/master
git fetchしたときに更新される

上流ブランチ(upstream branch)
コマンドの引数を省略したときにデフォルトととして対象となるブランチ

