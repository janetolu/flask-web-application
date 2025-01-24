# flask-web-application
### requirements.txt
Flask==2.0.3
pymongo==3.12.3

### README.md
# Flask MongoDB User Details App

## Overview
This is a Flask application that allows users to input their details, including their income and expenses in specific categories (fees, utilities, entertainment, shopping, and healthcare). The data is stored in a MongoDB database, and the app provides functionality to export all user details to a CSV file for data analysis.

---

## Prerequisites
1. Python 3.8 or above
2. MongoDB instance running locally or on a remote server
3. Install the required dependencies using `requirements.txt`

---

## Installation and Setup
1. **Clone the Repository**:
   ```
   git clone <repository_url>
   cd <repository_folder>
   ```

2. **Set Up MongoDB**:
   - Ensure MongoDB is running. The database connection string in the app is configured as:
     ```
     mongodb://admin:example@localhost:27017/chatal?authSource=admin
     ```
     - Update the connection string in the code if necessary.

3. **Install Required Packages**:
   ```
   pip install -r requirements.txt
   ```

4. **Run the Application**:
   ```
   python app.py
   ```
   The app will run on `http://127.0.0.1:5000` by default.

---

## Features
1. **User Input Form**:
   - Collect details like name, gender, age, income, and expenses.
   - Validate that total expenses do not exceed income.

2. **Database**:
   - Save user details in MongoDB under the `datacollection` database, using the `user_details` collection.

3. **Data Export**:
   - Retrieve all user data from MongoDB and export it to a CSV file (`user_details.csv`).
   - Export route: `GET /export_users`.

---

## API Endpoints
1. `POST /user`: Submit user details and validate expenses.
2. `GET /export_users`: Export all user data to a CSV file.

---

## File Descriptions
1. **`app.py`**:
   - Main Flask application file.

2. **`requirements.txt`**:
   - List of dependencies to run the app.

3. **`README.md`**:
   - Instructions for setting up and running the application.

---

## Example Usage
### Submitting User Details
1. Start the Flask app.
2. Access the `/user` endpoint using a form submission.

### Exporting to CSV
1. Access the `/export_users` endpoint via a browser or a REST client.
2. Download the `user_details.csv` file.

---

## Troubleshooting
- **MongoDB Connection Issues**: Ensure MongoDB is running and the connection string is correctly configured.
- **Dependency Issues**: Reinstall dependencies with:
  ```
  pip install --force-reinstall -r requirements.txt
  ```
