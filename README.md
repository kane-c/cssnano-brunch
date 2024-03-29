# cssnano-brunch  [![Greenkeeper badge](https://badges.greenkeeper.io/dlepaux/cssnano-brunch.svg)](https://greenkeeper.io/) [![Build Status][travis-badge]][travis]

- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Example](#example)
- [Testing](#testing)
- [License](#license)

[![NPM](https://nodei.co/npm/cssnano-brunch.png)](https://nodei.co/npm/cssnano-brunch/)
[![NPM](https://nodei.co/npm-dl/cssnano-brunch.png?months=3)](https://nodei.co/npm/cssnano-brunch/)

> A [Brunch][] plugin which optimizes CSS with [CSSNano][].

## <a name="installation"></a> Installation

```sh
npm install --save cssnano-brunch
```

## <a name="configuration"></a> Configuration

See the [CSSNano Options][] for more details.

```coffee
plugins:
  cssnano:
    autoprefixer: {add: true}
```

## <a name="usage"></a> Usage

cssnano-brunch is an optimizer so it will be only enabled in a production environment `brunch build -P`.

## <a name="example"></a> Example

Before
```css
h1::before, h1:before {
    margin: 10px 20px 10px 20px;
    color: #ff0000;
    -webkit-border-radius: 16px;
    border-radius: 16px;
    font-weight: normal;
    font-weight: normal;
    content: 'i ♥ cssnano';
}
/* invalid placement */
@charset "utf-8";
```
After
```css
@charset "utf-8";h1:before{margin:10px 20px;color:red;border-radius:1pc;font-weight:400;content:'i ♥ cssnano'}
```


## <a name="testing"></a> Testing

Just run `npm i && npm test`

## <a name="license"></a> License

MIT

[Brunch]: http://brunch.io
[CSSNano]: http://cssnano.co
[CSSNano Options]: http://cssnano.co/options/
[travis]: https://travis-ci.org/dlepaux/cssnano-brunch
[travis-badge]: https://img.shields.io/travis/dlepaux/cssnano-brunch.svg?style=flat

