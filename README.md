# css via npm

<a href="http://twitter.com/sethdvincent" style="font-size:50%">@sethdvincent</a>
<a href="http://sethvincent.com/css-via-npm" style="font-size:50%">sethvincent.com/css-via-npm</a>


---

## npm is great for js.

---

## it's great for css, too.

---

## simple workflow

- `npm i --save cool-css`
- `@import "cool-css";`
- `npm run bundle-css`

---

## bootstrap? sure.

- `npm i --save bootstrap`
- `@import "bootstrap";`
- `npm run bundle-css`

---

## hey, what's that `bundle-css` command?

---

## There are a few tools for bundling css.

- [sheetify](http://npmjs.org/sheetify)
- [rework-npm](http://npmjs.org/rework-npm)
- [parcelify](http://npmjs.org/parcelify)

---

```json
{
  "style": "style.css",
}
```
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

## ok.

---

## css tomorrow yesterday

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


## include local css files in a bundle by using a relative path

```css
@import "./example.css";
```

---

## usage example

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

## toy module example

---

- `npm i -S pizza-background`
- `@import "pizza-background";`
- `npm run bundle-css`
- add bundled css script tag
- `<body class="pizza"></body>`

---
<img src="pizza.gif" alt="pizza.gif">
---

## now you publish a css module!

<a href="http://twitter.com/sethdvincent" style="font-size:50%">@sethdvincent</a>
<a href="http://sethvincent.com/css-via-npm" style="font-size:50%">sethvincent.com/css-via-npm</a>