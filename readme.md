# GraphQL Server Example

This project is a simple GraphQL server example using Apollo Server Express and PostgreSQL as the database. It provides a basic setup for a GraphQL API with CRUD operations for users, posts, and comments.

## Installation

To set up and run this project, follow these steps:

1. Clone the repository: `git clone https://github.com/Born0/graphql-server-example.git`
2. Install the dependencies: `npm install`
3. Create a PostgreSQL database named `graphql` with a user `postgres` and password `groot`.
4. Start the server: `node server.js`

## API Documentation

The GraphQL API is accessible at `http://localhost:4000/graphql`. You can use a tool like GraphQL Playground or Apollo Client to interact with the API.

### Queries

* `users`: Retrieves a list of all users.
* `posts`: Retrieves a list of all posts.
* `post(id: ID!)`: Retrieves a single post by its ID.

### Mutations

* `createUser(name: String!, email: String!)`: Creates a new user.
* `createPost(title: String!, content: String!, authorId: ID!)`: Creates a new post.
* `createComment(content: String!, authorId: ID!, postId: ID!)`: Creates a new comment.

### Schema

The schema is defined in `schema.js` and includes the following types:

* `User`: Represents a user with an ID, name, email, and a list of posts.
* `Post`: Represents a post with an ID, title, content, author, and a list of comments.
* `Comment`: Represents a comment with an ID, content, author, and post.

### Database

The database is set up using PostgreSQL. The database connection is defined in `db.js`.

### Running the Server

To run the server, execute `node server.js` in the project directory. The server will start and be accessible at `http://localhost:4000/graphql`.

### Testing

No tests are currently implemented for this project. Contributions are welcome to add tests for the resolvers and database queries.

### Contributing

Contributions are welcome to improve the project. Please open a pull request with your changes.

