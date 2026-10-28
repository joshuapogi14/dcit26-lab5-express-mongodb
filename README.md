# DCIT 26 Laboratory 5: Express and MongoDB

## Student Records REST API

This project is a Student Records REST API developed using Node.js, Express, MongoDB, and Mongoose for DCIT 26: Application Development and Emerging Technologies.

The application allows users to create, read, update, and delete student records. Student information is stored in a MongoDB database.

## Technologies Used

- Node.js
- Express.js
- MongoDB
- Mongoose
- dotenv
- nodemon

## Project Setup

1. Clone the GitHub repository.
2. Open the project folder in Visual Studio Code.
3. Open the terminal.
4. Install the required dependencies:

   `npm install`

## MongoDB Configuration

1. Install MongoDB Community Server and MongoDB Compass.
2. Make sure the MongoDB Server is running.
3. Create a `.env` file in the main project folder.
4. Add the following configuration:

   ```env
   MONGODB_URI=mongodb://127.0.0.1:27017/lab5_students
   PORT=5000
   ```

5. Save the `.env` file.

The `.env` file is excluded from GitHub using `.gitignore`. The `.env.example` file provides a sample configuration.

## How to Run the Server

Open the terminal in the project folder and run:

`npm run dev`

The server will start on port 5000 after successfully connecting to MongoDB.

Expected terminal output:

```text
MongoDB connected successfully
Server running on port 5000
```

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | /api/health | Check API status |
| GET | /api/students | Retrieve all student records |
| GET | /api/students/:id | Retrieve a student by ID |
| POST | /api/students | Create a new student record |
| PUT | /api/students/:id | Update a student record |
| DELETE | /api/students/:id | Delete a student record |

## Sample Student JSON

```json
{
  "fullName": "Alex Santos",
  "course": "BSIT",
  "yearLevel": 2,
  "section": "IT-2A"
}
```

## Student Model

The Student model contains the following fields:

- **fullName** — Required string
- **course** — Required string
- **yearLevel** — Required number from 1 to 4
- **section** — Optional string
- **createdAt** — Date automatically set to the current time

## Error Handling

The API returns appropriate HTTP status codes:

- **200** — Successful request
- **201** — Student successfully created
- **400** — Invalid input or malformed student ID
- **404** — Student record not found
- **500** — Internal server error

## API Testing

The API can be tested using Postman, Thunder Client, or curl.

Test all CRUD operations and verify that student records are saved in MongoDB Compass. Records should remain available after restarting the server.

## GitHub Submission

The completed project must be uploaded to a GitHub repository named:

`dcit26-lab5-express-mongodb`

The repository must include the source code, `README.md`, `.gitignore`, `.env.example`, `package.json`, and `package-lock.json`.

The local `.env` file and `node_modules` folder must not be committed.

The completed work must be pushed to the `main` branch, and the repository URL must be submitted along with screenshots of successful GET, POST, PUT, and DELETE requests and saved records in MongoDB Compass or mongosh.