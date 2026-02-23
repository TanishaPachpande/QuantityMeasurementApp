# QuantityMeasurementApp

## ✅ UC13 – Centralized Arithmetic Logic (DRY Refactor)
📌 **Overview:**

- UC13 refactors arithmetic operations from UC12 to enforce the DRY principle.

- Instead of repeating validation and conversion logic in:

  - add()

  - subtract()

  - divide()

- All common logic is moved to centralized private helper methods.

✔ Public API remains unchanged
✔ All UC12 test cases pass
✔ Behavior remains identical

🚨 **Problem in UC12:**

- Duplicate validation logic in every arithmetic method

- Repeated base-unit conversion code

- Hard to maintain

- Risk of inconsistent error handling

- Difficult to scale for future operations

🛠 **Solution in UC13:**
1️⃣ ArithmeticOperation Enum

Handles operation logic:

- ADD

- SUBTRACT

- DIVIDE

Each enum constant defines its own compute() logic.

2️⃣ Centralized Validation

validateArithmeticOperands(...)

Handles:

- Null checks

- Cross-category checks

- Finiteness checks

- Target unit validation

3️⃣ Core Arithmetic Helper

performBaseArithmetic(...)

Steps:

- Convert both quantities to base unit

- Execute operation via enum

- Return base result

🔁 Refactored Flow

Example:

q1.subtract(q2, FEET)

→ validateArithmeticOperands(...)
→ performBaseArithmetic(q2, SUBTRACT)
→ Convert result to FEET
→ Return new Quantity

🧠 **Key Concepts:**

- DRY Principle

- Enum-based operation dispatch

- Lambda expressions (DoubleBinaryOperator)

- Centralized validation strategy

- Backward compatibility

- Refactoring without behavioral change
