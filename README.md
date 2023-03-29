 # Superhero Tracker API


The Superhero Tracker API is a Rails-based API that allows you to track superheroes and their superpowers. It includes three main resources: Hero, Power, and HeroPower. The API provides endpoints for creating, reading, updating, and deleting data.

## Getting Started
### Prerequisites

To use the Superhero Tracker API, you'll need the following tools installed on your machine:

- Ruby 2.7.4 or higher
- Rails 6.1.4 or higher
- PostgreSQL 13.4 or higher

### Installation

To install the Superhero Tracker API, follow these steps:

1. Clone the repository: `git@github.com:febiasm/Phase-4-code-challenge-.git`
2. Install the dependencies: `bundle install`
3. Create the database: `rails db:create`
4. Run the migrations: `rails db:migrate`
5. Seed the database: `rails db:seed`
6. Start the server: `rails s`
7. Navigate to `http://localhost:3000/` in your web browser to verify that the server is running.

## API Endpoints

The Superhero Tracker API provides the following endpoints:

GET /heroes
Returns a list of all the heroes in the database. The response is an array of objects, where each object represents a hero and includes the following attributes:

- id (integer): the hero's unique identifier
- name (string): the hero's real name
- super_name (string): the hero's superhero name

## GET /heroes/:id

Returns the details for a single hero. The response is an object that includes the following attributes:

- id (integer): the hero's unique identifier
- name (string): the hero's real name
- super_name (string): the hero's superhero name
- powers (array): an array of objects representing the hero's superpowers, where each object includes the following attributes:
- id (integer): the superpower's unique identifier
- name (string): the superpower's name
- description (string): a brief description of the superpower.

## Author

[Trevor Thiru ](www.github.com/febiasm)

## License

This project is licensed under the MIT License.



