car-lite
========

A mini web frontend to visualise GlobalPlayer CarPlay/AndroidAuto

https://calaldees.github.io/car-lite/


What
----

* A simple browser based visualiser allows Global staff to debug backend api returns from `bff-car-guacamole.musicradio.com`
  * Car-Lite URLs/`curls` can be shared with the team via chat
  * Single static file - No libraries/frameworks/dependencies - No build chain


Why
---

* Developers
  * Simulating an entire device and compiling code takes time, technical expertise and system resources
    * We wasted time as a team, finding devices, starting simulators, compiling the client, communicating about where the issue was visible
* Editors
  * Wider editorial participation by visualising our content across a variety of platforms
  * Visualise how the content looks on car
    * e.g.
      * Car does not have articles/videos
      * Are some titles readable on limited devices?
      * Do some quads make sense with only 3 items (Android)
* QA/Testing
  * Useful for verifying backend/data returns
  * Not suitable for client testing - it is not a real client
  * Not suitable for automating testing user flow/journeys - we have Tavern/API tests for this


Future
------

* Support for visualising personalised/audience content
  * (Will need more advanced CORS handling)
* Other lites?
  * mobile-lite?
  * alexa-lite?
  *tv-lite?
* Host the tool internally? (Currently on github pages as proof of concept)
  * This was a collaboration between developers and design
  * Designers do not have git access to our internal git repos
  * For ease of collaboration we used public github repo and hosted the static file on github pages
* [incredibleBulk](https://github.com/calaldees/incredibleBulkAPI) cache support
  * Keep history over time and see content from snapshots


Local Use
---------

* Option 1: Serve with `python` on `localhost:8000`
  * `make` (+refresh your browser)
  * ```bash
    python3 -m http.server
    open http://localhost:8000/index.html
    ```
* Option 2: Local file `file:///local_path/car-lite/index.html`
