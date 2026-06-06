# Patient Management System API 🏥

A foundational Patient Management System API built from scratch using Python and FastAPI. It features complete CRUD operations, strict data validation via Pydantic, and automated health metric calculations with lightweight JSON storage. Designed as a hands-on project to master backend architecture, API routing, and system debugging.

## ✨ Features

* **Full CRUD Operations:** Create, Read, Update, and Delete patient records seamlessly.
* **Automated Health Metrics:** Automatically calculates Body Mass Index (BMI) and assigns a health verdict (Underweight, Normal, Overweight, Obese) based on user input.
* **Strict Data Validation:** Utilizes Pydantic models to ensure all incoming data is accurately typed and formatted before processing.
* **Dynamic Sorting:** View and sort patient data by specific attributes like height, weight, or BMI in ascending or descending order.
* **Lightweight Storage:** Uses a local `patients.json` file for fast, accessible data storage without the need for a complex external database setup.

## 🛠️ Tech Stack

* **Language:** Python
* **Framework:** FastAPI
* **Data Validation:** Pydantic
* **Server:** Uvicorn

## 🚀 Getting Started

Follow these instructions to set up and run the API on your local machine.

### Prerequisites
Make sure you have Python installed (Python 3.7+ is recommended).

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```

2.  **Install the required dependencies:**
    ```bash
    pip install fastapi uvicorn pydantic
    ```

3.  **Run the development server:**
    ```bash
    uvicorn main:app --reload
    ```
    *Note: The `--reload` flag enables auto-reloading, so the server will restart automatically when you make code changes.*

4.  **Access the API:**
    Open your browser and navigate to `http://127.0.0.1:8000`.

## 📖 Interactive Documentation

FastAPI automatically generates interactive API documentation. Once your server is running, you can explore and test the endpoints directly from your browser:

* **Swagger UI:** `http://127.0.0.1:8000/docs`
* **ReDoc:** `http://127.0.0.1:8000/redoc`

## 🔗 API Endpoints

Here is a quick overview of the available routes:

### General
* `GET /` - Returns a welcome message.
* `GET /about` - Returns details about the API.

### Patient Operations
* `POST /create` - Add a new patient record.
* `GET /view` - Retrieve all patient records.
* `GET /patient/{patient_id}` - Retrieve a specific patient by their ID.
* `GET /sort` - Sort patients by `height`, `weight`, or `bmi` (supports `asc` or `desc` order).
* `PUT /edit/{patient_id}` - Update an existing patient's details.
* `DELETE /delete/{patient_id}` - Remove a patient record from the database.

## 📂 Data Structure

Patient data is stored in `patients.json` with the following structure:

```json
{
  "P001": {
    "name": "Jane Doe",
    "city": "Agra",
    "age": 25,
    "gender": "Female",
    "height": 1.65,
    "weight": 60.0,
    "bmi": 22.04,
    "verdict": "Normal"
  }
}
