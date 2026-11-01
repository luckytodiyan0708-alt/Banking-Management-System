# Banking Management System using Oracle PL/SQL

## Requirements
- Oracle Database 12c or later
- Oracle SQL Developer

## How to run
1. Open Oracle SQL Developer and connect to your own schema.
2. Open `Banking_Management_System_PL_SQL.sql`.
3. Press **F5 (Run Script)**, not Ctrl+Enter.
4. Open **View > DBMS Output**, click the green plus, and enable output for your connection if needed.
5. Review the Script Output and query results.

The script drops and recreates only these project objects in the connected schema:
`BANK_PKG`, `TRG_VALIDATE_BANK_TXN`, `BANK_TRANSACTIONS`, `ACCOUNTS`, and `CUSTOMERS`.
Do not run it in a schema containing objects with those names that you need to keep.

## Modules
- Customer registration
- Savings/current account opening
- Deposit
- Withdrawal with insufficient-balance validation
- Account-to-account transfer
- Balance enquiry
- Account statement using an explicit cursor
- Transaction validation trigger
- Package specification and package body
- Primary keys, foreign keys, UNIQUE and CHECK constraints
- Exception handling and transaction savepoints

## Important design note
Package procedures intentionally do not issue COMMIT. The caller controls the transaction boundary. The demonstration block commits after all sample operations succeed and rolls back if the demonstration fails.

This is an educational MCA project, not production-ready banking software. A real banking platform needs authentication, authorization, audit controls, encryption, regulatory controls, reconciliation, fraud monitoring, and independent security testing.
