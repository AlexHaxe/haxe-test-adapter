# Haxe Test Explorer for Visual Studio Code

[![Build Status](https://travis-ci.org/vshaxe/haxe-test-adapter.svg?branch=master)](https://travis-ci.org/vshaxe/haxe-test-adapter) [![Version](https://vsmarketplacebadge.apphb.com/version-short/vshaxe.haxe-test-adapter.svg)](https://marketplace.visualstudio.com/items?itemName=vshaxe.haxe-test-adapter) [![Installs](https://vsmarketplacebadge.apphb.com/installs-short/vshaxe.haxe-test-adapter.svg)](https://marketplace.visualstudio.com/items?itemName=vshaxe.haxe-test-adapter)


A test adapter for VSCode using the [Test Explorer UI](https://marketplace.visualstudio.com/items?itemName=hbenl.vscode-test-explorer) extension.

![VSCode Test Adapter for Haxe](images/haxe-test-adapter.gif)

## Features

* Records [munit](https://github.com/massiveinteractive/MassiveUnit), [utest](https://github.com/haxe-utest/utest) and [`haxe.unit`](https://api.haxe.org/haxe/unit/TestRunner.html) test results as JSON files
* Shows latest test results in VSCode using the Test Explorer UI extension
* Supports filtering / running individual tests directly from VSCode
* Currently only works for Node.js and sys targets

## Usage

Simply add `-lib test-adapter` to your `buildTest.hxml` / test configuration. After running your tests you should see a folder named `.unittest` in your project root, containing test results, test positions and filters.

## Build from sources

```bash
cd ~/.vscode/extensions
git clone https://github.com/vshaxe/haxe-test-adapter
cd haxe-test-adapter
npm install
haxe build.hxml
```

## TODO

* ~~add file name and line numbers for all test functions~~
* add ~~file name and~~ line numbers for all test functions for Haxe 3 builds
* ~~running of tests~~
* ~~filter tests when running~~
* implement filtering for haxe.unit
* add support for additional unittest frameworks