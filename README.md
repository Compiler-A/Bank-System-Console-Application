# 🏦 Bank System Console Application

A fully-featured console-based banking system built in **C++** using Object-Oriented Programming principles. This project covers client management, user authentication, financial transactions, currency exchange, and more — all backed by file-based persistent storage.

---

## 📌 About The Project

This was developed as a learning project to practice **OOP in C++**, covering real-world concepts like class inheritance, encapsulation, file I/O, and screen-based UI design in a console environment.

The system is split across **4 main modules** (Projects 01–04), each adding more features on top of the previous one, until it becomes a complete banking application.

---

## ✨ Features

### 👤 Client Management
- Add new clients
- Update client information
- Delete clients
- Find / search for a client by account number
- List all clients

### 🔐 User Management & Authentication
- Login screen with username & password
- Role-based permissions per user
- Add, update, delete, and find users
- List all system users
- Login activity register/log

### 💰 Transactions
- **Deposit** funds into an account
- **Withdraw** funds from an account
- **Transfer** funds between two accounts
- View **Transfer Log** (full history with date, amount, source & destination)
- View **Total Balances** across all clients

### 💱 Currency Exchange
- List all currencies with live rates
- Find a specific currency
- Update currency exchange rates
- Currency calculator (convert between any two currencies)

---

## 🗂️ Project Structure

```
├── Full Project (01 to 04).cpp     # Entry point (main)
│
├── Core Classes
│   ├── clsPerson.h                 # Base class: FirstName, LastName, Email, Phone
│   ├── clsBankClient.h             # Inherits clsPerson — full client logic + file I/O
│   ├── clsUser.h                   # System user with permissions
│   └── clsCurrency.h               # Currency data & exchange logic
│
├── Utility Classes
│   ├── clsString.h                 # String manipulation helpers
│   ├── clsDate.h                   # Date & time utilities
│   ├── clsInputValidate.h          # Input validation
│   └── clsUtil.h                   # General utility functions
│
├── Screen Classes (UI Layer)
│   ├── clsMainScreen.h
│   ├── clsLoginScreen.h
│   ├── clsAddNewClientScreen.h
│   ├── clsUpdateClientScreen.h
│   ├── clsDeleteClientScreen.h
│   ├── clsFindClientScreen.h
│   ├── clsClientListScreen.h
│   ├── clsDepositScreen.h
│   ├── clsWithdrawScreen.h
│   ├── clsTransferScreen.h
│   ├── clsTransferLogScreen.h
│   ├── clsTotalBalancesScreen.h
│   ├── clsTransactionsScreen.h
│   ├── clsManageUsersScreen.h
│   ├── clsAddNewUserScreen.h
│   ├── clsUpdateUserScreen.h
│   ├── clsDeleteUserScreen.h
│   ├── clsFindUserScreen.h
│   ├── clsListUsersScreen.h
│   ├── clsLoginRegisterScreen.h
│   ├── clsCurrencyExchangeMainScreen.h
│   ├── clsCurrenciesListScreen.h
│   ├── clsFindCurrencyScreen.h
│   ├── clsUpdateCurrencyRateScreen.h
│   └── clsCurrencyCalculatorScreen.h
│
└── Data Files
    ├── Clients.txt                 # Persistent client records
    ├── Users.txt                   # System users & permissions
    ├── Currencies.txt              # Currency data & exchange rates
    ├── TransfersLog.txt            # Full log of all transfers
    └── LoginRegister.txt           # Login activity history
```

---

## 🏗️ Architecture & Design

The project follows **Object-Oriented Programming** principles throughout:

- **Inheritance** — `clsBankClient` and `clsUser` both inherit from `clsPerson`
- **Encapsulation** — Private fields with getters/setters (using `__declspec(property)`)
- **Separation of Concerns** — Logic classes are fully separated from Screen (UI) classes
- **File-Based Persistence** — All data is stored and retrieved from `.txt` files using a custom `#//# `delimiter
- **Mode Pattern** — Entities use an `enMode` enum (`EmptyMode`, `AddNewMode`, `UpdateMode`) to manage their state

---

## 🛠️ Build & Run

### Requirements
- Windows OS
- Visual Studio (any recent version)
- C++17 or later

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/Compiler-A/Bank-System-Console-Application.git
   ```
2. Open `Full Project (01 to 04).sln` in **Visual Studio**
3. Build the solution (`Ctrl + Shift + B`)
4. Run the project (`F5` or `Ctrl + F5`)

> ⚠️ Make sure the `.txt` data files (`Clients.txt`, `Users.txt`, `Currencies.txt`, etc.) are in the **same directory** as the executable, or the working directory of the project.

---

## 📷 How It Works

When launched, the application shows a **Login Screen**. After successful authentication, the user is taken to the **Main Menu** where they can navigate to any of the system's modules depending on their assigned permissions.

All data is read from and written to plain text files, making the system fully persistent without needing a database.

---

## 🧠 What I Learned

- Designing class hierarchies with inheritance in C++
- Separating business logic from UI (screen classes)
- Reading from and writing to files using `fstream`
- Using enums to manage object state
- Building a fully navigable console menu system
- Input validation and error handling in C++

---

## 🔗 Related Project

This console application was the foundation for a **Desktop GUI version** built later:

👉 [Bank System Desktop Application](https://github.com/Compiler-A/Bank-System-Desktop-Application)

---

## 📄 License

This project is open source and available for learning purposes.