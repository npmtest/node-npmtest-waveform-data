# npmtest-waveform-data

#### basic test coverage for  [waveform-data (v2.0.1)](https://github.com/bbc/waveform-data.js)  [![npm package](https://img.shields.io/npm/v/npmtest-waveform-data.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-waveform-data) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-waveform-data.svg)](https://travis-ci.org/npmtest/node-npmtest-waveform-data)

#### Audio Waveform Data Manipulation API – resample, offset and segment waveform data in JavaScript.

[![NPM](https://nodei.co/npm/waveform-data.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/waveform-data)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-waveform-data/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-waveform-data/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-waveform-data/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-waveform-data/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-waveform-data/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-waveform-data/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-waveform-data/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-waveform-data/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-waveform-data/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-waveform-data/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-waveform-data/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-waveform-data/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-waveform-data/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-waveform-data/build/test-report.html](https://npmtest.github.io/node-npmtest-waveform-data/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-waveform-data/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-waveform-data/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-waveform-data/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-waveform-data/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-waveform-data/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-waveform-data/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-waveform-data/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-waveform-data/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Thomas Parisot"
    },
    "bugs": {
        "url": "https://github.com/bbc/waveform-data.js/issues"
    },
    "dependencies": {},
    "description": "Audio Waveform Data Manipulation API – resample, offset and segment waveform data in JavaScript.",
    "devDependencies": {
        "brfs": "^1.4.3",
        "browserify": "^13.0.0",
        "chai": "^3.5.0",
        "grunt": "^0.4.1",
        "grunt-cli": "^0.1.13",
        "grunt-jsdoc-md": "github:oncletom/grunt-jsdoc-md",
        "jshint": "^2.5.1",
        "karma": "^1.3.0",
        "karma-browserify": "^5.1.0",
        "karma-chrome-launcher": "^2.0.0",
        "karma-firefox-launcher": "^1.0.0",
        "karma-mocha": "^1.3.0",
        "karma-safari-launcher": "^1.0.0",
        "mocha": "^3.2.0",
        "nyc": "^10.0.0",
        "sinon": "^1.10.3",
        "sinon-chai": "^2.6.0",
        "testling": "^1.6.1",
        "watchify": "^3.7.0",
        "xvfb-maybe": "^0.1.3"
    },
    "directories": {},
    "dist": {
        "shasum": "306cedc9a02465e94277b213bbe0d03c7c5c989a",
        "tarball": "https://registry.npmjs.org/waveform-data/-/waveform-data-2.0.1.tgz"
    },
    "gitHead": "a878f8e22d34669dd8524e60223f44a13e362bd6",
    "homepage": "https://github.com/bbc/waveform-data.js",
    "keywords": [
        "webaudio",
        "waveform",
        "audio",
        "visualisation"
    ],
    "license": "LGPL-3.0",
    "main": "waveform-data.js",
    "maintainers": [
        {
            "name": "bbcrd"
        },
        {
            "name": "oncletom"
        }
    ],
    "name": "waveform-data",
    "nyc": {
        "check-coverage": true,
        "reporter": [
            "text",
            "html"
        ]
    },
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/bbc/waveform-data.js.git"
    },
    "scripts": {
        "build": "npm run build-waveform-data && npm run build-waveform-webaudio",
        "build-waveform-data": "browserify -r ./waveform-data.js -s WaveformData -o dist/waveform-data.js",
        "build-waveform-webaudio": "browserify -r ./webaudio.js -s WaveformDataWebaudioBuilder -o dist/webaudio.js",
        "lint": "jshint -c .jshintrc ./lib ./test",
        "posttest-node": "npm run lint",
        "prepublish": "npm run build",
        "pretest": "npm run build",
        "test": "npm run test-node && npm run test-browsers",
        "test-browsers": "xvfb-maybe ./node_modules/karma/bin/karma start",
        "test-node": "nyc mocha -R dot 'test/unit/*.js' 'test/unit/adapters/*.js'",
        "test-watch": "xvfb-maybe ./node_modules/karma/bin/karma start --no-single-run"
    },
    "testling": {
        "files": "test/unit/*.js",
        "harness": "mocha-bdd",
        "browsers": [
            "ie/9..10",
            "ff/latest..nightly",
            "chrome/latest..canary",
            "opera/latest..next",
            "safari/latest",
            "ipad/latest",
            "android/latest"
        ]
    },
    "version": "2.0.1",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
