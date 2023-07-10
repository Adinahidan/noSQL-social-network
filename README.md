# noSQL-social-network


## Description

This is an API for a social network web application where users can share their thoughts, react to friends' thoughts, and manage their friend list. It utilizes Express.js for routing, MongoDB as the NoSQL database, and Mongoose as the ODM. The API is designed to handle large amounts of unstructured data efficiently.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Routes](#api-routes)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository.
2. Install the required dependencies by running the following command:
   -npm install

3. Run the application using the following command:
   -npm start


## Usage

1. Open your preferred API testing tool (e.g., Insomnia).
2. Test the API routes by sending requests to the appropriate endpoints (detailed information available in the [API Routes](#api-routes) section below).
3. Use the responses to interact with user data, thoughts, reactions, and friend lists in the social network.

## API Routes

### `/api/users`

- `GET /api/users`
- Retrieves all users.
- `GET /api/users/:userId`
- Retrieves a single user by ID and includes thoughts and friend data.
- `POST /api/users`
- Creates a new user.
- Request body should include `username` and `email`.
- `PUT /api/users/:userId`
- Updates an existing user by ID.
- `DELETE /api/users/:userId`
- Deletes a user by ID.
- Associated thoughts will also be removed.

### `/api/users/:userId/friends/:friendId`

- `POST /api/users/:userId/friends/:friendId`
- Adds a new friend to a user's friend list.
- `DELETE /api/users/:userId/friends/:friendId`
- Removes a friend from a user's friend list.

### `/api/thoughts`

- `GET /api/thoughts`
- Retrieves all thoughts.
- `GET /api/thoughts/:thoughtId`
- Retrieves a single thought by ID.
- `POST /api/thoughts`
- Creates a new thought.
- Request body should include `thoughtText`, `username`, and `userId`.
- `PUT /api/thoughts/:thoughtId`
- Updates an existing thought by ID.
- `DELETE /api/thoughts/:thoughtId`
- Deletes a thought by ID.

### `/api/thoughts/:thoughtId/reactions`

- `POST /api/thoughts/:thoughtId/reactions`
- Creates a new reaction for a thought.
- Request body should include `reactionBody` and `username`.
- `DELETE /api/thoughts/:thoughtId/reactions/:reactionId`
- Removes a reaction from a thought by reaction ID.

## Contributing

Contributions to this project are welcome! If you have any ideas, suggestions, or bug reports, please open an issue or submit a pull request.



