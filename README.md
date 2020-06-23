## Minimal Rust + WASM Example

An extremely minimal Rust + WASM example that
[works with GitHub pages](http://tuzz.github.io/minimal-rust-wasm).
It demonstrates how to write to the DOM and how to call a JavaScript function
from Rust. Hopefully this will serve as a helpful reference.

### Usage

In one tab run:

```sh
$ ./bin/setup
$ ./bin/wasm_watch
```

In another tab run:

```sh
$ ./bin/server
```

If you're not on a Mac, you'll need to install `binaryen` a different way.

### Make a change

Try changing "Hello, world!" to "Hello, foo!" in `src/wasm_main.rs`. The
`./bin/wasm_watch` script should automatically rebuild the project and
`./bin/server` should reload the web page once that's done. Neat!

### Deploying

To deploy to GitHub pages run:

```sh
$ ./bin/deploy
```

It will compile the project then copy `index.html`, `target/index.wasm` and
`target/index.js` to a `tmp/` directory. This is then deployed to the gh-pages
branch for the current git repository.

### Documentation

Now that you have a working Rust/WASM workflow, refer to
[the book](https://rustwasm.github.io/book/) and the
[web_sys](https://rustwasm.github.io/wasm-bindgen/api/web_sys/) crate for more
information.
