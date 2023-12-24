# Intersections API

The Intersections API is a Node.js application that provides an API endpoint for finding intersecting lines between a given line string and a set of randomly spread lines. The API uses Express.js and integrates with the Turf.js library for spatial calculations.

## Requirements

- Node.js (v12 or higher)
- Postman

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/Akarsh3053/intersections-API-turfJS
   ```
2. Install the dependencies:
   ```bash
   npm install
   ```
4. Set up environment variables:
   Create a .env file in the root directory and configure the following variables:
   ```bash
   AUTH_TOKEN="password"
   ```
6. Start the server:
   ```bash
   npm start
   ```
  The API server will start running on http://localhost:3000.

## API Endpoint: http://localhost:3000/api/intersections
This endpoint accepts a GeoJSON line string in the request body and finds intersecting lines from the set of randomly spread lines.

Request Body:
  ```bash
  {
    "type": "LineString",
    "coordinates": [
      [-96.79512, 32.77823],
      [-96.79469, 32.77832],
      [-96.79433, 32.77728]
    ]
  }
  ```
Response:

If there are no intersections, the API returns an empty array [].
If intersections exist, the API returns an array of objects containing the intersecting line IDs and the intersection points.

Authentication
The API endpoint is protected with header-based authentication. Include the Authorization header with the value of the configured authentication token.

```bash
Authorization: password
```

## Testing the API with Postman
To test the API using Postman:
- Launch Postman.
- Create a new POST request.
- Set the request URL to http://localhost:3000/api/intersections.
- Add the Authorization header with the value as password.
- In the request body, provide a GeoJSON line string in the following format:
```bash
{
  "type": "LineString",
  "coordinates": [
    [-96.79512, 32.77823],
    [-96.79469, 32.77832],
    [-96.79433, 32.77728]
  ]
}
```
- Send the request and check the response for the intersecting lines.

## Tech Used 
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white) ![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB) ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
