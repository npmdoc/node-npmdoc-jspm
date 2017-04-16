# api documentation for  [jspm (v0.16.53)](https://github.com/jspm/jspm)  [![npm package](https://img.shields.io/npm/v/npmdoc-jspm.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-jspm) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-jspm.svg)](https://travis-ci.org/npmdoc/node-npmdoc-jspm)
#### Registry and format agnostic JavaScript package manager

[![NPM](https://nodei.co/npm/jspm.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/jspm)

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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module jspm](#apidoc.module.jspm)
1.  [function <span class="apidocSignatureSpan">jspm.</span>Builder (_config)](#apidoc.element.jspm.Builder)
1.  [function <span class="apidocSignatureSpan">jspm.</span>Loader ()](#apidoc.element.jspm.Loader)
1.  [function <span class="apidocSignatureSpan">jspm.</span>bundle (expression, fileName, options)](#apidoc.element.jspm.bundle)
1.  [function <span class="apidocSignatureSpan">jspm.</span>bundleSFX (expression, fileName, options)](#apidoc.element.jspm.bundleSFX)
1.  [function <span class="apidocSignatureSpan">jspm.</span>dlLoader (transpiler)](#apidoc.element.jspm.dlLoader)
1.  [function <span class="apidocSignatureSpan">jspm.</span>import (name, parentName)](#apidoc.element.jspm.import)
1.  [function <span class="apidocSignatureSpan">jspm.</span>install (name, target, options)](#apidoc.element.jspm.install)
1.  [function <span class="apidocSignatureSpan">jspm.</span>normalize (name, parentName)](#apidoc.element.jspm.normalize)
1.  [function <span class="apidocSignatureSpan">jspm.</span>promptDefaults (_useDefaults)](#apidoc.element.jspm.promptDefaults)
1.  [function <span class="apidocSignatureSpan">jspm.</span>setPackagePath (packagePath)](#apidoc.element.jspm.setPackagePath)
1.  [function <span class="apidocSignatureSpan">jspm.</span>unbundle ()](#apidoc.element.jspm.unbundle)
1.  [function <span class="apidocSignatureSpan">jspm.</span>uninstall (names)](#apidoc.element.jspm.uninstall)
1.  number <span class="apidocSignatureSpan">jspm.</span>_eventsCount
1.  object <span class="apidocSignatureSpan">jspm.</span>Builder.prototype
1.  object <span class="apidocSignatureSpan">jspm.</span>_events
1.  object <span class="apidocSignatureSpan">jspm.</span>api
1.  object <span class="apidocSignatureSpan">jspm.</span>domain
1.  string <span class="apidocSignatureSpan">jspm.</span>version

#### [module jspm.Builder](#apidoc.module.jspm.Builder)
1.  [function <span class="apidocSignatureSpan">jspm.</span>Builder (_config)](#apidoc.element.jspm.Builder.Builder)

#### [module jspm.Builder.prototype](#apidoc.module.jspm.Builder.prototype)
1.  [function <span class="apidocSignatureSpan">jspm.Builder.prototype.</span>buildStatic (expressionOrTree, outFile, opts)](#apidoc.element.jspm.Builder.prototype.buildStatic)
1.  [function <span class="apidocSignatureSpan">jspm.Builder.prototype.</span>bundle (expressionOrTree, outFile, opts)](#apidoc.element.jspm.Builder.prototype.bundle)

#### [module jspm.api](#apidoc.module.jspm.api)
1.  [function <span class="apidocSignatureSpan">jspm.api.</span>Builder (_config)](#apidoc.element.jspm.api.Builder)
1.  [function <span class="apidocSignatureSpan">jspm.api.</span>Loader ()](#apidoc.element.jspm.api.Loader)
1.  [function <span class="apidocSignatureSpan">jspm.api.</span>bundle (expression, fileName, options)](#apidoc.element.jspm.api.bundle)
1.  [function <span class="apidocSignatureSpan">jspm.api.</span>bundleSFX (expression, fileName, options)](#apidoc.element.jspm.api.bundleSFX)
1.  [function <span class="apidocSignatureSpan">jspm.api.</span>dlLoader (transpiler)](#apidoc.element.jspm.api.dlLoader)
1.  [function <span class="apidocSignatureSpan">jspm.api.</span>import (name, parentName)](#apidoc.element.jspm.api.import)
1.  [function <span class="apidocSignatureSpan">jspm.api.</span>install (name, target, options)](#apidoc.element.jspm.api.install)
1.  [function <span class="apidocSignatureSpan">jspm.api.</span>normalize (name, parentName)](#apidoc.element.jspm.api.normalize)
1.  [function <span class="apidocSignatureSpan">jspm.api.</span>promptDefaults (_useDefaults)](#apidoc.element.jspm.api.promptDefaults)
1.  [function <span class="apidocSignatureSpan">jspm.api.</span>setPackagePath (packagePath)](#apidoc.element.jspm.api.setPackagePath)
1.  [function <span class="apidocSignatureSpan">jspm.api.</span>unbundle ()](#apidoc.element.jspm.api.unbundle)
1.  [function <span class="apidocSignatureSpan">jspm.api.</span>uninstall (names)](#apidoc.element.jspm.api.uninstall)
1.  number <span class="apidocSignatureSpan">jspm.api.</span>_eventsCount
1.  object <span class="apidocSignatureSpan">jspm.api.</span>_events
1.  object <span class="apidocSignatureSpan">jspm.api.</span>domain
1.  string <span class="apidocSignatureSpan">jspm.api.</span>version



# <a name="apidoc.module.jspm"></a>[module jspm](#apidoc.module.jspm)

#### <a name="apidoc.element.jspm.Builder"></a>[function <span class="apidocSignatureSpan">jspm.</span>Builder (_config)](#apidoc.element.jspm.Builder)
- description and source-code
```javascript
function Builder(_config) {
  config.loadSync();
  SystemJSBuilder.call(this, toFileURL(config.pjson.baseURL));

  var cfg = config.loader.getConfig();

  if (cfg.depCache)
    delete cfg.depCache;
  if (cfg.bundles)
    delete cfg.bundles;
  if (cfg.baseURL)
    delete cfg.baseURL;

  this.config(cfg, true);

  if (typeof _config == 'object')
    this.config(_config, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jspm.Loader"></a>[function <span class="apidocSignatureSpan">jspm.</span>Loader ()](#apidoc.element.jspm.Loader)
- description and source-code
```javascript
Loader = function () {
  config.loadSync();

  var cfg = config.loader.getConfig();
  cfg.baseURL = toFileURL(config.pjson.baseURL);

  var loader = new SystemJSLoader();
  loader.config(cfg);

  return loader;
}
```
- example usage
```shell
...

/*
 * Loader API
 */

var apiLoader;
API.normalize = function(name, parentName) {
  apiLoader = apiLoader || new API.Loader();
  return apiLoader.normalize(name, parentName);
};

API.import = function(name, parentName) {
  apiLoader = apiLoader || new API.Loader();
  return apiLoader.import(name, parentName);
};
...
```

#### <a name="apidoc.element.jspm.bundle"></a>[function <span class="apidocSignatureSpan">jspm.</span>bundle (expression, fileName, options)](#apidoc.element.jspm.bundle)
- description and source-code
```javascript
bundle = function (expression, fileName, options) {
  return bundle.bundle(expression, fileName, options);
}
```
- example usage
```shell
...
*/
API.Builder = bundle.Builder;

// options.inject
// options.sourceMaps
// options.minify
API.bundle = function(expression, fileName, options) {
 return bundle.bundle(expression, fileName, options);
};

/*
* Remove the bundle configuration.
* This will allow you to move back to separate file mode
* returns a promise
*/
...
```

#### <a name="apidoc.element.jspm.bundleSFX"></a>[function <span class="apidocSignatureSpan">jspm.</span>bundleSFX (expression, fileName, options)](#apidoc.element.jspm.bundleSFX)
- description and source-code
```javascript
bundleSFX = function (expression, fileName, options) {
  return bundle.bundleSFX(expression, fileName, options);
}
```
- example usage
```shell
...

/*
* Creates a distributable script file that can be used entirely on its own independent of SystemJS and jspm.
* returns a promise
* options.minify, options.sourceMaps
*/
API.bundleSFX = function(expression, fileName, options) {
 return bundle.bundleSFX(expression, fileName, options);
};


/*
* Package Management API
*
...
```

#### <a name="apidoc.element.jspm.dlLoader"></a>[function <span class="apidocSignatureSpan">jspm.</span>dlLoader (transpiler)](#apidoc.element.jspm.dlLoader)
- description and source-code
```javascript
dlLoader = function (transpiler) {
  return core.checkDlLoader(transpiler);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jspm.import"></a>[function <span class="apidocSignatureSpan">jspm.</span>import (name, parentName)](#apidoc.element.jspm.import)
- description and source-code
```javascript
import = function (name, parentName) {
  apiLoader = apiLoader || new API.Loader();
  return apiLoader.import(name, parentName);
}
```
- example usage
```shell
...
API.normalize = function(name, parentName) {
apiLoader = apiLoader || new API.Loader();
return apiLoader.normalize(name, parentName);
};

API.import = function(name, parentName) {
apiLoader = apiLoader || new API.Loader();
return apiLoader.import(name, parentName);
};

API.Loader = function() {
config.loadSync();

var cfg = config.loader.getConfig();
cfg.baseURL = toFileURL(config.pjson.baseURL);
...
```

#### <a name="apidoc.element.jspm.install"></a>[function <span class="apidocSignatureSpan">jspm.</span>install (name, target, options)](#apidoc.element.jspm.install)
- description and source-code
```javascript
install = function (name, target, options) {
  return install.install(name, target, options);
}
```
- example usage
```shell
...
* Package Management API
*

/*
* Installs a library in the current folder
* returns a promise
*
* jspm.install('jquery')
* jspm.install('jquery', 'github:components/jquery@^2.0.0')
* jspm.install('jquery', '2')
* jspm.install('jquery', 'github:components/jquery')
* jspm.install('jquery', { force: true });
* jspm.install({ jquery: '1.2.3' }, { force: true })
* jspm.install(true, options) // install from package.json
*
...
```

#### <a name="apidoc.element.jspm.normalize"></a>[function <span class="apidocSignatureSpan">jspm.</span>normalize (name, parentName)](#apidoc.element.jspm.normalize)
- description and source-code
```javascript
normalize = function (name, parentName) {
  apiLoader = apiLoader || new API.Loader();
  return apiLoader.normalize(name, parentName);
}
```
- example usage
```shell
...
/*
 * Loader API
 */

var apiLoader;
API.normalize = function(name, parentName) {
  apiLoader = apiLoader || new API.Loader();
  return apiLoader.normalize(name, parentName);
};

API.import = function(name, parentName) {
  apiLoader = apiLoader || new API.Loader();
  return apiLoader.import(name, parentName);
};
...
```

#### <a name="apidoc.element.jspm.promptDefaults"></a>[function <span class="apidocSignatureSpan">jspm.</span>promptDefaults (_useDefaults)](#apidoc.element.jspm.promptDefaults)
- description and source-code
```javascript
promptDefaults = function (_useDefaults) {
  ui.useDefaults(_useDefaults);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jspm.setPackagePath"></a>[function <span class="apidocSignatureSpan">jspm.</span>setPackagePath (packagePath)](#apidoc.element.jspm.setPackagePath)
- description and source-code
```javascript
setPackagePath = function (packagePath) {
  if (config.loaded && process.env.jspmConfigPath !== path.resolve(packagePath, 'package.json'))
    throw new Error('Configuration has already been loaded. Call setPackagePath before using other APIs.');
  process.env.jspmConfigPath = path.resolve(packagePath, 'package.json');
}
```
- example usage
```shell
...
var API = module.exports = new EventEmitter();

API.setPackagePath = function(packagePath) {
 if (config.loaded && process.env.jspmConfigPath !== path.resolve(packagePath, 'package.json'))
   throw new Error('Configuration has already been loaded. Call setPackagePath before using other APIs.');
 process.env.jspmConfigPath = path.resolve(packagePath, 'package.json');
};
API.setPackagePath('.');

/*
* jspm.on('log', function(type, msg) { console.log(msg); });
* jspm.on('prompt', function(prompt, callback) {
*   if (prompt.type == 'confirm')
*     callback({ confirm: true });
*   if (prompt.type == 'input')
...
```

#### <a name="apidoc.element.jspm.unbundle"></a>[function <span class="apidocSignatureSpan">jspm.</span>unbundle ()](#apidoc.element.jspm.unbundle)
- description and source-code
```javascript
unbundle = function () {
  return bundle.unbundle();
}
```
- example usage
```shell
...

/*
* Remove the bundle configuration.
* This will allow you to move back to separate file mode
* returns a promise
*/
API.unbundle = function() {
 return bundle.unbundle();
};


/*
* Creates a distributable script file that can be used entirely on its own independent of SystemJS and jspm.
* returns a promise
* options.minify, options.sourceMaps
...
```

#### <a name="apidoc.element.jspm.uninstall"></a>[function <span class="apidocSignatureSpan">jspm.</span>uninstall (names)](#apidoc.element.jspm.uninstall)
- description and source-code
```javascript
uninstall = function (names) {
  return install.uninstall(names);
}
```
- example usage
```shell
...
API.install = function(name, target, options) {
  return install.install(name, target, options);
};

/* Uninstalls a library in the current folder.
 * returns a promise
 *
 * jspm.uninstall('jquery')
 * jspm.uninstall(['jquery', 'handlebars'])
 *
 */
API.uninstall = function(names) {
  return install.uninstall(names);
};
...
```



# <a name="apidoc.module.jspm.Builder"></a>[module jspm.Builder](#apidoc.module.jspm.Builder)

#### <a name="apidoc.element.jspm.Builder.Builder"></a>[function <span class="apidocSignatureSpan">jspm.</span>Builder (_config)](#apidoc.element.jspm.Builder.Builder)
- description and source-code
```javascript
function Builder(_config) {
  config.loadSync();
  SystemJSBuilder.call(this, toFileURL(config.pjson.baseURL));

  var cfg = config.loader.getConfig();

  if (cfg.depCache)
    delete cfg.depCache;
  if (cfg.bundles)
    delete cfg.bundles;
  if (cfg.baseURL)
    delete cfg.baseURL;

  this.config(cfg, true);

  if (typeof _config == 'object')
    this.config(_config, true);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jspm.Builder.prototype"></a>[module jspm.Builder.prototype](#apidoc.module.jspm.Builder.prototype)

#### <a name="apidoc.element.jspm.Builder.prototype.buildStatic"></a>[function <span class="apidocSignatureSpan">jspm.Builder.prototype.</span>buildStatic (expressionOrTree, outFile, opts)](#apidoc.element.jspm.Builder.prototype.buildStatic)
- description and source-code
```javascript
buildStatic = function (expressionOrTree, outFile, opts) {
  if (outFile && typeof outFile === 'object') {
    opts = outFile;
    outFile = undefined;
  }

  opts = opts || {};

  if (outFile)
    opts.outFile = outFile;

  if (!('format' in opts))
    opts.format = 'global';

  if (!('lowResSourceMaps' in opts))
    opts.lowResSourceMaps = true;

  return SystemJSBuilder.prototype.buildStatic.call(this, expressionOrTree, opts);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jspm.Builder.prototype.bundle"></a>[function <span class="apidocSignatureSpan">jspm.Builder.prototype.</span>bundle (expressionOrTree, outFile, opts)](#apidoc.element.jspm.Builder.prototype.bundle)
- description and source-code
```javascript
bundle = function (expressionOrTree, outFile, opts) {
  if (outFile && typeof outFile === 'object') {
    opts = outFile;
    outFile = undefined;
  }

  opts = opts || {};

  if (outFile)
    opts.outFile = outFile;

  if (!('normalize' in opts))
    opts.normalize = true;

  if (!('lowResSourceMaps' in opts))
    opts.lowResSourceMaps = true;

  var self = this;

  return SystemJSBuilder.prototype.bundle.call(this, expressionOrTree, opts)
  .then(function(output) {

    // Add the bundle to config if the inject flag was given
    if (opts.injectConfig && opts.outFile) {
      // NB deprecate
      output.bundleName = output.bundleName || self.getCanonicalName(toFileURL(path.resolve(opts.outFile)));
      var bundleName = output.bundleName;

      if (!config.loader.bundles)
        config.loader.bundles = {};

      config.loader.bundles[bundleName] = output.modules;
      return config.save()
      .then(function() {
        return output;
      });
    }

    return output;
  });
}
```
- example usage
```shell
...
*/
API.Builder = bundle.Builder;

// options.inject
// options.sourceMaps
// options.minify
API.bundle = function(expression, fileName, options) {
 return bundle.bundle(expression, fileName, options);
};

/*
* Remove the bundle configuration.
* This will allow you to move back to separate file mode
* returns a promise
*/
...
```



# <a name="apidoc.module.jspm.api"></a>[module jspm.api](#apidoc.module.jspm.api)

#### <a name="apidoc.element.jspm.api.Builder"></a>[function <span class="apidocSignatureSpan">jspm.api.</span>Builder (_config)](#apidoc.element.jspm.api.Builder)
- description and source-code
```javascript
function Builder(_config) {
  config.loadSync();
  SystemJSBuilder.call(this, toFileURL(config.pjson.baseURL));

  var cfg = config.loader.getConfig();

  if (cfg.depCache)
    delete cfg.depCache;
  if (cfg.bundles)
    delete cfg.bundles;
  if (cfg.baseURL)
    delete cfg.baseURL;

  this.config(cfg, true);

  if (typeof _config == 'object')
    this.config(_config, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jspm.api.Loader"></a>[function <span class="apidocSignatureSpan">jspm.api.</span>Loader ()](#apidoc.element.jspm.api.Loader)
- description and source-code
```javascript
Loader = function () {
  config.loadSync();

  var cfg = config.loader.getConfig();
  cfg.baseURL = toFileURL(config.pjson.baseURL);

  var loader = new SystemJSLoader();
  loader.config(cfg);

  return loader;
}
```
- example usage
```shell
...

/*
 * Loader API
 */

var apiLoader;
API.normalize = function(name, parentName) {
  apiLoader = apiLoader || new API.Loader();
  return apiLoader.normalize(name, parentName);
};

API.import = function(name, parentName) {
  apiLoader = apiLoader || new API.Loader();
  return apiLoader.import(name, parentName);
};
...
```

#### <a name="apidoc.element.jspm.api.bundle"></a>[function <span class="apidocSignatureSpan">jspm.api.</span>bundle (expression, fileName, options)](#apidoc.element.jspm.api.bundle)
- description and source-code
```javascript
bundle = function (expression, fileName, options) {
  return bundle.bundle(expression, fileName, options);
}
```
- example usage
```shell
...
*/
API.Builder = bundle.Builder;

// options.inject
// options.sourceMaps
// options.minify
API.bundle = function(expression, fileName, options) {
 return bundle.bundle(expression, fileName, options);
};

/*
* Remove the bundle configuration.
* This will allow you to move back to separate file mode
* returns a promise
*/
...
```

#### <a name="apidoc.element.jspm.api.bundleSFX"></a>[function <span class="apidocSignatureSpan">jspm.api.</span>bundleSFX (expression, fileName, options)](#apidoc.element.jspm.api.bundleSFX)
- description and source-code
```javascript
bundleSFX = function (expression, fileName, options) {
  return bundle.bundleSFX(expression, fileName, options);
}
```
- example usage
```shell
...

/*
* Creates a distributable script file that can be used entirely on its own independent of SystemJS and jspm.
* returns a promise
* options.minify, options.sourceMaps
*/
API.bundleSFX = function(expression, fileName, options) {
 return bundle.bundleSFX(expression, fileName, options);
};


/*
* Package Management API
*
...
```

#### <a name="apidoc.element.jspm.api.dlLoader"></a>[function <span class="apidocSignatureSpan">jspm.api.</span>dlLoader (transpiler)](#apidoc.element.jspm.api.dlLoader)
- description and source-code
```javascript
dlLoader = function (transpiler) {
  return core.checkDlLoader(transpiler);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jspm.api.import"></a>[function <span class="apidocSignatureSpan">jspm.api.</span>import (name, parentName)](#apidoc.element.jspm.api.import)
- description and source-code
```javascript
import = function (name, parentName) {
  apiLoader = apiLoader || new API.Loader();
  return apiLoader.import(name, parentName);
}
```
- example usage
```shell
...
API.normalize = function(name, parentName) {
apiLoader = apiLoader || new API.Loader();
return apiLoader.normalize(name, parentName);
};

API.import = function(name, parentName) {
apiLoader = apiLoader || new API.Loader();
return apiLoader.import(name, parentName);
};

API.Loader = function() {
config.loadSync();

var cfg = config.loader.getConfig();
cfg.baseURL = toFileURL(config.pjson.baseURL);
...
```

#### <a name="apidoc.element.jspm.api.install"></a>[function <span class="apidocSignatureSpan">jspm.api.</span>install (name, target, options)](#apidoc.element.jspm.api.install)
- description and source-code
```javascript
install = function (name, target, options) {
  return install.install(name, target, options);
}
```
- example usage
```shell
...
* Package Management API
*

/*
* Installs a library in the current folder
* returns a promise
*
* jspm.install('jquery')
* jspm.install('jquery', 'github:components/jquery@^2.0.0')
* jspm.install('jquery', '2')
* jspm.install('jquery', 'github:components/jquery')
* jspm.install('jquery', { force: true });
* jspm.install({ jquery: '1.2.3' }, { force: true })
* jspm.install(true, options) // install from package.json
*
...
```

#### <a name="apidoc.element.jspm.api.normalize"></a>[function <span class="apidocSignatureSpan">jspm.api.</span>normalize (name, parentName)](#apidoc.element.jspm.api.normalize)
- description and source-code
```javascript
normalize = function (name, parentName) {
  apiLoader = apiLoader || new API.Loader();
  return apiLoader.normalize(name, parentName);
}
```
- example usage
```shell
...
/*
 * Loader API
 */

var apiLoader;
API.normalize = function(name, parentName) {
  apiLoader = apiLoader || new API.Loader();
  return apiLoader.normalize(name, parentName);
};

API.import = function(name, parentName) {
  apiLoader = apiLoader || new API.Loader();
  return apiLoader.import(name, parentName);
};
...
```

#### <a name="apidoc.element.jspm.api.promptDefaults"></a>[function <span class="apidocSignatureSpan">jspm.api.</span>promptDefaults (_useDefaults)](#apidoc.element.jspm.api.promptDefaults)
- description and source-code
```javascript
promptDefaults = function (_useDefaults) {
  ui.useDefaults(_useDefaults);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jspm.api.setPackagePath"></a>[function <span class="apidocSignatureSpan">jspm.api.</span>setPackagePath (packagePath)](#apidoc.element.jspm.api.setPackagePath)
- description and source-code
```javascript
setPackagePath = function (packagePath) {
  if (config.loaded && process.env.jspmConfigPath !== path.resolve(packagePath, 'package.json'))
    throw new Error('Configuration has already been loaded. Call setPackagePath before using other APIs.');
  process.env.jspmConfigPath = path.resolve(packagePath, 'package.json');
}
```
- example usage
```shell
...
var API = module.exports = new EventEmitter();

API.setPackagePath = function(packagePath) {
 if (config.loaded && process.env.jspmConfigPath !== path.resolve(packagePath, 'package.json'))
   throw new Error('Configuration has already been loaded. Call setPackagePath before using other APIs.');
 process.env.jspmConfigPath = path.resolve(packagePath, 'package.json');
};
API.setPackagePath('.');

/*
* jspm.on('log', function(type, msg) { console.log(msg); });
* jspm.on('prompt', function(prompt, callback) {
*   if (prompt.type == 'confirm')
*     callback({ confirm: true });
*   if (prompt.type == 'input')
...
```

#### <a name="apidoc.element.jspm.api.unbundle"></a>[function <span class="apidocSignatureSpan">jspm.api.</span>unbundle ()](#apidoc.element.jspm.api.unbundle)
- description and source-code
```javascript
unbundle = function () {
  return bundle.unbundle();
}
```
- example usage
```shell
...

/*
* Remove the bundle configuration.
* This will allow you to move back to separate file mode
* returns a promise
*/
API.unbundle = function() {
 return bundle.unbundle();
};


/*
* Creates a distributable script file that can be used entirely on its own independent of SystemJS and jspm.
* returns a promise
* options.minify, options.sourceMaps
...
```

#### <a name="apidoc.element.jspm.api.uninstall"></a>[function <span class="apidocSignatureSpan">jspm.api.</span>uninstall (names)](#apidoc.element.jspm.api.uninstall)
- description and source-code
```javascript
uninstall = function (names) {
  return install.uninstall(names);
}
```
- example usage
```shell
...
API.install = function(name, target, options) {
  return install.install(name, target, options);
};

/* Uninstalls a library in the current folder.
 * returns a promise
 *
 * jspm.uninstall('jquery')
 * jspm.uninstall(['jquery', 'handlebars'])
 *
 */
API.uninstall = function(names) {
  return install.uninstall(names);
};
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
