# Rust🦀 and WebAssembly🕸

<!-- # Rust 🦀 and WebAssembly 🕸 -->

この小さな本は[Rust][]と[WebAssembly][]を組み合わせて使う方法を書いています。

<!-- This small book describes how to use [Rust][] and [WebAssembly][] together. -->

## この本の対象読者は？

<!-- ## Who is this book for? -->

この本は速く信頼性のあるウェブのコードのために、RustをWebAssemblyにコンパイルすることに興味があるすべての人に向けた本です。読者はある程度Rustを知っていて、JavaScriptやHTMLやCSSに親しみを持っていることが推奨されます。しかし、それらのエキスパートである必要はありません。

<!-- This book is for anyone interested in compiling Rust to WebAssembly for fast,
reliable code on the Web. You should know some Rust, and be familiar with
JavaScript, HTML, and CSS. You don't need to be an expert in any of them. -->

まだRustを知りませんか？[プログラミング言語Rustから始めましょう。][trpl]

<!-- Don't know Rust yet? [Start with *The Rust Programming Language* first.][trpl] -->

JavaScriptやHTMLやCSSを知りませんか？[MDNでそれらを学びましょう。][mdn]

<!-- Don't know JavaScript, HTML, or CSS? [Learn about them on MDN.][mdn] -->

## この本の読み方

<!-- ## How to read this book -->

初めに[背景とコンセプト][background]に親しみを持ち、そして[RustとWebAssemblyを組み合わせて使う動機][why-rust-wasm]も同様に読むのがよいでしょう。

<!-- You should read [the motivation for using Rust and WebAssembly
together][why-rust-wasm], as well as familiarize yourself with the [background
and concepts][background] first. -->

[チュートリアル][tutorial]は最初から最後まで読むように書かれています。読者はチュートリアルのコードを自分で書き、コンパイルし、実行しながら追いかけることが望ましいです。
もしこれまでにRustとWebAssemblyを組み合わせて使ったことがないのならチュートリアルをやりましょう！

<!-- The [tutorial][] is written to be read from start to finish. You should follow
along: writing, compiling, and running the tutorial's code yourself. If you
haven't used Rust and WebAssembly together before, do the tutorial! -->

[リファレンスの節][reference]は任意の順序で読むことができます。

<!-- The [reference sections][reference] may be perused in any order. -->

> **💡 Tip:** ページ上部の🔍アイコンをクリックまたはキーボードの`s`を押すことでこの本の中を検索できます。

<!-- > **💡 Tip:** You can search through this book by clicking on the 🔍 icon at the
> top of the page, or by pressing the `s` key. -->

## この本に貢献する

<!-- ## Contributing to this book -->

この本はオープンソースです！タイポを見つけましたか？何か見落としがありますか？[**プルリクエストを送ってください！**][repo] (訳注: この和訳のリポジトリは[こちら][repo-ja]にあります)

<!-- This book is open source! Find a typo? Did we overlook something? [**Send us a
pull request!**][repo] -->

[Rust]: https://www.rust-lang.org
[WebAssembly]: https://webassembly.org/
[trpl]: https://doc.rust-jp.rs/book/second-edition/
[mdn]: https://developer.mozilla.org/ja/docs/Learn
[why-rust-wasm]: ./why-rust-and-webassembly.html
[background]: ./background-and-concepts.html
[tutorial]: ./game-of-life/introduction.html
[reference]: ./reference/index.html
[repo]: https://github.com/rustwasm/book
[repo-ja]: https://github.com/moshg/rustwasm-book-ja
