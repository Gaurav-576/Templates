
# FastAPI MongoDB Application

This project is a **medium-scale** application using FastAPI with MongoDB integration. The folder structure is designed to maintain clean, modular, and scalable code.

## Project Structure

```
app/
├── auth/
│   ├── __init__.py
│   ├── authentication.py
│   └── verification.py
├── config/
│   ├── __init__.py
│   └── settings.py
├── crud/
│   ├── __init__.py
│   └── user_crud.py
├── database/
│   ├── __init__.py
│   └── connection.py
├── models/
│   ├── __init__.py
│   ├── admin_model.py
│   └── user_model.py
├── routes/
│   ├── __init__.py
│   └── user_route.py
├── schemas/
│   ├── __init__.py
│   ├── admin_schema.py
│   └── user_schema.py
├── services/
│   ├── __init__.py
│   ├── email_services.py
│   └── message_services.py
├── utils/
│   ├── __init__.py
│   └── helpers.py
├── tests/
│   ├── __init__.py
│   ├── test_main.py
│   ├── test_routes.py
│   └── test_users.py
└── main.py
```

### Folder Details

- **`auth/`**
  - **`authentication.py`**: Contains logic for user authentication, including login and token generation.
  - **`verification.py`**: Handles verification processes such as email or password verification.

- **`config/`**
  - **`settings.py`**: Stores configuration settings like MongoDB connection URI, environment variables, etc.

- **`crud/`**
  - **`user_crud.py`**: Implements CRUD (Create, Read, Update, Delete) operations for the User model. This is where database interactions occur.

- **`database/`**
  - **`connection.py`**: Handles MongoDB connection setup. The `MongoClient` is initialized here, and the database and collections are accessed.

- **`models/`**
  - **`admin_model.py`**: Defines the Pydantic model for Admin, specifying the data structure and validation.
  - **`user_model.py`**: Defines the Pydantic model for User, specifying the data structure and validation.

- **`routes/`**
  - **`user_route.py`**: Defines API endpoints related to User operations. These are the routes exposed by the FastAPI application.

- **`schemas/`**
  - **`admin_schema.py`**: Contains schema definitions for Admin data validation.
  - **`user_schema.py`**: Contains schema definitions for User data validation.

- **`services/`**
  - **`email_services.py`**: Contains logic for handling email-related services, such as sending verification emails.
  - **`message_services.py`**: Contains logic for handling messaging services, such as sending notifications.

- **`utils/`**
  - **`helpers.py`**: Contains utility functions or helper methods that are used across the application.

- **`tests/`**
  - **`test_main.py`**: Contains unit tests for the core application logic.
  - **`test_routes.py`**: Contains unit tests for API routes to ensure they work as expected.
  - **`test_users.py`**: Contains unit tests specifically for user-related operations.

- **`main.py`**
  - The entry point of the application where the FastAPI app instance is created, and routes are included.

### Environment Variables

- **`.env`**: Contains environment-specific variables such as MongoDB credentials, API keys, etc. Make sure this file is added to `.gitignore` to prevent sensitive data from being exposed.

### Dependencies

- **`requirements.txt`**: Lists all the Python dependencies required to run the project. Install them using:
  ```bash
  pip install -r requirements.txt
  ```

### Getting Started

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/yourrepository.git
   cd yourrepository
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**:
   - Create a `.env` file in the root directory and add your MongoDB credentials and other configurations.

4. **Run the application**:
   ```bash
   uvicorn app.main:app --reload
   ```

5. **Running Tests**:
   - Execute tests using:
     ```bash
     pytest
     ```

### Contributing

Feel free to contribute to this project by creating pull requests, reporting issues, or suggesting new features. Follow the contributing guidelines provided in `CONTRIBUTING.md`.

### License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
