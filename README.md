# 💼 Java Employee Payroll System

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![OOP](https://img.shields.io/badge/OOP-Principles-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

A **console-based Employee Payroll Management System** built with Java, demonstrating core Object-Oriented Programming (OOP) principles including **abstraction**, **encapsulation**, **inheritance**, and **polymorphism**.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [OOP Concepts Demonstrated](#oop-concepts-demonstrated)
- [Project Structure](#project-structure)
- [Class Diagram](#class-diagram)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Application](#running-the-application)
- [Usage](#usage)
- [Code Examples](#code-examples)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 Overview

This project implements a **Payroll System** that manages employee records and calculates salaries for different types of employees. It showcases how abstract classes and inheritance can be used to create a flexible and maintainable codebase.

The system supports:
- **Full-Time Employees**: Fixed monthly salary
- **Part-Time Employees**: Hourly rate × hours worked

---

## ✨ Features

✅ **Employee Management**: Add, remove, and display employee records  
✅ **Salary Calculation**: Automatic salary computation based on employee type  
✅ **Abstract Design**: Uses abstract classes for extensibility  
✅ **Polymorphism**: Method overriding for specialized behavior  
✅ **Encapsulation**: Private fields with public getters  
✅ **Console Interface**: Simple terminal-based interaction  

---

## 🧩 OOP Concepts Demonstrated

| Concept | Implementation |
|---------|----------------|
| **Abstraction** | `Employee` abstract class with `calculateSalary()` abstract method |
| **Inheritance** | `fullTimeEmployee` and `partTimeEmployee` extend `Employee` |
| **Encapsulation** | Private fields (`name`, `id`, `monthlySalary`, etc.) with public getters |
| **Polymorphism** | Overridden `calculateSalary()` and `toString()` methods |
| **Collections** | `ArrayList<Employee>` for managing employee records |

---

## 📁 Project Structure

```
Java-Employee-Payroll-System-Project/
│
├── src/
│   └── Main.java              # Main application file containing all classes
│
├── out/                        # Compiled class files
│
├── Employee Payroll System.iml # IntelliJ IDEA module file
│
└── README.md                   # Project documentation
```

---

## 🏗️ Class Diagram

```
┌─────────────────────────┐
│   Employee (Abstract)   │
├─────────────────────────┤
│ - name: String          │
│ - id: int               │
├─────────────────────────┤
│ + getName(): String     │
│ + getId(): int          │
│ + calculateSalary(): double (abstract) │
│ + toString(): String    │
└───────────┬─────────────┘
            │
    ┌───────┴────────┐
    │                │
┌───▼──────────┐  ┌──▼─────────────────┐
│ fullTimeEmployee│  │ partTimeEmployee  │
├───────────────┤  ├────────────────────┤
│ - monthlySalary│  │ - hoursWorked     │
│               │  │ - hourlyRateySalary│
├───────────────┤  ├────────────────────┤
│ + calculateSalary() │  │ + calculateSalary()│
└───────────────┘  └────────────────────┘

┌──────────────────────────┐
│    PayrollSystem         │
├──────────────────────────┤
│ - employeeList: ArrayList│
├──────────────────────────┤
│ + addEmployee()          │
│ + removeEmployee()       │
│ + displayEmployees()     │
└──────────────────────────┘
```

---

## 🚀 Getting Started

### Prerequisites

- **Java Development Kit (JDK)** 8 or higher
- A Java IDE (IntelliJ IDEA, Eclipse, VS Code) or command-line tools

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/Java-Employee-Payroll-System-Project.git
   cd Java-Employee-Payroll-System-Project
   ```

2. **Open in your IDE**:
   - For IntelliJ IDEA: Open the project folder
   - For Eclipse: Import as existing Java project
   - For VS Code: Open the folder and ensure Java extensions are installed

### Running the Application

#### Using Command Line:

```bash
# Navigate to the src directory
cd src

# Compile the Java file
javac Main.java

# Run the application
java Main
```

#### Using IntelliJ IDEA:

1. Open the project
2. Right-click on `Main.java`
3. Select **Run 'Main.main()'**

---

## 💻 Usage

The application demonstrates the following operations:

1. **Creating Employees**:
   - Full-time employees with monthly salaries
   - Part-time employees with hourly rates

2. **Adding to Payroll System**:
   - Employees are added to the payroll management system

3. **Displaying Employee Details**:
   - Shows all employees with their calculated salaries

4. **Removing Employees**:
   - Removes employees by ID from the system

### Sample Output:

```
Initial Employee Details:
Employee[name=Vikash, id = 1, salary = 10000.0]
Employee[name=Himanshu, id = 2, salary = 70000.0]
Employee[name=Manish, id = 3, salary = 4000.0]
Removing Employee
Employee[name=Vikash, id = 1, salary = 10000.0]
Employee[name=Manish, id = 3, salary = 4000.0]
```

---

## 📝 Code Examples

### Creating a Full-Time Employee:

```java
fullTimeEmployee emp1 = new fullTimeEmployee("Vikash", 1, 10000);
payrollSystem.addEmployee(emp1);
```

### Creating a Part-Time Employee:

```java
partTimeEmployee emp3 = new partTimeEmployee("Manish", 3, 100, 40);
payrollSystem.addEmployee(emp3);
```

### Removing an Employee:

```java
payrollSystem.removeEmployee(2); // Removes employee with ID 2
```

---

## 🔮 Future Enhancements

- [ ] Add database integration (MySQL/PostgreSQL)
- [ ] Implement GUI using JavaFX or Swing
- [ ] Add employee search functionality
- [ ] Include tax deduction calculations
- [ ] Generate salary slips (PDF export)
- [ ] Add authentication and authorization
- [ ] Implement bonus and deduction management
- [ ] Add unit tests with JUnit
- [ ] Create REST API for web integration

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Himanshu Gupta**

- GitHub: [@himanshugupta91](https://github.com/himanshugupta91)
- LinkedIn: [Connect with me](https://linkedin.com/in/yourprofile)

---

## 🙏 Acknowledgments

- Inspired by real-world payroll management systems
- Built as a learning project to demonstrate OOP principles in Java
- Thanks to the Java community for excellent documentation and resources

---

<div align="center">

**⭐ Star this repository if you found it helpful!**

Made with ❤️ using Java

</div>
