# Demo Application

This folder includes the demo react application for redux-websocket. It can be used as a reference for how to implement redux-websocket in your own app and for testing new feature development.

The hosted demo is at [https://brianmcallister.github.io/redux-websocket/](https://brianmcallister.github.io/redux-websocket/). It connects to Postman's public echo server, `wss://ws.postman-echo.com/raw`, by default.

## Scripts

|Command|Description|
|--|--|
|`npm run build`|Build production app|
|`npm start`|Start webpack dev server for local development|
|`npm run start:server`|Start a websocket echo server on port 3000|

## Local Development Setup

The demo depends on the library through `file:..`, so it always uses your local build of redux-websocket. The build uses webpack 4, which needs `--openssl-legacy-provider` on Node 17 and later. The scripts set this for you.

- From the project root, run `NODE_OPTIONS=--openssl-legacy-provider npm install` to install dependencies and build the library.

- From the project root, run `NODE_OPTIONS=--openssl-legacy-provider npm run build:watch` to rebuild the library as you change it.

- In another terminal, from the demo folder, run `npm install` and then `npm start` to start the demo app.

- To use a local echo server instead of Postman's, run `npm run start:server` and connect the demo to `ws://localhost:3000`.
