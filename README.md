# CS3SY26_ProjectProposal by Aline Teresa Mendoza from CS Unit of PSHS

### Project Title or Name of the Application	: BudgeDING
### Section			   	      : 9 - Beryllium
### Group Members			    : SANTOS, Marquiz, SUDEEP, Shiloh, TAYAO, Josemaria
### Date (Proposal Date)  : Nov 5, 2026

### Project Description:
 - **BudgeDING** is a Python-based lightweight budgeting app designed to allocate your salary towards different categories of expenses.        Users will have to input user name, their own password, their salary, and percentages for each category.

- A brief summary of the project description and the need for it.

- Describes system components, features, and expected outputs clearly and logically. NOTE: Clearly described the elements(classes), their attributes and methods and how they will interact with each other.

- Include the description as well of your target demographics as the user of your application. 

- The description is then followed by the class diagram, depicting clearly what was described.

```mermaid
classDiagram
    class SimpleBudgetApplication {
        -UserManager userManager
        -BudgetPlanner budgetPlanner
        +run()
    }

    class UserManager {
        -List~User~ users
        +registerUser(user: User)
        +getUser(username: str) User
        +authenticate(username: str, password: str) bool
    }

    class User {
        -str username
        -str password
        +verifyPassword(password: str) bool
    }

    class BudgetPlanner {
        -float salary
        -List~BudgetCategory~ categories
        +setSalary(amount: float)
        +validatePercentages() bool
        +calculateBreakdown()
    }

    class BudgetCategory {
        #str name
        #float percentage
        #float minPct
        #float maxPct
        +setPercentage(pct: float)
        +calculateAmount(salary: float) float
        +validateRange() bool
    }

    class Basics {
        +validateRange() bool
    }

    class GuiltFree {
        +validateRange() bool
    }

    class LongTermGoals {
        +validateRange() bool
    }

    class InvestingDebt {
        +validateRange() bool
    }

    class ShortTermGoals {
        +validateRange() bool
    }

    SimpleBudgetApplication --> UserManager : manages
    SimpleBudgetApplication --> BudgetPlanner : manages
    UserManager o-- User : stores
    BudgetPlanner o-- BudgetCategory : contains
    BudgetCategory <|-- Basics : inherits
    BudgetCategory <|-- GuiltFree : inherits
    BudgetCategory <|-- LongTermGoals : inherits
    BudgetCategory <|-- InvestingDebt : inherits
    BudgetCategory <|-- ShortTermGoals : inherits
```

### Goals:

To develop a functional, educational Python simulation that demonstrates how Object-Oriented Programming models real-world smart home automation while promoting awareness of household energy efficiency[cite: 7].

- Objective 1: Design and implement an inheritance hierarchy with one parent class (SmartDevice) and at least three specialized child classes (SmartLight, SmartThermostat, SmartLock) by the end of the 3rd Quarter[cite: 7].
- Objective 2: Build an interactive command-line menu (or tkinter GUI) in SmartHomeHub that lets users add devices, trigger sensor events, and view real-time automation logs[cite: 7].
- Objective n: Implement an accurate energy consumption calculator that reports total kilowatt-hours (kWh) used across simulated time intervals and test the system across at least 5 household scenarios before the 4th Quarter deadline[cite: 7].

[Click here for Rubrics and Sample projects](https://docs.google.com/document/d/1xKd1CqK6DcNWS2_oJPBNtY5n3I3Hqiw8FY3W295Iqfk/edit?usp=sharing)
