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

### Local

* Option 1: Serve with `python` on `localhost:8000`
  * `make` (+refresh your browser)
  * ```bash
    python3 -m http.server
    open http://localhost:8000/index.html
    ```
* Option 2: Local file `file:///local_path/car-lite/index.html`


Implementation Goals
--------------------

* No libraries/dependencies (just plain html, css, js)
* Single file
