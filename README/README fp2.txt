
# Functional Programming in Scala

## Project Overview

This project contains a series of exercises focused on functional programming using Scala. The primary objective is to implement various list manipulation functions using recursion, without relying on Scala's built-in methods such as `map` and `filter`. This project helps to deepen understanding of functional programming concepts and recursion.

## Technologies Used

- **Language**: Scala
- **Build Tool**: SBT (Scala Build Tool)

## Tasks and Implementation

### 1. Custom Map Function

**Description**: Implement a recursive `map` function for Scala's `List` type to apply a given function to each element in the list.

**Implementation**:
```scala
def map[A, B] (xs: List[A], f: A => B): List[B] = {
  xs match {
    case Nil => Nil
    case x :: xs => f(x) :: map(xs, f)
  }
}
```

### 2. Custom Filter Function

**Description**: Develop a recursive `filter` function for Scala's `List` type to filter elements based on a given predicate.

**Implementation**:
```scala
def filter[A] (xs: List[A], f: A => Boolean): List[A] = {
  xs match {
    case Nil => Nil
    case x :: xs => if (f(x)) x :: filter(xs, f) else filter(xs, f)
  }
}
```

### 3. List Append Function

**Description**: Create a recursive `append` function to concatenate two lists.

**Implementation**:
```scala
def append[A] (xs: List[A], ys: List[A]): List[A] = {
  xs match {
    case Nil => ys
    case x :: xs => x :: append(xs, ys)
  }
}
```

## Learning Outcomes

### Functional Programming

- **Recursion**: Gained a deep understanding of how to use recursion to process and manipulate lists.
- **Immutability**: Learned the importance of immutability in functional programming by avoiding mutable state and iterative constructs.

### Scala Proficiency

- **Higher-Order Functions**: Improved skills in defining and using higher-order functions in Scala.
- **Clean Code**: Developed the ability to write clean, efficient, and idiomatic Scala code.

### Problem-Solving

- **Recursive Thinking**: Enhanced problem-solving skills by approaching problems from a recursive perspective.
- **Functional Paradigms**: Strengthened understanding of functional programming paradigms and their application in real-world scenarios.

## Usage

To compile and run the project, ensure you have SBT installed. Navigate to the project directory and use the following commands:

```sh
# Compile the project
sbt compile

# Run the tests
sbt test
```

## Conclusion

This project serves as a valuable exercise in mastering functional programming with Scala. By implementing recursive solutions for common list operations, it provides a solid foundation in both the theory and practice of functional programming principles.
