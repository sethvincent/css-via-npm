# css via npm

<a href="http://twitter.com/sethdvincent" style="font-size:50%">@sethdvincent</a>

---

## npm is great for js.

---

## hey, it's great for css, too.

---

## simple workflow

- `npm install cool-css-package`
- `@import "cool-css-package";` in main CSS file.
- `npm run bundle-css`

---

## bootstrap? sure.

- `npm install --save bootstrap`
- `@import "bootstrap";`
- `npm run bundle-css`

---

## hey, what's that `bundle-css` command?

---

## There are a few command-line tools for bundling css that's distributed on npm.

- [sheetify](http://npmjs.org/sheetify)
- [rework-npm](http://npmjs.org/rework-npm)
- [parcelify](http://npmjs.org/parcelify)

---

## example bundle-css script

```json
"scripts": {
  "bundle-css":  "sheetify style.css > bundle.css"
}
```

---

## modular css

---

## hi i'd like some button styles please.

---

## modular css projects

- [basscss](npmjs.org/basscss)
- [tachyons](npmjs.org/tachyons)
- [suitcss](npmjs.org/suitcss)
- [topcoat](npmjs.org/topcoat)
- [csskit](npmjs.org/csskit)

---

## preprocessors?

---

## yes.

---

## CSS4

- [cssnext](http://npmjs.org/cssnext)
- [rework](http://npmjs.org/rework)
- [postcss](http://npmjs.org/postcss)

--- 

## example bundle-css script with cssnext

```json
"scripts": {
  "bundle-css":  "sheetify style.css | cssnext > bundle.css"
}
```

---

## publishing css modules

- package.json `style` property
- publish preprocessed file in `style` property
- offer source files as option.

---

## scss example:

```css
@import "example/source.scss";
```

---

## css4 example:

```css
@import "example/style-css4.css";
```

---

## include local css files in a bundle by using a relative path

```css
@import "./example.css";
```

---

## detailed example

how do i use this?

---

## css dependencies

```bash
npm i --save normalize.css basscss-grid csskit
```

---

## dev dependencies

```bash
npm i --save-dev sheetify cssnext
```

---

## files:

- css/
  - index.css
  - fonts.css
  - layout.css
  - forms.css
  - etc.

---

## index.css

```css
@import "normalize.css";
@import "basscss-grid";
@import "csskit";

@import "./fonts.css";
@import "./layout.css";
/* etc. */
```

---

## bundle-css script

```json
"scripts": {
  "bundle-css":  "sheetify css/index.css | cssnext > public/bundle.css"
}
```

---

## thanks!

<a href="http://twitter.com/sethdvincent" style="font-size:50%">@sethdvincent</a>