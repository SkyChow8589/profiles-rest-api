# REST API Project with Django and Django REST Framework

Welcome to the REST API project! This project demonstrates how to build and deploy a REST API from scratch using Django, Django REST Framework, Python, and other supporting tools. The deployed REST API is accessible at: [http://ec2-3-139-237-146.us-east-2.compute.amazonaws.com/api/](http://ec2-3-139-237-146.us-east-2.compute.amazonaws.com/api/)

## Project Overview
This REST API provides core functionalities such as:

- Creating and updating user profiles
- User authentication and login
- Posting status updates
- Viewing status update feeds

The project follows best practices for backend development and is designed to be both functional and maintainable.

---

## Features
- **User Management:**
  - User registration
  - User login with authentication
- **Status Updates:**
  - Create, read, update, and delete (CRUD) status updates
  - View a feed of status updates
- **Browsable API:**
  - A self-documenting API interface provided by Django REST Framework

---

## Technology Stack
- **Frameworks:**
  - Django 2.2
  - Django REST Framework 3.9
- **Database:**
  - SQLite (default for development)
- **Tools:**
  - Vagrant
  - VirtualBox
  - ModHeaders (for testing and debugging headers)
  - Atom (as the preferred code editor)
- **Deployment:**
  - AWS EC2 instance

---

## Setup and Installation

### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd <repository-directory>
```

### Step 2: Set Up the Development Environment
1. Install Vagrant and VirtualBox on your system.
2. Start the Vagrant virtual machine:
   ```bash
   vagrant up
   vagrant ssh
   ```

### Step 3: Install Dependencies
Navigate to the project directory within the virtual machine and install Python dependencies:
```bash
cd /vagrant
pip install -r requirements.txt
```

### Step 4: Run the Server
Start the Django development server:
```bash
python manage.py runserver 0.0.0.0:8000
```
Access the local development server at `http://127.0.0.1:8000`.

---

## Deployment
The API is deployed at: [http://ec2-3-139-237-146.us-east-2.compute.amazonaws.com/api/](http://ec2-3-139-237-146.us-east-2.compute.amazonaws.com/api/)

---

## Usage
### Endpoints
- **User Profile:**
  - `POST /api/profile/`: Create a new user profile
  - `PUT /api/profile/{id}/`: Update a user profile
  - `GET /api/profile/`: View all profiles

- **Authentication:**
  - `POST /api/auth/login/`: User login
  - `POST /api/auth/logout/`: User logout

- **Status Updates:**
  - `POST /api/status/`: Create a status update
  - `GET /api/status/`: Retrieve all status updates
  - `PUT /api/status/{id}/`: Update a status update
  - `DELETE /api/status/{id}/`: Delete a status update

### Testing with ModHeaders
Use ModHeaders (a browser extension) to test API endpoints by modifying HTTP headers, including authentication tokens.

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## Contributing
Contributions are welcome! If you find any bugs or have suggestions, feel free to create an issue or submit a pull request.
