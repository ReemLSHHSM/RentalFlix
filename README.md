# RentalFlix   

## Overview

This document describes the Entity-Relationship Diagram (ERD) for the movie reservation system. The ERD includes three main entities: `Customer`, `Movie`, and `Reservation`. The relationships between these entities are detailed below.

## Entities and Relationships

### Customer Table

- **Purpose**: Stores information about customers.
- **Attributes**:
  - `CustomerID` (PK): Unique identifier for each customer.
  - `Name`: Name of the customer.
  - `Address`: Address of the customer.
  - `Phone`: Contact phone number.
  - `Email`: Contact email address.

### Movie Table

- **Purpose**: Stores information about movies.
- **Attributes**:
  - `MovieID` (PK): Unique identifier for each movie.
  - `Title`: Title of the movie.
  - `Genre`: Genre of the movie.
  - `ReleaseYear`: Release year of the movie.

### Reservation Table

- **Purpose**: Manages reservations for movies made by customers.
- **Attributes**:
  - `ReservationID` (PK): Unique identifier for each reservation.
  - `CustomerID` (FK): ID of the customer who made the reservation.
  - `MovieID` (FK): ID of the reserved movie.
  - `ReservationDate`: Date when the reservation was made.
  - `Status`: Status of the reservation (e.g., active, fulfilled, canceled).

### Relationships

1. **Customer to Reservation**:
   - **Type**: One-to-Many
   - **Description**: Each customer can make multiple reservations. The `CustomerID` in the `Reservation` table references the `CustomerID` in the `Customer` table.

2. **Movie to Reservation**:
   - **Type**: One-to-Many
   - **Description**: Each movie can have multiple reservations. The `MovieID` in the `Reservation` table references the `MovieID` in the `Movie` table.

## Diagram

Below is a simplified ERD diagram representing the relationships between the tables:   
![RentalFlix__RentalFlix ](  )