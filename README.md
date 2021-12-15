# README

## About

This is Wails 2.0 + ReactJS Template
Tested on Windows and MacOS

To create a project using this template run:
`wails init -n [Your Appname] -t https://github.com/AlienRecall/wails-react-template`

## Building 

To build this project in debug mode, use `wails build`. For production, use `wails build -production`.
To generate a platform native package, add the `-package` flag.

## Live Development

To run in live development mode, run `wails dev` in the project directory. In another terminal, go into the `frontend` 
directory and run `npm run dev`. The frontend dev server will run on http://localhost:34115. Connect to this
in your browser and connect to your application. 


## Known Issues

Sadly I still not found a way to correclty run frontend in development mode so the only solution is to rebuild at every frontend change (if you got a way make an issue thanks)