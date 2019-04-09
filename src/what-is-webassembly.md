# WebAssemblyとは？

<!-- # What is WebAssembly? -->

WebAssembly (wasm) とは単純な機械モデルと[広範な仕様][extensive specification]を伴った実行可能形式のことです。wasmはポータブルかつコンパクトで、ネイティブと同じかそれに近いスピードで実行されるように設計されています。

<!-- WebAssembly (wasm) is a simple machine model and executable format with an
[extensive specification]. It is designed to be portable, compact, and execute
at or near native speeds. -->

プログラミング言語として、WebAssemblyは方法は異なっているが同じ構造を表現する二つのフォーマットから成ります:

<!-- As a programming language, WebAssembly is comprised of two formats that
represent the same structures, albeit in different ways: -->

1. `.wat`テキストフォーマット ("**W**eb**A**ssembly **T**ext"から`wat`と呼ばれます) は[S式][S-expressions]を使い、SchemeやClojureのようなLispファミリー言語との類似性があります。

<!-- 1. The `.wat` text format (called `wat` for "**W**eb**A**ssembly **T**ext") uses
   [S-expressions], and bears some resemblance to the Lisp family of languages
   like Scheme and Clojure. -->

2. `.wasm`バイナリフォーマットは低レベルでwasm仮想機械に使用されることを意図されています。概念的にはELFやMach-Oに似ています。

<!-- 2. The `.wasm` binary format is lower-level and intended for consumption
   directly by wasm virtual machines. It is conceptually similar to ELF and
   Mach-O. -->

参考として、wat形式の階乗関数はこのようになります: 

<!-- For reference, here is a factorial function in `wat`: -->

```
(module
  (func $fac (param f64) (result f64)
    get_local 0
    f64.const 1
    f64.lt
    if (result f64)
      f64.const 1
    else
      get_local 0
      get_local 0
      f64.const 1
      f64.sub
      call $fac
      f64.mul
    end)
  (export "fac" (func $fac)))
```

もし`wasm`ファイルがどのように見えるかに興味があるなら、[wat2wasm demo][wat2wasm demo]を上のコードに使うことができます。

<!-- If you're curious about how a `wasm` file looks like you can use the [wat2wasm
demo] with the above code. -->

## 線形メモリ

<!-- ## Linear Memory -->

WebAssemblyはとても単純な[メモリモデル][memory model]を持っています。wasmモジュールは一つの本質的にバイトのフラットな配列である「線形メモリ」にアクセスすることができます。このメモリはページサイズ (64K) の倍数で[拡張][memory can be grown]することができます。縮小することはできません。

<!-- WebAssembly has a very simple [memory model]. A wasm module has access to a
single "linear memory", which is essentially a flat array of bytes. This
[memory can be grown] by a multiple of the page size (64K). It cannot be shrunk. -->


## WebAssemblyはウェブだけのためのもの？

<!-- ## Is WebAssembly Just for the Web? -->

今のところ一般にJavaScriptとウェブのコミュニティに注目を集めていますが、wasmはホスト環境について一切の仮定をしません。それゆえ、wasmは将来様々な文脈で使用される「ポータブルな実行ファイル」形式になるというと推測するのは理にかなっています。しかし*今現在*、wasmはたいてい (ウェブ上や[Node.js]上のものを含めて) 多くの種類を持つJavaScript (JS) と関連付けられています。

<!-- Although it has currently gathered attention in the JavaScript and Web
communities in general, wasm makes no assumptions about its host
environment. Thus, it makes sense to speculate that wasm will become a "portable
executable" format that is used in a variety of contexts in the future. As of
*today*, however, wasm is mostly related to JavaScript (JS), which comes in many
flavors (including both on the Web and [Node.js]). -->

[memory model]: https://webassembly.github.io/spec/core/syntax/modules.html#syntax-mem
[memory can be grown]: https://webassembly.github.io/spec/core/syntax/instructions.html#syntax-instr-memory
[extensive specification]: https://webassembly.github.io/spec/
[value types]: https://webassembly.github.io/spec/core/syntax/types.html#value-types
[Node.js]: https://nodejs.org
[S-expressions]: https://ja.wikipedia.org/wiki/S%E5%BC%8F
[wat2wasm demo]: https://cdn.rawgit.com/WebAssembly/wabt/aae5a4b7/demo/wat2wasm/
