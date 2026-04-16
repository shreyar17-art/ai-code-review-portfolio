# Correction Task: Refactoring Business Logic

**Task Context:** The user provided two redundant Python functions used for calculating customer discounts (Standard and VIP).
**Concept Tested:** Code deduplication, DRY principles, and fixing logical inconsistencies.

---

## Original Code

```python
def calculate_standard_discount(price):
    discount = price * 0.10
    final_price = price - discount
    return final_price

def calculate_vip_discount(price):
    # VIPs should get a 25% discount, but the logic below calculates 20%
    discount = price * 0.20
    final_price = price - discount
    return final_price
```

---

## My Correction & Justification

### The Issues (Claim & Evidence):
1.  **Code Duplication (DRY Violation):** The two functions perform the exact same mathematical operations with hardcoded discount percentages. 
2.  **Logical Bug:** `calculate_vip_discount` has a mismatch between its documentation (25%) and implementation (20%). 

### Implication:
Hardcoding business logic across multiple functions makes the codebase brittle. If we need to change how discounts are applied (e.g., adding tax before discount), we have to update multiple places, increasing the chance of errors. Furthermore, VIP customers are currently being overcharged due to the logical bug.

### Refactoring (Actionable Advice):
We should consolidate the logic into a single, scalable function that takes the discount rate as a parameter, establishing clean, modular code.

```python
def calculate_discount(price, discount_rate):
    """
    Calculates the final price after applying a percentage discount.
    Standard: 0.10
    VIP: 0.25
    """
    if discount_rate < 0 or discount_rate > 1:
        raise ValueError("Discount rate must be between 0.0 and 1.0")
        
    return price * (1 - discount_rate)

# Client Usage:
standard_price = calculate_discount(100.0, 0.10)
vip_price = calculate_discount(100.0, 0.25) # Fixed the logical bug
```
