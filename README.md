# QuantityMeasurementApp

## ✅ UC12 – Subtraction & Division Operations
📌 **Overview:**

UC12 extends Quantity<U> by adding two new arithmetic operations:

- subtract() → returns Quantity<U>

- divide() → returns double (dimensionless ratio)

Works across Length, Weight, and Volume without modifying existing architecture.

➖ Subtraction
✔ Features

 - Supports cross-unit subtraction (same category)

 - Implicit result unit → first operand’s unit

 - Optional explicit target unit

 - Maintains immutability

 - Prevents cross-category operations


➗ Division
✔ Features

 - Returns dimensionless ratio (double)

 - Supports cross-unit division

 - Prevents division by zero

 - Prevents cross-category division


🔒 **Validation & Safety:**

- Null checks

- Category checks

- Finite number validation

- Division-by-zero protection

- Immutability preserved

🧠 **Key Concepts:**

- Non-commutative operations

- Base unit normalization

- Generic scalability

- SOLID consistency

- Arithmetic integration with existing system
