# Medium-Scaled FastAPI and MongoDB Integration

## Table of Contents
1. [Introduction](#introduction)
2. [Folder Structure](#folder-structure)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Contributing](#contributing)
6. [License](#license)

## Introduction
This repository showcases a medium-scale folder structure for integrating **FastAPI** with **MongoDB**, aimed at providing a solid foundation for developing web applications. 

FastAPI is a modern, fast web framework for building APIs with Python 3.6+ based on standard Python type hints, making it easy to create robust and efficient applications. MongoDB, a NoSQL database, offers flexibility and scalability, making it an ideal choice for applications that require handling large volumes of data.

In this medium-scale setup, we focus on achieving a balance between simplicity and organization, enabling developers to maintain clear separation of concerns across various components. The structure supports scalability, making it easier to add new features and functionalities as your application grows.

This guide will provide you with an overview of the folder structure, installation steps, and usage instructions for getting your FastAPI and MongoDB application up and running quickly.

## Folder Structure
The medium-scale folder structure is organized as follows:

```plaintext
medium-scaled/
├── app/
│   ├── auth/
│   │   ├── __init__.py
│   │   ├── authentication.py
│   │   └── verification.py
│   ├── config/
│   │   ├── __init__.py
│   │   └── settings.py
│   ├── crud/
│   │   ├── __init__.py
│   │   └── user_crud.py
│   ├── database/
│   │   ├── __init__.py
│   │   └── connection.py
│   ├── models/
│   │   ├── __init__.py
│   │   ├── admin_model.py
│   │   └── user_model.py
│   ├── routes/
│   │   ├── __init__.py
│   │   ├── admin_route.py
│   │   └── user_route.py
│   ├── schemas/
│   │   ├── __init__.py
│   │   ├── admin_schema.py
│   │   └── user_schema.py
│   ├── services/
│   │   ├── __init__.py
│   │   ├── email_services.py
│   │   └── message_services.py
│   └── utils/
│       ├── __init__.py
│       └── helpers.py
├── tests/
│   ├── __init__.py
│   ├── test_main.py
│   ├── test_routes.py
│   └── test_users.py
├── .env
├── .gitignore
├── README.md
├── requirements.txt
```

### Explanation of the Structure:

- **`app/`**: Contains the core application code and modules for the FastAPI project.
  - **`main.py`**: The entry point for the FastAPI application. This file typically includes the FastAPI instance creation, middleware, and includes the route definitions.
  
  - **`auth/`**: Responsible for user authentication and verification functionalities.
    - **`__init__.py`**: Indicates that this directory is a Python package.
    - **`authentication.py`**: Contains functions and classes for user authentication, such as login and token generation.
    - **`verification.py`**: Includes methods for verifying user credentials and account status.

  - **`config/`**: Holds configuration settings for the application.
    - **`__init__.py`**: Indicates that this directory is a Python package.
    - **`settings.py`**: Contains application settings such as database connection strings, environment variables, and any other configuration options.

  - **`crud/`**: Contains functions for creating, reading, updating, and deleting records from the database.
    - **`__init__.py`**: Indicates that this directory is a Python package.
    - **`user_crud.py`**: Includes functions specifically related to user data management, such as creating new users, retrieving user information, and updating user profiles.

  - **`database/`**: Manages database connections and sessions.
    - **`__init__.py`**: Indicates that this directory is a Python package.
    - **`connection.py`**: Responsible for establishing and managing the connection to the database, including any ORM setup if needed.

  - **`models/`**: Defines the data models that represent the application's data structure.
    - **`__init__.py`**: Indicates that this directory is a Python package.
    - **`admin_model.py`**: Contains the model definitions for admin users, including attributes and methods specific to admin functionalities.
    - **`user_model.py`**: Contains the model definitions for regular users, including attributes and methods related to user data.

  - **`routes/`**: Defines the API routes for handling client requests.
    - **`__init__.py`**: Indicates that this directory is a Python package.
    - **`admin_route.py`**: Contains the route definitions related to admin functionalities, such as user management and admin-specific actions.
    - **`user_route.py`**: Contains the route definitions for user-related actions, such as registration, login, and profile management.

  - **`schemas/`**: Contains Pydantic models for data validation and serialization.
    - **`__init__.py`**: Indicates that this directory is a Python package.
    - **`admin_schema.py`**: Defines the data validation schema for admin users, including the expected input and output formats.
    - **`user_schema.py`**: Defines the data validation schema for regular users, ensuring that the data conforms to expected formats.

  - **`services/`**: Contains business logic and service functions that interact with the application’s data and models.
    - **`__init__.py`**: Indicates that this directory is a Python package.
    - **`email_services.py`**: Includes functions for sending emails, such as welcome emails or password reset instructions.
    - **`message_services.py`**: Contains functions for sending notifications or messages within the application.

  - **`utils/`**: Utility functions and helpers that can be used throughout the application.
    - **`__init__.py`**: Indicates that this directory is a Python package.
    - **`helpers.py`**: Contains reusable helper functions that can assist in various tasks across the application.

- **`tests/`**: Contains unit and integration tests for the application.
  - **`__init__.py`**: Indicates that this directory is a Python package.
  - **`test_main.py`**: Includes tests for the main application functionality and setup.
  - **`test_routes.py`**: Contains tests for the API routes to ensure they behave as expected.
  - **`test_users.py`**: Includes tests specifically for user-related functionalities, such as CRUD operations.

- **`.env`**: A file for environment variables used in the application, such as sensitive information and configuration settings.

- **`.gitignore`**: Specifies files and directories that should be ignored by Git, ensuring sensitive data and unnecessary files are not tracked.

- **`README.md`**: A markdown file that provides an overview of the project, including installation instructions, usage guidelines, and any other relevant information.

- **`requirements.txt`**: A text file listing the required Python packages and their versions for the project, allowing for easy installation using pip.


## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/yourrepository.git
   cd yourrepository/medium-scaled
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up your environment variables in the `.env` file.

## Usage
To run the FastAPI application, execute:
```bash
uvicorn main:app --reload
```
Access the application at `http://127.0.0.1:8000`. 

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements.

## License
This project is licensed under the MIT License.
