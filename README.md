# Django Chart API

This project provides a set of REST API endpoints for delivering data used in various charts. The data is hardcoded for demonstration purposes.

## API Endpoints

- **Candlestick Data**
  - **URL:** `/api/candlestick-data/`
  - **Method:** GET
  - **Response:**
    ```json
    {
      "data": [
        {"x": "2023-01-01", "open": 30, "high": 40, "low": 25, "close": 35},
        {"x": "2023-01-02", "open": 35, "high": 45, "low": 30, "close": 40},
        {"x": "2023-01-03", "open": 40, "high": 50, "low": 35, "close": 45},
        {"x": "2023-01-04", "open": 45, "high": 55, "low": 40, "close": 50}
      ]
    }
    ```

- **Line Chart Data**
  - **URL:** `/api/line-chart-data/`
  - **Method:** GET
  - **Response:**
    ```json
    {
      "labels": ["Jan", "Feb", "Mar", "Apr"],
      "data": [10, 20, 30, 40]
    }
    ```

- **Bar Chart Data**
  - **URL:** `/api/bar-chart-data/`
  - **Method:** GET
  - **Response:**
    ```json
    {
      "labels": ["Product A", "Product B", "Product C"],
      "data": [100, 150, 200]
    }
    ```

- **Pie Chart Data**
  - **URL:** `/api/pie-chart-data/`
  - **Method:** GET
  - **Response:**
    ```json
    {
      "labels": ["Red", "Blue", "Yellow"],
      "data": [300, 50, 100]
    }
    ```

## Installation

### Prerequisites

- Python 3.12 or later
- Django 5.1.1 or later

2. **Create a virtual environment:**

python -m venv venv
Activate the virtual environment:

**On Windows:**

venv\Scripts\activate


**On macOS/Linux:**

source venv/bin/activate


**Install dependencies:**

pip install -r requirements.txt


**Apply migrations:**


python manage.py migrate

**Create a superuser:**

python manage.py createsuperuser

Follow the prompts to set up the superuser account.

**Run the development server:**

python manage.py runserver


The server will start at http://127.0.0.1:8000/. or http://localhost:8000/

**Access the API endpoints:**

Candlestick Data: http://127.0.0.1:8000/api/candlestick-data/
Line Chart Data: http://127.0.0.1:8000/api/line-chart-data/
Bar Chart Data: http://127.0.0.1:8000/api/bar-chart-data/
Pie Chart Data: http://127.0.0.1:8000/api/pie-chart-data/

**Configuration**
CORS Configuration: The project is configured to allow requests from http://localhost:3000. This can be adjusted in settings.py under CORS_ALLOWED_ORIGINS.


Simply install python set the path in environment variables then open the project folder in vs code or any editor 