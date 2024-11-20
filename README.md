
# NetSuite REST API OpenAPI Specification

This repository contains the OpenAPI (Swagger) specification for the NetSuite REST API (version 2024.2). The YAML file provided here allows developers to interact with NetSuite's REST API using tools like Swagger Editor, Postman, or to generate client libraries in various programming languages.

## Overview

- **API Version**: 2024.2  
- **Specification File**: `netsuite_rest_api.yaml`  
- **Supported Record Types**:
  - Customer
  - Invoice
  - Sales Order
  - Item  
- **Authentication**: OAuth 2.0 (Client Credentials Flow)  

## Features

- **Comprehensive Endpoints**: Includes paths for listing, creating, retrieving, updating, and deleting records.  
- **Data Models**: Detailed schemas for each record type, including nested objects.  
- **Extensibility**: Easily add more record types or customize existing ones based on your NetSuite configuration.  

## Getting Started

### Prerequisites

- **NetSuite Account**: You must have an active NetSuite account with REST Web Services enabled.  
- **OAuth 2.0 Credentials**: Obtain your Client ID and Client Secret from NetSuite.  
- **Tools**:
  - Swagger Editor or any OpenAPI-compatible tool.
  - Optional: Postman for API testing.  

### Installation

1. Clone the Repository:
   ```bash
   git clone https://github.com/yourusername/netsuite-rest-api-specification.git
   ```
2. Navigate to the Directory:
   ```bash
   cd netsuite-rest-api-specification
   ```
3. Open the YAML File:
   Use your preferred text editor to open `netsuite_rest_api.yaml`.

4. Replace Account ID:
   Find `{accountId}` in the `servers` section and the `tokenUrl` under `securitySchemes`.
   Replace it with your actual NetSuite account ID.
   ```yaml
   servers:
     - url: https://123456.suitetalk.api.netsuite.com/services/rest/record/v1
   ```
   Save the File.

## Usage

### Using Swagger Editor

1. Open Swagger Editor:
   Go to [https://editor.swagger.io/](https://editor.swagger.io/).
2. Import the YAML File:
   Click on `File > Import File` and select `netsuite_rest_api.yaml`.
3. Explore the API:
   Navigate through the available endpoints and models.
4. Set Up Authentication:
   Click on the Authorize button (padlock icon).
   Enter your Client ID and Client Secret.  
   Scope should be `rest_webservices`.

### Testing Endpoints

#### List Customers:
- **Method**: GET  
- **Endpoint**: `/customer`  

#### Create an Invoice:
- **Method**: POST  
- **Endpoint**: `/invoice`  
- **Body**: Provide an Invoice object as per the schema.  

## Authentication

The API uses OAuth 2.0 Client Credentials Flow.

- **Token URL**:
  ```bash
  https://{accountId}.suitetalk.api.netsuite.com/services/rest/auth/oauth2/v1/token
  ```
- **Scopes**:
  - `rest_webservices`: Access to NetSuite REST web services.

### Obtaining OAuth 2.0 Credentials

1. Log in to NetSuite.
2. Navigate to: `Setup > Integration > Manage Integrations > New`.
3. Create a New Integration:
   - Enable OAuth 2.0.
   - Note down the Client ID and Client Secret.

## Extending the Specification

### Add New Record Types:
- Duplicate existing paths and schemas.  
- Update the record type names and properties.

### Customize Schemas:
- Modify the properties under each schema to match your NetSuite fields.

## Contributing

Contributions are welcome!

1. Fork the repository.  
2. Create a new branch for your feature or bugfix.  
3. Commit your changes.  
4. Push the branch to your fork.  
5. Submit a Pull Request.  

## License

This project is licensed under the MIT License.

## Contact

- **Author**: Philip Denys 
- **Email**: philip.denys@logitail.com  
- **GitHub**: @philip-denys  

## Resources

- **NetSuite REST API Browser**: Official Documentation  
- **Swagger Editor**: [https://editor.swagger.io/](https://editor.swagger.io/)  
- **NetSuite Support**: Support Center  

## Disclaimer

This repository is not affiliated with or endorsed by NetSuite. It is intended for educational and developmental purposes.

---

