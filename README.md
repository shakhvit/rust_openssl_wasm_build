# rust_openssl_wasm_build

This repository contains a simple example of building rust-openssl crate to WASM.

A simple AES test implemented in main is taken from the OpenSSL documentaiton: https://docs.rs/openssl/latest/openssl/aes/index.html


# Prerequisites

Emscripten compiler toolkit: https://github.com/emscripten-core/emsdk

I have a `3.1.3` version installed, but assume another versions will work as well.

After cloning the repo above do the following:

```bash
cd emsdk
./emsdk install 3.1.3
./emsdk activate 3.1.3
source ./emsdk_env.sh
```

# WASM build

```bash
rustup target add wasm32-unknown-emscripten
cargo build --all --target=wasm32-unknown-emscripten
```

# RUN

```bash
node target/wasm32-unknown-emscripten/build/wasm_rust_openssl.js  # should print "SUCCESS!"
```

