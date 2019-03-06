xnpm
=======

[![NPM version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]
[![appveyor build status][appveyor-image]][appveyor-url]
[![David deps][david-image]][david-url]

[npm-image]: https://img.shields.io/npm/v/xnpm.svg?style=flat
[npm-url]: https://npmjs.org/package/xnpm
[travis-image]: https://img.shields.io/travis/xnpm/xnpm.svg?style=flat
[travis-url]: https://travis-ci.org/xnpm/xnpm
[appveyor-image]: https://ci.appveyor.com/api/projects/status/17kfr8eitdi7rljr?svg=true
[appveyor-url]: https://ci.appveyor.com/project/fengmk2/urllib
[david-image]: https://img.shields.io/david/xnpm/xnpm.svg?style=flat
[david-url]: https://david-dm.org/xnpm/xnpm

![logo](https://raw.github.com/xnpm/xnpmjs.org/master/logo.png)

xnpm: npm client for [xnpmjs.org](https://xnpmjs.org)


## Requirements

|        | Minimum | Recommended |
|--------|---------|-------------|
| NodeJS | 4.0.0   | stable      |

## Install

```bash
$ npm install xnpm -g
```

If you're in China, maybe you should install it from our [China mirror](https://npm.taobao.org):

```bash
$ npm install xnpm -g --registry=https://registry.npm.taobao.org
```

## Usage

Support all commands just like `npm`.

### Sync packages from `npm`

```bash
$ xnpm sync [moduleName]
```

### Open package document or git web url

```bash
$ xnpm doc [name]
$ xnpm doc -g [name] # open git web url directly
```

## Build your own private registry npm cli

```bash
$ npm install xnpm -g

# then alias it
$ alias mynpm='xnpm --registry=http://registry.npm.example.com \
  --registryweb=http://npm.example.com \
  --userconfig=$HOME/.mynpmrc'
```

## Install with orginal npm cli

xnpm using [npminstall](https://github.com/xnpm/npminstall) by default.
If you don't like symlink mode for `node_modules`, you can change the installer to orginal npm.
But you will lose the fatest install speed.

```bash
$ xnpm i --by=npm react-native
```

## License

[MIT](LICENSE.txt)
