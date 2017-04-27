# npmdoc-broken-link-checker

#### basic api documentation for  [broken-link-checker (v0.7.4)](https://github.com/stevenvachon/broken-link-checker)  [![npm package](https://img.shields.io/npm/v/npmdoc-broken-link-checker.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-broken-link-checker) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-broken-link-checker.svg)](https://travis-ci.org/npmdoc/node-npmdoc-broken-link-checker)

#### Find broken links, missing images, etc in your HTML.

[![NPM](https://nodei.co/npm/broken-link-checker.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/broken-link-checker)

- [https://npmdoc.github.io/node-npmdoc-broken-link-checker/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-broken-link-checker/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-broken-link-checker/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-broken-link-checker/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-broken-link-checker/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-broken-link-checker/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Steven Vachon",
        "url": "http://www.svachon.com/"
    },
    "bin": {
        "blc": "bin/blc",
        "broken-link-checker": "bin/blc"
    },
    "bugs": {
        "url": "https://github.com/stevenvachon/broken-link-checker/issues"
    },
    "dependencies": {
        "bhttp": "^1.2.1",
        "calmcard": "~0.1.1",
        "chalk": "^1.1.3",
        "char-spinner": "^1.0.1",
        "condense-whitespace": "^1.0.0",
        "default-user-agent": "^1.0.0",
        "errno": "~0.1.4",
        "extend": "^3.0.0",
        "http-equiv-refresh": "^1.0.0",
        "humanize-duration": "^3.9.1",
        "is-stream": "^1.0.1",
        "is-string": "^1.0.4",
        "limited-request-queue": "^2.0.0",
        "link-types": "^1.1.0",
        "maybe-callback": "^2.1.0",
        "nopter": "~0.3.0",
        "parse5": "^2.1.5",
        "robot-directives": "~0.3.0",
        "robots-txt-guard": "~0.1.0",
        "robots-txt-parse": "~0.0.4",
        "urlcache": "~0.6.0",
        "urlobj": "0.0.10"
    },
    "description": "Find broken links, missing images, etc in your HTML.",
    "devDependencies": {
        "chai": "^3.5.0",
        "chai-as-promised": "^5.3.0",
        "chai-like": "~0.1.9",
        "chai-things": "~0.2.0",
        "es6-promise": "^3.2.1",
        "mocha": "^3.0.2",
        "object.assign": "^4.0.4",
        "slashes": "^1.0.5",
        "st": "^1.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "a874a18d1d35f3e937b2ae8347cac2f753d176e8",
        "tarball": "https://registry.npmjs.org/broken-link-checker/-/broken-link-checker-0.7.4.tgz"
    },
    "engines": {
        "node": ">= 0.10"
    },
    "files": [
        "bin",
        "lib",
        "license"
    ],
    "gitHead": "b809bec1dac7bd89162edad37f0263c777f64d75",
    "homepage": "https://github.com/stevenvachon/broken-link-checker",
    "keywords": [
        "404",
        "html",
        "hyperlink",
        "links",
        "seo",
        "url"
    ],
    "license": "MIT",
    "main": "lib",
    "maintainers": [
        {
            "name": "stevenvachon"
        }
    ],
    "name": "broken-link-checker",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/stevenvachon/broken-link-checker.git"
    },
    "scripts": {
        "test": "mocha test/ --reporter spec --check-leaks --bail",
        "test-watch": "mocha test/ --reporter spec --check-leaks --bail -w"
    },
    "version": "0.7.4"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
