#gifmin

> Minify gif images seamlessly

## Usage

```js
var testGifArrayBuffer=new ArrayBuffer(10)
var module = {
             print: console.log,
             printErr: console.log,
             files: [
                      {
                            "name": "in.gif",
                            "buffer": new Uint8Array(testGifArrayBuffer)
                       }
                  ],
                  arguments: ["-O3","--colors=32","in.gif","-o","out.gif"]
             };
var result=gifmin(module)
//console.log(result)
//=>{outputFiles:{"out.gif":ArrayBuffer},code:0}
```

## API

### gifmin(module)

Returns `Promise<Object[]>` in the format `{outputFiles: Object, code: Number}`.

#### module

Type: `Array`

agruments to be optimized.
