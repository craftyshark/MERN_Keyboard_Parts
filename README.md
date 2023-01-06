# Data Browser for Keyboard Parts

This is a web application for browsing and recommending keyboard parts. It is built using the MERN stack:

* **MongoDB** is a NoSQL database used to store the keyboard parts data.
* **Express** is a Node.js framework used to create the back-end API for the application.
* **React** is a JavaScript library used to build the front-end user interface.
* **Node.js** is a JavaScript runtime used to run the back-end server and the front-end build process.

## Features

* Browse keyboard parts by type (e.g. switches, cases, PCBs) and filter by various criteria (e.g. manufacturer, price).
* View details of a specific keyboard part, including a description and images.
* Add new keyboard parts to the database and update existing ones.
* Get recommendations for additional keyboard parts based on a list of selected parts.

## Setting up the Development Environment

1. Install [Node.js](https://nodejs.org/) and [MongoDB](https://www.mongodb.com/download-center/community).
2. Clone this repository and navigate to the project directory.
3. Run `npm install` to install the required dependencies.
4. Run `npm run dev` to start the development server.
5. Open your code editor and edit the source code in the `src` directory.

## Designing the Data Model

The keyboard parts data is stored in a MongoDB database. Each type of keyboard part (e.g. switches, cases, PCBs) is represented by a separate collection, with the following fields for each document:

* `manufacturer`: the company that makes the keyboard part.
* `model`: the specific name or number of the keyboard part.
* `price`: the cost of the keyboard part.
* `description`: a text field with a detailed description of the keyboard part.
* `images`: an array of image URLs for the keyboard part.

## Building the Back-End API

The back-end API is created using the Express framework and exposes the following endpoints:

* `GET /api/parts`: retrieves a list of keyboard parts matching a given set of filters.
* `GET /api/parts/:id`: retrieves the details of a specific keyboard part by ID.
* `POST /api/parts`: adds a new keyboard part to the database.
* `PUT /api/parts/:id`: updates an existing keyboard part in the database.
* `DELETE /api/parts/:id`: deletes a keyboard part from the database.

The API uses the MongoDB Node.js driver to connect to the database and perform CRUD operations.

## Building the Front-End UI

The front-end user interface is built using React and allows users to:

* Browse a list of keyboard parts and filter by various criteria.
* View the details of a specific keyboard part, including a description and images.
* Add new keyboard parts to the database or update existing ones.

The UI communicates with the back-end API using HTTP requests to retrieve and update data.

## Implementing the Recommendation Feature

The recommendation feature uses a machine learning model built with a library like TensorFlow.js to suggest additional keyboard parts based on a list of
