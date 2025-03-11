# Library Management System

A Django-based Library Management System that allows for the management of books, users, and loan records. This system helps librarians manage book inventories, issue books to members, track overdue fines, and search for books in the catalog.

## Features

- **Book Management**: Add, update, and remove books from the library collection.
- **Book Search**: Search books by title, author, or ISBN.
- **Book Checkout**: Issue books to members and track due dates.
- **Book Return**: Handle book returns and calculate overdue fines if necessary.
- **Member Management**: Add and manage member details (name, contact information, etc.).
- **Overdue Fines**: Automatically calculate fines for overdue books based on the number of late days.
- **Library Inventory**: View and manage the current book inventory and availability.

## Requirements

- Python 3.x
- Django 3.x (or the version you're using)
- SQLite3 (default database used by Django)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/library-management-system.git
    ```

2. Navigate to the project directory:
    ```bash
    cd library-management-system
    ```

3. Create a virtual environment (optional but recommended):
    ```bash
    python -m venv venv
    ```

4. Activate the virtual environment:
    - On Windows:
      ```bash
      venv\Scripts\activate
      ```
    - On macOS/Linux:
      ```bash
      source venv/bin/activate
      ```

5. Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```

6. Apply the migrations to set up the database:
    ```bash
    python manage.py migrate
    ```

7. Create a superuser to access the Django admin panel:
    ```bash
    python manage.py createsuperuser
    ```

8. Run the development server:
    ```bash
    python manage.py runserver
    ```

9. Open your browser and visit `http://127.0.0.1:8000/` to use the system.

## Usage

- **Admin Panel**: Access the Django admin panel at `http://127.0.0.1:8000/admin/` to manage books, members, and loan records.
- **Library Management Interface**: Use the provided interface to:
  - **Manage Books**: Add new books, update details, or remove books.
  - **Search Books**: Search for books by title, author, or ISBN.
  - **Loan Management**: Issue books to members, check their due dates, and manage returns.
  - **Overdue Fines**: View overdue fines for members based on late book returns.

## Database Structure

This system uses SQLite3 as the default database, and the following models are used:

- **Book**: Stores information about books (title, author, ISBN, available copies).
- **Member**: Stores member details (name, contact information).
- **Loan**: Records the details of book loans (book ID, member ID, issue date, due date, return date).
- **Fine**: Tracks overdue fines (member ID, fine amount, due date).

## Example

Once the system is set up, you can:

1. Add a new book via the Django admin or the interface.
2. Issue books to members and track their due dates.
3. Return books and calculate overdue fines if applicable.

```bash
# In the Django admin panel:
1. Navigate to the "Books" section and add a new book.
2. Navigate to the "Members" section to add new members.
3. Issue a book by selecting a member and loaning them a book.
4. Track the return of books and calculate fines for overdue items.
