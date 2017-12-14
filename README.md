#gifmin

> Minify gif images seamlessly.Ported [gifsicle](https://github.com/kohler/gifsicle) using emscripten.
  This project is inspired by [opencore-amr-js](https://github.com/yxl/opencore-amr-js).

## Usage

```js
var gifBuffer=new ArrayBuffer(10);
var colors=32;
var result=gifmin(gifBuffer,colors);
//console.log(result)
//=>ArrayBuffer or false
```

## API

### gifmin(gifBuffer,colors)

#### Parameters

###### gifBuffer

Type: `ArrayBuffer`

Gif Buffer to be optimized.

###### colors

Type: `number`

Reduce the number of distinct colors in each output GIF to num or less. Num must be between 2 and 256.

------------------------------------------------------------------------------------------------------------

#### Return value

If the function succeeds, the return value is *a promise for a buffer*.
If the function fails, the return value is *false*.


##Remarks

emscripten command: `emcc -O1 *.cpp -o gif.js`

