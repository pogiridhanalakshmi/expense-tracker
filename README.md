# Expense Tracker

A web-based application for tracking and summarizing personal or business expenses. View daily, weekly, and monthly summaries, filter by category and date, and analyze spending with charts.

![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat&logo=php&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white)

---

## Features

- **User authentication** — Sign up, login, logout with session management
- **Expense CRUD** — Add, update, and delete expenses with category and description
- **Summaries** — Daily, weekly, and monthly expense overviews
- **Charts** — Category-wise and date-wise visualizations (Canvas.js)
- **Filter & sort** — Filter by category, sort by amount or date
- **Responsive UI** — Tailwind CSS, mobile-friendly layout

---

## Tech Stack

| Layer    | Technologies        |
|----------|---------------------|
| Frontend | HTML, Tailwind CSS, JavaScript |
| Backend  | PHP                 |
| Database | MySQL               |

---

## Project Structure

```
Expense_tracker-main/
├── Expense_tracker-main/     # Application root (place in XAMPP htdocs)
│   ├── index.php             # Landing page
│   ├── login.php / signup.php / logout.php
│   ├── expense.php            # Expense list (filter, sort)
│   ├── expense_form.php       # Add/Edit expense
│   ├── expense_fetch.php      # Expense data API
│   ├── chart.php             # Charts (category, monthly, yearly)
│   ├── delete.php            # Delete expense
│   ├── about.php             # Contact us
│   ├── connection.php        # DB config
│   ├── header.php / footer.php
│   ├── js/                   # Scripts (canvas, fonts, main)
│   ├── images/               # Assets
│   └── *.sql                 # DB schemas (signup, expense, contact)
├── .gitignore
└── README.md
```

---

## How to Run

### Prerequisites

- [XAMPP](https://www.apachefriends.org/) (Apache + MySQL + PHP)
- A modern browser

### Setup

1. **Install XAMPP** and start **Apache** and **MySQL** from the XAMPP Control Panel.

2. **Create the database**
   - Open **phpMyAdmin** (http://localhost/phpmyadmin).
   - Create a database named **`p2`** (or update `connection.php` to use your DB name).
   - Import the SQL files from `Expense_tracker-main/`:
     - `signup (2).sql` — users table
     - `expense (2).sql` — expenses table
     - `contact.sql` — contact messages (optional)

3. **Deploy the project**
   - Copy the **`Expense_tracker-main`** folder (the inner one) into `C:\xampp\htdocs\`.
   - So the app is at: `C:\xampp\htdocs\Expense_tracker-main\`

4. **Configure DB** (if needed)
   - Edit `Expense_tracker-main/connection.php` and set:
     - `$server`, `$username`, `$password`, `$db` to match your MySQL setup.

5. **Open in browser**
   - Go to: **http://localhost/Expense_tracker-main/**

---

## Database

- **DB name:** `p2` (change in `connection.php` if different)
- **Tables:** `signup` (users), `expense` (expenses with category, amount, date), `contact` (optional)

---

## License

This project is open source and available for educational and personal use.
