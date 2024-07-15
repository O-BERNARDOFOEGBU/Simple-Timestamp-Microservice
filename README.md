# Timestamp Microservice

This project is a Timestamp Microservice built with Node.js and Express. It returns the Unix timestamp and the UTC date string for a given date, or the current date if no date is provided.

## Table of Contents

- [Live Demo](#live-demo)
- [Features](#features)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Setup and Installation](#setup-and-installation)
- [Examples](#examples)
- [Technologies Used](#technologies-used)
- [License](#license)

## Live Demo

You can see the live demo of the project [here](https://timestamp-microservice.freecodecamp.rocks).

## Features

- Returns Unix timestamp and UTC date string for a given date.
- Handles both date strings and Unix timestamps.
- Returns the current date if no date is provided.
- Returns an error message for invalid dates.

## Usage

To use the microservice, you can make GET requests to the specified API endpoints.

## API Endpoints

- `/api/:date?`
  - `date` (optional): A date string or Unix timestamp.

### Response

The API returns a JSON object with the following structure:

```json
{
  "unix": <timestamp>,
  "utc": "<date_string>"
}
```

If the date is invalid, it returns:

```json
{
  "error": "Invalid Date"
}
```

###Setup and Installation
Prerequisites
Node.js
npm
Installation
Clone the repository:

```json
git clone https://github.com/O-BERNARDOFOEGBU/Simple-Timestamp-Microservice/
cd timestamp-microservice
Install the dependencies:
npm install
Start the server:
npm start
The server will start on port 3000 by default.
```

###Examples

Valid Date String
Request: GET /api/2015-12-25

Response:

```json
{
  "unix": 1451001600000,
  "utc": "Fri, 25 Dec 2015 00:00:00 GMT"
}
```

Valid Unix Timestamp
Request: GET /api/1451001600000

Response:

```json
{
  "unix": 1451001600000,
  "utc": "Fri, 25 Dec 2015 00:00:00 GMT"
}
```

Current Date
Request: GET /api

Response:

```json
{
"unix": <current_unix_timestamp>,
"utc": "<current_utc_date_string>"
}
```

Invalid Date
Request: GET /api/invalid-date

Response:

```json
{
  "error": "Invalid Date"
}
```

## Technologies Used

Node.js
Express
Cors
License
This project is licensed under the MIT License. See the LICENSE file for details.
