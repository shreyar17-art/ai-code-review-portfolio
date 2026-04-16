# JavaScript & React Evaluation Expertise

This document outlines key focus areas when I evaluate JS/TS/React generation from LLMs.

## Core Evaluation Pillars

1.  **React Rendering & State Management:** 
    *   Identifying unnecessary re-renders.
    *   Ensuring strict adherence to hooks rules.
    *   Evaluating object/array mutability issues in `useState`.

2.  **Asynchronous JavaScript:**
    *   Checking for proper `Promise` handling (`async/await` syntax).
    *   Ensuring `useEffect` cleanup functions are present to prevent memory leaks.

3.  **Security (XSS Mitigation):**
    *   Scrutinizing `dangerouslySetInnerHTML`.
    *   Ensuring inputs are sanitized before rendering or passing to APIs.

*(See the `samples/` directory for full JavaScript/React evaluation case studies).*
