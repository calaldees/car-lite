car-lite
========

A mini web frontend to visualise GlobalPlayer CarPlay/AndroidAuto

1. install CORS browser plugin (see below)
2. `make run` (+refresh your browser)


Use
---

### Local

* Currently only works on from `localhost` as CORS headers are not setup for bff-car yet
  * To run this locally, I installed a browser extension to allow CORS from `://localhost` or `files:///`
      * https://addons.mozilla.org/en-GB/firefox/addon/cors-everywhere/
      * Activation Whitelist (regex)
          * ```
            /^https?:\/\/[\w\d.]*localhost(:\d+)?\//i
            /^file:/i
              ```

```
file:///some_path/car-lite/index.html
```
 or
```bash
python3 -m http.server
open http://localhost:8000/index.html
```

### Remote

* TODO
    * Add `localhost` or CORS headers on the api servers so the browser extension is not needed


Implementation Goals
--------------------

* No libraries/dependencies (just plain html, css, js)
* Single file
