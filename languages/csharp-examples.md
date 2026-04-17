# C# & .NET Evaluation Expertise

This document outlines my methodology for evaluating AI-generated C# and .NET code, focusing on performance, resource safety, and modern idioms.

## Core Evaluation Pillars

1.  **Resource Management (IDisposable):** 
    *   Verifying deterministic disposal of unmanaged resources (database connections, file streams, network sockets).
    *   Ensuring the `using` statement or declaration pattern is used to handle exceptions safely.
    *   Identifying common "fake" disposal patterns (manual `Close()` without error handling).

2.  **Asynchronous Programming (async/await):**
    *   Scrutinizing `async void` anti-patterns and ensuring transition to `async Task`.
    *   Evaluating proper exception propagation across `await` boundaries.
    *   Checking for `ConfigureAwait(false)` in library code to prevent deadlocks.

3.  **LINQ & Data Processing:**
    *   Detecting "Deferred Execution" bugs where queries are re-run unnecessarily.
    *   Ensuring proper materialization (`.ToList()`, `.ToArray()`) when results are stored or accessed multiple times.
    *   Evaluating algorithmic complexity within LINQ chains.

4.  **Serialization & APIs:**
    *   Handling nullability in JSON deserialization (`System.Text.Json`).
    *   Ensuring proper validation of external data inputs.

*(See the `samples/` directory for full C# / .NET evaluation case studies, including ranking-task-3 and ranking-task-6).*
