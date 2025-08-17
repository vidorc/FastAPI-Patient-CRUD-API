FastAPI Patient CRUD API
A clean and simple boilerplate for building a Create, Read, Update, and Delete (CRUD) API for patient records using Python and the FastAPI framework.

🚀 Features
Create: Add new patients to the database.

Read: Retrieve a single patient or a list of all patients.

Update: Modify existing patient information.

Delete: Remove patients from the database.

Modern Tech: Built with Python 3.8+ and FastAPI.

Async Support: Takes full advantage of Python's async and await for high performance.

Interactive Docs: Automatic, interactive API documentation provided by Swagger UI and ReDoc.

🛠️ Technologies Used
Backend: Python, FastAPI

Server: Uvicorn

Data Validation: Pydantic

Pydantic Data Model
We use Pydantic to define the data schema for our patient records. This ensures that any data sent to the API conforms to the expected structure and types.

Here's an example of the Patient model:

from pydantic import BaseModel
from typing import Optional

class Patient(BaseModel):
    id: Optional[int] = None
    name: str
    age: int
    height: float # in centimeters
    weight: float # in kilograms

⚙️ Setup and Installation
Clone the repository:

git clone https://github.com/your-username/fastapi-patient-crud.git
cd fastapi-patient-crud

Create and activate a virtual environment:

macOS/Linux:

python3 -m venv venv
source venv/bin/activate

Windows:

python -m venv venv
.\venv\Scripts\activate

Install the dependencies:

pip install -r requirements.txt

▶️ Running the Application
To run the application locally, use uvicorn:

uvicorn main:app --reload

The --reload flag will automatically restart the server whenever you make changes to the code.

The application will be available at http://127.0.0.1:8000.

📚 API Documentation
Once the application is running, you can access the interactive API documentation at one of the following URLs:

Swagger UI: http://127.0.0.1:8000/docs

ReDoc: http://127.0.0.1:8000/redoc

API Endpoints
Here is a summary of the available API endpoints for managing patients:

Method

Endpoint

Description

POST

/patients/

Create a new patient.

GET

/patients/

Get a list of all patients.

GET

/patients/{patient_id}

Get a single patient by their ID.

PUT

/patients/{patient_id}

Update a patient by their ID.

DELETE

/patients/{patient_id}

Delete a patient by their ID.
