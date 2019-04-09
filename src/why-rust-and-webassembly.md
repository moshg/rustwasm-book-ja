# なぜRust and WebAssembly？

<!-- # Why Rust and WebAssembly? -->

## 低レベル制御と高レベルエルゴノミクス

<!-- ## Low-Level Control with High-Level Ergonomics -->

JavaScript製ウェブアプリは信頼性のあるパフォーマンスを達成し、維持するのに苦労します。JavaScriptの動的型システムとガベージコレクションによる停止は役に立ちません。見たところ、不運にもJITにとって良いパスを外れてしまった場合、コードの小さい変更は劇的なパフォーマンスの低下を引き起こします。

<!-- JavaScript Web applications struggle to attain and retain reliable performance.
JavaScript's dynamic type system and garbage collection pauses don't help.
Seemingly small code changes can result in drastic performance regressions if
you accidentally wander off the JIT's happy path. -->

Rustはプログラマーに低レベルな制御と信頼性のあるパフォーマンスをもたらします。RustにはJavaScriptを悩ませる非決定的なガベージコレクションによる停止がありません。プログラマは間接や単相化やメモリレイアウトの制御ができます。

<!-- Rust gives programmers low-level control and reliable performance. It is free
from the non-deterministic garbage collection pauses that plague JavaScript.
Programmers have control over indirection, monomorphization, and memory layout. -->

## .wasmの小ささ

<!-- ## Small `.wasm` Sizes -->

.wasmはネットワーク越しにダウンロードしなければならないので、コードサイズはとても重要です。Rustはランタイムを持っておらず、ガベージコレクタのような余分な肥大化したインクルードを持たないので.wasmのサイズを小さくできます。(コードサイズは) 実際に使う機能の分だけの負担です。

<!-- Code size is incredibly important since the `.wasm` must be downloaded over the
network. Rust lacks a runtime, enabling small `.wasm` sizes because there is no
extra bloat included like a garbage collector. You only pay (in code size) for
the functions you actually use. -->

## すべてを書き直さ*ない*

<!-- ## Do *Not* Rewrite Everything -->

既にあるコードベースを捨てる必要はありません。直ちに効果を得るために最もパフォーマンスに敏感なJavaScriptの関数をRustに移植するところから始められます。そしてもしそうしたいなら、そこでやめることもできます。

<!-- Existing code bases don't need to be thrown away. You can start by porting your
most performance-sensitive JavaScript functions to Rust to gain immediate
benefits. And you can even stop there if you want to. -->

他とうまく協調する

<!-- ## Plays Well With Others -->

Rust and WebAssemblyは既にあるJavaScriptのツールと組み合わせられます。ECMScriptのモジュールがサポートされていて、npmやWebpackやGreenkeeperのような既に気に入っているツールを使い続けられます。

<!-- Rust and WebAssembly integrates with existing JavaScript tooling. It supports
ECMAScript modules and you can continue using the tooling you already love, like
npm, Webpack, and Greenkeeper. -->

## 当然の快適さ

<!-- ## The Amenities You Expect -->

Rustは開発者が当然のものと思うようになった現代的な快適さを備えています。例えば:

<!-- Rust has the modern amenities that developers have come to expect, such as: -->

* cargoを使った強力なパッケージマネジメント、

<!-- * strong package management with `cargo`, -->

* 表現力のある (そしてゼロコストの) 抽象化、

<!-- * expressive (and zero-cost) abstractions, -->

そして歓迎的なコミュニティです！😊

<!-- * and a welcoming community! 😊 -->
