# IT313 TypeScript Foundations

## Problem

This project is a TypeScript version of the Enrollment Eligibility Checker from Laboratory 2.

The program calculates the average of each enrollee's prelim, midterm, and final grades and determines whether the student is PASSING or on PROBATION.

## TypeScript Concepts Used

### Basic Types
The program uses string, number, and boolean-related type checking where needed.

### Interfaces
The `Enrollee` interface defines the structure of student data.

The `EligibilityReport` interface defines the structure of the generated eligibility report.

### Enum
The `EnrollmentStatus` enum contains Passing and Probation.

This prevents the program from using arbitrary status strings.

### Type Alias and Union Type
The `BatchId` type alias uses `string | number`.

A `typeof` check is used to narrow the type before using the value.

### Optional Property
The `remarks?: string` property is optional because only probation students need a consultation remark.

### Generics
The `groupBy<T>()` function is generic and is used to group eligibility reports by status.

### Modules
The `gradeUtils.ts` file exports `computeAverage()` as a named export and `getStatus()` as a default export.

The main script imports both functions.

### Async and Await
`getEnrollees()` returns a `Promise<Enrollee[]>` and uses a short delay to simulate a registrar API.

The `main()` function uses `async`, `await`, and `try/catch`.

### map and reduce
`map()` creates the typed eligibility reports.

`reduce()` calculates the class average.

## How to Run

Install the dependencies:

```bash
npm install
Type-check the project:
npx tsc --noEmit
Run the main program:
npx ts-node main.ts
The gradeUtils.ts file is a module used by main.ts. It exports the utility functions and enum used by the main program.

