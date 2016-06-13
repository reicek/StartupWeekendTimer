![App Screenshot](https://i.imgsafe.org/edab88880f.png)
StartupWeekend Timer
====================
###### by César Antón Dorantes <a href="https://twitter.com/reicek">@reicek</a>

This is a progressive real time web app built using Polymer and Firebase meant to aid Startup Weekend event's facilitators in the final pitchs timings.

### Demo

https://startupweekend-timer.firebaseapp.com

![App Screenshot](https://i.imgsafe.org/ed96cb4a50.png)

### Setup

##### Prerequisites

You need NodeJS and NPM installed.

https://nodejs.org/en/download/

Run the following commands from you console.

    npm install -g polymer-cli
    bower install

##### New to progressive web apps?

Here's a Google codelab that will familiarize you with all the technology on this project.

https://codelabs.developers.google.com/codelabs/your-first-pwapp/

### Start the development server

This command serves the app at `http://localhost:8080` and provides basic URL
routing for the app:

    polymer serve

### Build for production

This command performs HTML, CSS, and JS minification on the application
dependencies, and generates a service-worker.js file with code to pre-cache the
dependencies based on the entrypoint and fragments specified in `polymer.json`.

    polymer build

### Deploy to production

Once rebuilt, the app can be deployed using Firebase hosting; to do so first install the Firebase client.

    npm install -g firebase-tools

Firebase hosting allows to convientently deploy from the console.

    firebase deploy

### Extend

You can extend the app by adding more elements that will be demand-loaded
e.g. based on the route, or to progressively render non-critical sections
of the application.  Each new demand-loaded fragment should be added to the
list of `fragments` in the included `polymer.json` file.  This will ensure
those components and their dependencies are added to the list of pre-cached
components (and will have bundles created in the fallback `bundled` build).
