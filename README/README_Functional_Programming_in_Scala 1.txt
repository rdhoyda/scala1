
# Functional Programming in Scala

## Project Overview

This project is a comprehensive exploration of functional programming (FP) concepts using Scala. It involves solving various algorithmic problems and implementing functions in a purely functional manner, emphasizing immutability, recursion, and the use of higher-order functions.

## Technologies Used

- **Programming Language:** Scala
- **Build Tool:** SBT (Scala Build Tool)

## Project Structure

The project includes the following key components:

- **Function Implementations:** Various functions implemented using recursion.
- **Utility Functions:** Helpers for logging and debugging.
- **Testing:** Ensures code correctness and functionality.

## Key Concepts

### Functional Programming Principles

- **Immutability:** Avoiding mutable state and side effects.
- **Recursion:** Replacing loops with recursive function calls.
- **Pure Functions:** Functions that always produce the same output for the same input and have no side effects.
- **Higher-Order Functions:** Functions that take other functions as parameters or return them as results.

### Project Components

1. **Factorial Function:**
   - Implemented using simple recursion.
   - Extended with logging for debugging purposes.

2. **Logging Utility:**
   - A utility function to log recursive calls and their results.

## Example Code

### Factorial Function

```scala
def fact(n: Int): Int =
  if n <= 1 then 1
  else n * fact(n - 1)

// Factorial with logging
def factLog(n: Int): Int =
  log(s"fact($n)") {
    if n <= 1 then 1
    else n * factLog(n - 1)
  }
```

### Logging Utility

```scala
def log[X](prefix: String)(computeResult: => X) =
  println(prefix)
  val result = computeResult
  println(s"$prefix : $result")
  result
```

## Learning Outcomes

This project provided an in-depth understanding of functional programming and its application in solving algorithmic problems. Key learnings include:

- Mastery of recursion and avoiding imperative constructs like loops and variable reassignment.
- Enhanced ability to write clean, maintainable, and efficient Scala code.
- Improved debugging skills using logging techniques.
- Understanding of higher-order functions and their use in creating flexible and reusable code.

## Getting Started

### Prerequisites

- **Scala:** Ensure you have Scala installed on your machine. You can download it from [Scala's official website](https://www.scala-lang.org/download/).
- **SBT:** Install SBT to manage dependencies and run the project. Instructions can be found on [SBT's official website](https://www.scala-sbt.org/download.html).

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Compile the project:
   ```bash
   sbt compile
   ```

3. Run the tests to ensure everything is working correctly:
   ```bash
   sbt test
   ```

### Running the Code

You can run the implemented functions and see their output by executing:
```bash
sbt run
```

## Contribution

Contributions are welcome! If you have suggestions for improvements or new features, feel free to fork the repository and create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Special thanks to the Scala community for their excellent resources and support.
- Inspired by various functional programming tutorials and courses.
