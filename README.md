car-lite
========

A mini web frontend to visualise GlobalPlayer CarPlay/AndroidAuto



Use
---

* This frontend is intended for local development use.
* It requires access to a range of api endpoints on differnet origins
* To run this locally, I installed a browser extension to allow CORS from `://localhost` or `files:///`
    * https://addons.mozilla.org/en-GB/firefox/addon/cors-everywhere/
    * Activation Whitelist (regex)
        * ```
          /^https?:\/\/[\w\d.]*localhost(:\d+)?\//i
          /^file:/i
            ```

```
file:///some_path/index.html?endpoint=https://bff-car-guacamole.musicradio.com
```

```bash
python3 -m http.server
open http://localhost:8000/index.html?endpoint=https://bff-car-guacamole.musicradio.com
```


Goal
----

* No libraries/dependencies (just plain html, css, js)
* Single file
* Longer term
    * Add `localhost` or CORS headers on the api servers so the browser extension is not needed