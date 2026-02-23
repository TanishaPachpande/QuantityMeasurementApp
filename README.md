# QuantityMeasurementApp

## ✅ UC7 – Addition with Explicit Target Unit
📌 **Overview:**

UC7 extends UC6 by allowing the caller to explicitly specify the result unit during addition.

Unlike UC6 (which returns the result in the first operand’s unit), UC7 gives full control over the output unit.

Example:
1 FEET + 12 INCHES → YARDS = ~0.667 YARDS

🎯 **Objective:**

Provide an overloaded method:

add(length1, length2, targetUnit)

that:

- Validates operands and target unit

- Converts both values to base unit (feet)

- Adds them

- Converts the sum to the specified target unit

- Returns a new immutable QuantityLength

⚙️ **Logic:**

- Validate inputs (non-null, finite values)

- Convert both operands to base unit

- Add values

- Convert result to targetUnit

- Return new object (immutability preserved)


🧠 **Key Concepts:**

- Method overloading

- Explicit parameter control

- Base unit normalization

- Reusable conversion logic (from UC5/UC6)

- Immutability

- Floating-point precision handling

- Commutativity preservation

- Strong input validation

🧪 **Test Coverage:**

- Explicit target same as first operand

- Explicit target same as second operand

- Target different from both operands

- All unit combinations

- Null target validation

- Large & small scale conversions

Zero & negative values

Precision tolerance (epsilon comparison)
