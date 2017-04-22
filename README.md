# npmdoc-pdfmake

#### api documentation for  [pdfmake (v0.1.27)](http://pdfmake.org)  [![npm package](https://img.shields.io/npm/v/npmdoc-pdfmake.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-pdfmake) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-pdfmake.svg)](https://travis-ci.org/npmdoc/node-npmdoc-pdfmake)

#### Client/server side PDF printing in pure JavaScript

[![NPM](https://nodei.co/npm/pdfmake.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/pdfmake)

- [https://npmdoc.github.io/node-npmdoc-pdfmake/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-pdfmake/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pdfmake/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pdfmake/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-pdfmake/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-pdfmake/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Bartek Pampuch"
    },
    "bugs": {
        "url": "https://github.com/bpampuch/pdfmake/issues"
    },
    "config": {
        "blanket": {
            "pattern": "src",
            "data-cover-never": [
                "node_modules",
                "tests"
            ]
        }
    },
    "dependencies": {
        "linebreak": "^0.3.0",
        "lodash": "^4.17.4",
        "pdfkit": "^0.8.0"
    },
    "description": "Client/server side PDF printing in pure JavaScript",
    "devDependencies": {
        "brfs": "^1.4.3",
        "expose-loader": "^0.7.3",
        "gulp": "^3.9.1",
        "gulp-each": "^0.5.0",
        "gulp-file-contents-to-json": "^0.2.1",
        "gulp-header": "^1.8.8",
        "gulp-jshint": "^2.0.4",
        "gulp-rename": "^1.2.2",
        "gulp-replace": "^0.5.4",
        "gulp-sourcemaps": "^2.4.1",
        "gulp-spawn-mocha": "^3.1.0",
        "gulp-uglify": "^2.1.2",
        "gulp-util": "^3.0.8",
        "iconv-lite": "^0.4.15",
        "jshint": "^2.9.4",
        "json-loader": "^0.5.4",
        "mocha": "^3.2.0",
        "sinon": "^2.1.0",
        "string-replace-webpack-plugin": "^0.1.3",
        "transform-loader": "^0.2.4",
        "webpack": "^2.3.2",
        "webpack-stream": "^3.2.0"
    },
    "directories": {
        "test": "tests"
    },
    "dist": {
        "shasum": "7c146dabb20a28724fdb56bfd3d42f89bc7c431b",
        "tarball": "https://registry.npmjs.org/pdfmake/-/pdfmake-0.1.27.tgz"
    },
    "gitHead": "ebf896bb1d75c0da62a1cf46892478c6480cceb6",
    "homepage": "http://pdfmake.org",
    "keywords": [
        "pdf",
        "javascript",
        "printing",
        "layout"
    ],
    "license": "MIT",
    "main": "src/printer.js",
    "maintainers": [
        {
            "name": "bpampuch"
        },
        {
            "name": "danawoodman"
        },
        {
            "name": "liborm85"
        },
        {
            "name": "miltador"
        }
    ],
    "name": "pdfmake",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/bpampuch/pdfmake.git"
    },
    "scripts": {
        "build": "gulp build",
        "test": "gulp"
    },
    "version": "0.1.27",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
