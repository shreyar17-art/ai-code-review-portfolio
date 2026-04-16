# Review Methodology

My evaluation process follows a strict **3-Pass Review Approach** emphasizing systematic evaluation to ensure AI models generate secure, optimal, and maintainable software.

## The 3-Pass Review Approach

### Pass 1: Correctness & Security (The Dealbreakers)
*   **Functional Correctness:** Does the code solve the problem as described in the prompt? Are edge cases handled?
*   **Security Vulnerabilities:** Is the code vulnerable to OWASP Top 10 threats? Are inputs sanitized? Are parameterized queries utilized?

### Pass 2: Performance & Architecture (The Scalability Check)
*   **Algorithmic Efficiency:** Is the time and space complexity optimal?
*   **Language Idioms:** Does the code use standard, modern language features (e.g., Python list comprehensions, accurate React memoization)?
*   **Architecture:** Are the functions modular? Is the Single Responsibility Principle maintained?

### Pass 3: Maintainability & Readability (The Developer Experience)
*   **Documentation:** Are edge cases and complex logic properly documented?
*   **Naming Conventions:** Are variables and functions named expressively?
*   **Formatting:** Does it conform to PEP 8, Prettier, or standard Java conventions?

## Justification Framework

For every evaluation, I use the **CEIA Framework**:
*   **Claim:** Directly state the flaw or strength.
*   **Evidence:** Point to the exact line of code or algorithmic behavior.
*   **Implication:** Explain the consequences (e.g., a data breach, excessive re-renders).
*   **Actionable Advice:** Provide the exact code or conceptual fix required.
