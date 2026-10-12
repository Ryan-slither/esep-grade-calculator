# ESEP Grade Calculator

This library is a simple utility to calculate your grades.

Runtime requirements:
Golang 1.24+

Run unit tests:
```
cd grade-calculator/
go test ./...
```

Run unit tests with code coverage:
```
cd grade-calculator/
go test -coverprofile=coverage.txt ./...
```

## Repo Overview

### grade-calculator: contains the core application code with a few files
- go.mod: sets the module name for future importing of repo packages and the go version to run with
- grade_calculator.go: Creates some initial types and functions to implement the library functionality. GradeCalculator is the container for the current assignments, exams, and essays that are graded. Grade is a struct that contains the name of the assignment, the grade it received, and the type of grade (assignment, exam, essay). There are some other functions that include basic math and logic to compute averages of the grades and determine what letter grade that value represents.
- grade_calculator_test.go: Contains a few unit tests that test the core functionality of the library. Each test has an expected letter grade, a grade calculator with some added assignments with their respective grade values, and computes the final letter grade from the weighted average of those grades. If the final letter grade matches the expected value, the test passes. 