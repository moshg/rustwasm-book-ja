# チュートリアル: ライフゲーム

<!-- # Tutorial: Conway's Game of Life -->

これは[ライフゲーム][gol]をRust and WebAssemblyで実装するチュートリアルです。

<!-- This is a tutorial that implements [Conway's Game of Life][gol] in Rust and
WebAssembly. -->

[gol]: https://ja.wikipedia.org/wiki/%E3%83%A9%E3%82%A4%E3%83%95%E3%82%B2%E3%83%BC%E3%83%A0

## このチュートリアルの対象読者は？

<!-- ## Who is this tutorial for? -->

このチュートリアルは既に基本的なRustとJavaScriptの経験があり、RustとWebAssemblyとJavaScriptを組み合わせて使う方法を学びたい人のためのものです。

<!-- This tutorial is for anyone who already has basic Rust and JavaScript
experience, and wants to learn how to use Rust, WebAssembly, and JavaScript
together. -->

読者はRustやJavaScriptやHTMLの基本的な読み書きが気楽にできるべきです。熟練者である必要はまったくありません。

<!-- You should be comfortable reading and writing basic Rust, JavaScript, and
HTML. You definitely do not need to be an expert. -->

## 何を学ぶのか？

<!-- ## What will I learn? -->

* WebAssemblyへコンパイルするためにRustのツールチェインをセットアップする方法。

<!-- * How to set up a Rust toolchain for compiling to WebAssembly. -->

* Rust、WebAssembly、JavaScript、HTML、CSSから成る複数言語プログラムを開発するワークフロー。

<!-- * A workflow for developing polyglot programs made from Rust, WebAssembly,
  JavaScript, HTML, and CSS. -->

* RustとWebAssembly両方の強みを、そしてさらにJavaScriptの強みを最大限に生かすAPIをデザインする方法。

<!-- * How to design APIs to take maximum advantage of both Rust and WebAssembly's
  strengths and also JavaScript's strengths. -->

* RustからコンパイルされたWebAssemblyモジュールをデバッグする方法。

<!-- * How to debug WebAssembly modules compiled from Rust. -->

* Rust and WebAssemblyのプログラムをより速くするためにプロファイルする方法。

<!-- * How to time profile Rust and WebAssembly programs to make them faster. -->

* Rust and WebAssemblyのプログラムをより小さくし、ネットワーク越しのダウンロードをより速くするためのサイズプロファイルの方法。

<!-- * How to size profile Rust and WebAssembly programs to make `.wasm` binaries
  smaller and faster to download over the network. -->
