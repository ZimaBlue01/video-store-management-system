# Application Notebooks

This folder contains the **core application logic** for the **Video Store Management System**.
Each Jupyter Notebook is responsible for a specific system function, following a modular and structured backend design approach.

The notebooks work together to provide customer management, video registration, hire/return functionality, and database interaction using MySQL.

---

## 📂 Notebook Overview

### 🔹 `db_config_and_test.ipynb`
- Establishes the connection to the MySQL database
- Reads database credentials from the environment file
- Verifies that the database connection is successful

---

### 🔹 `videoDB_tables_creation.ipynb`
- Creates all required database tables
- Defines core entities:
  - Customer
  - Video
  - Hire
- Ensures correct table relationships and constraints

---

### 🔹 `modules_initialisation.ipynb`
- Loads external libraries and shared helper modules
- Centralizes imports to ensure consistency across notebooks
- Improves maintainability and reduces duplication

---

### 🔹 `register_customer_func.ipynb`
- Implements customer registration logic
- Accepts customer details (name, surname, address, phone number)
- Prevents duplicate customer records
- Inserts validated customer data into the database

---

### 🔹 `video_register_func.ipynb`
- Handles video registration
- Stores movie details such as:
  - Movie name
  - Movie type (`R` = New release, `B` = Old release)
- Inserts video records into the database

---

### 🔹 `hire_functions.ipynb`
- Contains all hire and return logic
- Handles:
  - Hiring a video (with date tracking)
  - Returning a video
  - Availability checks
- Updates transaction records accurately in the database

---

### 🔹 `sample_data_insert.ipynb`
- Inserts sample data into the database
- Used to test system functionality
- Helps verify database integrity and logic flow

---

### 🔹 `video_store_main.ipynb`
- Acts as the **main application entry point**
- Provides a menu-driven interface for users
- Calls all functional modules using `%run`
- Coordinates the full system workflow

---

## ▶️ Execution Order (Important)

To run the system correctly:

1. Run:
   - `db_config_and_test.ipynb`
   - `videoDB_tables_creation.ipynb`
   - `modules_initialisation.ipynb`

2. Open **`video_store_main.ipynb`**
3. Run the first cell to load required modules:
   ```python
   %run register_customer_func.ipynb
   %run video_register_func.ipynb
   %run hire_functions.ipynb


4. Continue running the remaining cells to start the application

🖥️ Final Application Interface

The image below shows the final menu-driven interface presented to the user when the system is running:

![Video Store Management System](assets/vsms_ui.png)


This interface allows users to:

Register customers

Register movies

Hire out movies

Return movies

Check movie availability

Exit the application

✅ Purpose of This Design

This notebook-based structure:

Encourages modular development

Simulates backend service separation

Improves readability and maintainability

Makes the system easy to extend or refactor into .py modules in the future
