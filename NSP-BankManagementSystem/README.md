# BankPro

A Java 17+ Swing banking workspace using FlatLaf and MySQL Connector/J.

## Setup

1. Install Java 17+ and Maven.
2. Create a MySQL database named `bankpro` and a database account with access to it.
3. Copy `database.properties.example` to `database.properties` and enter the connection URL, username, and password.
4. Run `mvn compile exec:java`.
5. Start the app and choose **First time? Create administrator**. The first administrator password is stored using PBKDF2.

On the first connection the application creates its tables. Use the first-time setup action to create the first administrator. Passwords use PBKDF2. No demo balances or sample transactions are presented as bank records.

## Screens

- Sign in and authenticated workspace
- Dashboard overview and shortcuts
- Customer and account record lists with search, add, edit, and status changes
- Role-aware navigation for administrators, tellers, and read-only viewers
- Staff user creation/status controls and audit log records
- Profile password changes with PBKDF2 storage
- Deposit, withdrawal, and transfer forms with balance checks and transactional updates
- Transaction explorer and CSV report export
- User management, audit log, settings, and help workspace
- Sign out returns to sign-in

## Theme

The palette is centralized in `src/main/java/Main.java` at the `NAVY`, `BLUE`, `BG`, `INK`, `MUTED`, and `LINE` constants. Change those values to adjust the BankPro theme.

## Quality checklist

- [ ] Configure MySQL, create the first administrator in the app, and verify sign-in.
- [ ] Add customers and accounts and confirm they appear after refresh.
- [ ] Post deposits, withdrawals, and transfers; check insufficient funds and same-account transfer handling.
- [ ] Verify teller and viewer navigation and administrator user controls.
- [ ] Change a password and confirm audit entries are recorded.
- [ ] Search table records and export a report to CSV.
- [ ] Resize the window and check the navigation and tables.

## Scope

This college project started without a service layer or schema. It now initializes a small BankPro schema and supports administrator setup, teller/viewer accounts, customer and account editing, status changes, transaction receipts, and core audit entries. Charts, pagination, account statements, and detailed audit filters remain future extensions. Staff accounts are limited to teller and viewer roles; the last active administrator cannot be disabled.





