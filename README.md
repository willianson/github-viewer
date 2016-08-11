# Github Viewer
Version 1.0

### Setup

##### Requisites:


Install [bower](https://bower.io/docs/api#install):

    $ npm install -g bower
    $ bower install

Install [polymer-cli](https://github.com/Polymer/polymer-cli):

    $ npm install -g polymer-cli

### Server

This command serves the app at `http://localhost:8080` and provides basic URL
routing for the app:

    $ polymer serve


### Build

This command performs HTML, CSS, and JS minification on the application
dependencies, and generates a service-worker.js file with code to pre-cache the
dependencies based on the entrypoint and fragments specified in `polymer.json`.
The minified files are output to the `build/unbundled` folder, and are suitable
for serving from a HTTP/2+Push compatible server.

    $ polymer build

### Test the build

This command serves the minified version of the app in an unbundled state, as it would
be served by a push-compatible server:

    $ polymer serve build/unbundled

This command serves the minified version of the app generated using fragment bundling:

    $ polymer serve build/bundled
