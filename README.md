# [App] GoRestaurant
This application allow you to make food orders, favorite plates and see your older orders. All the resources used by this application comes from a fake [`API`](#api).

## Table of Contents
* [Screenshots](#screenshots)
* [Installing](#installing)
  * [Configuring](#configuring)
    * [.env](#env)
    * [API](#api)
* [Usage](#usage)
  * [OS](#os)
* [Running the tests](#running-the-tests)
  * [Coverage report](#coverage-report)

# Screenshots
Click to expand.<br>
<img src="https://raw.githubusercontent.com/GilsondaGama/GoStack11-Desafio-11-GoRestaurant-Mobile/master/screenshots/home.jpg" width="32%" />
<img src="https://raw.githubusercontent.com/GilsondaGama/GoStack11-Desafio-11-GoRestaurant-Mobile/master/screenshots/dashboard.jpg" width="32%" />
<img src="https://raw.githubusercontent.com/GilsondaGama/GoStack11-Desafio-11-GoRestaurant-Mobile/master/screenshots/filtered.jpg" width="32%" />
<img src="https://raw.githubusercontent.com/GilsondaGama/GoStack11-Desafio-11-GoRestaurant-Mobile/master/screenshots/order.jpg" width="32%" />
<img src="https://raw.githubusercontent.com/GilsondaGama/GoStack11-Desafio-11-GoRestaurant-Mobile/master/screenshots/orders.jpg" width="32%" />
<img src="https://raw.githubusercontent.com/GilsondaGama/GoStack11-Desafio-11-GoRestaurant-Mobile/master/screenshots/favorites.jpg" width="32%" />

# Installing
Easy peasy lemon squeezy:
```
$ yarn
```
Or:
```
$ npm install
```
> Was installed and configured the [`eslint`](https://eslint.org/) and [`prettier`](https://prettier.io/) to keep the code clean and patterned.

## Configuring
Configure your environment variables and remember to start the [Json Server](https://github.com/typicode/json-server) API before to start this app.

### .env
In this file you may configure the API's url. Rename the `.env.example` in the root directory to `.env` then just update with your settings.

key|description|default
---|---|---
API_URL|API's url|`http://localhost:3333`

### API
This application make usage of a third party library to create a fake API, you can see more information about it in [JSON Server](https://github.com/typicode/json-server) repository.

To start the API run:
```
$ yarn json-server server.json -p 3333
```
Or:
```
$ npx json-server server.json -p 3333
```
In case of any change in the API's `port` or `host` remember to update the `.env`'s `API_URL` property too.
> Also, maybe you need run reverse command to the API's port: `adb reverse tcp:3333 tcp:3333`

# Usage
The first build must be through USB connection, so connect your device (or just open your emulator) and run:
```
$ yarn android
```
> For iOS use `ios` instead of `android`

In the next times you can just start the Metro Bundler server:
```
$ yarn start
```
Or:
```
$ npm run start
```
> See for more information in [Running On Device](https://reactnative.dev/docs/running-on-device).

## OS
This app was tested only with Android through USB connection and [Genymotion](https://www.genymotion.com/) (Emulator), is strongly recommended to use the same operational system, but of course you can use an emulator or a real device connected through wifi or USB.

# Running the tests
[Jest](https://jestjs.io/) was the choice to test the app, to run:
```
$ yarn test
```
Or:
```
$ npm run test
```

## Coverage report
You can see the coverage report inside `tests/coverage`. They are automatically created after the tests run.
