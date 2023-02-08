This repository contains a simple example of building rust-openssl create to WASM.

Source code is taken from the OpenSSL documentation: https://docs.rs/openssl/latest/openssl/aes/index.html


# Prerequisites

Emscripten compiler toolkit: https://github.com/emscripten-core/emsdk

I have a `3.1.3` version installed, but I assume another versions will work as well.

# WASM build

```bash
rustup target add wasm32-unknown-emscripten
cargo build --all --target=wasm32-unknown-emscripten
```

# RUN

```bash
node target/wasm32-unknown-emscripten/build/wasm_rust_openssl.js  # should print "SUCCESS!"
```

