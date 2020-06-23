# template

John Smith

---

## スライドの作り方

---

### 書き方

`slides.md` に一般的な
マークダウン記法で記述します。

スライドのタイトルやスタイルなどの設定は
`config.yml` に記述します。

***

### 特殊なマークダウン記法

以下のようなスライド用の
特殊なマークダウン記法が利用可能です。

* 改ページ
* 縦スライド
* 発表者ノート

詳細は下のページに。

---

### 改ページ

通常の改ページは `---` です。

----

水平バーは `----` で挿入可能です。

---

### 縦スライド

改ページとして `***` を使用すると、
次に `***` で改ページを行うまで、
改ページを行うごとに縦にページを追加します。

---

### 発表者ノート

次のように発表者ノートを記述することができます。

<pre>
  ```note
  あんなことやこんなことを話す。
  ```
</pre>

発表者ノートはスライド上で s キーを押して
speaker note view に切り替えると表示されます。

```note
あんなことやこんなことを話す。
```

***

### スライドの生成方法

```shell
cd /path/to/slides.md/directory
reveal-ck generate
```

上記のコマンドで `slides.md` と `config.yml` から
slides ディレクトリ以下にスライドを生成します。

いずれかのファイルを更新したら
上記のコマンドでスライドを生成し直してください。

---

### プレビュー

```shell
reveal-ck serve
```

上記のコマンドでブラウザで[プレビュー](http://localhost:10000)できます。

`slides.md` の変更は即座に反映されますが、
`config.yml` を変更した場合は一旦止めて
`reveal-ck generate` し直してください。

---

## スライドの操作方法

| Key    | Action                 |
| ------ | ---------------------- |
| ?      | show help              |
| cursor | move page              |
| s      | open speaker note view |
| ESC    | overview               |
| f      | fullscreen             |

---

## スライドの公開方法

スライドのディレクトリごと
master ブランチへ追加するだけで
GitHub Pages で直接閲覧可能になります。

---

## Appendix

* [reveal.js](https://revealjs.com/)
* [reveal-ck](http://jedcn.github.io/reveal-ck/)
