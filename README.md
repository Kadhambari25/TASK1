# TASK1

# domain
# Car Rental System
This project is a Vehicle/Car Rental System database design.  

## ER Diagram
The ER diagram below shows the relationships between the different entities in the system:
![ER diagram](https://github.com/user-attachments/assets/9158fefe-6e4a-4d69-bbd5-e94bd4fd5320)

## SQL Script
The SQL file contains the `CREATE TABLE` commands for all tables in this database.
- [View the SQL Script](car_rental.sql)
- 
## About the Project
The goal of this project is to design a simple database for a Car Rental System.  
It keeps track of:
- Customers
- Vehicles
- Rental transactions
- Daily rentals
- Weekly rental
  
## Tables Overview
| Table Name | Primary Key | Description |
|------------|------------|-------------|
| **CUSTOMER** | `Cust_ID` | Stores customer details like name and phone number |
| **CAR** | `Vehicle_ID` | Stores car information, rates, and availability |
| **RENTALS** | `Rental_No` | Tracks rental transactions for each customer and vehicle |
| **DAILY** | `Rental_No` | Tracks daily-based rentals |
| **WEEKLY** | `Rental_No` | Tracks weekly-based rentals |

## Keys Used

### Primary Keys
A primary key uniquely identifies each record in a table.
- CUSTOMER → `Cust_ID`
- CAR → `Vehicle_ID`
- RENTALS → `Rental_No`
- DAILY → `Rental_No`
- WEEKLY → `Rental_No`

### Foreign Keys
A foreign key links a record in one table to a record in another table.
- `RENTALS.Cust_ID` → CUSTOMER(Cust_ID)
- `RENTALS.Vehicle_ID` → CAR(Vehicle_ID)
- `DAILY.Rental_No` → RENTALS(Rental_No)
- `WEEKLY.Rental_No` → RENTALS(Rental_No)

