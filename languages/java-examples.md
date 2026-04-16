# Java Evaluation Expertise

This document outlines key focus areas when I evaluate Java generation from LLMs.

## Core Evaluation Pillars

1.  **Object-Oriented Integrity:** 
    *   Reviewing encapsulation principles.
    *   Ensuring interfaces are utilized for loose coupling.
    *   Evaluating SOLID principles adherence.

2.  **Null Safety & Validation:**
    *   Strict checks against `NullPointerException`.
    *   Usage of `Optional<T>` where appropriate instead of raw null returns.
    *   String/regex validation (e.g., verifying `email.contains("@")` vs strict regex patterns).

3.  **Memory & Concurrency:**
    *   Checking for proper usage of `ExecutorService` instead of manual thread spawning.
    *   Ensuring resource closures via `try-with-resources`.

*(See the `samples/` directory for full Java evaluation case studies, specifically String parsing and validation).*
