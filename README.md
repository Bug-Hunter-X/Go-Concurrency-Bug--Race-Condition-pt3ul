# Go Concurrency Bug: Race Condition

This repository demonstrates a common concurrency bug in Go: a race condition when incrementing a shared variable across multiple goroutines.

## The Bug

The `bug.go` file contains a program that uses goroutines to increment a shared variable `x`.  Without proper synchronization, multiple goroutines can access and modify `x` simultaneously, leading to unexpected results.  The program may print an incorrect final value of `x` because of race conditions.

## The Solution

The `bugSolution.go` file shows how to fix the race condition using a mutex.  A mutex ensures that only one goroutine can access and modify `x` at a time, preventing data corruption.

## How to Run

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `go run bug.go` to see the incorrect result (due to race conditions).
4. Run `go run bugSolution.go` to see the correct result (with race condition solved).

This example highlights the importance of proper synchronization mechanisms when working with shared resources in concurrent Go programs.