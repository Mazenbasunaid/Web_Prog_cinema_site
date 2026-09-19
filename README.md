# Cinema Booking Site

A PHP + MySQL web app for browsing movies and booking tickets — register, log in, browse what's showing, and book a seat. Loosely inspired by sites like Cinema City.

## Features

- User registration and login (passwords hashed with `password_hash`)
- Browse movies with posters and descriptions
- Book a movie and track bookings per user
- Session-based authentication via cookies

## Tech

- PHP (vanilla, no framework)
- MySQL / MariaDB
- Vanilla CSS

## Setup

1. Create a MySQL/MariaDB database named `cinema` and import the schema + sample data:
   ```
   mysql -u root -p cinema < cinema.sql
   ```
2. Update the database connection settings in `utils/init.php` if your local MySQL setup differs from the defaults (`root` user, no password, `localhost`).
3. Serve the project with PHP's built-in server from the project root:
   ```
   php -S localhost:8000
   ```
4. Visit `http://localhost:8000` in your browser.

> Note: `cinema.sql` ships with placeholder demo accounts for local testing only — no real user data.

## Project structure

```
├── index.php                  # Homepage / movie listing
├── login.php / register.php   # Auth pages
├── booking.php                # Booking flow
├── poster.php                 # Movie poster display
├── logout.php
├── includes/                  # Shared head/nav partials
├── utils/init.php             # DB connection + session bootstrap
└── cinema.sql                 # Database schema + sample data
```

## Background

Built as a university web programming project during my BSc in Computer Science Engineering.
