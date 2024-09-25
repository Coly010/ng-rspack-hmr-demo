# HMR Repro Demo

Run `npm install` 
Note: You may need to run `npm install --force`

Serve the app: `npx nx serve angularapp`
Open Browser at `http://localhost:4200`
Make a change to `apps/angularapp/src/app/nx-welcome.component.ts` (like updating `world = 'app'` to something).

Note the browser is receiving the HMR update (check network tab to see the js file being downloaded and containing the updated content)

Note the warning in the console which seems to indicate that the HMR update failed:

```
[HMR] Update failed: Loading hot update chunk main failed.
(missing: http://localhost:4200/main.1aaab5af6f9acbd93193.hot-update.mjs)
ChunkLoadError
    at http://localhost:4200/main.js:2219:15
    at new ZoneAwarePromise (webpack://angularapp/../../node_modules/zone.js/fesm2015/zone.js?9252:2749:33)
    at loadUpdateChunk (http://localhost:4200/main.js:2214:9)
    at http://localhost:4200/main.js:2669:18
    at Array.forEach (<anonymous>)
    at __webpack_require__.hmrC.jsonp (http://localhost:4200/main.js:2664:11)
    at http://localhost:4200/main.js:1793:36
    at Array.reduce (<anonymous>)
    at http://localhost:4200/main.js:1789:44
    at _ZoneDelegate.invoke (webpack://angularapp/../../node_modules/zone.js/fesm2015/zone.js?9252:498:172)
```
