# Next.css Core Module

Core Module is part of [Next.css framework](https://github.com/nextcss). This module contains
original Material Color Palette CSS styles for your Next.css project. You can use in all modern
websites with module bundlers, like webpack, rollup, parcel.

**[Next.css on GitHub](https://github.com/nextcss)**

## How to Install

You can install with npm or yarn package managers.

```shell
npm i @nextcss/core @nextcss/reset @nextcss/material-colors
yarn add @nextcss/core @nextcss/reset @nextcss/material-colors
```

Simple import to your project, and add class rules to you HTML tags. Check available selector rules
below.

```javascript
import '@nextcss/reset';
import '@nextcss/core';
import '@nextcss/material-colors';
```

## How to use

Example feature list block. [Watch the resolution here](https://7q75l.csb.app/) Learn more about
available CSS selectors below.

```html
<section class="fs-16 lh-1.6 bg-grey-50 fg-grey-700 py-50">
  <!-- Container -->
  <div class="container-lg">
    <!-- Intro -->
    <div class="container-md text-center mb-20">
      <h1 class="fs-24 md:fs-30 fw-500 fg-grey-900 mb-10">Why Next.css</h1>
      <p>The world’s developers thinking in pixels, we also thinking in pixels.</p>
    </div>
    <!-- Feature list -->
    <div class="flex flex-wrap">
      <!-- Feature box -->
      <a href="#" class="md:w-12/6 lg:w-12/4 p-15">
        <div class="bg-white p-25 radius-3 shadow-1">
          <h2 class="fs-20 fw-500 fg-grey-900 mb-8">Shooting Stars</h2>
          <p class="leading-relaxed text-base mb-4">
            Fingerstache flexitarian street art 8-bit waistcoat. ...
          </p>
          <span class="fg-pink-500 inline-flex align-center">Learn More →</span>
        </div>
      </a>
      <!-- Repeated block here -->
      ...
    </div>
  </div>
</section>
```

# Selectors

## Containers

Containers are used to limit the width of content, preventing content from overflowing beyond the
specified size.

### Example:

```html
<div class="container-xl">
  <p>Padding</p>
</div>
```

| Classname    | Max. width | Classname      | Max. width |
| ------------ | ---------- | -------------- | ---------- |
| container-xs | 480px      | container-xs/2 | 240px      |
| container-sm | 640px      | container-sm/2 | 320px      |
| container-md | 768px      | container-md/2 | 384px      |
| container-lg | 1024px     | container-lg/2 | 512px      |
| container-xl | 1280px     | container-xl/2 | 640px      |

## Padding

Padding is used to create space around an element's content, inside of any defined borders.

### Example:

```html
<div class="px-5 py-10">
  <p>Padding</p>
</div>
```

| Classname  | Side       | Values with 1px step | Values with 5px step |
| ---------- | ---------- | -------------------- | -------------------- |
| p-{value}  | around     | [0...10]px           | [15...500]px         |
| px-{value} | horizontal | [0...10]px           | [15...500]px         |
| py-{value} | vertical   | [0...10]px           | [15...500]px         |
| pt-{value} | top        | [0...10]px           | [15...500]px         |
| pb-{value} | bottom     | [0...10]px           | [15...500]px         |
| pl-{value} | left       | [0...10]px           | [15...500]px         |
| pr-{value} | right      | [0...10]px           | [15...500]px         |

## Margins

Margins are used to create space around elements, outside of any defined borders.

### Example:

```html
<div class="mx-5 my-10">
  <p>Padding</p>
</div>
```

| Classname  | Side       | Values with 1px step | Values with 5px step |
| ---------- | ---------- | -------------------- | -------------------- |
| m-{value}  | around     | [0...10]px           | [15...500]px         |
| mx-{value} | horizontal | [0...10]px           | [15...500]px         |
| my-{value} | vertical   | [0...10]px           | [15...500]px         |
| mt-{value} | top        | [0...10]px           | [15...500]px         |
| mb-{value} | bottom     | [0...10]px           | [15...500]px         |
| ml-{value} | left       | [0...10]px           | [15...500]px         |
| mr-{value} | right      | [0...10]px           | [15...500]px         |

## Borders

Borders allow you to specify the style, width, and color of an element's border.

### Example

```html
<div class="mx-5 my-10">
  <p>Padding</p>
</div>
```

### Border with

| Classname  | Side       | Values with 1px step | Values with 5px step |
| ---------- | ---------- | -------------------- | -------------------- |
| b-{value}  | around     | [0...10]px           | [15...500]px         |
| bx-{value} | horizontal | [0...10]px           | [15...500]px         |
| by-{value} | vertical   | [0...10]px           | [15...500]px         |
| bt-{value} | top        | [0...10]px           | [15...500]px         |
| bb-{value} | bottom     | [0...10]px           | [15...500]px         |
| bl-{value} | left       | [0...10]px           | [15...500]px         |
| br-{value} | right      | [0...10]px           | [15...500]px         |

### Border style

| Classname | Usage  | Styles                                                              |
| --------- | ------ | ------------------------------------------------------------------- |
| b-{style} | common | [none\|solid\|dashed\|dotted\|double\|groove\|inset\|outset\|ridge] |
| b-{style} | tables | [collapse\|separate]                                                |

### Border radius

| Classname      | Values with 1px step | Values with 5px step | Specific values |
| -------------- | -------------------- | -------------------- | --------------- |
| radius-{value} | [0...10]px           | [15...500]px         | [1000\|10000]px |

### Floating and Box sizing

| Classname     | Values                    |
| ------------- | ------------------------- |
| float-{value} | [left\|right\|none]       |
| clear-{value} | [left\|right\|both\|none] |
| box-{value}   | [border\|content]         |

# Production build

We strongly recommend to use `postcss` with `autoprefixer` and `postcss-purgecss`. This stack will
extend the CSS rules with browser specific prefixes, like `-webkit` and will remove unused styles in
production build.

```shell
npm i -D postcss autoprefixer @fullhuman/postcss-purgecss
```

Our `postcss.config.js` config. You need to configure the `content` parameter for your project.

```js
module.exports = {
  plugins:
    process.env.NODE_ENV === 'production'
      ? [
          'autoprefixer',
          [
            '@fullhuman/postcss-purgecss',
            {
              content: ['./{pages,components}/**/*.{js,jsx}'],
              safelist: ['html', 'body'],
              defaultExtractor: (content) => content.match(/[\w-/:]+(?<!:)/g) || [],
            },
          ],
        ]
      : ['autoprefixer'],
};
```

## License

MIT License. Copyright (c) 2021 Zsolt Tovis
