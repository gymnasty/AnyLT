# Any LT

なんでもござれの Lightning Talk のスライドを保存するリポジトリ。

## トーク一覧

* [テンプレート](https://gymnasty.github.io/AnyLT/talks/template/slides/)

---

## リポジトリ管理

### 閲覧権限

作成されたスライドは一般に公開されます。
スライドの内容にはご注意ください。

### ブランチ運用

メインブランチは master ブランチです。
最終的に master ブランチに変更が入るようにしてください。

その他は特にルールはありません。
ブランチを切って作業してから master へマージするなり、
直接 master を編集するなり好きにしてください。

### ファイル構成

* README.md
  * このドキュメントです。
  * 各スライドのページへのリンクを冒頭に記載します。
* talks
  * スライドの本体です。
  * talks/<名前>/<トピック名> ディレクトリを作成し、そこに各スライドを保存します。
* templates
  * スライドのテンプレートです。

## スライドの書き方

スライドは reveal-ck を使って markdown で記述します。

### 準備

1. ruby をインストールする (バージョン 2.0 以上)
2. reveal-ck をインストールする
3. ruby 本体と gems のディレクトリにパスを通す

#### MacOS の場合

```sh
brew install ruby
# PATH の設定は .bashrc とか .zshrc とかに書いておく
export PATH="/usr/local/opt/ruby/bin:$PATH"
export PATH="/usr/local/lib/ruby/gems/2.7.0/bin:$PATH"
gem install reveal-ck
```

### 書き方

1. `talks/<名前>/<トピック名>` のディレクトリを作成する
2. `talks/template` 直下の `slides.md` と `config.yml` を上記のディレクトリにコピーする
3. 上記のディレクトリ内で `reveal-ck generate` を実行する
4. `reveal-ck serve` を実行する
5. [プレビュー](http://localhost:10000) を確認する

あとは `slides.md` を編集するだけ。
`slides.md` を編集して保存するとプレビューがホットリロードされる。

`config.yml` を変更した場合は `reveal-ck generate` からやり直す。

## スライドの公開方法

master ブランチにスライドのディレクトリをコミットして push するだけです。

以下へアクセスするとスライドが表示されます。

`https://gymnasty.github.io/AnyLT/talks/<名前>/<トピック名>/slides/`
