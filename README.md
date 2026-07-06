# Rust_MongoDB_Project

Rust MongoDB Project

A REST API project built using Rust, Warp, and MongoDB for managing books. This application demonstrates how to create a backend service in Rust with asynchronous request handling and MongoDB integration.

The API supports creating, reading, updating, and deleting book records while storing data inside MongoDB.

⸻

Features

* Create a new book
* Retrieve all books
* Update an existing book
* Delete a book
* MongoDB database integration
* Async request handling
* Structured error handling
* JSON request and response support
* Clean modular architecture
* RESTful API design

⸻

Tech Stack

Backend

* Rust
* Warp
* Tokio
* MongoDB
* Serde
* Chrono
* Futures
* ThisError

⸻

Project Structure

Rust-MongoDB-Project/
│
├── Cargo.toml
├── Cargo.lock
├── README.md
├── src/
│   ├── main.rs
│   ├── db.rs
│   ├── handler.rs
│   └── error.rs
│
└── target/

File Description

main.rs

Responsible for:

* Starting the server
* Registering routes
* Connecting the database
* Initializing middleware
* Running the application

db.rs

Responsible for:

* Database connection
* MongoDB queries
* Data conversion
* CRUD operations

handler.rs

Responsible for:

* Handling API requests
* Processing request data
* Returning responses

error.rs

Responsible for:

* Custom error definitions
* Rejection handling
* Error response generation

⸻

Database Schema

Books are stored with the following structure:

{
    "id":"6855a2e3f16ea38f66c40e90",
    "name":"Atomic Habits",
    "author":"James Clear",
    "num_pages":320,
    "added_at":"2026-07-06T10:30:00Z",
    "tags":[
        "self-help",
        "productivity"
    ]
}

⸻

Installation

Clone the repository:

git clone https://github.com/Hellboy28D/Rust_MongoDB_Project.git

Move into the project directory:

cd Rust_MongoDB_Project

Install dependencies:

cargo build

⸻

MongoDB Setup

Make sure MongoDB is installed and running locally.

Start MongoDB:

mongod

Default database connection:

mongodb://127.0.0.1:27017

Database:

booky

Collection:

books

⸻

Run Application

Start the server:

cargo run

Expected output:

Started on port 8080

Server URL:

http://localhost:8080

⸻

API Endpoints

Create Book

POST

/book

Request body:

{
    "name":"Atomic Habits",
    "author":"James Clear",
    "num_pages":320,
    "tags":[
        "self-help",
        "productivity"
    ]
}

Response:

201 Created

⸻

Get All Books

GET

/book

Response:

[
    {
        "id":"6855a2e3f16ea38f66c40e90",
        "name":"Atomic Habits",
        "author":"James Clear",
        "num_pages":320,
        "added_at":"2026-07-06T10:30:00Z",
        "tags":[
            "self-help",
            "productivity"
        ]
    }
]

⸻

Update Book

PUT

/book/{id}

Request body:

{
    "name":"Updated Book",
    "author":"Updated Author",
    "num_pages":250,
    "tags":[
        "updated",
        "rust"
    ]
}

Response:

200 OK

⸻

Delete Book

DELETE

/book/{id}

Response:

200 OK

⸻

Error Handling

The application includes custom error handling for:

* Invalid request body
* Invalid MongoDB object IDs
* Database connection issues
* MongoDB query failures
* Invalid routes
* Unsupported HTTP methods

Example response:

{
    "message":"Internal Server Error"
}

⸻

Future Improvements

Possible improvements for this project:

* Authentication and authorization
* JWT implementation
* Pagination
* Search functionality
* Sorting and filtering
* Docker support
* Unit testing
* API documentation with Swagger
* Logging support
* Environment variables support
* Deployment support

⸻

Learning Outcomes

This project demonstrates:

* Building APIs using Rust
* Working with asynchronous programming
* Integrating MongoDB
* Creating REST services
* Structuring Rust applications
* Error handling patterns
* JSON serialization and deserialization

⸻

Author

Hellboy

⸻

License

This project is open-source and available under the MIT License.
