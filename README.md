# QuantityMeasurementApp

📌 **Overview:**

The Quantity Measurement App validates equality of measurements using proper object-oriented design and Java best practices.

The project currently supports:

- UC1 – Feet Measurement Equality

- UC2 – Feet and Inches Measurement Equality (separate units)

- UC3 – Cross-Unit Equality (Feet ↔ Inches Conversion)

The implementation focuses on value-based comparison, floating-point precision handling, null safety, and clean design.

## ✅ UC1 – Feet Measurement Equality
🎯 **Objective:**

To compare two measurements in feet and determine whether they are equal.

🏗️ **Design:**

- Inner class Feet

- private final double value

- Immutable design

- Overridden equals() using Double.compare()

🧪 **Test Cases Covered:**

- Same value

- Different value

- Null comparison

- Same reference

- Invalid input

## ✅ UC2 – Feet and Inches Measurement Equality
🎯 **Objective:**

To support equality checks for both Feet and Inches independently.

Feet ↔ Feet comparison

Inches ↔ Inches comparison
(No conversion between units)

🏗️ **Design:**

- Separate Feet and Inches classes

- Immutable values

- Proper equals() implementation

- Static methods to reduce dependency on main()


## ✅ UC3 – Cross-Unit Equality (Feet and Inches Conversion)
🎯 **Objective:**

To compare measurements across units by converting them to a common base value.


🏗️ **Design Improvement:**

- Conversion logic added between units

- Comparison performed after normalizing values

- Maintains:

  - Null safety

  - Type safety

  - Floating-point precision handling

⚙️ **Implementation Approach:**

- Convert feet to inches (1 ft = 12 inches)

- Or convert inches to feet

- Use Double.compare() for final equality check

🧪 **Test Cases Covered:**

- Same unit equality

- Cross-unit equality (1 ft == 12 inches)

- Cross-unit inequality

- Null comparison

- Invalid input handling


💡 **Key Concepts Practiced**:

- Object Equality Contract

- Floating-Point Precision Handling

- Cross-Unit Conversion Logic

- Null & Type Safety

- Encapsulation & Immutability

- DRY Principle Awareness
