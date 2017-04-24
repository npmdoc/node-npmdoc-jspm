# npmdoc-jspm

#### api documentation for  [jspm (v0.16.53)](https://github.com/jspm/jspm)  [![npm package](https://img.shields.io/npm/v/npmdoc-jspm.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-jspm) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-jspm.svg)](https://travis-ci.org/npmdoc/node-npmdoc-jspm)

#### Registry and format agnostic JavaScript package manager

[![NPM](https://nodei.co/npm/jspm.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/jspm)

- [https://npmdoc.github.io/node-npmdoc-jspm/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-jspm/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jspm/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jspm/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-jspm/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-jspm/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": "",
    "bin": {
        "jspm": "./jspm.js"
    },
    "bugs": {
        "url": "https://github.com/jspm/jspm/issues"
    },
    "dependencies": {
        "chalk": "^1.1.1",
        "core-js": "^1.2.6",
        "glob": "^6.0.1",
        "graceful-fs": "^4.1.2",
        "jspm-github": "^0.13.17",
        "jspm-npm": "^0.26.12",
        "jspm-registry": "^0.4.0",
        "liftoff": "^2.2.0",
        "minimatch": "^3.0.0",
        "mkdirp": "~0.5.1",
        "ncp": "^2.0.0",
        "proper-lockfile": "^1.1.2",
        "request": "^2.67.0",
        "rimraf": "^2.4.4",
        "rsvp": "^3.1.0",
        "semver": "^5.1.0",
        "systemjs": "0.19.46",
        "systemjs-builder": "0.15.36",
        "traceur": "0.0.105",
        "uglify-js": "^2.6.1"
    },
    "description": "Registry and format agnostic JavaScript package manager",
    "devDependencies": {
        "istanbul": "^0.3.13",
        "jshint": "~2.8.0",
        "mocha": "~2.2.5"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "56f351f49594c8933e5e01b65145acaebfcfb59e",
        "tarball": "https://registry.npmjs.org/jspm/-/jspm-0.16.53.tgz"
    },
    "files": [
        "lib",
        "LICENSE",
        "CONTRIBUTORS",
        "README.md",
        "api.js",
        "cli.js",
        "jspm.js",
        "docs"
    ],
    "gitHead": "4e014a499e17eb812770911f27dbc561a7789e42",
    "homepage": "https://github.com/jspm/jspm",
    "license": "Apache-2.0",
    "main": "./api.js",
    "maintainers": [
        {
            "name": "guybedford"
        }
    ],
    "name": "jspm",
    "optionalDependencies": {},
    "registry": "npm",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/jspm/jspm.git"
    },
    "scripts": {
        "coverage": "npm run istanbul -- --report html",
        "gitbook": "gitbook build docs",
        "istanbul": "istanbul cover ./node_modules/.bin/_mocha -i='lib/**/*.js'",
        "jshint": "jshint api.js cli.js jspm.js lib test",
        "mocha": "mocha",
        "test": "npm run jshint && npm run mocha"
    },
    "version": "0.16.53"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
