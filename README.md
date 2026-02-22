# QuantityMeasurementApp

📌 **Overview:**

The Quantity Measurement App demonstrates a progressive design evolution for validating equality of length measurements.

The project evolves across four use cases:

- UC1 – Feet Measurement Equality

- UC2 – Feet and Inches Equality (separate units)

- UC3 – Cross-Unit Equality (Feet ↔ Inches conversion)

- UC4 – Extended Unit Support (Yards & Centimeters)


## ✅ UC1 – Feet Measurement Equality
🎯 **Objective:**

Compare two measurements in feet and determine equality.

🏗️ **Design:**

- Inner Feet class

- Immutable (private final double)

- Overridden equals() using Double.compare()

🧪 **Test Coverage:**

- Same value

- Different value

- Null comparison

- Same reference

- Invalid input


## ✅ UC2 – Feet and Inches Equality (Independent Units)
🎯 **Objective:**

- Add support for Inches, while treating Feet and Inches separately.

- Feet ↔ Feet comparison

- Inches ↔ Inches comparison

- No cross-unit conversion

🏗️ **Design:**

- Separate Feet and Inches classes

- Immutable values

- Proper equals() implementation

- Static helper methods


## ✅ UC3 – Cross-Unit Equality (Generic Design)
🎯 **Objective:**

Enable comparison across units using conversion logic.


🏗️ **Refactoring:**

- Introduced generic QuantityLength class

- Introduced LengthUnit enum

- Centralized conversion logic

- Removed duplication from UC2

⚙️ **Implementation:**

- Convert both values to a common base unit

- Use Double.compare() for equality


## ✅ UC4 – Extended Unit Support (Yards & Centimeters)
🎯 **Objective:**

Extend UC3 to support:

- YARDS

- CENTIMETERS

Without modifying the core class logic.

🏗️ **Scalability Enhancement:**

Updated LengthUnit enum with:

- YARDS → 1 yard = 3 feet

- CENTIMETERS → 1 cm = 0.393701 inches

No changes required in QuantityLength class — demonstrating scalable design.

⚙️ **Supported Comparisons:**
- Yard Conversions

  1 yard = 3 feet

  1 yard = 36 inches

  Yard ↔ Feet

  Yard ↔ Inches

  Yard ↔ Yard

- Centimeter Conversions

  1 cm = 0.393701 inches

  Cm ↔ Inches

  Cm ↔ Feet

  Cm ↔ Yard

  Cm ↔ Cm


🧠 **Key Concepts Demonstrated:**

🔹 Object Equality Contract

   Reflexive, Symmetric, Transitive, Consistent, Null-safe.

🔹 Floating-Point Precision

   Safe comparison using Double.compare().

🔹 Generic & Scalable Design

   Adding new units requires only enum modification.

🔹 DRY Principle

   No duplication of unit-specific classes.

🔹 Enum Extensibility

   Type-safe unit management.

🔹 Mathematical Accuracy

   Centralized and precise conversion factors.

🔹 Backward Compatibility

   All UC1, UC2, and UC3 functionality remains intact.
