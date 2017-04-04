# api documentation for  [uncss (v0.14.1)](https://github.com/giakki/uncss)  [![npm package](https://img.shields.io/npm/v/npmdoc-uncss.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-uncss) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-uncss.svg)](https://travis-ci.org/npmdoc/node-npmdoc-uncss)
#### Remove unused CSS styles

[![NPM](https://nodei.co/npm/uncss.png?downloads=true)](https://www.npmjs.com/package/uncss)

[![apidoc](https://npmdoc.github.io/node-npmdoc-uncss/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-uncss_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-uncss/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-uncss/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-uncss/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Giakki"
    },
    "bin": {
        "uncss": "bin/uncss"
    },
    "bugs": {
        "url": "https://github.com/giakki/uncss/issues"
    },
    "config": {
        "blanket": {
            "pattern": [
                "src/lib.js",
                "src/uncss.js",
                "src/utility.js"
            ]
        }
    },
    "dependencies": {
        "async": "^1.5.2",
        "bluebird": "~3.1.5",
        "commander": "~2.9.0",
        "glob": "~6.0.1",
        "is-absolute-url": "~2.0.0",
        "is-html": "~1.0.0",
        "lodash": "~4.0.1",
        "object-assign": "^4.0.1",
        "phridge": "~2.0.0",
        "postcss": "~5.0.14",
        "request": "~2.69.0"
    },
    "description": "Remove unused CSS styles",
    "devDependencies": {
        "chai": "~3.5.0",
        "chai-resemble": "~0.4.1",
        "grunt": "~0.4.5",
        "grunt-eslint": "^18.0.0",
        "grunt-mocha-cov": "~0.4.0",
        "load-grunt-tasks": "~3.4.0",
        "time-grunt": "~1.3.0"
    },
    "directories": {},
    "dist": {
        "shasum": "baf4b170beae165b33187131d3b1dcd43236984e",
        "tarball": "https://registry.npmjs.org/uncss/-/uncss-0.14.1.tgz"
    },
    "engines": {
        "node": ">= 0.12.0"
    },
    "files": [
        "bin",
        "src",
        "LICENSE.md"
    ],
    "gitHead": "d19b523694fa46205189726c291ac1cfb807f7bf",
    "homepage": "https://github.com/giakki/uncss",
    "keywords": [
        "optimize",
        "optimise",
        "unused",
        "selector",
        "CSS",
        "HTML"
    ],
    "license": "MIT",
    "main": "src/uncss.js",
    "maintainers": [
        {
            "name": "giakki",
            "email": "martino.giacomo@gmail.com"
        }
    ],
    "name": "uncss",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/giakki/uncss.git"
    },
    "scripts": {
        "test": "grunt test"
    },
    "version": "0.14.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module uncss](#apidoc.module.uncss)
1.  [function <span class="apidocSignatureSpan">uncss.</span>postcssPlugin ()](#apidoc.element.uncss.postcssPlugin)
1.  object <span class="apidocSignatureSpan">uncss.</span>phantom
1.  object <span class="apidocSignatureSpan">uncss.</span>utility

#### [module uncss.phantom](#apidoc.module.uncss.phantom)
1.  [function <span class="apidocSignatureSpan">uncss.phantom.</span>cleanupAll ()](#apidoc.element.uncss.phantom.cleanupAll)
1.  [function <span class="apidocSignatureSpan">uncss.phantom.</span>findAll (page, sels)](#apidoc.element.uncss.phantom.findAll)
1.  [function <span class="apidocSignatureSpan">uncss.phantom.</span>fromLocal (filename, options)](#apidoc.element.uncss.phantom.fromLocal)
1.  [function <span class="apidocSignatureSpan">uncss.phantom.</span>fromRaw (html, options)](#apidoc.element.uncss.phantom.fromRaw)
1.  [function <span class="apidocSignatureSpan">uncss.phantom.</span>fromRemote (url, options)](#apidoc.element.uncss.phantom.fromRemote)
1.  [function <span class="apidocSignatureSpan">uncss.phantom.</span>getStylesheets (page, options)](#apidoc.element.uncss.phantom.getStylesheets)
1.  [function <span class="apidocSignatureSpan">uncss.phantom.</span>init (instance)](#apidoc.element.uncss.phantom.init)

#### [module uncss.postcssPlugin](#apidoc.module.uncss.postcssPlugin)
1.  [function <span class="apidocSignatureSpan">uncss.</span>postcssPlugin ()](#apidoc.element.uncss.postcssPlugin.postcssPlugin)
1.  [function <span class="apidocSignatureSpan">uncss.postcssPlugin.</span>postcss (css, result)](#apidoc.element.uncss.postcssPlugin.postcss)
1.  [function <span class="apidocSignatureSpan">uncss.postcssPlugin.</span>process (css, opts)](#apidoc.element.uncss.postcssPlugin.process)

#### [module uncss.utility](#apidoc.module.uncss.utility)
1.  [function <span class="apidocSignatureSpan">uncss.utility.</span>isWindows ()](#apidoc.element.uncss.utility.isWindows)
1.  [function <span class="apidocSignatureSpan">uncss.utility.</span>parseErrorMessage (error, cssStr)](#apidoc.element.uncss.utility.parseErrorMessage)
1.  [function <span class="apidocSignatureSpan">uncss.utility.</span>parsePaths (source, stylesheets, options)](#apidoc.element.uncss.utility.parsePaths)
1.  [function <span class="apidocSignatureSpan">uncss.utility.</span>parseUncssrc (filename)](#apidoc.element.uncss.utility.parseUncssrc)
1.  [function <span class="apidocSignatureSpan">uncss.utility.</span>readStylesheets (files)](#apidoc.element.uncss.utility.readStylesheets)



# <a name="apidoc.module.uncss"></a>[module uncss](#apidoc.module.uncss)

#### <a name="apidoc.element.uncss.postcssPlugin"></a>[function <span class="apidocSignatureSpan">uncss.</span>postcssPlugin ()](#apidoc.element.uncss.postcssPlugin)
- description and source-code
```javascript
function creator() {
    var transformer = initializer.apply(undefined, arguments);
    transformer.postcssPlugin = name;
    transformer.postcssVersion = new _processor2.default().version;
    return transformer;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.uncss.phantom"></a>[module uncss.phantom](#apidoc.module.uncss.phantom)

#### <a name="apidoc.element.uncss.phantom.cleanupAll"></a>[function <span class="apidocSignatureSpan">uncss.phantom.</span>cleanupAll ()](#apidoc.element.uncss.phantom.cleanupAll)
- description and source-code
```javascript
function cleanupAll() {
    phridge.disposeAll();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.uncss.phantom.findAll"></a>[function <span class="apidocSignatureSpan">uncss.phantom.</span>findAll (page, sels)](#apidoc.element.uncss.phantom.findAll)
- description and source-code
```javascript
function findAll(page, sels) {
    return page.run(sels, function (args) {
        return this.evaluate(function (selectors) {
            // Unwrap noscript elements
            Array.prototype.forEach.call(document.getElementsByTagName('noscript'), function (ns) {
                var wrapper = document.createElement('div');
                wrapper.innerHTML = ns.innerText;
                // Insert each child of the <noscript> as its sibling
                Array.prototype.forEach.call(wrapper.children, function (child) {
                    ns.parentNode.insertBefore(child, ns);
                });
            });
            // Do the filtering
            selectors = selectors.filter(function (selector) {
                try {
                    if (document.querySelector(selector)) {
                        return true;
                    }
                } catch (e) {
                    return true;
                }
                return false;
            });
            return {
                selectors: selectors
            };
        }, args);
    }).then(function (res) {
        if (res === null) {
            return [];
        }
        return res.selectors;
    });
}
```
- example usage
```shell
...
   css.walkRules(function (rule) {
       usedSelectors = _.concat(usedSelectors, rule.selectors.map(dePseudify));
   });
   // TODO: Can this be written in a more straightforward fashion?
   return promise.map(usedSelectors, function (selector) {
       return selector;
   }).then(function(selector) {
       return phantom.findAll(page, selector);
   });
}

/**
* Get all the selectors mentioned in {css}
* @param  {Object} css        The postcss.Root node
* @return {Array}
...
```

#### <a name="apidoc.element.uncss.phantom.fromLocal"></a>[function <span class="apidocSignatureSpan">uncss.phantom.</span>fromLocal (filename, options)](#apidoc.element.uncss.phantom.fromLocal)
- description and source-code
```javascript
function fromLocal(filename, options) {
    return promise.promisify(fs.readFile)(filename, 'utf-8').then(function (html) {
        return fromRaw(html, options);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.uncss.phantom.fromRaw"></a>[function <span class="apidocSignatureSpan">uncss.phantom.</span>fromRaw (html, options)](#apidoc.element.uncss.phantom.fromRaw)
- description and source-code
```javascript
function fromRaw(html, options) {
    var page = phantom.createPage(),
        htmlroot = path.join(process.cwd(), options.htmlroot || '');

    return promise.resolve(page.run(htmlroot, utility.isWindows(), ResourceHandler).then(function () {
        return page.run(html, function (raw) {
            this.setContent(raw, 'local');
        });
    }).then(resolveWithPage(page, options)));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.uncss.phantom.fromRemote"></a>[function <span class="apidocSignatureSpan">uncss.phantom.</span>fromRemote (url, options)](#apidoc.element.uncss.phantom.fromRemote)
- description and source-code
```javascript
function fromRemote(url, options) {
<span class="apidocCodeCommentSpan">    /* If the protocol is unspecified, default to HTTP */
</span>    if (!/^http/.test(url)) {
        url = 'http:' + url;
    }

    return promise.resolve(phantom.openPage(url).then(function (page) {
        return resolveWithPage(page, options)();
    }));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.uncss.phantom.getStylesheets"></a>[function <span class="apidocSignatureSpan">uncss.phantom.</span>getStylesheets (page, options)](#apidoc.element.uncss.phantom.getStylesheets)
- description and source-code
```javascript
function getStylesheets(page, options) {
    if (_.isArray(options.media) === false) {
        options.media = [options.media];
    }
    var media = _.union(['', 'all', 'screen'], options.media);
    return page.run(function () {
        return this.evaluate(function () {
            return Array.prototype.map.call(document.querySelectorAll('link[rel="stylesheet"]'), function (link) {
                return {
                    href: link.href,
                    media: link.media
                };
            });
        });
    }).then(function (stylesheets) {
        stylesheets = _
            .toArray(stylesheets)
<span class="apidocCodeCommentSpan">            /* Match only specified media attributes, plus defaults */
</span>            .filter(function (sheet) {
                return media.indexOf(sheet.media) !== -1;
            })
            .map(function (sheet) {
                return sheet.href;
            });
        return stylesheets;
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.uncss.phantom.init"></a>[function <span class="apidocSignatureSpan">uncss.phantom.</span>init (instance)](#apidoc.element.uncss.phantom.init)
- description and source-code
```javascript
function init(instance) {
    if (instance) {
        phantom = instance;
        return null;
    }

    // Convert to bluebird promise
    return new promise(function (resolve) {
        resolve(phridge.spawn({
            ignoreSslErrors: 'yes',
            sslProtocol: 'any'
        }));
    }).then(function (ph) {
<span class="apidocCodeCommentSpan">        /* Phridge outputs everything to stdout by default */
</span>        ph.childProcess.cleanStdout.unpipe();
        ph.childProcess.cleanStdout.pipe(process.stderr);
        phantom = ph;
    }).disposer(phridge.disposeAll);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.uncss.postcssPlugin"></a>[module uncss.postcssPlugin](#apidoc.module.uncss.postcssPlugin)

#### <a name="apidoc.element.uncss.postcssPlugin.postcssPlugin"></a>[function <span class="apidocSignatureSpan">uncss.</span>postcssPlugin ()](#apidoc.element.uncss.postcssPlugin.postcssPlugin)
- description and source-code
```javascript
function creator() {
    var transformer = initializer.apply(undefined, arguments);
    transformer.postcssPlugin = name;
    transformer.postcssVersion = new _processor2.default().version;
    return transformer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.uncss.postcssPlugin.postcss"></a>[function <span class="apidocSignatureSpan">uncss.postcssPlugin.</span>postcss (css, result)](#apidoc.element.uncss.postcssPlugin.postcss)
- description and source-code
```javascript
postcss = function (css, result) { // eslint-disable-line no-unused-vars
    opts = assign(opts, {
        // This is used to pass the css object in to processAsPostCSS
        rawPostCss: css
    });

    return new promise(function (resolve, reject) {
        serializedQueue.push(opts, function (err) {
            if (err) {
                reject(err);
            } else {
                resolve();
            }
        });
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.uncss.postcssPlugin.process"></a>[function <span class="apidocSignatureSpan">uncss.postcssPlugin.</span>process (css, opts)](#apidoc.element.uncss.postcssPlugin.process)
- description and source-code
```javascript
process = function (css, opts) {
    return postcss([creator(opts)]).process(css, opts);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.uncss.utility"></a>[module uncss.utility](#apidoc.module.uncss.utility)

#### <a name="apidoc.element.uncss.utility.isWindows"></a>[function <span class="apidocSignatureSpan">uncss.utility.</span>isWindows ()](#apidoc.element.uncss.utility.isWindows)
- description and source-code
```javascript
function isWindows() {
    return os.platform() === 'win32';
}
```
- example usage
```shell
...
 * @param  {Object}  options
 * @return {promise}
 */
function fromRaw(html, options) {
    var page = phantom.createPage(),
        htmlroot = path.join(process.cwd(), options.htmlroot || '');

    return promise.resolve(page.run(htmlroot, utility.isWindows(), ResourceHandler).then(function () {
        return page.run(html, function (raw) {
            this.setContent(raw, 'local');
        });
    }).then(resolveWithPage(page, options)));
}

/**
...
```

#### <a name="apidoc.element.uncss.utility.parseErrorMessage"></a>[function <span class="apidocSignatureSpan">uncss.utility.</span>parseErrorMessage (error, cssStr)](#apidoc.element.uncss.utility.parseErrorMessage)
- description and source-code
```javascript
function parseErrorMessage(error, cssStr) {
<span class="apidocCodeCommentSpan">    /* TODO: FIXME */
</span>    /* Base line for conveying the line number in the error message */
    var zeroLine = 0;

    if (error.line) {
        var lines = cssStr.split('\n');
        if (lines.length) {
            /* We get the filename of the css file that contains the error */
            var i = error.line - 1;
            while (i >= 0 && !error.filename) {
                if (lines[i].substr(0, 21) === '/*** uncss> filename:') {
                    error.filename = lines[i].substring(22, lines[i].length - 4);
                    zeroLine = i;
                }
                i--;
            }
            for (var j = error.line - 6; j < error.line + 5; j++) {
                if (j - zeroLine < 0 || j >= lines.length) {
                    continue;
                }
                var line = lines[j];
                /* It could be minified CSS */
                if (line.length > 120 && error.column) {
                    line = line.substring(error.column - 40, error.column);
                }
                error.message += '\n\t' + (j + 1 - zeroLine) + ':    ';
                error.message += j === error.line - 1 ? ' -> ' : '    ';
                error.message += line;
            }
        }
    }
    if (zeroLine > 0) {
        error.message = error.message.replace(/[0-9]+:/, error.line - zeroLine + ':');
    }
    error.message = 'uncss/node_modules/css: unable to parse ' + error.filename + ':\n' + error.message + '\n';
    return error;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.uncss.utility.parsePaths"></a>[function <span class="apidocSignatureSpan">uncss.utility.</span>parsePaths (source, stylesheets, options)](#apidoc.element.uncss.utility.parsePaths)
- description and source-code
```javascript
function parsePaths(source, stylesheets, options) {
    return stylesheets.map(function (sheet) {
        var sourceProtocol;

        if (sheet.substr(0, 4) === 'http') {
<span class="apidocCodeCommentSpan">            /* No need to parse, it's already a valid path */
</span>            return sheet;
        }

        /* Check if we are fetching over http(s) */
        if (isURL(source)) {
            sourceProtocol = url.parse(source).protocol;

            if (sheet.substr(0, 2) === '//') {
                /* Use the same protocol we used for fetching this page.
                 * Default to http.
                 */
                return sourceProtocol ? sourceProtocol + sheet : 'http:' + sheet;
            }
            return url.resolve(source, sheet);
        }

        /* We are fetching local files
         * Should probably report an error if we find an absolute path and
         *   have no htmlroot specified.
         */
        /* Fix the case when there is a query string or hash */
        sheet = sheet.split('?')[0].split('#')[0];

        /* Path already parsed by PhantomJS */
        if (sheet.substr(0, 5) === 'file:') {
            sheet = url.parse(sheet).path.replace('%20', ' ');
            /* If on windows, remove first '/' */
            sheet = isWindows() ? sheet.substring(1) : sheet;

            if (options.htmlroot) {
                return path.join(options.htmlroot, sheet);
            }
            sheet = path.relative(path.join(path.dirname(source)), sheet);
        }

        if (sheet[0] === '/' && options.htmlroot) {
            return path.join(options.htmlroot, sheet);
        } else if (isHTML(source)) {
            return path.join(options.csspath, sheet);
        }
        return path.join(path.dirname(source), options.csspath, sheet);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.uncss.utility.parseUncssrc"></a>[function <span class="apidocSignatureSpan">uncss.utility.</span>parseUncssrc (filename)](#apidoc.element.uncss.utility.parseUncssrc)
- description and source-code
```javascript
function parseUncssrc(filename) {
    var options = JSON.parse(fs.readFileSync(filename, 'utf-8'));

<span class="apidocCodeCommentSpan">    /* RegExps can't be stored as JSON, therefore we need to parse them manually.
     * A string is a RegExp if it starts with '/', since that wouldn't be a valid CSS selector.
     */
</span>    options.ignore = options.ignore ? options.ignore.map(strToRegExp) : undefined;
    options.ignoreSheets = options.ignoreSheets ? options.ignoreSheets.map(strToRegExp) : undefined;

    return options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.uncss.utility.readStylesheets"></a>[function <span class="apidocSignatureSpan">uncss.utility.</span>readStylesheets (files)](#apidoc.element.uncss.utility.readStylesheets)
- description and source-code
```javascript
function readStylesheets(files) {
    return promise.map(files, function (filename) {
        if (isURL(filename)) {
            return request({
                url: filename,
                headers: { 'User-Agent': 'UnCSS' }
            }).spread(function (response, body) {
                return body;
            });
        } else if (fs.existsSync(filename)) {
            return fs.readFileAsync(filename, 'utf-8').then(function (contents) {
                return contents;
            });
        }
        throw new Error('UnCSS: could not open ' + path.join(process.cwd(), filename));
    }).then(function (res) {
        // res is an array of the content of each file in files (in the same order)
        for (var i = 0, len = files.length; i < len; i++) {
            // We append a small banner to keep track of which file we are currently processing
            // super helpful for debugging
            var banner = '/*** uncss> filename: ' + files[i].replace(/\\/g, '/') + ' ***/\n';
            res[i] = banner + res[i];
        }
        return res;
    });
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
