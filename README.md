# [wasm-demo](https://hungry-knuth-07c061.netlify.com/hello.html)

> Demo for wasm intro talk!

## To get started

### Step 1

- We need a pre-complied tool chain to compile the high languages (C, C++, Rust etc) to WASM (binary format in .wasm, .js files).

```bash
git clone https://github.com/emscripten-core/emsdk.git
cd emsdk
./emsdk install latest
./emsdk activate latest
```

> If it fails add the below line in emsdk.py

```python
import ssl
ssl._create_default_https_context = ssl._create_unverified_context
```

### Step 2

Run the below command to create `.wasm` and `.js` hello files.

```bash
emcc hello.c -o hello.html
```

### Step 3

To create web server to run the compiled code.

```bash
emrun --no_browser --port 8080 .
```
