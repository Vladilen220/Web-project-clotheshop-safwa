# El Safwa Clothes Shop (Educational Project)

PHP + MySQL web application for a clothing shop workflow (users, products, orders, and admin actions).

## Tech Stack

- PHP (server-side rendering)
- MySQL / MariaDB
- HTML, CSS, JavaScript
- Bootstrap / MDB assets included in the repository

## Project Structure (Important Paths)

- `index.php` – home page entry point
- `Classes/` – database and business classes
- `Members/Admin/` – admin panel pages and actions
- `Members/User/` – user account pages
- `products&orders/` – product listing and ordering pages
- `elsafwa.sql` – database schema and seed data

## Prerequisites

- PHP 8.x (CLI and web support)
- MySQL 5.7+ or MariaDB 10+
- A local web server environment:
	- Option A: PHP built-in server
	- Option B: XAMPP / WAMP / Laragon

## Local Setup

1. Clone or extract this repository.
2. Create a new database named `elsafwa`.
3. Import `elsafwa.sql` into that database.
4. Confirm DB connection settings in `Classes/DB.php`:

	 ```php
	 $con = mysqli_connect("localhost", "root", "", "elsafwa");
	 ```

	 Update host/user/password if your MySQL setup is different.

## Run (PHP Built-in Server)

From the project root:

```powershell
php -S 127.0.0.1:8080 -t .
```

Then open:

- `http://127.0.0.1:8080/index.php`

## Run (XAMPP/WAMP/Laragon)

1. Place the project inside your web root directory.
2. Start Apache and MySQL.
3. Import `elsafwa.sql` in phpMyAdmin.
4. Open the project URL in your browser.

## Troubleshooting

- **Database connection failed**
	- Recheck credentials in `Classes/DB.php`.
	- Ensure MySQL service is running.

- **Page loads without styles/scripts**
	- Run from the project root so relative asset paths resolve correctly.

- **Works on Windows but not Linux/macOS**
	- Some include paths use different letter casing (for example `Navigation&footer` vs `navigation&footer`). Linux/macOS is case-sensitive.

## Notes

- This repository is for educational use.
- Keep sensitive credentials out of source control if deploying beyond local development.
