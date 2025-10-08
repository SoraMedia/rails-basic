# Ruby on Rails 学習プログラム "基礎編"

環境構築がすでに完了している Ruby on Rails 7 のリポジトリになります。devcontianer の拡張機能（VScode）と Docker が使用できる環境であれば簡単にセットアップができるよう設計されていますので、ご活用ください。

### 環境構築

#### devcontainer の install

[インストール参考資料](https://blog.kinto-technologies.com/posts/2022-12-10-VSCodeDevContainer/)

#### git の設定

1. 前の研修で git と Github について学習済みのはずです。自分の Gihub アカウントに、まず空のリポジトリを作成しましょう。
2. そして、以下のコマンドを実行します。(user.name と user.email はご自身のものを入力)

```
git config --global user.name xxxx
git config --global user.email xxxx@xxxx.com
```

#### 動作確認

##### devcontainer の起動

1. vscode 上で「ctrl + shift + P」を入力
2. 「Dev Containers: Rebuild and Reopen in Container 」を選択

##### devcontainer 起動後

1. vscode の確認
   追加で入れた拡張機能やディレクトリ構成があっていることを確認する。

2. git の確認
   下記のコマンドでホスト側で行った確認と同じ出力が出ることを確認。

```
ssh -T git@github.com
```

3. .git を削除 (初回のみ)

```
rm -rf .git
```

4. 先に作成した空のリポジトリにクローンしたこのリポジトリをプッシュ。 (初回のみ)

- リポジトリへのプッシュ方法は作成したリポジトリに記載されていますのでご確認を。

5. 以下のコマンドを実行し、localhost:3000 にアクセスする

```
rails db:create db:migrate
rails s
```
