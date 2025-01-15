# API for Product Name Matching

## Objective
Create a RESTful API that enables product name reconciliation. The API will use a database containing lists of products, and when a variation of a product name is provided as input, the endpoint should find and return the closest matching product from the database.

## Requirements

### Database Setup
- Design and set up a database to store product lists.
- Each product should have a unique identifier and a standard name.

### API Endpoints
- **GET /products/match:** Accepts a product name variation as a query parameter.
- The endpoint will search for the closest matching product name in the database and return the result.

### Matching Logic
- Return the product with the highest match score.

### Response Structure
- Return a JSON response containing:
  - `input_name`: The input product name variation.
  - `matched_product`: The closest matching product.
  - `match_score`: A confidence score of the match.

### Error Handling
- Handle cases where no close matches are found with appropriate error messages.
- Return status codes:
  - `200 OK` for successful matches.
  - `404 Not Found` if no suitable match is found.
  - `500 Internal Server Error` for unexpected issues.

### Testing Data
- A file containing product names and their closest variants will be provided for testing purposes.
