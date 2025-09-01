# Petstore API Testing Project
## Overview
This project provides a "comprehensive API Testing suite" for the Petstore API (v2 & v3), covering "Positive and Negative test scenarios","error handling" and "response time validations".
It demonstrates practical skills in "API Testing","Test Documentation" and "Report generation" using Postman,Allure and Excel.

## Project Structure
Petstore/
│
├── Collections/
│ └── PetStore API Tests.Postman_Collection.json # Postman collection with all test cases positive and negative
├── Environment/
│ └── pet.postman_environment.json # Postman environment variables
├── Testcases/
│ └── Testcases for Petstore API.xlsx # Detailed test cases (positive & negative)
├── allure_report/ # Allure report generated after test execution

## Technologies Used
 **Postman** – API testing and Validation
 **Newman** –  Execution of Postman collection  
 **Allure** –  Beautiful Reporting and Visualization 
 **GitHub** – Version control and project showcase  
 **Excel** – Test case documentation  

## Test Coverage
 **Positive Scenarios** – Valid inputs for all endpoints  
 **Negative Scenarios** – Invalid inputs, edge cases, and error handling  
 **Response Time Checks** – Ensures API responses are within acceptable limits (<3000ms)  
 **Error Handling Validation** – Covers 400, 404, 405, 500 status codes depending on API version  
 
## Important Notes
1. Some test cases, like "Get Pet by ID" or "Get Store by ID," may show `404 Not Found` in Allure even if they pass in Postman due to **environment variables or execution order differences**.  
2. User API v3 currently returns `500 Internal Server Error` for all test cases. This is **API-specific behavior**, not a script issue.  
3. In User API v2, responses are as expected, but in v3, behavior may differ.  
4. Login/logout endpoints behave differently because they use GET methods soonly tested basic testcases.

## How to Run Tests

### Using Postman
1. Import the collection: `PetStore API Tests.Postman_Collection.json`  
2. Load environment variables: `pet.postman_environment.json`  
3. Run the collection manually or via the **Collection Runner**  

### Using Newman & Allure
1. Install Newman and Allure:  
run these command
npm install -g newman
npm install -g allure-commandline --save
Run the collection with Allure reporting:

newman run PetStore API Tests.Postman_Collection.json -e pet.postman_environment.json -r allure
allure serve allure-results

### Contribution

This repository is intended for learning, practice, and demonstration of API testing skills. Contributions, suggestions, and improvements are welcome.

## Acknowledments
1.Swagger petstore API for providing endponits
2.Postman for API testing tools
3.Allure for reporting and visualization
4.Inspired by best practices in API testing and QA Documentation

## Contact
For any queries or suggestion please contact
[Navya KM](https://github.com/navyakm9)   |[Email Me](mailto:navyakm.13@gmail.com)

## Thank you for visiting this Project!
  This repository is a demonstration of practical API testing skills, ideal for learning, practice or portfolio showcase.
