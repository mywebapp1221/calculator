# calculator

このリポジトリの`index.html`にあるページへ、`image/IMG_20251207_132950699_HDR.jpg`を表示する写真プレビューを追加しました。

## GitHub Pagesで公開する手順

1. リポジトリをGitHubにプッシュ（既にリモートがある場合は不要）

	```powershell
	git add .
	git commit -m "Add photo preview to index.html"
	git push origin main
	```

2. GitHub上で公開（簡単な方法：`main`ブランチを使う）
	- リポジトリのページへ行く → `Settings` → `Pages` を開く。
	- `Source` を `Deploy from a branch` にして、`Branch` を `main`、`/ (root)` を選択して `Save`。
	- 数分で `https://<your-username>.github.io/<repository>/` のようなURLで公開されます。

3. 別方式（`gh-pages`ブランチを作る）

	```powershell
	git checkout --orphan gh-pages
	git reset --hard
	git add index.html image/ -f
	git commit -m "Publish site"
	git push -u origin gh-pages --force
	git checkout main
	```

4. 確認
	- GitHub Pages設定画面に表示される公開URLをブラウザで開いて、写真が表示されていることを確認してください。

必要なら、公開設定の代行（私がコミットやgh-pagesの作成を行う）もできます。続けますか？