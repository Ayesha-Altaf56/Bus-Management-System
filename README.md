# Bus Booking Management System

A text-based command-line interface (CLI) application for managing bus reservations, users, and administrative tasks. Built with Java, this project uses file-based persistence for straightforward data storage and management.

## Features

### 👨‍💼 Admin Module
- **Secure Authentication:** Login and Sign Up functionality for administrators.
- **Profile Management:** View and update administrative profiles.
- **User Management:** Add, update, delete, search, and view all registered users.
- **Booking Management:** Add, update, delete, search, and view all passenger bookings.
- **Bus Fleet Management:** Load and manage route and fare data for multiple bus services including:
  - Daewoo Express
  - Faisal Movers
  - Silk Line
  - Kainat Travels
  - Al Makkah Travels

### 👤 User Module
- **Secure Authentication:** Sign Up and Sign In functionality for standard users with password strength validation.
- **Profile Management:** View and update personal details (Name, Phone, Email, Password).
- **Bus Booking:** Search and book buses by source, destination, and date.
- **Seat Selection:** Select seats using a text-based layout and automatically calculate fares based on economy or business class selection.
- **Dashboard:** View accrued loyalty points and complete booking history.

## Architecture & Data Storage

The system leverages simple text files (`.txt`) to persist data locally, acting as a lightweight database:
- `admins.txt` - Stores administrator credentials and details.
- `User.txt` & `users.txt` - Stores user account information and loyalty points.
- `booking.txt` & `Bookings.txt` - Maintains a record of all bus bookings.
- `*travels.txt` / `*movers.txt` / `*express.txt` - Individual files containing specific bus numbers, routes, plate numbers, and class fares for each respective service.

## Prerequisites

- Java Development Kit (JDK) 8 or higher.

## How to Run

1. Open your terminal or command prompt.
2. Navigate to the project directory:
   ```bash
   cd "d:\Projects\bus management system"
   ```
3. Compile the Java files:
   ```bash
   javac Main.java AdminModule.java FinalUserModule.java graphics.java
   ```
4. Run the main application:
   ```bash
   java Main
   ```
5. Follow the interactive on-screen menus to navigate between the Admin and User panels.

## Project Structure

- `Main.java`: The main entry point of the application displaying the primary selection menu.
- `AdminModule.java`: Handles all administrative logic, file read/write operations for admin features, and entity management.
- `FinalUserModule.java`: Handles user authentication, profile management, search, and bus booking logic.
- `graphics.java`: Contains ASCII art and styling elements for the console output.
