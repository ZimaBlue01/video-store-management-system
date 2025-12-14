![Video Store Management System](assets/py_image.png)



# Video Store Management System (Python & MySQL)

This project is a **database-driven Video Store Management System** built using **Python, MySQL, and Object-Oriented Programming (OOP)** principles.

The system allows a video store to manage customers, videos, and hire transactions through a modular, backend-focused application.

---

## 📌 Project Overview

The Video Store Management System was designed to solve the following problems:

- Register and manage customers
- Maintain a catalog of available videos
- Track video hire and return transactions
- Prevent duplicate customer records
- Enforce video availability rules
- Store and retrieve data using a MySQL database

The application is implemented using **Jupyter Notebooks** for modularity and clarity, with each notebook responsible for a specific part of the system.

---

## 🛠 Technologies Used

- **Python**
- **MySQL**
- **mysql-connector-python**
- **Jupyter Notebook**
- **Object-Oriented Programming (OOP)**
- **Environment-based configuration (`.env`)**

---

## 📂 Project Structure

video-store-management-system
│
├── README.md
│
├── notebooks/
│ ├── db_config_and_test.ipynb
│ ├── videoDB_tables_creation.ipynb
│ ├── modules_initialisation.ipynb
│ ├── register_customer_func.ipynb
│ ├── video_register_func.ipynb
│ ├── hire_functions.ipynb
│ ├── sample_data_insert.ipynb
│ └── video_store_main.ipynb
│
├── env/
│ └── DB_details.env.example
│
└── assets/


---

## ⚙️ Database Configuration

The system connects to a **MySQL database** named:



video_store


Database credentials are managed using an environment file.

### Setup instructions:

1. Navigate to the `env/` folder  
2. Rename:


DB_details.env.example → DB_details.env

3. Update the file with your local MySQL credentials:
```env
DB_HOST=127.0.0.1
DB_PORT=3306
DB_USER=your_username
DB_PASS=your_password
DB_NAME=video_store


⚠️ The real .env file is intentionally excluded from version control.

▶️ How to Run the Project
1️⃣ Open Jupyter Notebook

Use Anaconda Navigator or your preferred Jupyter environment.

2️⃣ Run the setup notebooks

Execute the following notebooks first:

db_config_and_test.ipynb

videoDB_tables_creation.ipynb

modules_initialisation.ipynb

3️⃣ Load functional modules

In video_store_main.ipynb, run the first cell containing:

%run register_customer_func.ipynb
%run video_register_func.ipynb
%run hire_functions.ipynb


This makes all system functions available.

4️⃣ Run the main application

Continue running the remaining cells in:

video_store_main.ipynb

🎯 Core Features

Register new customers (with duplicate checks)

Register new videos (Red box / Black box classification)

Hire out videos

Return videos

Check video availability

Automatically track hire and return dates

Database-backed transaction logging

🧠 Design Approach

This project follows Object-Oriented Programming (OOP) principles to ensure:

Modular design

Code reusability

Scalability

Maintainability

Each functional responsibility is separated into its own notebook, simulating a backend service architecture.

🚀 Future Improvements

Convert notebooks into Python modules (.py)

Add a web or CLI interface

Implement user authentication

Add reporting and analytics

Containerize with Docker

👤 Author

Muhammed Uwais Adam
Python Programming | Backend Systems | Databases | Software Design
