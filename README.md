# QuantityMeasurementApp

## ✅ UC6 – Addition of Two Length Units
📌 **Overview:**

UC6 extends UC5 by adding addition support for length measurements.

Two QuantityLength objects (same category: length) can be added even if they use different units.
The result is returned in the unit of the first operand.

Example:
1 FEET + 12 INCHES = 2 FEET

🎯 **Objective:**

- Provide an add() method that:

- Validates inputs

- Converts both values to a base unit

- Adds them

- Converts the result back to the first operand’s unit

- Returns a new immutable QuantityLength object

⚙️ **Logic:**

- Validate operands (non-null, finite values)

- Convert both to base unit (feet)

- Add values

- Convert sum to first operand’s unit

- Return new QuantityLength

🧠 **Key Concepts:**

- Arithmetic on value objects

- Unit conversion reuse (from UC5)

- Base unit normalization

- Immutability

- Floating-point precision handling

- Commutativity (A + B = B + A)

- Input validation & exception handling

🧪 **Test Coverage:**

- Same-unit addition

- Cross-unit addition

- Commutativity

- Zero (identity element)

- Negative values

- Large & small numbers

- Null handling
