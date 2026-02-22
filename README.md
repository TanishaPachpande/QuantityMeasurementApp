# QuantityMeasurementApp

## UC1 – Feet Measurement Equality
📖 **Overview:**

This use case verifies equality between two measurements in feet.
It follows proper object-oriented principles and ensures accurate floating-point comparison using Java best practices.

🎯 **Objective:**

To compare two numerical values (in feet) and determine whether they are equal using a value-based equality approach.

🏗️ **Design:**

- QuantityMeasurementApp contains an inner class Feet

- Feet class:

   - Stores measurement as private final double

   - Immutable design

   - Encapsulated value

- equals() method is overridden to ensure proper object comparison

⚙️ **Equality Implementation:**

- The equals() method follows Java’s equality contract:

  ✔ Reflexive

  ✔ Symmetric

  ✔ Transitive

  ✔ Consistent

  ✔ Null-safe

- Comparison is done using:

  - Reference check (this == obj)

  - Null check

  - Type check using getClass()

  - Double.compare() for precise floating-point comparison

🧪 **Test Cases Covered:**

- Same Value → 1.0 ft equals 1.0 ft → true

- Different Value → 1.0 ft vs 2.0 ft → false

- Null Comparison → comparison with null → false

- Same Reference → object compared to itself → true

- Invalid Input Handling

💡 **Key Concepts Practiced:**

- Object Equality Contract

- Floating-Point Precision Handling

- Null & Type Safety

- Encapsulation & Immutability

- Unit Testing Best Practices
