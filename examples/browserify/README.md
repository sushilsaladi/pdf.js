## Overview

Example to demonstrate PDF.js library usage with browserify.

## Getting started

Build project and install the example dependencies:

  $ gulp dist
  $ cd examples/browserify
  $ npm install

To build browserify bundles, run `gulp build`.  If you are running
a web server, you can observe the build results at
http://localhost:8888/examples/browserify/index.html

See main.js, worker.js and gulpfile.js files. Please notice that PDF.js
packaging requires packaging of the main application and PDF.js worker code,
and the workerSrc path shall be set to the latter file.

Alternatives to the gulp commands (without compression) are:

  $ mkdir -p ../../build/browserify
  $ node_modules/.bin/browserify main.js -o ../../build/browserify/bundle.js
  $ node_modules/.bin/browserify worker.js -o ../../build/browserify/pdf.worker.bundle.js