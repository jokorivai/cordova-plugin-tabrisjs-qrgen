# Cordova - TabrisJS QR Code Generator plugin

for Android and iOS, by [Joko Rivai](https://github.com/jokorivai)


## 0. Index

1. [Description](#1-description)
2. [Screenshots](#2-screenshots)
3. [Installation](#3-installation)
	3. [Automatically (Cordoa CLI)](#automatically-cordova-cli)
	3. [Manually](#manually)
4. [Credits](#5-credits)
5. [Changelog](#6-changelog)

## 1. Description

This plugin allows you to generate QR Code within TabrisJS apps using plain javascript. Only for TabrisJS apps. Supported on Android and iOS (as platforms supported by TabrisJS).

This plugin is an adaptation of [Kazuhiko Arase](http://www.d-project.com/) Javascript QR Code Generator Library, initially released under MIT License.

Currently [TabrisJS](https://tabrisjs.com/) does not have any QR Code generator library, so this plugin may help you create QR Code TabrisJS within your TabrisJS applications.

* This plugins is pure JavaScript. No Java code used.
* QR Code generated to TabrisJS Canvas, or as in-memory image you can draw later to TabrisJS Canvas.
* Compatible with [Cordova CLI](https://cordova.apache.org/docs/en/latest/reference/cordova-cli/index.html).

## 2. Screenshots

iOS

![ScreenShot2](screenshots/MI_20161011_160630.jpg)


Android

![ScreenShot1](screenshots/MI_20161011_160604.png)



## 3. Installation

### Automatically (Cordova CLI)
Cordova - TabrisJS QR Code Generator plugin is compatible with [Cordova CLI](https://cordova.apache.org/docs/en/latest/reference/cordova-cli/index.html), here's how it works with the CLI (backup your project first!):

Using the Cordova CLI and the [Cordova Plugin Registry](http://plugins.cordova.io)
```
$ cordova plugin add cordova-plugin-tabrisjs-qrgen
```

Or instal using Git repository
```
$ cordova plugin add https://github.com/jokorivai/cordova-plugin-tabrisjs-qrgen.git
```

tabrisjscard.js is brought in automatically. There is no need to change or add anything in your code to make it available.
Please note that this plugin is NOT for HTML/WebView based Cordova apps. This plugin is ONLY for TabrisJS Cordova apps.

To create QR Code, call
```js
// reference to the plugin
var QRCodeGenerator = window.tabrisJsPlugins.GenerateQRToCanvas;
// create card:
QRCodeGenerator(textData, canvasObject, width, height);
```

Or
```js
window.tabrisJsPlugins.GenerateQRToCanvas(textData, canvasObject, width, height);
```

### Manually
You'd better use the CLI, but here goes:

Grab a copy of `tabrisjsqrcode.js`, from `extracted-zip\www\` and put it to your project source's `www` folder and reference it:
```js
var QRCode = require('./tabrisjsqrcode.js');
QRCode.GenerateQRToCanvas(textData, canvasObject, width, height);
```

## 4. CREDITS

This plugin is based on [TabrisJS](http://tabrisjs.com).
The QR Code Javascript Generator code was entirely created by [Kazuhiko Arase](http://www.d-project.com/)
TabrisJS adaptation was done by me.

This library is now trying to stick on Google Material Design specs, thanks to [mpost](https://github.com/mpost) for commenting
on [This TabrisJS Issue](https://github.com/eclipsesource/tabris-js/issues/886).

## 5. CHANGELOG

2018-04-16: 
  * Initial Commit