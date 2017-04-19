# npmtest-jasmine-spec-reporter

#### test coverage for  [jasmine-spec-reporter (v4.0.0)](https://github.com/bcaudan/jasmine-spec-reporter)  [![npm package](https://img.shields.io/npm/v/npmtest-jasmine-spec-reporter.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-jasmine-spec-reporter) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-jasmine-spec-reporter.svg)](https://travis-ci.org/npmtest/node-npmtest-jasmine-spec-reporter)

#### Spec reporter for jasmine behavior-driven development framework

[![NPM](https://nodei.co/npm/jasmine-spec-reporter.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/jasmine-spec-reporter)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-jasmine-spec-reporter/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-jasmine-spec-reporter/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/test-report.html](https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-jasmine-spec-reporter/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-jasmine-spec-reporter/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jasmine-spec-reporter/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jasmine-spec-reporter/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-jasmine-spec-reporter/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Bastien Caudan"
    },
    "bugs": {
        "url": "https://github.com/bcaudan/jasmine-spec-reporter/issues"
    },
    "dependencies": {
        "colors": "1.1.2"
    },
    "description": "Spec reporter for jasmine behavior-driven development framework",
    "devDependencies": {
        "@types/colors": "1.1.2",
        "@types/jasmine": "2.5.47",
        "@types/node": "7.0.12",
        "codecov": "2.1.0",
        "diff": "3.2.0",
        "jasmine": "2.5.3",
        "jasmine-core": "2.5.2",
        "nyc": "10.2.0",
        "protractor": "5.1.1",
        "tslint": "5.1.0",
        "tslint-eslint-rules": "4.0.0",
        "typescript": "2.2.2"
    },
    "directories": {},
    "dist": {
        "shasum": "1f73b59edc47cef0b58f8e31dd4715ffedc96466",
        "tarball": "https://registry.npmjs.org/jasmine-spec-reporter/-/jasmine-spec-reporter-4.0.0.tgz"
    },
    "gitHead": "d267341a9faeaa0f3550746836f0bba48f430325",
    "homepage": "https://github.com/bcaudan/jasmine-spec-reporter",
    "keywords": [
        "jasmine",
        "reporter",
        "bdd",
        "spec",
        "protractor"
    ],
    "license": "Apache-2.0",
    "main": "built/main.js",
    "maintainers": [
        {
            "name": "bcaudan"
        }
    ],
    "name": "jasmine-spec-reporter",
    "nyc": {
        "exclude": [
            "spec"
        ]
    },
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/bcaudan/jasmine-spec-reporter.git"
    },
    "scripts": {
        "coverage": "nyc npm test",
        "coverage:codecov": "npm run coverage && nyc report --reporter=json && codecov -f coverage/*.json",
        "examples:test:node": "cd examples/node && npm test",
        "examples:test:protractor": "cd examples/protractor && npm test",
        "examples:test:typescript": "cd examples/typescript && npm test",
        "examples:update": "npm run examples:update:node && npm run examples:update:protractor && npm run examples:update:typescript",
        "examples:update:node": "cd examples/node && rm -rf node_modules && npm install",
        "examples:update:protractor": "cd examples/protractor && rm -rf node_modules && npm install",
        "examples:update:typescript": "cd examples/typescript && rm -rf node_modules && npm install",
        "lint": "tslint -c tslint.json --type-check --project tsconfig.json && tslint -c tslint.json --type-check --project spec/tsconfig.json",
        "posttest": "npm run lint",
        "prepublish": "tsc",
        "pretest": "tsc && tsc -p spec/tsconfig.json",
        "test": "jasmine",
        "test:integration": "npm run pretest && npm run examples:update && jasmine JASMINE_CONFIG_PATH=spec/support/jasmine-integration.json"
    },
    "types": "built/main.d.ts",
    "version": "4.0.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
