# znn-pow-links.js

How to build the code yourself

```sh
 emcc -O3 -s WASM=1 -s EXTRA_EXPORTED_RUNTIME_METHODS='["cwrap"]' -s EXPORT_ALL=1 -s LINKABLE=1 src/cpp/pow_links.cpp src/cpp/sha3.c src/cpp/bridge.cpp -o build/znn-pow-links.js
```

How to test the code yourself
```js
python3 -m http.server --directory examples/
```

Navigate to [http://127.0.0.1:8000/](http://127.0.0.1:8000/).
If you see `2ffd000000000000`, it means everything worked correctly. It may take some time to compute the answer. 

If you see `The answer should be here` on the other hand, it means that the answer is not there and something went wrong.