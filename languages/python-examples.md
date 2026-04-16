# Python Evaluation Expertise

This document outlines key focus areas when I evaluate Python generation from LLMs.

## Core Evaluation Pillars

1.  **Pythonic Idioms:** 
    *   I look for list/dictionary comprehensions instead of raw `for` loops where appropriate.
    *   Proper use of built-ins (`zip`, `enumerate`, `any`, `all`).
    *   Verification of `yield` for memory-efficient generators.

2.  **Security & Type Safety:**
    *   Ensuring type hints (`typing`) are used accurately for maintainability.
    *   Protecting against `eval()` or unsanitized `exec()` outputs in AI responses.
    *   Proper parameterized queries for database interactions (avoiding f-strings for SQL).

3.  **Exception Handling:**
    *   Rejecting raw `except Exception:` blocks.
    *   Enforcing specific, granular error catching and robust error messaging.

*(See the `samples/` directory for full Python evaluation case studies).*
