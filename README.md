# SQL-Capstone-Project
## Overview
AirlineDB is a comprehensive relational database system designed to manage airline operations, including flight bookings, passenger information, flight schedules, and aircraft management. The system models the complete lifecycle of air travel, from initial booking through passenger check-in and boarding pass issuance. It handles complex scenarios such as multi-passenger bookings, connecting flights, round-trip tickets, and seat assignments across different aircraft configurations.

 ## Key Features
### Booking Management

- Supports multiple passengers per booking with individual ticket issuance
- Each ticket is uniquely numbered and contains passenger information
- Handles both single and multi-segment journeys (connecting flights and round-trips)
- All tickets within a booking share the same flight segments

### Passenger and Ticket Handling

- Stores passenger identification details including name and document number
- Recognizes that passenger information may change over time
- Treats each passenger as unique for simplified data management
- Links tickets to specific flight segments through the ticket_flights relationship

### Flight Operations

- Manages flights between airports with unique flight numbers
- Flights with identical numbers share departure and destination points but differ by date
- Tracks flight schedules and routes across the airport network
- Connects flights to specific aircraft models

### Check-in and Boarding

- Issues boarding passes during flight check-in process
- Assigns specific seat numbers to passengers
- Enforces unique flight-seat combinations to prevent double bookings
- Validates that passengers can only check in for flights included in their tickets

### Aircraft and Seating

- Maintains aircraft model information with seating configurations
- Defines seat distribution across different travel classes
- Assumes one standard cabin configuration per aircraft model
- Links seat availability to specific aircraft types

## Technologies Used
### Database Architecture

- Relational Database Management System (RDBMS): The system is built on relational database principles with normalized tables and referential integrity
- Entity-Relationship Model: Uses a well-defined ER diagram to represent relationships between entities
- Data Normalization: Implements proper normalization to reduce redundancy and maintain data integrity

### Database Components

- Tables: Core entities include bookings, tickets, flights, airports, aircrafts, seats, boarding_passes, and ticket_flights
- Primary Keys: Unique identifiers for each entity (ticket numbers, flight numbers, booking references)
- Foreign Keys: Establishes relationships between related entities
- Constraints: Ensures data integrity through unique constraints (e.g., flight-seat combinations)

### Optional Enhancement Technologies

- Database Triggers: Can be implemented for advanced validation (e.g., verifying seat numbers match aircraft configurations)
- Application-Level Validation: Business logic can be enforced at the application layer
- Indexing: Likely uses indexes on frequently queried fields for performance optimization

## Conclusion
- AirlineDB represents a robust and well-structured database solution for airline management systems. Its comprehensive design addresses the complex requirements of modern air travel operations, from multi-passenger bookings to seat assignments. The system's relational architecture ensures data integrity while maintaining flexibility for various travel scenarios including connecting flights and round-trips.
- The database's normalized structure minimizes data redundancy and provides a solid foundation for building airline reservation and management applications. While the schema intentionally omits certain validations (such as seat number verification) in favor of trigger-based or application-level implementation, this design choice offers flexibility in how business rules are enforced.
- Overall, AirlineDB serves as an effective model for understanding airline operations data management and can be adapted to various scales of airline operations, from small regional carriers to large international airlines. Its clear entity relationships and logical data organization make it both maintainable and scalable for real-world airline management applications.
