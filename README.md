🎭 Joke API Server 🚀
A simple and fun RESTful API server built with Express.js to manage and serve jokes. This API allows you to fetch random jokes, filter jokes by type, add new jokes, update existing ones, and even delete jokes. Perfect for learning, testing, or just having a good laugh!

🌟 Features
Random Joke: Get a random joke from the collection.

Joke by ID: Fetch a specific joke by its unique ID.

Filter Jokes: Filter jokes by type (e.g., Science, Puns, Wordplay).

Add Joke: Post a new joke to the collection.

Update Joke: Modify an existing joke using PUT or PATCH.

Delete Joke: Remove a specific joke or clear the entire collection (with master key authentication).

🛠️ Technologies Used
Express.js

Node.js

JavaScript

Postman (for testing)

🚀 Getting Started
Prerequisites
Node.js installed on your machine.

A package manager like npm or yarn.

Installation
Clone the repository:

bash
Copy
git clone https://github.com/your-username/joke-api-server.git
Navigate to the project directory:

bash
Copy
cd joke-api-server
Install dependencies:

bash
Copy
npm install
Start the server:

bash
Copy
npm start
The server will run on http://localhost:3000.

📚 API Endpoints
Endpoint	Method	Description
/random	GET	Get a random joke.
/jokes/:id	GET	Get a specific joke by its ID.
/filter?type=<type>	GET	Filter jokes by type (e.g., Science, Puns, Wordplay).
/jokes	POST	Add a new joke. Requires text and type in the request body.
/jokes/:id	PUT	Replace an existing joke by its ID. Requires text and type in the request body.
/jokes/:id	PATCH	Partially update an existing joke by its ID.
/jokes/:id	DELETE	Delete a specific joke by its ID.
/all?key=<masterKey>	DELETE	Delete all jokes. Requires the master key for authorization.
🛡️ Master Key Authentication
To delete all jokes, you need to provide the master key as a query parameter:

Copy
DELETE /all?key=4VGP2DN-6EWM4SJ-N6FGRHV-Z3PR3TT
📦 Example Requests
Get a Random Joke
bash
Copy
GET /random
Get a Joke by ID
bash
Copy
GET /jokes/1
Filter Jokes by Type
bash
Copy
GET /filter?type=Science
Add a New Joke
bash
Copy
POST /jokes
Body: {
  "text": "Why did the programmer quit his job? He didn't get arrays.",
  "type": "Programming"
}
Update a Joke (PUT)
bash
Copy
PUT /jokes/1
Body: {
  "text": "Why don't programmers like nature? It has too many bugs.",
  "type": "Programming"
}
Delete a Joke
bash
Copy
DELETE /jokes/1
Delete All Jokes
bash
Copy
DELETE /all?key=4VGP2DN-6EWM4SJ-N6FGRHV-Z3PR3TT
🧪 Testing
You can test the API using tools like Postman or directly via curl commands.

🤝 Contributing
Contributions are welcome! If you'd like to improve this project, please follow these steps:

Fork the repository.

Create a new branch (git checkout -b feature/YourFeatureName).

Commit your changes (git commit -m 'Add some feature').

Push to the branch (git push origin feature/YourFeatureName).

Open a pull request.
