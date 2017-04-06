# api documentation for  [broken-link-checker (v0.7.4)](https://github.com/stevenvachon/broken-link-checker)  [![npm package](https://img.shields.io/npm/v/npmdoc-broken-link-checker.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-broken-link-checker) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-broken-link-checker.svg)](https://travis-ci.org/npmdoc/node-npmdoc-broken-link-checker)
#### Find broken links, missing images, etc in your HTML.

[![NPM](https://nodei.co/npm/broken-link-checker.png?downloads=true)](https://www.npmjs.com/package/broken-link-checker)

[![apidoc](https://npmdoc.github.io/node-npmdoc-broken-link-checker/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-broken-link-checker_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-broken-link-checker/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-broken-link-checker/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-broken-link-checker/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Steven Vachon",
        "email": "contact@svachon.com",
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
            "name": "stevenvachon",
            "email": "contact@svachon.com"
        }
    ],
    "name": "broken-link-checker",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module broken-link-checker](#apidoc.module.broken-link-checker)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.</span>HtmlChecker (options, handlers)](#apidoc.element.broken-link-checker.HtmlChecker)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.</span>HtmlUrlChecker (options, handlers)](#apidoc.element.broken-link-checker.HtmlUrlChecker)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.</span>SiteChecker (options, handlers)](#apidoc.element.broken-link-checker.SiteChecker)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.</span>UrlChecker (options, handlers)](#apidoc.element.broken-link-checker.UrlChecker)
1.  object <span class="apidocSignatureSpan">broken-link-checker.</span>HtmlChecker.prototype
1.  object <span class="apidocSignatureSpan">broken-link-checker.</span>HtmlUrlChecker.prototype
1.  object <span class="apidocSignatureSpan">broken-link-checker.</span>SiteChecker.prototype
1.  object <span class="apidocSignatureSpan">broken-link-checker.</span>UrlChecker.prototype
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>BLC_EXTERNAL
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>BLC_HTML
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>BLC_INTERNAL
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>BLC_INVALID
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>BLC_KEYWORD
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>BLC_ROBOTS
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>BLC_SAMEPAGE
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>BLC_SCHEME
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>BLC_UNKNOWN
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EACCES
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EADDRINFO
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EADDRINUSE
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EADDRNOTAVAIL
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EAFNOSUPPORT
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EAGAIN
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EAIFAMNOSUPPORT
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EAISERVICE
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EAISOCKTYPE
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EALREADY
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EBADF
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EBUSY
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ECANCELED
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ECHARSET
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ECONNABORTED
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ECONNREFUSED
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ECONNRESET
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EDESTADDRREQ
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EEXIST
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EFAULT
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EHOSTUNREACH
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EINTR
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EINVAL
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EIO
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EISCONN
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EISDIR
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ELOOP
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EMFILE
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EMSGSIZE
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENAMETOOLONG
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENETDOWN
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENETUNREACH
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENFILE
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENOBUFS
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENODEV
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENOENT
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENOMEM
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENONET
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENOSPC
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENOSYS
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENOTCONN
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENOTDIR
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENOTEMPTY
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENOTFOUND
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENOTSOCK
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ENOTSUP
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EOF
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EPERM
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EPIPE
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EPROTO
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EPROTONOSUPPORT
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EPROTOTYPE
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EROFS
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ESHUTDOWN
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ESPIPE
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ESRCH
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_ETIMEDOUT
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_EXDEV
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_OK
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>ERRNO_UNKNOWN
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_100
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_101
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_102
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_200
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_201
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_202
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_203
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_204
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_205
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_206
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_207
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_208
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_226
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_300
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_301
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_302
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_303
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_304
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_305
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_307
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_308
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_400
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_401
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_402
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_403
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_404
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_405
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_406
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_407
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_408
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_409
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_410
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_411
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_412
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_413
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_414
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_415
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_416
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_417
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_418
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_421
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_422
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_423
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_424
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_425
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_426
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_428
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_429
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_431
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_451
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_500
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_501
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_502
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_503
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_504
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_505
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_506
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_507
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_508
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_509
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_510
1.  string <span class="apidocSignatureSpan">broken-link-checker.</span>HTTP_511

#### [module broken-link-checker.HtmlChecker](#apidoc.module.broken-link-checker.HtmlChecker)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.</span>HtmlChecker (options, handlers)](#apidoc.element.broken-link-checker.HtmlChecker.HtmlChecker)

#### [module broken-link-checker.HtmlChecker.prototype](#apidoc.module.broken-link-checker.HtmlChecker.prototype)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>__getCache ()](#apidoc.element.broken-link-checker.HtmlChecker.prototype.__getCache)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>clearCache ()](#apidoc.element.broken-link-checker.HtmlChecker.prototype.clearCache)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>numActiveLinks ()](#apidoc.element.broken-link-checker.HtmlChecker.prototype.numActiveLinks)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>numQueuedLinks ()](#apidoc.element.broken-link-checker.HtmlChecker.prototype.numQueuedLinks)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>pause ()](#apidoc.element.broken-link-checker.HtmlChecker.prototype.pause)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>resume ()](#apidoc.element.broken-link-checker.HtmlChecker.prototype.resume)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>scan (html, baseUrl, robots)](#apidoc.element.broken-link-checker.HtmlChecker.prototype.scan)

#### [module broken-link-checker.HtmlUrlChecker](#apidoc.module.broken-link-checker.HtmlUrlChecker)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.</span>HtmlUrlChecker (options, handlers)](#apidoc.element.broken-link-checker.HtmlUrlChecker.HtmlUrlChecker)

#### [module broken-link-checker.HtmlUrlChecker.prototype](#apidoc.module.broken-link-checker.HtmlUrlChecker.prototype)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>__getCache ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.__getCache)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>clearCache ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.clearCache)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>dequeue (id)](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.dequeue)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>enqueue (pageUrl, customData)](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.enqueue)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>numActiveLinks ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.numActiveLinks)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>numPages ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.numPages)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>numQueuedLinks ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.numQueuedLinks)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>pause ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.pause)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>resume ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.resume)

#### [module broken-link-checker.SiteChecker](#apidoc.module.broken-link-checker.SiteChecker)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.</span>SiteChecker (options, handlers)](#apidoc.element.broken-link-checker.SiteChecker.SiteChecker)

#### [module broken-link-checker.SiteChecker.prototype](#apidoc.module.broken-link-checker.SiteChecker.prototype)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>clearCache ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.clearCache)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>dequeue (id)](#apidoc.element.broken-link-checker.SiteChecker.prototype.dequeue)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>enqueue (firstPageUrl, customData)](#apidoc.element.broken-link-checker.SiteChecker.prototype.enqueue)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>numActiveLinks ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.numActiveLinks)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>numPages ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.numPages)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>numQueuedLinks ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.numQueuedLinks)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>numSites ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.numSites)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>pause ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.pause)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>resume ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.resume)

#### [module broken-link-checker.UrlChecker](#apidoc.module.broken-link-checker.UrlChecker)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.</span>UrlChecker (options, handlers)](#apidoc.element.broken-link-checker.UrlChecker.UrlChecker)

#### [module broken-link-checker.UrlChecker.prototype](#apidoc.module.broken-link-checker.UrlChecker.prototype)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>__getCache ()](#apidoc.element.broken-link-checker.UrlChecker.prototype.__getCache)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>clearCache ()](#apidoc.element.broken-link-checker.UrlChecker.prototype.clearCache)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>dequeue (id)](#apidoc.element.broken-link-checker.UrlChecker.prototype.dequeue)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>enqueue (url, baseUrl, customData)](#apidoc.element.broken-link-checker.UrlChecker.prototype.enqueue)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>numActiveLinks ()](#apidoc.element.broken-link-checker.UrlChecker.prototype.numActiveLinks)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>numQueuedLinks ()](#apidoc.element.broken-link-checker.UrlChecker.prototype.numQueuedLinks)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>pause ()](#apidoc.element.broken-link-checker.UrlChecker.prototype.pause)
1.  [function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>resume ()](#apidoc.element.broken-link-checker.UrlChecker.prototype.resume)



# <a name="apidoc.module.broken-link-checker"></a>[module broken-link-checker](#apidoc.module.broken-link-checker)

#### <a name="apidoc.element.broken-link-checker.HtmlChecker"></a>[function <span class="apidocSignatureSpan">broken-link-checker.</span>HtmlChecker (options, handlers)](#apidoc.element.broken-link-checker.HtmlChecker)
- description and source-code
```javascript
function HtmlChecker(options, handlers)
{
	var thisObj = this;
	
	reset(this);
	
	this.handlers = handlers || {};
	this.options = options = parseOptions(options);
	
	this.urlChecker = new UrlChecker(this.options,
	{
		link: function(result)
		{
			maybeCallback(thisObj.handlers.link)(result);
		},
		end: function()
		{
			// If stream finished
			if (thisObj.parsed === true)
			{
				complete(thisObj);
			}
		}
	});
}
```
- example usage
```shell
...
npm install broken-link-checker
'''
The rest of this document will assist you with how to use the API.


## Classes

### 'blc.HtmlChecker(options, handlers)'
Scans an HTML document to find broken links.

* 'handlers.complete' is fired after the last result or zero results.
* 'handlers.html' is fired after the HTML document has been fully parsed.
  * 'tree' is supplied by [parse5](https://npmjs.com/parse5)
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
...
```

#### <a name="apidoc.element.broken-link-checker.HtmlUrlChecker"></a>[function <span class="apidocSignatureSpan">broken-link-checker.</span>HtmlUrlChecker (options, handlers)](#apidoc.element.broken-link-checker.HtmlUrlChecker)
- description and source-code
```javascript
function HtmlUrlChecker(options, handlers)
{
	var thisObj = this;
	
	reset(this);
	
	this.handlers = handlers || {};
	this.options = options = parseOptions(options);
	
	this.htmlUrlQueue = new RequestQueue(
	{
		maxSockets: 1,
		rateLimit: this.options.rateLimit
	},
	{
		item: function(input, done)
		{
			thisObj.currentCustomData = input.data.customData;
			thisObj.currentDone = done;
			thisObj.currentPageUrl = input.url;
			
			streamHtml(thisObj.currentPageUrl, thisObj.__getCache(), thisObj.options).then( function(result)
			{
				thisObj.currentResponse = result.response;
				
				thisObj.currentRobots = new RobotDirectives({ userAgent: thisObj.options.userAgent });
				
				robotHeaders(thisObj);
				
				// Passes robots instance so that headers are included in robot exclusion checks
				thisObj.htmlChecker.scan(result.stream, result.response.url, thisObj.currentRobots);
			})
			.catch( function(error)
			{
				completedPage(thisObj, error);
			});
		},
		end: function()
		{
			// Clear references for garbage collection
			reset(thisObj);
			
			maybeCallback(thisObj.handlers.end)();
		}
	});
	
	this.htmlChecker = new HtmlChecker(this.options,
	{
		html: function(tree, robots)
		{
			maybeCallback(thisObj.handlers.html)(tree, robots, thisObj.currentResponse, thisObj.currentPageUrl, thisObj.currentCustomData
);
		},
		_filter: function(result)
		{
			// Undocumented handler for excluding links via custom constraints
			return maybeCallback(thisObj.handlers._filter)(result);
		},
		junk: function(result)
		{
			maybeCallback(thisObj.handlers.junk)(result, thisObj.currentCustomData);
		},
		link: function(result)
		{
			maybeCallback(thisObj.handlers.link)(result, thisObj.currentCustomData);
		},
		complete: function()
		{
			completedPage(thisObj, null);
		}
	});
}
```
- example usage
```shell
...
	link: function(result){},
	complete: function(){}
});

htmlChecker.scan(html, baseUrl);
'''

### 'blc.HtmlUrlChecker(options, handlers)'
Scans the HTML content at each queued URL to find broken links.

* 'handlers.end' is fired when the end of the queue has been reached.
* 'handlers.html' is fired after a page's HTML document has been fully parsed.
  * 'tree' is supplied by [parse5](https://npmjs.com/parse5).
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' and 'X-Robots-Tag'
robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
...
```

#### <a name="apidoc.element.broken-link-checker.SiteChecker"></a>[function <span class="apidocSignatureSpan">broken-link-checker.</span>SiteChecker (options, handlers)](#apidoc.element.broken-link-checker.SiteChecker)
- description and source-code
```javascript
function SiteChecker(options, handlers)
{
	var thisObj = this;
	
	reset(this);
	
	this.handlers = handlers || {};
	this.options = options = parseOptions(options);
	
	this.sitePagesChecked = new UrlCache({ expiryTime: this.options.cacheExpiryTime });
	
	this.siteUrlQueue = new RequestQueue(
	{
		maxSockets: 1,
		rateLimit: this.options.rateLimit
	},
	{
		item: function(input, done)
		{
			thisObj.currentCustomData = input.data.customData;
			thisObj.currentDone = done;
			thisObj.currentSiteUrl = input.url;  // TODO :: strip after hostname?
			
			// Support checking sites multiple times
			thisObj.sitePagesChecked.clear();
			
			if (options.honorRobotExclusions === true)
			{
				getRobotsTxt(thisObj.currentSiteUrl, options).then( function(robots)
				{
					thisObj.currentRobotsTxt = robots;
					
					maybeCallback(thisObj.handlers.robots)(robots, thisObj.currentCustomData);
				<span class="apidocCodeCommentSpan">/*})
				.catch( function(error)
				{
					maybeCallback(thisObj.handlers.robots)(error, null);
				})
				.then( function()
				{*/
</span>					enqueuePage(thisObj, thisObj.currentSiteUrl, thisObj.currentCustomData);
				});
			}
			else
			{
				enqueuePage(thisObj, thisObj.currentSiteUrl, thisObj.currentCustomData);
			}
		},
		end: function()
		{
			// Reduce memory usage
			thisObj.sitePagesChecked.clear();
			
			// Clear references for garbage collection
			reset(thisObj);
			
			maybeCallback(thisObj.handlers.end)();
		}
	});
	
	this.htmlUrlChecker = new HtmlUrlChecker(this.options,
	{
		html: function(tree, robots, response, pageUrl, customData)
		{
			// If was redirected
			if (response.url !== pageUrl)
			{
				thisObj.sitePagesChecked.set(response.url, true);
				
				for (var i=0; i<response.redirects.length; i++)
				{
					// Avoid rechecking any redirected pages
					thisObj.sitePagesChecked.set( response.redirects[i].url, true );
				}
			}
			
			maybeCallback(thisObj.handlers.html)(tree, robots, response, pageUrl, customData);
		},
		_filter: function(result)  // undocumented handler
		{
			// Additional filters for excluding links
			return maybeCheckLink(thisObj, result);
		},
		junk: function(result, customData)
		{
			maybeCallback(thisObj.handlers.junk)(result, customData);
			
			maybeEnqueuePage(thisObj, result, customData);
		},
		link: function(result, customData)
		{
			maybeCallback(thisObj.handlers.link)(result, customData);
			
			maybeEnqueuePage(thisObj, result, customData);
		},
		page: function(error, pageUrl, customData)
		{
			maybeCallback(thisObj.handlers.page)(error, pageUrl, customData);
			
			// Only the first page should supply an error to "site" handler
			if (thisObj.sitePagesChecked.length() <= 1)
			{
				thisObj.currentPageError = error;
			}
		},
		end: function()
		{
			maybeCallback(thisObj.handlers.site)(thisObj.currentPageError, thisObj.currentSiteUrl, thisObj.currentCustomData);
			
			// Auto-starts next site, if any
			// If not, fires "end"
			thisObj.currentDone();
		}
	});
}
```
- example usage
```shell
...
	page: function(error, pageUrl, customData){},
	end: function(){}
});

htmlUrlChecker.enqueue(pageUrl, customData);
'''

### 'blc.SiteChecker(options, handlers)'
Recursively scans (crawls) the HTML content at each queued URL to find broken links.

* 'handlers.end' is fired when the end of the queue has been reached.
* 'handlers.html' is fired after a page's HTML document has been fully parsed.
  * 'tree' is supplied by [parse5](https://npmjs.com/parse5).
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' and 'X-Robots-Tag'
robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
...
```

#### <a name="apidoc.element.broken-link-checker.UrlChecker"></a>[function <span class="apidocSignatureSpan">broken-link-checker.</span>UrlChecker (options, handlers)](#apidoc.element.broken-link-checker.UrlChecker)
- description and source-code
```javascript
function UrlChecker(options, handlers)
{
	var thisObj = this;
	
	this.handlers = handlers || {};
	this.options = options = parseOptions(options);

	this.cache = new UrlCache(
	{
		expiryTime: this.options.cacheExpiryTime,
		normalizeUrls: false
	});
	
	this.linkQueue = new RequestQueue(
	{
		maxSockets:        this.options.maxSockets,
		maxSocketsPerHost: this.options.maxSocketsPerHost,
		rateLimit:         this.options.rateLimit
	},
	{
		item: function(input, done)
		{
			// TODO :: make this more reusable
			function handle_checkUrl(result)
			{
				maybeCallback(thisObj.handlers.link)(result, input.data.customData);
				
				// Auto-starts next queue item, if any
				// If not, fires "end"
				done();
			}
			
			if (input.data.linkObj !== undefined)
			{
				checkUrl(input.data.linkObj, null, thisObj.cache, thisObj.options).then(handle_checkUrl);
			}
			else
			{
				// TODO :: send url object -- remove orgUrl?
				checkUrl(input.data.orgUrl, input.data.baseUrl, thisObj.cache, thisObj.options).then(handle_checkUrl);
			}
		},
		end: function()
		{
			maybeCallback(thisObj.handlers.end)();
		}
	});
}
```
- example usage
```shell
...
	site: function(error, siteUrl, customData){},
	end: function(){}
});

siteChecker.enqueue(siteUrl, customData);
'''

### 'blc.UrlChecker(options, handlers)'
Requests each queued URL to determine if they are broken.

* 'handlers.end' is fired when the end of the queue has been reached.
* 'handlers.link' is fired for each result (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.dequeue(id)' removes a URL from the queue. Returns 'true' on success or an 'Error' on failure.
...
```



# <a name="apidoc.module.broken-link-checker.HtmlChecker"></a>[module broken-link-checker.HtmlChecker](#apidoc.module.broken-link-checker.HtmlChecker)

#### <a name="apidoc.element.broken-link-checker.HtmlChecker.HtmlChecker"></a>[function <span class="apidocSignatureSpan">broken-link-checker.</span>HtmlChecker (options, handlers)](#apidoc.element.broken-link-checker.HtmlChecker.HtmlChecker)
- description and source-code
```javascript
function HtmlChecker(options, handlers)
{
	var thisObj = this;
	
	reset(this);
	
	this.handlers = handlers || {};
	this.options = options = parseOptions(options);
	
	this.urlChecker = new UrlChecker(this.options,
	{
		link: function(result)
		{
			maybeCallback(thisObj.handlers.link)(result);
		},
		end: function()
		{
			// If stream finished
			if (thisObj.parsed === true)
			{
				complete(thisObj);
			}
		}
	});
}
```
- example usage
```shell
...
npm install broken-link-checker
'''
The rest of this document will assist you with how to use the API.


## Classes

### 'blc.HtmlChecker(options, handlers)'
Scans an HTML document to find broken links.

* 'handlers.complete' is fired after the last result or zero results.
* 'handlers.html' is fired after the HTML document has been fully parsed.
  * 'tree' is supplied by [parse5](https://npmjs.com/parse5)
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
...
```



# <a name="apidoc.module.broken-link-checker.HtmlChecker.prototype"></a>[module broken-link-checker.HtmlChecker.prototype](#apidoc.module.broken-link-checker.HtmlChecker.prototype)

#### <a name="apidoc.element.broken-link-checker.HtmlChecker.prototype.__getCache"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>__getCache ()](#apidoc.element.broken-link-checker.HtmlChecker.prototype.__getCache)
- description and source-code
```javascript
__getCache = function ()
{
	return this.urlChecker.__getCache();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broken-link-checker.HtmlChecker.prototype.clearCache"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>clearCache ()](#apidoc.element.broken-link-checker.HtmlChecker.prototype.clearCache)
- description and source-code
```javascript
clearCache = function ()
{
	return this.urlChecker.clearCache();
}
```
- example usage
```shell
...
* 'handlers.complete' is fired after the last result or zero results.
* 'handlers.html' is fired after the HTML document has been fully parsed.
* 'tree' is supplied by [parse5](https://npmjs.com/parse5)
* 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
* 'html' can be a stream or a string.
* 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.
...
```

#### <a name="apidoc.element.broken-link-checker.HtmlChecker.prototype.numActiveLinks"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>numActiveLinks ()](#apidoc.element.broken-link-checker.HtmlChecker.prototype.numActiveLinks)
- description and source-code
```javascript
numActiveLinks = function ()
{
	return this.urlChecker.numActiveLinks();
}
```
- example usage
```shell
...
* 'handlers.html' is fired after the HTML document has been fully parsed.
* 'tree' is supplied by [parse5](https://npmjs.com/parse5)
* 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
* 'html' can be a stream or a string.
* 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.
...
```

#### <a name="apidoc.element.broken-link-checker.HtmlChecker.prototype.numQueuedLinks"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>numQueuedLinks ()](#apidoc.element.broken-link-checker.HtmlChecker.prototype.numQueuedLinks)
- description and source-code
```javascript
numQueuedLinks = function ()
{
	return this.urlChecker.numQueuedLinks();
}
```
- example usage
```shell
...
  * 'tree' is supplied by [parse5](https://npmjs.com/parse5)
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
  * 'html' can be a stream or a string.
  * 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.

'''js
...
```

#### <a name="apidoc.element.broken-link-checker.HtmlChecker.prototype.pause"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>pause ()](#apidoc.element.broken-link-checker.HtmlChecker.prototype.pause)
- description and source-code
```javascript
pause = function ()
{
	return this.urlChecker.pause();
}
```
- example usage
```shell
...
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
  * 'html' can be a stream or a string.
  * 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.

'''js
var htmlChecker = new blc.HtmlChecker(options, {
...
```

#### <a name="apidoc.element.broken-link-checker.HtmlChecker.prototype.resume"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>resume ()](#apidoc.element.broken-link-checker.HtmlChecker.prototype.resume)
- description and source-code
```javascript
resume = function ()
{
	return this.urlChecker.resume();
}
```
- example usage
```shell
...
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
  * 'html' can be a stream or a string.
  * 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.

'''js
var htmlChecker = new blc.HtmlChecker(options, {
	html: function(tree, robots){},
...
```

#### <a name="apidoc.element.broken-link-checker.HtmlChecker.prototype.scan"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlChecker.prototype.</span>scan (html, baseUrl, robots)](#apidoc.element.broken-link-checker.HtmlChecker.prototype.scan)
- description and source-code
```javascript
scan = function (html, baseUrl, robots)
{
	var tree;
	var thisObj = this;
	
	if (this.active === false)
	{
		// Prevent user error with undocumented arugment
		if (robots instanceof RobotDirectives === false)
		{
			robots = new RobotDirectives({ userAgent: this.options.userAgent });
		}
		
		this.active = true;
		this.baseUrl = baseUrl;
		this.robots = robots;
		
		parseHtml(html).then( function(document)
		{
			tree = document;
			return scrapeHtml(document, thisObj.robots);
		})
		.then( function(links)
		{
			maybeCallback(thisObj.handlers.html)(tree, thisObj.robots);
			
			for (var i=0, numLinks=links.length; i<numLinks; i++)
			{
				enqueueLink(links[i], thisObj);
			}
			
			thisObj.parsed = true;
			
			// If no links found or all links already checked
			if (thisObj.urlChecker.numActiveLinks()===0 && thisObj.urlChecker.numQueuedLinks()===0)
			{
				complete(thisObj);
			}
		});
		
		return true;
	}
	
	return false;
}
```
- example usage
```shell
...
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
  * 'html' can be a stream or a string.
  * 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.

'''js
var htmlChecker = new blc.HtmlChecker(options, {
	html: function(tree, robots){},
	junk: function(result){},
...
```



# <a name="apidoc.module.broken-link-checker.HtmlUrlChecker"></a>[module broken-link-checker.HtmlUrlChecker](#apidoc.module.broken-link-checker.HtmlUrlChecker)

#### <a name="apidoc.element.broken-link-checker.HtmlUrlChecker.HtmlUrlChecker"></a>[function <span class="apidocSignatureSpan">broken-link-checker.</span>HtmlUrlChecker (options, handlers)](#apidoc.element.broken-link-checker.HtmlUrlChecker.HtmlUrlChecker)
- description and source-code
```javascript
function HtmlUrlChecker(options, handlers)
{
	var thisObj = this;
	
	reset(this);
	
	this.handlers = handlers || {};
	this.options = options = parseOptions(options);
	
	this.htmlUrlQueue = new RequestQueue(
	{
		maxSockets: 1,
		rateLimit: this.options.rateLimit
	},
	{
		item: function(input, done)
		{
			thisObj.currentCustomData = input.data.customData;
			thisObj.currentDone = done;
			thisObj.currentPageUrl = input.url;
			
			streamHtml(thisObj.currentPageUrl, thisObj.__getCache(), thisObj.options).then( function(result)
			{
				thisObj.currentResponse = result.response;
				
				thisObj.currentRobots = new RobotDirectives({ userAgent: thisObj.options.userAgent });
				
				robotHeaders(thisObj);
				
				// Passes robots instance so that headers are included in robot exclusion checks
				thisObj.htmlChecker.scan(result.stream, result.response.url, thisObj.currentRobots);
			})
			.catch( function(error)
			{
				completedPage(thisObj, error);
			});
		},
		end: function()
		{
			// Clear references for garbage collection
			reset(thisObj);
			
			maybeCallback(thisObj.handlers.end)();
		}
	});
	
	this.htmlChecker = new HtmlChecker(this.options,
	{
		html: function(tree, robots)
		{
			maybeCallback(thisObj.handlers.html)(tree, robots, thisObj.currentResponse, thisObj.currentPageUrl, thisObj.currentCustomData
);
		},
		_filter: function(result)
		{
			// Undocumented handler for excluding links via custom constraints
			return maybeCallback(thisObj.handlers._filter)(result);
		},
		junk: function(result)
		{
			maybeCallback(thisObj.handlers.junk)(result, thisObj.currentCustomData);
		},
		link: function(result)
		{
			maybeCallback(thisObj.handlers.link)(result, thisObj.currentCustomData);
		},
		complete: function()
		{
			completedPage(thisObj, null);
		}
	});
}
```
- example usage
```shell
...
	link: function(result){},
	complete: function(){}
});

htmlChecker.scan(html, baseUrl);
'''

### 'blc.HtmlUrlChecker(options, handlers)'
Scans the HTML content at each queued URL to find broken links.

* 'handlers.end' is fired when the end of the queue has been reached.
* 'handlers.html' is fired after a page's HTML document has been fully parsed.
  * 'tree' is supplied by [parse5](https://npmjs.com/parse5).
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' and 'X-Robots-Tag'
robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
...
```



# <a name="apidoc.module.broken-link-checker.HtmlUrlChecker.prototype"></a>[module broken-link-checker.HtmlUrlChecker.prototype](#apidoc.module.broken-link-checker.HtmlUrlChecker.prototype)

#### <a name="apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.__getCache"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>__getCache ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.__getCache)
- description and source-code
```javascript
__getCache = function ()
{
	return this.htmlChecker.__getCache();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.clearCache"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>clearCache ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.clearCache)
- description and source-code
```javascript
clearCache = function ()
{
	return this.htmlChecker.clearCache();
}
```
- example usage
```shell
...
* 'handlers.complete' is fired after the last result or zero results.
* 'handlers.html' is fired after the HTML document has been fully parsed.
* 'tree' is supplied by [parse5](https://npmjs.com/parse5)
* 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
* 'html' can be a stream or a string.
* 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.
...
```

#### <a name="apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.dequeue"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>dequeue (id)](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.dequeue)
- description and source-code
```javascript
dequeue = function (id)
{
	return this.htmlUrlQueue.dequeue(id);
}
```
- example usage
```shell
...
  * 'tree' is supplied by [parse5](https://npmjs.com/parse5).
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' and 'X-Robots-Tag'
robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not) within the current page.
* 'handlers.page' is fired after a page's last result, on zero results, or if the HTML could not be retrieved.

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.dequeue(id)' removes a page from the queue. Returns 'true' on success or an 'Error' on failure.
* '.enqueue(pageUrl, customData)' adds a page to the queue. Queue items are auto-dequeued when their requests are complete. Returns
 a queue ID on success or an 'Error' on failure.
  * 'customData' is optional data that is stored in the queue item for the page.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numPages()' returns the total number of pages in the queue.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the queue, but will not pause any active requests.
* '.resume()' will resume the queue.
...
```

#### <a name="apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.enqueue"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>enqueue (pageUrl, customData)](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.enqueue)
- description and source-code
```javascript
enqueue = function (pageUrl, customData)
{
	return this.htmlUrlQueue.enqueue(
	{
		url: pageUrl,
		data: { customData:customData }
	});
}
```
- example usage
```shell
...
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' and 'X-Robots-Tag'
robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not) within the current page.
* 'handlers.page' is fired after a page's last result, on zero results, or if the HTML could not be retrieved.

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.dequeue(id)' removes a page from the queue. Returns 'true' on success or an 'Error' on failure.
* '.enqueue(pageUrl, customData)' adds a page to the queue. Queue items are auto-dequeued when their requests are complete. Returns
 a queue ID on success or an 'Error' on failure.
  * 'customData' is optional data that is stored in the queue item for the page.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numPages()' returns the total number of pages in the queue.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the queue, but will not pause any active requests.
* '.resume()' will resume the queue.
...
```

#### <a name="apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.numActiveLinks"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>numActiveLinks ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.numActiveLinks)
- description and source-code
```javascript
numActiveLinks = function ()
{
	return this.htmlChecker.numActiveLinks();
}
```
- example usage
```shell
...
* 'handlers.html' is fired after the HTML document has been fully parsed.
* 'tree' is supplied by [parse5](https://npmjs.com/parse5)
* 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
* 'html' can be a stream or a string.
* 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.
...
```

#### <a name="apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.numPages"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>numPages ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.numPages)
- description and source-code
```javascript
numPages = function ()
{
	return this.htmlUrlQueue.length();
}
```
- example usage
```shell
...
* 'handlers.page' is fired after a page's last result, on zero results, or if the HTML could not be retrieved.

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.dequeue(id)' removes a page from the queue. Returns 'true' on success or an 'Error' on failure.
* '.enqueue(pageUrl, customData)' adds a page to the queue. Queue items are auto-dequeued when their requests are complete. Returns
 a queue ID on success or an 'Error' on failure.
  * 'customData' is optional data that is stored in the queue item for the page.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numPages()' returns the total number of pages in the queue.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the queue, but will not pause any active requests.
* '.resume()' will resume the queue.

'''js
var htmlUrlChecker = new blc.HtmlUrlChecker(options, {
	html: function(tree, robots, response, pageUrl, customData){},
...
```

#### <a name="apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.numQueuedLinks"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>numQueuedLinks ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.numQueuedLinks)
- description and source-code
```javascript
numQueuedLinks = function ()
{
	return this.htmlChecker.numQueuedLinks();
}
```
- example usage
```shell
...
  * 'tree' is supplied by [parse5](https://npmjs.com/parse5)
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
  * 'html' can be a stream or a string.
  * 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.

'''js
...
```

#### <a name="apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.pause"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>pause ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.pause)
- description and source-code
```javascript
pause = function ()
{
	this.htmlChecker.pause();
	return this.htmlUrlQueue.pause();
}
```
- example usage
```shell
...
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
  * 'html' can be a stream or a string.
  * 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.

'''js
var htmlChecker = new blc.HtmlChecker(options, {
...
```

#### <a name="apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.resume"></a>[function <span class="apidocSignatureSpan">broken-link-checker.HtmlUrlChecker.prototype.</span>resume ()](#apidoc.element.broken-link-checker.HtmlUrlChecker.prototype.resume)
- description and source-code
```javascript
resume = function ()
{
	this.htmlChecker.resume();
	return this.htmlUrlQueue.resume();
}
```
- example usage
```shell
...
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
  * 'html' can be a stream or a string.
  * 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.

'''js
var htmlChecker = new blc.HtmlChecker(options, {
	html: function(tree, robots){},
...
```



# <a name="apidoc.module.broken-link-checker.SiteChecker"></a>[module broken-link-checker.SiteChecker](#apidoc.module.broken-link-checker.SiteChecker)

#### <a name="apidoc.element.broken-link-checker.SiteChecker.SiteChecker"></a>[function <span class="apidocSignatureSpan">broken-link-checker.</span>SiteChecker (options, handlers)](#apidoc.element.broken-link-checker.SiteChecker.SiteChecker)
- description and source-code
```javascript
function SiteChecker(options, handlers)
{
	var thisObj = this;
	
	reset(this);
	
	this.handlers = handlers || {};
	this.options = options = parseOptions(options);
	
	this.sitePagesChecked = new UrlCache({ expiryTime: this.options.cacheExpiryTime });
	
	this.siteUrlQueue = new RequestQueue(
	{
		maxSockets: 1,
		rateLimit: this.options.rateLimit
	},
	{
		item: function(input, done)
		{
			thisObj.currentCustomData = input.data.customData;
			thisObj.currentDone = done;
			thisObj.currentSiteUrl = input.url;  // TODO :: strip after hostname?
			
			// Support checking sites multiple times
			thisObj.sitePagesChecked.clear();
			
			if (options.honorRobotExclusions === true)
			{
				getRobotsTxt(thisObj.currentSiteUrl, options).then( function(robots)
				{
					thisObj.currentRobotsTxt = robots;
					
					maybeCallback(thisObj.handlers.robots)(robots, thisObj.currentCustomData);
				<span class="apidocCodeCommentSpan">/*})
				.catch( function(error)
				{
					maybeCallback(thisObj.handlers.robots)(error, null);
				})
				.then( function()
				{*/
</span>					enqueuePage(thisObj, thisObj.currentSiteUrl, thisObj.currentCustomData);
				});
			}
			else
			{
				enqueuePage(thisObj, thisObj.currentSiteUrl, thisObj.currentCustomData);
			}
		},
		end: function()
		{
			// Reduce memory usage
			thisObj.sitePagesChecked.clear();
			
			// Clear references for garbage collection
			reset(thisObj);
			
			maybeCallback(thisObj.handlers.end)();
		}
	});
	
	this.htmlUrlChecker = new HtmlUrlChecker(this.options,
	{
		html: function(tree, robots, response, pageUrl, customData)
		{
			// If was redirected
			if (response.url !== pageUrl)
			{
				thisObj.sitePagesChecked.set(response.url, true);
				
				for (var i=0; i<response.redirects.length; i++)
				{
					// Avoid rechecking any redirected pages
					thisObj.sitePagesChecked.set( response.redirects[i].url, true );
				}
			}
			
			maybeCallback(thisObj.handlers.html)(tree, robots, response, pageUrl, customData);
		},
		_filter: function(result)  // undocumented handler
		{
			// Additional filters for excluding links
			return maybeCheckLink(thisObj, result);
		},
		junk: function(result, customData)
		{
			maybeCallback(thisObj.handlers.junk)(result, customData);
			
			maybeEnqueuePage(thisObj, result, customData);
		},
		link: function(result, customData)
		{
			maybeCallback(thisObj.handlers.link)(result, customData);
			
			maybeEnqueuePage(thisObj, result, customData);
		},
		page: function(error, pageUrl, customData)
		{
			maybeCallback(thisObj.handlers.page)(error, pageUrl, customData);
			
			// Only the first page should supply an error to "site" handler
			if (thisObj.sitePagesChecked.length() <= 1)
			{
				thisObj.currentPageError = error;
			}
		},
		end: function()
		{
			maybeCallback(thisObj.handlers.site)(thisObj.currentPageError, thisObj.currentSiteUrl, thisObj.currentCustomData);
			
			// Auto-starts next site, if any
			// If not, fires "end"
			thisObj.currentDone();
		}
	});
}
```
- example usage
```shell
...
	page: function(error, pageUrl, customData){},
	end: function(){}
});

htmlUrlChecker.enqueue(pageUrl, customData);
'''

### 'blc.SiteChecker(options, handlers)'
Recursively scans (crawls) the HTML content at each queued URL to find broken links.

* 'handlers.end' is fired when the end of the queue has been reached.
* 'handlers.html' is fired after a page's HTML document has been fully parsed.
  * 'tree' is supplied by [parse5](https://npmjs.com/parse5).
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' and 'X-Robots-Tag'
robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
...
```



# <a name="apidoc.module.broken-link-checker.SiteChecker.prototype"></a>[module broken-link-checker.SiteChecker.prototype](#apidoc.module.broken-link-checker.SiteChecker.prototype)

#### <a name="apidoc.element.broken-link-checker.SiteChecker.prototype.clearCache"></a>[function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>clearCache ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.clearCache)
- description and source-code
```javascript
clearCache = function ()
{
	// Does not clear 'sitePagesChecked' because it would mess up any current scans
	return this.htmlUrlChecker.clearCache();
}
```
- example usage
```shell
...
* 'handlers.complete' is fired after the last result or zero results.
* 'handlers.html' is fired after the HTML document has been fully parsed.
* 'tree' is supplied by [parse5](https://npmjs.com/parse5)
* 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
* 'html' can be a stream or a string.
* 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.
...
```

#### <a name="apidoc.element.broken-link-checker.SiteChecker.prototype.dequeue"></a>[function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>dequeue (id)](#apidoc.element.broken-link-checker.SiteChecker.prototype.dequeue)
- description and source-code
```javascript
dequeue = function (id)
{
	return this.siteUrlQueue.dequeue(id);
}
```
- example usage
```shell
...
  * 'tree' is supplied by [parse5](https://npmjs.com/parse5).
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' and 'X-Robots-Tag'
robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not) within the current page.
* 'handlers.page' is fired after a page's last result, on zero results, or if the HTML could not be retrieved.

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.dequeue(id)' removes a page from the queue. Returns 'true' on success or an 'Error' on failure.
* '.enqueue(pageUrl, customData)' adds a page to the queue. Queue items are auto-dequeued when their requests are complete. Returns
 a queue ID on success or an 'Error' on failure.
  * 'customData' is optional data that is stored in the queue item for the page.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numPages()' returns the total number of pages in the queue.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the queue, but will not pause any active requests.
* '.resume()' will resume the queue.
...
```

#### <a name="apidoc.element.broken-link-checker.SiteChecker.prototype.enqueue"></a>[function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>enqueue (firstPageUrl, customData)](#apidoc.element.broken-link-checker.SiteChecker.prototype.enqueue)
- description and source-code
```javascript
enqueue = function (firstPageUrl, customData)
{
	return this.siteUrlQueue.enqueue(
	{
		url: firstPageUrl,
		data: { customData:customData }
	});
}
```
- example usage
```shell
...
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' and 'X-Robots-Tag'
robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not) within the current page.
* 'handlers.page' is fired after a page's last result, on zero results, or if the HTML could not be retrieved.

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.dequeue(id)' removes a page from the queue. Returns 'true' on success or an 'Error' on failure.
* '.enqueue(pageUrl, customData)' adds a page to the queue. Queue items are auto-dequeued when their requests are complete. Returns
 a queue ID on success or an 'Error' on failure.
  * 'customData' is optional data that is stored in the queue item for the page.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numPages()' returns the total number of pages in the queue.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the queue, but will not pause any active requests.
* '.resume()' will resume the queue.
...
```

#### <a name="apidoc.element.broken-link-checker.SiteChecker.prototype.numActiveLinks"></a>[function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>numActiveLinks ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.numActiveLinks)
- description and source-code
```javascript
numActiveLinks = function ()
{
	return this.htmlUrlChecker.numActiveLinks();
}
```
- example usage
```shell
...
* 'handlers.html' is fired after the HTML document has been fully parsed.
* 'tree' is supplied by [parse5](https://npmjs.com/parse5)
* 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
* 'html' can be a stream or a string.
* 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.
...
```

#### <a name="apidoc.element.broken-link-checker.SiteChecker.prototype.numPages"></a>[function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>numPages ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.numPages)
- description and source-code
```javascript
numPages = function ()
{
	return this.htmlUrlChecker.numPages();
}
```
- example usage
```shell
...
* 'handlers.page' is fired after a page's last result, on zero results, or if the HTML could not be retrieved.

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.dequeue(id)' removes a page from the queue. Returns 'true' on success or an 'Error' on failure.
* '.enqueue(pageUrl, customData)' adds a page to the queue. Queue items are auto-dequeued when their requests are complete. Returns
 a queue ID on success or an 'Error' on failure.
  * 'customData' is optional data that is stored in the queue item for the page.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numPages()' returns the total number of pages in the queue.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the queue, but will not pause any active requests.
* '.resume()' will resume the queue.

'''js
var htmlUrlChecker = new blc.HtmlUrlChecker(options, {
	html: function(tree, robots, response, pageUrl, customData){},
...
```

#### <a name="apidoc.element.broken-link-checker.SiteChecker.prototype.numQueuedLinks"></a>[function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>numQueuedLinks ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.numQueuedLinks)
- description and source-code
```javascript
numQueuedLinks = function ()
{
	return this.htmlUrlChecker.numQueuedLinks();
}
```
- example usage
```shell
...
  * 'tree' is supplied by [parse5](https://npmjs.com/parse5)
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
  * 'html' can be a stream or a string.
  * 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.

'''js
...
```

#### <a name="apidoc.element.broken-link-checker.SiteChecker.prototype.numSites"></a>[function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>numSites ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.numSites)
- description and source-code
```javascript
numSites = function ()
{
	return this.siteUrlQueue.length();
}
```
- example usage
```shell
...
* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.dequeue(id)' removes a site from the queue. Returns 'true' on success or an 'Error' on failure.
* '.enqueue(siteUrl, customData)' adds [the first page of] a site to the queue. Queue items are auto-dequeued when their requests
 are complete. Returns a queue ID on success or an 'Error' on failure.
  * 'customData' is optional data that is stored in the queue item for the site.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numPages()' returns the total number of pages in the queue.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.numSites()' returns the total number of sites in the queue.
* '.pause()' will pause the queue, but will not pause any active requests.
* '.resume()' will resume the queue.

**Note:** 'options.filterLevel' is used for determining which links are recursive.

'''js
var siteChecker = new blc.SiteChecker(options, {
...
```

#### <a name="apidoc.element.broken-link-checker.SiteChecker.prototype.pause"></a>[function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>pause ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.pause)
- description and source-code
```javascript
pause = function ()
{
	this.htmlUrlChecker.pause();
	return this.siteUrlQueue.pause();
}
```
- example usage
```shell
...
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
  * 'html' can be a stream or a string.
  * 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.

'''js
var htmlChecker = new blc.HtmlChecker(options, {
...
```

#### <a name="apidoc.element.broken-link-checker.SiteChecker.prototype.resume"></a>[function <span class="apidocSignatureSpan">broken-link-checker.SiteChecker.prototype.</span>resume ()](#apidoc.element.broken-link-checker.SiteChecker.prototype.resume)
- description and source-code
```javascript
resume = function ()
{
	this.htmlUrlChecker.resume();
	return this.siteUrlQueue.resume();
}
```
- example usage
```shell
...
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
  * 'html' can be a stream or a string.
  * 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.

'''js
var htmlChecker = new blc.HtmlChecker(options, {
	html: function(tree, robots){},
...
```



# <a name="apidoc.module.broken-link-checker.UrlChecker"></a>[module broken-link-checker.UrlChecker](#apidoc.module.broken-link-checker.UrlChecker)

#### <a name="apidoc.element.broken-link-checker.UrlChecker.UrlChecker"></a>[function <span class="apidocSignatureSpan">broken-link-checker.</span>UrlChecker (options, handlers)](#apidoc.element.broken-link-checker.UrlChecker.UrlChecker)
- description and source-code
```javascript
function UrlChecker(options, handlers)
{
	var thisObj = this;
	
	this.handlers = handlers || {};
	this.options = options = parseOptions(options);

	this.cache = new UrlCache(
	{
		expiryTime: this.options.cacheExpiryTime,
		normalizeUrls: false
	});
	
	this.linkQueue = new RequestQueue(
	{
		maxSockets:        this.options.maxSockets,
		maxSocketsPerHost: this.options.maxSocketsPerHost,
		rateLimit:         this.options.rateLimit
	},
	{
		item: function(input, done)
		{
			// TODO :: make this more reusable
			function handle_checkUrl(result)
			{
				maybeCallback(thisObj.handlers.link)(result, input.data.customData);
				
				// Auto-starts next queue item, if any
				// If not, fires "end"
				done();
			}
			
			if (input.data.linkObj !== undefined)
			{
				checkUrl(input.data.linkObj, null, thisObj.cache, thisObj.options).then(handle_checkUrl);
			}
			else
			{
				// TODO :: send url object -- remove orgUrl?
				checkUrl(input.data.orgUrl, input.data.baseUrl, thisObj.cache, thisObj.options).then(handle_checkUrl);
			}
		},
		end: function()
		{
			maybeCallback(thisObj.handlers.end)();
		}
	});
}
```
- example usage
```shell
...
	site: function(error, siteUrl, customData){},
	end: function(){}
});

siteChecker.enqueue(siteUrl, customData);
'''

### 'blc.UrlChecker(options, handlers)'
Requests each queued URL to determine if they are broken.

* 'handlers.end' is fired when the end of the queue has been reached.
* 'handlers.link' is fired for each result (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.dequeue(id)' removes a URL from the queue. Returns 'true' on success or an 'Error' on failure.
...
```



# <a name="apidoc.module.broken-link-checker.UrlChecker.prototype"></a>[module broken-link-checker.UrlChecker.prototype](#apidoc.module.broken-link-checker.UrlChecker.prototype)

#### <a name="apidoc.element.broken-link-checker.UrlChecker.prototype.__getCache"></a>[function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>__getCache ()](#apidoc.element.broken-link-checker.UrlChecker.prototype.__getCache)
- description and source-code
```javascript
__getCache = function ()
{
	return this.cache;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broken-link-checker.UrlChecker.prototype.clearCache"></a>[function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>clearCache ()](#apidoc.element.broken-link-checker.UrlChecker.prototype.clearCache)
- description and source-code
```javascript
clearCache = function ()
{
	return this.cache.clear();
}
```
- example usage
```shell
...
* 'handlers.complete' is fired after the last result or zero results.
* 'handlers.html' is fired after the HTML document has been fully parsed.
* 'tree' is supplied by [parse5](https://npmjs.com/parse5)
* 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
* 'html' can be a stream or a string.
* 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.
...
```

#### <a name="apidoc.element.broken-link-checker.UrlChecker.prototype.dequeue"></a>[function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>dequeue (id)](#apidoc.element.broken-link-checker.UrlChecker.prototype.dequeue)
- description and source-code
```javascript
dequeue = function (id)
{
	return this.linkQueue.dequeue(id);
}
```
- example usage
```shell
...
  * 'tree' is supplied by [parse5](https://npmjs.com/parse5).
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' and 'X-Robots-Tag'
robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not) within the current page.
* 'handlers.page' is fired after a page's last result, on zero results, or if the HTML could not be retrieved.

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.dequeue(id)' removes a page from the queue. Returns 'true' on success or an 'Error' on failure.
* '.enqueue(pageUrl, customData)' adds a page to the queue. Queue items are auto-dequeued when their requests are complete. Returns
 a queue ID on success or an 'Error' on failure.
  * 'customData' is optional data that is stored in the queue item for the page.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numPages()' returns the total number of pages in the queue.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the queue, but will not pause any active requests.
* '.resume()' will resume the queue.
...
```

#### <a name="apidoc.element.broken-link-checker.UrlChecker.prototype.enqueue"></a>[function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>enqueue (url, baseUrl, customData)](#apidoc.element.broken-link-checker.UrlChecker.prototype.enqueue)
- description and source-code
```javascript
enqueue = function (url, baseUrl, customData)
{
	// Undocumented internal use: enqueue(linkObj)
	if (isString(url)===false && url.broken_link_checker===true)
	{
		return this.linkQueue.enqueue(
		{
			url: url.url.parsed,
			data: { customData:customData, linkObj:url }
		});
	}
	// Documented use: enqueue(url, baseUrl)
	// or erroneous and let linkQueue sort it out
	else
	{
		return this.linkQueue.enqueue(
		{
			url: urlobj.resolve(baseUrl || "", urlobj.parse(url) ),  // URL must be absolute
			data: { orgUrl:url, baseUrl:baseUrl, customData:customData }
		});
	}
}
```
- example usage
```shell
...
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' and 'X-Robots-Tag'
robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not) within the current page.
* 'handlers.page' is fired after a page's last result, on zero results, or if the HTML could not be retrieved.

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.dequeue(id)' removes a page from the queue. Returns 'true' on success or an 'Error' on failure.
* '.enqueue(pageUrl, customData)' adds a page to the queue. Queue items are auto-dequeued when their requests are complete. Returns
 a queue ID on success or an 'Error' on failure.
  * 'customData' is optional data that is stored in the queue item for the page.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numPages()' returns the total number of pages in the queue.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the queue, but will not pause any active requests.
* '.resume()' will resume the queue.
...
```

#### <a name="apidoc.element.broken-link-checker.UrlChecker.prototype.numActiveLinks"></a>[function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>numActiveLinks ()](#apidoc.element.broken-link-checker.UrlChecker.prototype.numActiveLinks)
- description and source-code
```javascript
numActiveLinks = function ()
{
	return this.linkQueue.numActive();
}
```
- example usage
```shell
...
* 'handlers.html' is fired after the HTML document has been fully parsed.
* 'tree' is supplied by [parse5](https://npmjs.com/parse5)
* 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
* 'html' can be a stream or a string.
* 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.
...
```

#### <a name="apidoc.element.broken-link-checker.UrlChecker.prototype.numQueuedLinks"></a>[function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>numQueuedLinks ()](#apidoc.element.broken-link-checker.UrlChecker.prototype.numQueuedLinks)
- description and source-code
```javascript
numQueuedLinks = function ()
{
	return this.linkQueue.numQueued();
}
```
- example usage
```shell
...
  * 'tree' is supplied by [parse5](https://npmjs.com/parse5)
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
  * 'html' can be a stream or a string.
  * 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.

'''js
...
```

#### <a name="apidoc.element.broken-link-checker.UrlChecker.prototype.pause"></a>[function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>pause ()](#apidoc.element.broken-link-checker.UrlChecker.prototype.pause)
- description and source-code
```javascript
pause = function ()
{
	return this.linkQueue.pause();
}
```
- example usage
```shell
...
  * 'robots' is an instance of [robot-directives](https://npmjs.com/robot-directives) containing any '<meta>' robot exclusions.
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
  * 'html' can be a stream or a string.
  * 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.

'''js
var htmlChecker = new blc.HtmlChecker(options, {
...
```

#### <a name="apidoc.element.broken-link-checker.UrlChecker.prototype.resume"></a>[function <span class="apidocSignatureSpan">broken-link-checker.UrlChecker.prototype.</span>resume ()](#apidoc.element.broken-link-checker.UrlChecker.prototype.resume)
- description and source-code
```javascript
resume = function ()
{
	return this.linkQueue.resume();
}
```
- example usage
```shell
...
* 'handlers.junk' is fired with data on each skipped link, as configured in options.
* 'handlers.link' is fired with the result of each discovered link (broken or not).

* '.clearCache()' will remove any cached URL responses. This is only relevant if the 'cacheResponses' option is enabled.
* '.numActiveLinks()' returns the number of links with active requests.
* '.numQueuedLinks()' returns the number of links that currently have no active requests.
* '.pause()' will pause the internal link queue, but will not pause any active requests.
* '.resume()' will resume the internal link queue.
* '.scan(html, baseUrl)' parses & scans a single HTML document. Returns 'false' when there is a previously incomplete scan (and '
true' otherwise).
  * 'html' can be a stream or a string.
  * 'baseUrl' is the address to which all relative URLs will be made absolute. Without a value, links to relative URLs will output
 an "Invalid URL" error.

'''js
var htmlChecker = new blc.HtmlChecker(options, {
	html: function(tree, robots){},
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
