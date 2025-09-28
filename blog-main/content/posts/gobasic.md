---
title: "The Basics of Go"
date: 2025-09-28
author: "Dihan Ramanayaka" 
tags: ["Go", "Golang", "Programming", "Development", "Concurrency"]
---

## Introduction to Go

Go, or Golang, is an open-source programming language created by Google. It was designed to be simple, efficient, and reliable, focusing on easy-to-read code and excellent built-in support for **concurrency**. Its clean syntax makes it a favorite for modern web services, cloud infrastructure, and command-line tools.

This guide covers the core concepts you need to start writing Go programs.

***

## 1. Structure: Packages and the `main` Function

Every Go program is organized into **packages**. A program starts running in the `main` package and specifically in the `main` function.

```go
package main // The entry point for an executable program

import "fmt" // Import the package for formatted I/O (like printing to console)

func main() {
    // This is where execution begins
    fmt.Println("Hello, Gopher!")
}
````

### Key Concept: Packages

  * `main`: Used for standalone executable programs.
  * Other names (e.g., `net/http`): Used for reusable libraries.

-----

## 2\. Variables and Types

Go is a **statically typed** language, meaning variable types are checked at compile time.

### Declaring Variables

Go offers two common ways to declare variables:

1.  **Standard Declaration (Verbose):**
    ```go
    var username string = "Alice"
    var age int = 30
    ```
2.  **Short Declaration (Idiomatic):**
    The `:=` operator declares and initializes a variable, letting the Go compiler infer the type. This is the most common way to declare variables *inside* a function.
    ```go
    message := "Welcome to Go" // type is inferred as string
    isLearning := true         // type is inferred as bool
    ```

### Basic Data Types

| Type | Description | Example |
| :--- | :--- | :--- |
| `string` | Text, UTF-8 encoded. | `"Go is fast"` |
| `int` | Integer, size depends on the OS. | `42` |
| `float64` | Standard floating point number. | `3.14159` |
| `bool` | Boolean (True or False). | `false` |

-----

## 3\. Control Flow: `if` and `for`

Go keeps things simple by only having one looping construct: `for`. The parentheses around conditions are optional and generally omitted.

### Conditional Statements (`if`)

```go
score := 95

if score > 90 {
    fmt.Println("Grade A")
} else if score > 70 {
    fmt.Println("Grade B")
} else {
    fmt.Println("Needs improvement")
}
```

### Looping (`for`)

The `for` loop is highly versatile.

```go
// 1. Classic C-style loop
for i := 0; i < 5; i++ {
    fmt.Println("Iteration:", i)
}

// 2. While-style loop
j := 0
for j < 5 {
    j++
}

// 3. Range-based (for iterating over arrays, slices, maps)
primes := []int{2, 3, 5, 7}
for index, value := range primes {
    fmt.Printf("Prime at %d is %d\n", index, value)
}
```

-----

## 4\. Functions and Multiple Return Values

Functions are declared with the `func` keyword. A key feature of Go is the ability for functions to return **multiple values**, which is often used for returning a result *and* an error.

```go
func add(x int, y int) int {
    return x + y
}

func calculate(width int, height int) (area int, perimeter int) {
    area = width * height
    perimeter = 2 * (width + height)
    return // Returns the named return variables (area, perimeter)
}

func main() {
    sum := add(10, 5)
    fmt.Println("Sum:", sum) // Output: Sum: 15

    a, p := calculate(4, 5)
    fmt.Println("Area:", a, "Perimeter:", p) // Output: Area: 20 Perimeter: 18
}
```

-----

## 5\. Concurrency: Goroutines

Concurrency is built into Go's DNA. A **goroutine** is a lightweight, independent function that runs concurrently with others.

To start a new goroutine, simply add the `go` keyword before a function call:

```go
func worker(id int) {
    fmt.Println("Worker", id, "starting...")
    time.Sleep(time.Second) // Simulate work
    fmt.Println("Worker", id, "finished.")
}

func main() {
    for i := 1; i <= 3; i++ {
        go worker(i) // Starts a new, concurrent goroutine
    }

    // Wait for goroutines to finish (simplified, usually done with sync.WaitGroup)
    time.Sleep(2 * time.Second) 
}
```

This basic overview should give you a solid foundation to start experimenting with Go. Its power lies in its simplicity and robust handling of concurrent operations, making it an excellent language to learn today.

