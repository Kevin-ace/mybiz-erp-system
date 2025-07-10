
Built by https://www.blackbox.ai

---

# MyBiz ERP System

## Project Overview
MyBiz is an Enterprise Resource Planning (ERP) system developed using Flask. It integrates components for Customer Relationship Management (CRM), Sales, Accounting, and Project Management into a seamless web application. The system uses a SQLite database to manage and store data related to users, customers, products, sales orders, invoices, and projects.

## Installation
To set up the MyBiz ERP system locally, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/mybiz.git
   cd mybiz
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment:**
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

4. **Install the required dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

5. **Initialize the database:**
   Ensure you have the SQLite database created by running the application once:
   ```bash
   python app.py
   ```

6. **Access the application:**
   Open your web browser and go to `http://127.0.0.1:5000/`.

## Usage
Once the application is running, you can access different components using the following endpoints:

- **CRM:** `/crm`
- **Sales:** `/sales`
- **Accounting:** `/accounting`
- **Project Management:** `/project`

### Home Route
The home route (`/`) will return a welcome message in JSON format:
```json
{"message": "Welcome to MyBiz ERP system"}
```

## Features
- User authentication and management
- Customer management (add, view, edit customers)
- Product management (create, update, delete products)
- Sales order creation and tracking
- Invoice generation and status tracking
- Project management with associated tasks

## Dependencies
The project relies on the following Python libraries, which can be found in `requirements.txt`:
- Flask
- Flask-SQLAlchemy

Ensure these are installed to use the application properly.

## Project Structure
```
mybiz/
│
├── app.py                # Main application entry point
├── models.py             # Database models for application
├── extensions.py         # Database extension setup
└── routes/               # Directory containing route blueprints
    ├── crm.py           # CRM related routes
    ├── sales.py         # Sales related routes
    ├── accounting.py     # Accounting related routes
    └── project.py        # Project management related routes
```

### Additional Notes
- Ensure that Python 3.x is installed on your machine.
- For production, consider using a more robust database than SQLite and set appropriate configurations.
- Always keep dependencies up-to-date for security and performance improvements.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing
Contributions are welcome! Please submit a pull request with your proposed changes, and describe the purpose of the modifications.