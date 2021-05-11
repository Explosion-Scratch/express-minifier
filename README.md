# express-minifier

Automatically minify CSS, JS and HTML files! 

## How to use
```js
const minify = require("express-minifier");
app.use(minify(app));
```
done!

**But wait I want options 🥺**

okie doke:
```js
const minify = require("express-minify");
let opts = {
  send: false,//Don't minify res.send
};
app.use(minify(app, opts));
```
Options list:

- `send`: Minify `res.send()`'s
- `sendFile`: Minify `res.sendFile()`
- `static`: Minify `app.use(express.static(__dirname))`
- `minifyCSS`: Minify CSS
- `minifyJS`: Minify JS
- `minifyHMTL`: Minify HTML
- `cssOptions`: Options to pass to `clean-css` minifier.
- `htmlOptions`: Options to pass to `html-minifier`
