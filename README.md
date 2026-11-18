# PHP CRUD with AJAX and MySQL — Complete Project

The complete source code from the Simplified Dev Code Camp video
"PHP CRUD with AJAX and MySQL — Complete Project (No Page Refresh)".

Create, read, update and delete student records with jQuery AJAX —
the page never refreshes. The back end is object-oriented PHP with
PDO prepared statements, and every API endpoint returns JSON.

## Project structure

```
config/Database.php   PDO database connection class
models/Student.php    Student model (create / readAll / readOne / update / delete)
api/create.php        POST endpoint — add a student
api/read.php          GET endpoint — all students, one student (?id=), or search (?search=)
api/update.php        POST endpoint — update a student
api/delete.php        POST endpoint — delete a student
index.php             Bootstrap UI + jQuery AJAX (table, modal, live search)
database.sql          MySQL schema + sample data
```

## Requirements

- XAMPP (or any Apache + MySQL + PHP 8 setup)
- PHP 8.0 or higher with the PDO MySQL extension enabled

## Setup

1. Copy this project folder into your XAMPP `htdocs` folder,
   for example `htdocs/php-crud-ajax`.
2. Start **Apache** and **MySQL** from the XAMPP control panel.
3. Open **phpMyAdmin** (`http://localhost/phpmyadmin`), go to the
   **Import** tab and import `database.sql`.
   This creates the `crud_ajax_db` database, the `students` table
   and four sample students.
4. If your MySQL username/password are not `root` / empty, update
   them in `config/Database.php`.
5. Open `http://localhost/php-crud-ajax/index.php` in your browser.

## Try it

- Click **Add Student**, fill the form and save — the table updates instantly.
- Click **Edit** on any row to change it in the modal.
- Click **Delete** and confirm — the row disappears without a refresh.
- Type in the search box — the list filters as you type.
