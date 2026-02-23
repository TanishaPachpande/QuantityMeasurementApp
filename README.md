# QuantityMeasurementApp

## ✅ UC5 – Unit-to-Unit Conversion
📌 **Overview:**

UC5 extends UC4 by adding explicit unit conversion functionality between:

- FEET

- INCHES

- YARDS

- CENTIMETERS

Instead of only checking equality, the application now supports converting values across units using centralized conversion factors.

🎯 **Objective:**

Provide a public API:

convert(double value, LengthUnit source, LengthUnit target)

that converts a numeric value from a source unit to a target unit using base unit normalization.

⚙️ **Conversion Logic:**

- Validate input value (finite number)

- Validate source and target units (non-null)

- Normalize value to base unit

- Convert to target unit

- Return converted result

- Formula used:

result = value × (source.factor / target.factor)


🧠 **Key Concepts:**

- Enum-based conversion factors

- Base unit normalization

- Immutability & value objects

- Method overloading

Exception handling

Precision handling with floating-point tolerance
