# Yuva_Week4_Code-Refactoring-and-Optimization

Refactored Java command-line inventory manager, compatible with Java 8+ and requiring no external libraries to run.

## Features
- Add, list, search by ID, update, and delete books.
- Validates blank fields and publication years.
- Prevents duplicate ISBN values.
- Separates the `Book` model, `LibraryManager` business logic, and `Main` console interface.
- Uses an in-memory `ArrayList`; records reset when the program exits.

## Compile and run (PowerShell)
Open a terminal in the project root:
```powershell
mkdir out
javac -d out src/main/java/Book.java src/main/java/LibraryManager.java src/main/java/Main.java
java -cp out Main
```
If `out` already exists, continue with the compile command.

## Refactoring highlights
- Smaller methods and clearer names.
- Centralized validation and ISBN uniqueness checks.
- Validates replacement data before updating a record.
- Returns an unmodifiable copy of the book list.
- No measured performance benchmark was performed; improvements focus on structure and maintainability.
