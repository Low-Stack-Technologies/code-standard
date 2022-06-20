# Node.JS Instructions

## Node.JS & NPM
Download and install the `Current` version of Node.JS from [here.](https://nodejs.org/en/download/current/)

## PNPM
Because for performance gain from using PNPM compared to NPM we only just PNPM. Install PNPM using NPM `npm install -g pnpm` or another method described [here.](https://pnpm.io/installation)

## Setting up a new project
Initialize a new project with `pnpm init`. In the `package.json` it is important to add `"type": "module"` to enable module support and the scripts should have:
```json
"scripts": {
  "watch": "tsc --watch",
  "dev": "nodemon ./dist/app.js",
  "build": "tsc"
}
```
Change the `"author": ""` into `"authors": []` and make sure to include your name and email. Update the `"main": "index.js"` to `"main": "app.js"` unless there are special circumstances.

## Nodemon
To speed up the development process we use `Nodemon` to automatically restart the application when a change is made to the source. Install this with `pnpm i -D nodemon`.