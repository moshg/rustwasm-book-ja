# セットアップ

<!-- # Setup -->

このセクションはRustプログラムをWebAssemblyにコンパイルし、JavaScriptと組み合わせる方法を記述します。

<!-- This section describes how to set up the toolchain for compiling Rust programs
to WebAssembly and integrate them into JavaScript. -->

## Rustツールチェイン

<!-- ## The Rust Toolchain -->

`rustup`、`rustc`、`cargo`を含むツールチェインが必要になります。

<!-- You will need the standard Rust toolchain, including `rustup`, `rustc`, and
`cargo`. -->

[Rustツールチェインをインストールするためにこれらの手順に従ってください。][rust-install]

<!-- [Follow these instructions to install the Rust toolchain.][rust-install] -->

Rust and WebAssemblyの体験はstableのリリース列車に乗っています！それは実験的機能は要求しないということです。しかし、Rust 1.30またはそれ以上の新しいバージョンが要求されます。

<!-- The Rust and WebAssembly experience is riding the Rust release trains to stable!
That means we don't require any experimental feature flags. However, we do
require Rust 1.30 or newer. -->

## `wasm-pack`

<!-- ## `wasm-pack` -->

`wasm-pack`はRustにより生成されたWebAssemblyのビルド、テスト、パブリッシュのためのワンストップショップ (訳注: そこだけで全ての必要な買い物ができるような場所のこと) です。

<!-- `wasm-pack` is your one-stop shop for building, testing, and publishing
Rust-generated WebAssembly. -->

[ここで`wasm-pack`をゲットしましょう！][wasm-pack-install]

<!-- [Get `wasm-pack` here!][wasm-pack-install] -->

## `cargo-generate`

<!-- ## `cargo-generate` -->

[`cargo-generate`は既に存在しているGitリポジトリをテンプレートとして利用して新しいRustプロジェクトを迅速に立ち上げ、実行に移すことを助けます。][cargo-generate]

<!-- [`cargo-generate` helps you get up and running quickly with a new Rust project
by leveraging a pre-existing git repository as a template.][cargo-generate] -->

`cargo-generate`をこのコマンドでインストールしてください:

<!-- Install `cargo-generate` with this command: -->

```
cargo install cargo-generate
```

## `npm`

`npm`はJavaScriptのパッケージマネージャです。JavaScriptバンドラと開発サーバをインストールし、実行するために使用します。チュートリアルの最後に、コンパイルした`.wasm`を`npm`レジストリにパブリッシュします。

<!-- `npm` is a package manager for JavaScript. We will use it to install and run a
JavaScript bundler and development server. At the end of the tutorial, we will
publish our compiled `.wasm` to the `npm` registry. -->

[これらの手順に従って`npm`をインストールしてください。][npm-install]

<!-- [Follow these instructions to install `npm`.][npm-install] -->

既に`npm`をインストールしている場合、このコマンドで最新版であるか確認してください:

<!-- If you already have `npm` installed, make sure it is up to date with this
command: -->

```
npm install npm@latest -g
```

[rust-install]: https://www.rust-lang.org/tools/install
[npm-install]: https://www.npmjs.com/get-npm
[wasm-pack]: https://github.com/rustwasm/wasm-pack
[cargo-generate]: https://github.com/ashleygwilliams/cargo-generate
[wasm-pack-install]: https://rustwasm.github.io/wasm-pack/installer/
