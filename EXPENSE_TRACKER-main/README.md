# Expense Tracker Web Application

A full-stack expense management web application for tracking income, expenses, savings, and financial activity. It includes user authentication, dashboards, charts, transaction history, spending insights, and profile management.

Built with Flask, PostgreSQL, and Matplotlib.

## Features

- User registration and login
- Add income, expense, and savings transactions
- Dashboard with balance and financial summaries
- Category- and date-based statistics
- Financial graph generation
- Smart spending analysis and suggestions
- User profile management
- Balance calculation:

  ```text
  Balance = Total Income - Total Expenses - Total Savings
  ```

## Tech Stack

| Component | Technology |
| --- | --- |
| Frontend | HTML5, CSS3, Jinja templates |
| Backend | Python, Flask |
| Database | PostgreSQL |
| Charts | Matplotlib |
| Environment variables | python-dotenv |

## Project Structure

```text
EXPENSE_TRACKER-main/
├── static/
│   ├── css/
│   │   └── style.css
│   └── graphs/
│       └── graph_*.png              # Generated automatically
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── dashboard.html
│   ├── add_expense.html
│   ├── statistics.html
│   └── stats_result.html
├── utils/
│   ├── analyzer.py
│   ├── filters.py
│   └── graph.py
├── .env                             # Local environment configuration
├── .gitignore
├── app.py
├── requirements.txt
└── README.md
```

## Prerequisites

Before running the project, install:

- Python 3.9 or later
- PostgreSQL
- pip

Check Python and pip:

```powershell
py --version
pip --version
```

## Setup and Installation

### 1. Open the project folder

```powershell
cd expense-tracker-main\EXPENSE_TRACKER-main
```

### 2. Create a virtual environment

```powershell
py -m venv .venv
```

### 3. Activate the virtual environment

PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

If PowerShell blocks activation, run this once in the current terminal:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

Then activate it again:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 4. Install Python dependencies

```powershell
pip install -r requirements.txt
pip install python-dotenv psycopg2-binary
```

> `python-dotenv` and `psycopg2-binary` are required by `app.py`. Add them to `requirements.txt` if you want all dependencies installed with one command.

## Database Configuration

This project uses PostgreSQL.

Create a PostgreSQL database, for example:

```sql
CREATE DATABASE expense_tracker;
```

Create or update the `.env` file in the project root:

```env
SECRET_KEY=replace_with_a_long_random_secret_key
DATABASE_URL=postgresql://postgres:your_postgres_password@localhost:5432/expense_tracker
```

Replace:

- `postgres` with your PostgreSQL username if different
- `your_postgres_password` with your PostgreSQL password
- `expense_tracker` with your database name if different

The application creates its required tables automatically when it starts.

## Run the Application

With the virtual environment activated, run:

```powershell
python app.py
```

The server will start at:

```text
http://127.0.0.1:5000/
```

Open this address in your browser.

To stop the server, press:

```text
Ctrl + C
```

## Troubleshooting

### `ModuleNotFoundError: No module named 'dotenv'`

Run:

```powershell
pip install python-dotenv
```

### `ModuleNotFoundError: No module named 'psycopg2'`

Run:

```powershell
pip install psycopg2-binary
```

### PostgreSQL connection error

Check that:

- PostgreSQL is installed and running.
- The database exists.
- The `DATABASE_URL` in `.env` is correct.
- Your PostgreSQL username and password are valid.

### Port 5000 is already in use

Stop the other process using port `5000`, or update the `app.run()` configuration in `app.py` to use another port.

## License

This project is for educational purposes.


## Author

### Tanu Raj                │ 
