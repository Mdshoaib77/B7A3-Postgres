# Football Ticket Booking System Database

## Project Overview
This project is a PostgreSQL database design for a Football Ticket Booking System.

The system manages:

- Users (Football Fans and Ticket Managers)
- Football Matches
- Ticket Bookings

The database was designed using ERD and implemented with SQL queries.

---

## ERD Diagram

DrawSQL ERD Link:

https://drawsql.app/teams/md-shoaib/diagrams/football-ticket-booking-system

---

## Database Tables

### Users
Stores user information.

Attributes:
- user_id (Primary Key)
- full_name
- email
- role
- phone_number

### Matches
Stores football match information.

Attributes:
- match_id (Primary Key)
- fixture
- tournament_category
- base_ticket_price
- match_status

### Bookings
Stores booking information.

Attributes:
- booking_id (Primary Key)
- user_id (Foreign Key)
- match_id (Foreign Key)
- seat_number
- payment_status
- total_cost

---

## Relationships

- One User can have many Bookings.
- One Match can have many Bookings.
- Each Booking belongs to one User.
- Each Booking belongs to one Match.

---

## SQL Features Used

- CREATE TABLE
- PRIMARY KEY
- FOREIGN KEY
- UNIQUE
- CHECK Constraint
- INSERT INTO
- WHERE
- LIKE / ILIKE
- COALESCE
- INNER JOIN
- LEFT JOIN
- Subquery
- ORDER BY
- LIMIT
- OFFSET

---

## Queries Implemented

### Query 1
Retrieve available Champions League matches.

### Query 2
Search users whose names start with "Tanvir" or contain "Haque".

### Query 3
Show bookings with missing payment status using COALESCE.

### Query 4
Display booking details with user and match information using INNER JOIN.

### Query 5
Display all users and booking IDs using LEFT JOIN.

### Query 6
Find bookings with total cost higher than average booking cost.

### Query 7
Retrieve the top 2 most expensive matches after skipping the highest-priced match.

---

## Author

Md Shoaib

Course: PostgreSQL Database Assignment
