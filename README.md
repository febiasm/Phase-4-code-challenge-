## Pizza

This is a mini Rails API application for tracking pizza restaurants. It has three database tables (resources): Restaurant, Pizza, and RestaurantPizza. The Restaurant table has a many-to-many relationship with the Pizza table through the RestaurantPizza join table.

## Technologies Used
This web application was built using the following technologies:

- Rails
- ruby


### To get started with the project, follow these steps:

Clone the project using the following SSH key:  
 
    git@github.com:febiasm/Phase-4-code-challenge-.git

cd into the directory 

    cd Phase-4-code-challenge

oppen it with vs code or an other code app

    code .
## Usage
The application has the following main features: Restaurants

The application allows users to create restaurants, and to view a list of all restaurants or a single restaurant by ID. Users can also delete a restaurant by ID. Endpoints

  GET /restaurants - Returns a list of all restaurants as JSON data.
  
`GET /restaurants/:id` - Returns a single restaurant and its associated pizzas by ID as JSON data. Returns an error message and appropriate HTTP status code if the restaurant does not exist.


`DELETE /restaurants/:id` - Deletes a restaurant and its associated restaurant pizzas by ID. Returns an empty response body and appropriate HTTP status code. Returns an error message and appropriate HTTP status code if the restaurant does not exist.

### Guidelines
- Models
The project has three models: Restaurant, Pizza, and RestaurantPizza. The following relationships need to be established:

-  A Restaurant has many Pizzas through RestaurantPizza
-  A Pizza has many Restaurants through RestaurantPizza
-  A RestaurantPizza belongs to a Restaurant and belongs to a Pizza

Feel free to creat your own  models and migrations for the tables and add any code needed in the model files to establish the relationships. Then, run the migrations. You are welcome to generate your own seed data to test the application.

Validations
Add validations to the RestaurantPizza model:

Must have a price between 1 and 30

- Routes
Set up the following routes. Make sure to return `JSON` data in the format specified along with the appropriate HTTP verb.

`GET /restaurants`
 Return JSON data in the following format:

 
    [  {    "id": 1,    "name": "Sottocasa NYC",    "address": "298 Atlantic Ave, Brooklyn, NY 11201"  },  {    "id": 2,    "name": "PizzArte",    "address": "69 W 55th St, New York, NY 10019"  }]


`GET /restaurants/:id`
If the Restaurant exists, return JSON data in the following format:

 
    {
      "id": 1,
      "name": "Sottocasa NYC",
      "address": "298 Atlantic Ave, Brooklyn, NY 11201",
      "pizzas": [
        {
          "id": 1,
          "name": "Cheese",
          "ingredients": "Dough, Tomato Sauce, Cheese"
        },
        {
          "id": 2,
          "name": "Pepperoni",
          "ingredients": "Dough, Tomato Sauce, Cheese, Pepperoni"
        }
      ]
    }
If the Restaurant does not exist, return the following JSON data, along with the appropriate HTTP status code:

 
    {
      "error": "Restaurant not found"
    }

`DELETE /restaurants/:id`
If the Restaurant exists, it should be removed from the database, along with any RestaurantPizzas that are associated with it (a RestaurantPizza belongs to a Restaurant, so you need to delete the RestaurantPizzas before the Restaurant can be deleted).

After deleting the Restaurant, return an empty response body, along with the appropriate HTTP status code.

If the Restaurant does not exist, return the following JSON data, along with the appropriate HTTP status code:
 
    {
      "error": "Restaurant not found"
    }
#### Have fun!!!!


## Author
This project was contributed by Trevor Febias

## License
This project is licensed by MIT 