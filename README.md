# QuantityMeasurementApp

📌 **Overview:**

The Quantity Measurement App validates equality of measurements using proper object-oriented principles and Java best practices.

The project currently supports:

- UC1 – Feet Measurement Equality

- UC2 – Feet and Inches Measurement Equality

The implementation focuses on value-based comparison, floating-point precision handling, null safety, and clean design.

## ✅ UC1 – Feet Measurement Equality
🎯 **Objective:**

To compare two measurements in feet and determine whether they are equal.

🏗️ **Design:**

- Inner class Feet

- private final double value (immutable)

- Overridden equals() method

- Uses Double.compare() for floating-point precision

⚙️ **Equality Rules Followed:**

- Reflexive

- Symmetric

- Transitive

- Consistent

- Null-safe

🧪 **Test Cases Covered:**

- Same value comparison

- Different value comparison

- Null comparison

- Same reference check

- Invalid input handling


## ✅ UC2 – Feet and Inches Measurement Equality
🎯 **Objective:**

To extend UC1 by supporting equality checks for Inches along with Feet.

Both units are treated separately:

- Feet-to-Feet comparison

- Inches-to-Inches comparison

(No cross-unit conversion in this use case.)

🏗️ **Design:**

- Feet class

- Inches class

- Both:

  - Immutable (private final double)

  - Encapsulated values

  - Override equals() properly

- Static methods reduce dependency on main()

⚙️ **Implementation Flow:**

- Validate numeric input

- Instantiate corresponding objects

- Perform:

  - Reference check

  - Null check

  - Type check

  - Double.compare()

🧪 **Test Cases Covered:**

(Similar to UC1, applied to both units)

- Same value comparison

- Different value comparison

- Null comparison

- Same reference check

- Invalid input handling


💡 **Key Concepts Practiced:**

- Object Equality Contract

- Floating-Point Precision Handling

- Null & Type Safety

- Encapsulation & Immutability

- Unit Testing Best Practices

⚠️ **Current Design Limitation:**

- Using separate Feet and Inches classes introduces code duplication:

- Similar constructor logic

- Identical equals() implementation

- Same internal structure

- This violates the DRY (Don’t Repeat Yourself) principle.

