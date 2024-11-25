
# Argument Passing in Scala

## Overview

This project is focused on understanding and implementing the concept of argument passing in Scala. The tasks involve completing higher-order functions that manipulate instances of a custom class, `RefInt`, while adhering to functional programming paradigms. This project was implemented as part of a learning exercise to gain proficiency in Scala and functional programming techniques.

## Technologies Used

- **Scala**: A strong statically typed general-purpose programming language that supports both object-oriented and functional programming paradigms.
- **SBT (Scala Build Tool)**: An open-source build tool for Scala and Java projects, used to manage dependencies and automate the build process.

## Problem Statement

The primary goal of this project is to:
1. Implement higher-order functions that utilize instances of a custom class `RefInt`.
2. Adhere to functional programming principles by avoiding while loops and variable reassignment, instead using recursion.

## Project Structure

```
argpass.scala  - The main Scala file containing the class and functions to be implemented.
```

## Detailed Tasks

### 1. RefInt Class Implementation

The `RefInt` class encapsulates an integer value with the following methods:

- **get()**: Returns the current integer value.
- **set(m: Int)**: Updates the integer value to `m`.

### 2. Higher-Order Function Completion

#### Function: `refint1`

**Description:**

This function takes a function `f` as a parameter. The parameter `f` is a function that accepts an instance of `RefInt` and returns `Unit`. The task is to:
- Create a single instance of `RefInt`.
- Call the function `f` three times with this instance.
- Return a tuple of the three integers provided by `f` in the order they came back from the calls.

**Example Usage:**

```scala
def refint1(f: RefInt => Unit): (Int, Int, Int) = {
  // Implementation here
}
```

## Key Learnings

### Functional Programming Paradigms

- **Immutability**: Avoided the use of mutable variables (`var`), instead used immutable values (`val`).
- **Recursion**: Used recursion as an alternative to iterative loops (`while`, `for`).

### Higher-Order Functions

- **Definition**: Functions that take other functions as parameters or return them as results.
- **Usage**: Implemented a higher-order function `refint1` that manipulates instances of `RefInt`.

### Class Manipulation in Scala

- **Custom Class**: Defined and manipulated a custom class `RefInt`.
- **Method Implementation**: Implemented getter and setter methods to interact with class instances within a functional programming framework.

## How to Run the Project

1. **Install SBT**: Ensure SBT is installed on your machine. Follow the instructions [here](https://www.scala-sbt.org/download.html) to install SBT.

2. **Clone the Repository**: Clone the project repository to your local machine.

    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

3. **Compile the Project**: Use SBT to compile the project.

    ```bash
    sbt compile
    ```

4. **Run Tests**: Run the tests to ensure the implementation is correct.

    ```bash
    sbt test
    ```

## Conclusion

This project provided valuable experience in Scala and functional programming. By completing the tasks, I gained a deeper understanding of higher-order functions, recursion, and class manipulation in Scala. These skills are crucial for developing robust and maintainable code in functional programming languages.
