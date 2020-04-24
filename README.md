# :dancers: :+1: :notes: New Wave Festival website :musical_note: :dancer: :sunglasses:

This is a website for music festival. This project was built mainly to learn creating RESTful API server with Express.js. It also helped deepening my skills in React/Redux. 
Built as exercise during Kodilla webdeveloper bootcamp (Module 21.5).

## Screenshots

Coming soon.

## Live

Coming soon.

## Features

Frontend: Coming soon

Backend:
* REST API standard
* available HTTP requests: GET, POST, PUT, DELETE
* database is now an object of arrays created and imported from `db.js `(fake database)
* there are 3 groups of routes:
    - testimonials
    - concerts
    - seats
* available endpoints for **testimonials**:
    - `GET` `/api/testimonials` - returns whole content of testimonials array
    - `GET` `/api/testimonials/:id` - returns one testimonial from array, according to its id (if id is `random`, returns random testimonial)
    - `POST` `/api/testimonials` - adds new testimonial to array, based on data from body, and id generated by uuid
    - `PUT` `/api/testimonials/:id` - edits existing testimonial based on its id
    - `DELETE` `/api/testimonials/:id` - delete chosen testimonial from array
* analogous endpoints are created for **concerts** (but without `random` feature)
    - `GET` `/api/concerts` - returns whole content of concerts array
    - `GET` `/api/concerts/:id` - returns one concert from array, according to its id
    - `POST` `/api/concerts` - adds new concert to array, based on data from body, and id generated by uuid
    - `PUT` `/api/concerts/:id` - edits existing concert based on its id
    - `DELETE` `/api/concerts/:id` - delete chosen concert from array
* analogous endpoints are created for **seats** (but without `random` feature)
    - `GET` `/api/seats` - returns whole content of seats array
    - `GET` `/api/seats/:id` - returns one seat from array, according to its id
    - `POST` `/api/seats` - adds new seat to array, based on data from body, and id generated by uuid
    - `PUT` `/api/seats/:id` - edits existing seat based on its id
    - `DELETE` `/api/seats/:id` - delete chosen seat from array
* error links are catched by middleware and response with 404 message is sent to user

## Technologies / tools

Frontend:
* HTML
* CSS/Sass
* React
* Redux
* project was initialized with CRA (Create React App)

Backend:
* REST API architecture
* Node.js + Express.js (using `express.Router()`)
* cors middleware for enabling all cors origins
* uuid for random id generator 
* endpoints tested with Postman
* I used nodemon npm package (installed globally so not reflected in package.json dependencies)

Database:
* At this stage only simulated in `db.js` file

## Installation

* Download or clone this repo and run `yarn install` or `npm i` in your console to install backend dependecies.
* To install frontend dependencies, go into `client` folder and use the same command as above.

## Running

For backend server:
* `node server` or `nodemon server` for more convenient development (you need to specifically install nodemon in the second case) 
* default `yarn start` or `npm start` uses nodemon under the hood (need to be installed separately)

For frontend:
* go into `client` folder and run `yarn start` or `npm start`

## TODO's
- [ ] add validation: check if all data is provided and if no, respond with message with error (json msg and error code 404)
- [ ] add error handling in endpoints when there is no record with searched id