car-lite
========

A mini web frontend to visualise GlobalPlayer CarPlay/AndroidAuto

Why
---

* Developers
  * Simulating an entire device and compiling code takes time and resources
  * Debugging backend api returns
* Editors
  * Visualise how the data looks on a range of platforms
* Testing?
  * (Probably not needed as we have Tavern tests that check flow)
  * Currently no tools for automating CarPlay/AndroidAuto - use Playwright?

### Future?

* Consider [incredibleBulk](https://github.com/calaldees/incredibleBulkAPI) cache support
  * Keep history over time and see content from snapshots


Use
---

* Currently car-lite can only works on from `localhost`
  * CORS headers are not setup for prod/stg/dev `bff-car` yet

### Local

1. Install CORS browser plugin (see below)
2. `make run` (+refresh your browser)

#### CORS Extension

* Firefox
  * [cors-everywhere](https://addons.mozilla.org/en-GB/firefox/addon/cors-everywhere/)
    * [GitHub](https://github.com/spenibus/cors-everywhere-firefox-addon)
  * Edit Activation Whitelist (regex)
      * ```
        /^https?:\/\/[\w\d.]*localhost(:\d+)?\//i
        /^file:/i
          ```
* Chrome
  * [cors-unblock](https://chromewebstore.google.com/detail/cors-unblock/lfhmikememgdcahcdlaciloancbhjino)
  * Bring up cors-unblock and click `Start`

```
file:///local_path/car-lite/index.html
```
 or
```bash
python3 -m http.server
open http://localhost:8000/index.html
```

### Remote

* TODO
    * Add `localhost` or CORS headers on the prod/stg/dev servers so the browser extension is not needed


Implementation Goals
--------------------

* No libraries/dependencies (just plain html, css, js)
* Single file
