# okpage
Lean on modern browser standards, cloud tools, and good test and build practices to build an ok webpage. Forget about nodejs for a while.

**Sketch/Idea**

**okpage** 
* jslib subdir - minimal redux/lit-html lib that's high perf and supports good unit testing practices ...this lib (okpage.js) is available via cdnjs (npm presence exists purely to publish combined lib)
  * lit-html
  * redux
  * redo redux-loop (better api, just write a custom middleware) - separate project, publish via npm
  * ...this lib (okpage.js) is available via cdnjs (npm presence exists purely to publish combined lib)
* proto subdir - golang based project that provides a cli tool for generating dataclass-style  js classes from proto defs, plus rpc calls. rpc's use browser-standard fetch by default but remote call impl is pluggable. 
* twirp subdir - demonstration of simple twirp backend, gh actions for e2e testing (frontend + twirp backend), generation of fixtures from server tests for client-side-e2e testing, gcp cloud run examples/support
* examples (all tests gh-action automated and run via browserstack)
  * hello - demonstrate lit/redux, minimal unit test
  * frontend only - todo list app, unit tested
  * twirp e2e - todo list app

more okpage...
* demonstration of use of shadow roots for css isolation
* no semicolons, all quotes are double - but not much code so people can convert to whatever style they want pretty easily.
* qunit in-browser testing
  * qunit and tests are loaded async. 
  * ...script or simple golang cli to run on browserstack
  * ...gh action demonstration of integrating this, failing a build w/ good test failure message(s)


Develop it all in codespaces
