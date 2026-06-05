# My Coffee Shop ☕

A **Java Swing desktop application** for managing a coffee shop — built with pure Java, no external dependencies.

## Features

- **Employee Management** — Add, view, update, and remove employees (Chefs, Waiters, Cleaners) via an admin panel
- **Customer Ordering** — Browse a menu of coffees and snacks, select items with quantities, and place orders
- **Payment Processing** — Supports both hand cash and online payment (Bkash, Nagad, Rocket)
- **Admin Authentication** — Login and signup system with flat-file storage
- **User-friendly GUI** — Built entirely with Java Swing (JFrame, JTable, JOptionPane, etc.)

## Screenshots

*(Add screenshots here)*

## Tech Stack

- **Language:** Java (JDK 8+)
- **UI Framework:** Java Swing
- **Build System:** None (compile & run with `javac` / `java`)
- **Dependencies:** None (pure JDK)
- **Storage:** Flat-file (`data/user_data.txt`)

## Project Structure

```
├── Start.java                  # Entry point
├── Start11.java                # Alternative entry point (console test)
├── Employeee/                  # Employee model classes
│   ├── Employee.java           # Base employee class
│   ├── Chef.java               # Chef subclass
│   ├── Waiter.java             # Waiter subclass
│   ├── Cleaner.java            # Cleaner subclass
│   └── Manager.java            # Employee management logic
├── FileIo/
│   └── Registration.java       # File-based user registration
├── GUI/                        # All Swing UI screens
│   ├── Coffee.java             # Welcome / splash screen
│   ├── FirstPage.java          # Role selection (Admin / Customer)
│   ├── AdminLogin.java         # Admin login
│   ├── AdminSignUp.java        # Admin registration
│   ├── Admin1st.java           # Admin dashboard
│   ├── ChefInfo.java           # Chef CRUD table
│   ├── WaiterInfo.java         # Waiter CRUD table
│   ├── CleanerInfo.java        # Cleaner CRUD table
│   ├── CustomerInfo.java       # Customer information form
│   ├── MenuCard.java           # Menu with checkboxes & spinners
│   ├── Order.java              # Order summary
│   ├── Payment.java            # Payment method selection
│   ├── OnlinePayment.java      # Bkash / Nagad / Rocket
│   └── LastPage.java           # Final confirmation
├── Interface/
│   └── IinterfaceEmployee.java # Employee interface
├── Image/                      # Image assets for the UI
└── data/
    └── user_data.txt           # Admin credentials storage
```

## How to Run

1. **Compile** all Java files:
   ```bash
   javac Start.java
   ```

2. **Run** the application:
   ```bash
   java Start
   ```

Alternatively, compile the entire project:
```bash
javac -d . *.java Employeee/*.java FileIo/*.java GUI/*.java Interface/*.java
java Start
```

## Application Flow

```
Welcome Screen (Coffee.java)
  └── Role Selection (FirstPage.java)
        ├── Admin
        │     ├── Login / Sign Up
        │     └── Dashboard → Manage Chefs, Waiters, Cleaners
        └── Customer
              └── Info → Menu → Order → Payment
                    ├── Hand Cash
                    └── Online (Bkash / Nagad / Rocket)
```

## Notes

- The application is purely desktop-based with no network connectivity
- All menu items are priced at a flat rate of 100 (customizable in `MenuCard.java`)
- Admin credentials are stored in plain text in `data/user_data.txt`
- The project has no external library dependencies — just standard JDK

## License

This project is open source and available for educational purposes.
