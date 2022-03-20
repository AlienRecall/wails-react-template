# README

## About

This is Wails 2.0 + ReactJS Template
Tested on Windows and MacOS

To create a project using this template run:
`wails init -n [Your Appname] -t https://github.com/AlienRecall/wails-react-template`

## Building 

To build this project use `wails build`.

## Live Development

To run in live development mode, run `wails dev` in the project directory. The frontend dev server will run on http://localhost:34115. Wails will watch and re-build for every backend (golang) changes. Wails will also start [cra-build-watch](https://www.npmjs.com/package/cra-build-watch), which will watch for frontend changes and repack the javascript code.

## Known Issues

While Wails is started in development mode, it calls the configured command for *frontend:dev* and afterwards *frontend:dev:watcher*.
If *frontend:dev* is not set, it calls the *frontend:build* which we don't want to called. Therefor a dummy command (`cat`) is set for
*frontend:dev*. Furthermore after starting the frontend watcher process, it expect the javascript bundle to be available which is
not the case as *cra-build-watch* first cleans the build directory. Wails therefor fails to start the dev server. A simple
workaround is to do a change in a `.go` file to trigger a rebuild. Now the dev server should start.
