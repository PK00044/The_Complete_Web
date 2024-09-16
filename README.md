# The Complete WebApp

## Overview
This project demonstrates the development of a full-featured web application integrating critical components like servers, tunneling, APIs, databases, and user statistics tracking. The project uses FastAPI for API management, SQLite for data storage, Ngrok for secure tunneling, and a QR code linked user stats manager to track user behavior.

## Features
- **FastAPI Server**: Powered by Uvicorn, the server efficiently manages incoming requests and responses.
- **Ngrok Tunneling**: Establishes secure tunnels for remote access, ensuring data integrity and confidentiality.
- **RESTful APIs**: Facilitates communication between different software components and extends the functionality of the web application.
- **SQLite Database**: Manages efficient data storage and retrieval operations.
- **QR Code Linked User Stats**: Tracks user activity such as location, operating system, and usage time when users scan the QR code.

## Installation

### 6.2.1 Install FastAPI App
- Use the following command to install FastAPI:
  ```
  pip install fastapi
  ```

### 6.2.2 Create FastAPI App
- Create a Python file (e.g., `main.py`) and import FastAPI.
- Define routes for CRUD operations related to your SQLite database.

### 6.2.3 Define SQLAlchemy Models
- Use SQLAlchemy to define a model representing your database table (e.g., `PersonDB`).
- Define columns such as `id`, `name`, `age`, `gender`.

### 6.2.4 Set Up SQLite Database
- Connect to the SQLite database using SQLAlchemy.
- Configure the database URL as `sqlite:///mydb.sqlite`.
![Project Folder Structure](![Screenshot 2024-09-15 121147](https://github.com/user-attachments/assets/6d0303c0-4a89-4d7d-81fb-15fd4950e245))


### 6.2.5 Implement CRUD Operations
- Implement functions to create, read, update, and delete records in the database.
- Use `SessionLocal` for managing database interactions.

### 6.2.6 Install Uvicorn Server
- Install Uvicorn using the following command:
  ```
  pip install uvicorn
  ```
![Unicorn Server Setup](![image](https://github.com/user-attachments/assets/44a93190-6b89-4832-947e-c1162df6518f))

### 6.2.7 Install and Use Ngrok
- Download and install Ngrok from the official site.
- Use the following command to start a tunnel:
  ```
  ngrok http 8000
  ```
• Your local server is now accessible via https://excited-snipe-blatantly.ngrokfree.app.
![Unicorn Server Setup](![image](https://github.com/user-attachments/assets/c1c98572-3ca2-4af3-87a4-f66604473132))

## Running the Server and Tunneling

### 6.2.8 Uvicorn server and ngrok tunneling service
1. **Start the Uvicorn server**:
   ```
   uvicorn main:app --reload
   ```
   - The API documentation is accessible at [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs).
![Unicorn Server Setup](![image](https://github.com/user-attachments/assets/928d4f6e-3d12-4084-a751-0669c52a5349)))

2. **Ngrok Setup**:
   - Run Ngrok to make the server publicly accessible:
     ```
     ngrok http 8000
     ```
   - Your local server will now be accessible via the provided public URL.

## QR Codes for User Access
- QR codes allow users to access the API quickly by scanning with their smartphones.
- Example: Generate a QR code for the API documentation URL using tools like `qr.io`.
![Unicorn Server Setup](![image](https://github.com/user-attachments/assets/c1c98572-3ca2-4af3-87a4-f66604473132))

## Tracking User Stats
- Track user interactions with the service using tools like `qr.io`.
- Monitor user engagement, location, and other metrics for insights into usage patterns.
![Unicorn Server Setup](![image](https://github.com/user-attachments/assets/dc078522-fa3f-4b8a-9b8c-f7a6aeb2827b)
))


## Testing

### 5.1 Testing Process
- Testing ensures that the developed product meets the required standards.
- Includes creating test cases to validate functionality.

### 5.3 Test Cases for Project
- **Insert Record (POST):** Adding a record in FastAPI saves it in the backend database.
- **Delete Record (DELETE):** Deleting a record removes it from the SQLite database.
- **Search Records (GET):** Retrieve records using GET requests.
- **Update Record (PUT):** Modify existing records in the database.

| Sl No | Test Input              | Expected Result      | Observed Result | Remarks             |
|-------|-------------------------|----------------------|-----------------|---------------------|
| 1     | Insert a record (POST)   | 200 OK               | PASS            | New tuple inserted  |
| 2     | Insert a Record (POST)   | ERROR                | PASS            | Duplicate insertion |
| 3     | Search Records (GET)     | Display the records  | Displayed       | PASS                |
| 4     | Search a Record (GET)    | Display specific record | Displayed    | PASS                |
| 5     | Delete Record (DELETE)   | 200 OK               | PASS            | Record deleted      |
| 6     | Update Record (PUT)      | 200 OK               | PASS            | Item updated        |

## Conclusion
This project serves as a complete web application architecture, integrating servers, APIs, databases, tunneling, and QR code tracking. It provides practical insights into developing a scalable and secure web application.
