Wikipedia Desktop to mobile redirect

```// ==UserScript==
// @name         Wikipedia Desktop to Mobile Redirect
// @namespace    http://tampermonkey.net/
// @version      1.0
// @description  Redirect desktop Wikipedia to mobile version
// @match        https://*.wikipedia.org/*
// @exclude      https://*.m.wikipedia.org/*
// @grant        none
// ==/UserScript==

(function() {
    'use strict';
    let currentURL = window.location.href;
    let mobileURL = currentURL.replace(/\/\/(\w+)\.wikipedia\.org/, '//$1.m.wikipedia.org');
    window.location.replace(mobileURL);
})();
