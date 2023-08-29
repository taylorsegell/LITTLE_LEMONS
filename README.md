# Meta Developer Backend Developer Capstone

## Description
Welcome to the comprehensive guide for the final assignment of the Backend Developer Capstone Course within the Meta Backend Developer Professional Certificate on Coursera. This guide is tailored to new users who are taking their first steps into the world of Django and APIs. We will walk you through the project's structure, installation, setup, environment variables, API endpoints, and testing procedures in detail.

## Project Structure
This project consists of two key applications: `api` and `restaurant`. The `api` app handles the API endpoints for the project, while the `restaurant` app serves as the frontend. The `config` directory within the project folder holds crucial project settings.

## Installation
To get started, follow these steps:

1. Install the project dependencies using the following command:
    ```bash
    pipenv install
    ```

2. Activate the virtual environment:
    ```bash
    pipenv shell
    ```

## Setup
Configure your project's database settings in the `settings.py` file. The default settings are provided for a MySQL database, but you should adjust them according to your local setup.

```python
# settings.py

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'littlelemon',
        'HOST': 'localhost',
        'PORT': '3306',
        'USER': 'admin',
        'PASSWORD': '',
        'OPTIONS': {
            'init_command': "SET sql_mode='STRICT_TRANS_TABLES'",
        },
    },
}
```

## Environment Variables
For secure API requests in the restaurant app, you'll need to set up environment variables. Follow these steps:

1. Inside the `restaurant` app folder, create a file named `.env` and add the following lines, replacing `your_username` and `your_password` with your actual credentials:
    ```plaintext
    USERNAME=your_username
    PASSWORD=your_password
    ```

2. Make sure to have `django-environ` installed. You can install it by running:
    ```bash
    pipenv install
    ```

## API Endpoints
The `api` app provides four main endpoints, each with its own set of actions and authentication requirements. You'll need to use JSON Web Tokens (JWT) for authorization. Here's how you can interact with these endpoints:

### API Endpoints for `api` App

1. **Menu Items**
   - **GET**: Retrieve all menu items (Requires Token)
   - **POST**: Create a new menu item (Requires Token)

2. **Menu Item Detail**
   - **GET**: Retrieve details of a menu item (Requires Token)
   - **PUT**: Update a menu item (Requires Token)
   - **PATCH**: Partially update a menu item (Requires Token)
   - **DELETE**: Delete a menu item (Requires Token)

3. **Bookings**
   - **GET**: Retrieve all bookings (Requires Token)
   - **POST**: Create a new booking (Requires Token)

4. **Booking Detail**
   - **GET**: Retrieve details of a booking (Requires Token)
   - **PUT**: Update a booking (Requires Token)
   - **PATCH**: Partially update a booking (Requires Token)
   - **DELETE**: Delete a booking (Requires Token)

