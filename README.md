# Library App

## Description

Library App is a modular C# application for managing a library's books, patrons, and loans. It features a console interface, JSON-based data storage, and a clean separation of core logic, infrastructure, and presentation layers. The project is designed for extensibility and testability, with unit tests covering key business logic.

## Project Structure

- src/
  - Library.ApplicationCore/
    - Library.ApplicationCore.csproj
    - Entities/
      - Author.cs
      - Book.cs
      - BookItem.cs
      - Loan.cs
      - Patron.cs
    - Enums/
      - (enum files)
    - Interfaces/
      - ILoanRepository.cs
      - ILoanService.cs
      - IPatronRepository.cs
      - IPatronService.cs
    - Services/
      - LoanService.cs
      - PatronService.cs
  - Library.Console/
    - appSettings.json
    - CommonActions.cs
    - ConsoleApp.cs
    - ConsoleState.cs
    - Library.Console.csproj
    - Program.cs
    - Json/
      - Authors.json
      - Books.json
      - BookItems.json
      - Loans.json
      - Patrons.json
  - Library.Infrastructure/
    - Library.Infrastructure.csproj
    - Data/
      - JsonData.cs
      - JsonLoanRepository.cs
      - JsonPatronRepository.cs
- tests/
  - UnitTests/
    - LoanFactory.cs
    - PatronFactory.cs
    - UnitTests.csproj
    - ApplicationCore/
      - PatronService/
        - RenewMembership.cs
      - LoanService/
        - ReturnLoan.cs
        - ExtendLoan.cs
- README.md

## Key Classes and Interfaces

- **Entities**
  - `Author`, `Book`, `BookItem`, `Loan`, `Patron`: Core domain models representing library data.
- **Enums**
  - `LoanReturnStatus`, `LoanExtensionStatus`, `MembershipRenewalStatus`: Enumerations for operation results.
  - `EnumHelper`: Utility for enum descriptions.
- **Interfaces**
  - `ILoanRepository`, `IPatronRepository`: Abstractions for data access.
  - `ILoanService`, `IPatronService`: Abstractions for business logic services.
- **Services**
  - `LoanService`: Handles loan operations (return, extend).
  - `PatronService`: Handles patron membership operations.
- **Infrastructure**
  - `JsonData`: Loads and saves data from JSON files.
  - `JsonLoanRepository`, `JsonPatronRepository`: JSON-backed repository implementations.
- **Console**
  - `ConsoleApp`: Main console application logic and state management.
  - `CommonActions`, `ConsoleState`: Enums for user actions and app state.

## Usage

1. **Build the project**  
   Navigate to the repository root and run:
   ```sh
   dotnet build
   ```
