# E-Commerce Backend

This project aims to build a robust back end for an e-commerce website using modern technologies. By utilizing Express.js for API handling and Sequelize for MySQL database interaction, this application provides a solid foundation for managing categories, products, and tags.

## Installation

1. Clone this repository to your local machine.
2. Navigate to the project directory in your terminal.
3. Run the necessary command to install the required dependencies.
4. Create a `.env` file in the root directory and input your MySQL database credentials.

## Usage

1. Set up the database using the provided schema.sql file.
2. Seed the database with initial data.
3. Start the server to begin using the application.

## Database Models

This project encompasses the following database models:

### Category

- id (Integer, Primary Key, Auto Increment)
- category_name (String, Not Null)

### Product

- id (Integer, Primary Key, Auto Increment)
- product_name (String, Not Null)
- price (Decimal, Not Null)
- stock (Integer, Not Null, Default 10)
- category_id (Integer, References Category)

### Tag

- id (Integer, Primary Key, Auto Increment)
- tag_name (String, Not Null)

### ProductTag

- id (Integer, Primary Key, Auto Increment)
- product_id (Integer, References Product)
- tag_id (Integer, References Tag)

## API Routes

The project offers the following API routes:

- GET `/api/categories`: Retrieve all categories
- GET `/api/categories/:id`: Retrieve a specific category by ID
- POST `/api/categories`: Create a new category
- PUT `/api/categories/:id`: Update a category by ID
- DELETE `/api/categories/:id`: Delete a category by ID

- GET `/api/products`: Fetch all products
- GET `/api/products/:id`: Fetch a specific product by ID
- POST `/api/products`: Create a new product
- PUT `/api/products/:id`: Update a product by ID
- DELETE `/api/products/:id`: Delete a product by ID

- GET `/api/tags`: Get all tags
- GET `/api/tags/:id`: Get a single tag by ID
- POST `/api/tags`: Create a new tag
- PUT `/api/tags/:id`: Update a tag by ID
- DELETE `/api/tags/:id`: Delete a tag by ID

## Testing

Utilize tools like Insomnia Core or Postman to test the API routes. Refer to the provided walkthrough video for detailed testing examples.

## Contributing

Contributions are welcome! If you encounter any issues or have suggestions for enhancements, feel free to open a pull request.

## License

This project is licensed under the MIT License.
