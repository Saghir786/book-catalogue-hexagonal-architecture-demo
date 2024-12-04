# Project: Book Catalog System using Hexagonal Architecture in AWS

## Overview
This project is a Book Catalog System that demonstrates the use of hexagonal architecture implemented using Python and AWS. Hexagonal architecture, also known as the ports and adapters pattern, decouples the core business logic from the infrastructure and external components, making the system highly adaptable and testable.

We will use AWS Lambda functions as the primary adapters for the core logic, API Gateway as the client entry point for HTTP requests, and DynamoDB for data persistence.

## Features
- **REST API** to add, update, delete, and retrieve book information.
- **Serverless** architecture for scalability and easy maintenance.
- **Separation of Concerns**: Core business logic is decoupled from external dependencies.

## Architecture
- **Domain Layer**: Implements core business logic related to books (e.g., add, update, retrieve).
- **Primary Adapters**: AWS Lambda functions that expose HTTP endpoints via API Gateway.
- **Secondary Adapters**: Data persistence layer using DynamoDB to store book details.

## Tools & Technologies
- **Python**: For writing Lambda functions and core logic.
- **AWS Lambda**: Serverless compute for processing requests.
- **Amazon API Gateway**: Manages HTTP requests to Lambda functions.
- **DynamoDB**: For storing book information.
- **AWS SAM or Serverless Framework**: For managing Infrastructure as Code (IaC).


## Getting Started
### Prerequisites
- **AWS Account**: You need an AWS account to deploy the resources.
- **AWS CLI**: To interact with AWS services.
- **AWS SAM CLI**: For deploying the serverless application.
- **Python 3.8 or above**

### Installation
1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/book-catalog-system.git
   cd book-catalog-system
    ```

2. **Install Dependencies

```bash
pip install -r requirements.txt
```
3. **Deploy the Application

```bash
sam build
sam deploy --guided
```
Follow the prompts to deploy resources such as Lambda functions, API Gateway, and DynamoDB.

Usage
After deployment, you will receive an API Gateway URL.
Use tools like Postman or curl to interact with the API.
Example:
```bash
curl -X POST <API_URL>/books -d '{"title": "Clean Code", "author": "Robert C. Martin", "year": 2008}'
```
### Testing

Unit tests are provided in the tests/ directory.
Run tests using pytest:
```bash
pytest tests/
```

### Contributing
We welcome contributions! If you want to add features or report issues, feel free to create a pull request.

