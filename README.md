# 🏦 MyATM – Java ATM Simulation

A simple **ATM simulation system developed in Java** to demonstrate core Java programming concepts such as **Object-Oriented Programming (OOP), Collection Framework, Exception Handling, and basic account transaction management**.

## 📌 Project Overview

**MyATM** simulates the basic operations of an ATM. The application allows a user to create an account, log in using a password, check their balance, deposit money, withdraw money, and view their transaction history.

The project is implemented as a **single Java file (`MyATM.java`)**, making it simple to understand, run, maintain, and demonstrate during practical examinations or viva.

## ✨ Features

- 👤 User account registration
- 🔐 Password-based authentication
- 🔢 Maximum 3 login attempts
- 💰 Check account balance
- 💵 Deposit money
- 💸 Withdraw money
- 📋 View transaction history
- 🕒 Transaction date and time tracking
- ⚠️ Invalid amount validation
- 🚫 Insufficient funds handling
- ❌ Invalid menu option handling
- 🧩 Custom exception handling
- 📦 Collection Framework implementation

## 🧠 Java Concepts Demonstrated

### 1. Object-Oriented Programming

The project uses multiple classes within a single Java file:

- `MyATM`
- `ATM`
- `Account`
- `Transaction`
- `InvalidAmountException`
- `InsufficientFundsException`

The project demonstrates:

- **Encapsulation** – private fields and methods
- **Inheritance** – custom exceptions extend Java's `Exception` class
- **Abstraction** – ATM operations are handled through dedicated methods
- **Objects and Classes** – accounts and transactions are represented as objects

### 2. Collection Framework

The project uses Java collections to manage ATM data.

**HashMap**

```java
Map<String, Account> accounts = new HashMap<>();
```

Used to store user accounts.

**ArrayList**

```java
List<Transaction> transactions = new ArrayList<>();
```

Used to maintain the transaction history of an account.

### 3. Exception Handling

The application handles both built-in and custom exceptions.

Built-in exception:

```text
NumberFormatException
```

Custom exceptions:

```text
InvalidAmountException
InsufficientFundsException
```

This prevents invalid input and transaction errors from terminating the application unexpectedly.

### 4. BigDecimal

`BigDecimal` is used for handling account balances and transaction amounts.

This provides better precision for monetary calculations compared with using floating-point types such as `float` or `double`.

## 🔄 Application Flow

```text
Start
  │
  ▼
Enter Name
  │
  ▼
Create Password
  │
  ▼
Account Created
  │
  ▼
Password Authentication
  │
  ├── Incorrect → Retry (Maximum 3 Attempts)
  │
  ▼
ATM Menu
  │
  ├── Check Balance
  │
  ├── Deposit Money
  │
  ├── Withdraw Money
  │
  ├── Transaction History
  │
  └── Exit
  │
  ▼
End
```

## 💻 Requirements

- **Java JDK 8 or later**
- Command Prompt / PowerShell / Terminal
- Any Java-supported IDE such as:
  - IntelliJ IDEA
  - Eclipse
  - Visual Studio Code
  - NetBeans

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/DXorganization-spec/MyATM.git
```

### 2. Navigate to the project directory

```bash
cd MyATM
```

### 3. Compile the Java program

```bash
javac MyATM.java
```

### 4. Run the application

```bash
java MyATM
```

## 🖥️ Example Menu

```text
==============================================
                 MY-ATM MENU
==============================================

1. Check Balance
2. Deposit Money
3. Withdraw Money
4. Transaction History
5. Exit

==============================================
Choose an option:
```

## 💰 Default Account

When the application starts, the user creates an account.

The current implementation initializes the account with an opening balance of:

```text
₹1000.00
```

The user can then perform deposits and withdrawals.

## 📋 Transaction History

Every successful deposit or withdrawal is stored in the account's transaction history.

Each transaction records:

- Transaction type
- Amount
- Balance after transaction
- Date and time

Example:

```text
2026-10-15 18:30:20 | Deposit | ₹500.00 | Balance: ₹1500.00
2026-10-15 18:35:10 | Withdrawal | ₹200.00 | Balance: ₹1300.00
```

## ⚠️ Exception Scenarios

The application handles situations such as:

| Situation | Handling |
|---|---|
| Empty name | Registration stopped |
| Empty password | Registration stopped |
| Invalid amount | `NumberFormatException` |
| Zero/negative amount | `InvalidAmountException` |
| Withdrawal greater than balance | `InsufficientFundsException` |
| Invalid menu choice | Validation message |
| Incorrect password | Login retry |
| More than 3 failed attempts | Login terminated |

## 📂 Project Structure

```text
MyATM/
│
├── MyATM.java
└── README.md
```

The complete Java application is intentionally maintained in a **single file** for easier management and demonstration.

## 🎯 Project Objective

The main objective of this project is to demonstrate how fundamental Java concepts can be combined to build a simple real-world application.

The project focuses particularly on:

- Object-Oriented Programming
- Collection Framework
- Exception Handling
- User input handling
- Basic banking transaction logic

## 🔮 Future Enhancements

Possible future improvements include:

- Graphical User Interface (GUI)
- Multiple user accounts
- PIN-based authentication
- ATM-style interface
- Persistent data storage
- Database integration
- Account transfer functionality
- Mini statement generation
- Improved security

## 👨‍💻 Author

**Aditya Satpute**

### Project

**MyATM – Java ATM Simulation**

---

⭐ If you find this project useful, consider giving the repository a star!
