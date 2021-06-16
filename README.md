# Yard Coding Challenge

## Setup

1. Clone project `https://github.com/yardventure/coding-challenge.git`
2. Navigate to coding-challenge folder and run `yarn install` or `npm install`
3. After installation start project by using `yarn develop` or `npm develop`
4. Create temporary account

## Challenges

### 1. Challenge

Task: automatically update date field after reservation creation.

Steps:
1. Create new controller in `./api/reservation/controllers/reservation.js` file that will call a function after creating a reservation.
2. Setup function to update freshly created reservation `payUntil` field to today's date.

Expected result:
1. Navigate to `Reservation` content. Select `Add New Reservation` and press `Save` new reservation without providing any details.
2. Project should update `payUntil` field to today's date. (If new reservation was created `2021-06-16` then `payUntil` date field after creation should be `2021-06-16`)

Docs:
1. https://strapi.io/documentation/developer-docs/latest/development/backend-customization.html#lifecycle-hooks
2. You can use `beforeCreate` function to solve this challenge, but in the end, it's up to you!


### 2. Challenge

Task: create custom route to update reservation stage.

Steps:
1. Create new `PUT` method route in `./api/reservation/config/routes.json` with path `/reservation/stage/:id/:stage`
2. New route will call a function `reservation.updateStage` which will be written in `./api/reservation/controllers/reservation.js` file.
3. `updateStage` function has to update reservation new stage

Expected result:
1. Let's say we have a reservation with id `1` which has stage `pending`
2. After calling `http://localhost:1337/reservation/stage/1/confirmed` reservation with id `1` stage will be changed to `confirmed`

Docs:
1. https://strapi.io/documentation/developer-docs/latest/development/backend-customization.html#routing
2. https://strapi.io/documentation/developer-docs/latest/development/backend-customization.html#controllers

2021
