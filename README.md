# QuantityMeasurementApp

## ✅ UC9 – Weight Measurement (Equality, Conversion & Addition)
📌 **Overview:**

- UC9 extends the application to support a new measurement category: Weight.

- Supported units:

  - KILOGRAM (kg) – Base unit

  - GRAM (g) – 1 g = 0.001 kg

  - POUND (lb) – 1 lb ≈ 0.453592 kg

- Weight functionality mirrors the length design (UC1–UC8) while remaining fully independent.

🎯 **Objective:**

Implement:

- Equality comparison across weight units

- Unit conversion between kg, g, lb

- Addition (implicit & explicit target unit)

- Category type safety (weight ≠ length)

⚙️ **Design Structure:**

🔹 WeightUnit (Standalone Enum)

  Responsible for:

  - convertToBaseUnit(value) → converts to kilograms

  - convertFromBaseUnit(baseValue) → converts from kilograms

  Base unit: Kilogram

🔹 QuantityWeight (Immutable Class)

  Responsible for:

  - equals() (base unit comparison)

  - convertTo(targetUnit)

  - add(weight)

  - add(weight, targetUnit)

All arithmetic normalizes through kilograms.


🧠 **Key Concepts:**

- Multiple measurement categories

- Base unit normalization (kg for weight)

- Enum-based conversion responsibility (UC8 pattern)

- Immutability

- Floating-point precision with epsilon

- Equality contract (reflexive, symmetric, transitive)

- Method overloading for addition

- Category type safety

🧪 **Test Coverage:**

- Same-unit equality (kg, g, lb)

- Cross-unit equality (kg ↔ g ↔ lb)

- Conversion between all unit pairs

- Addition (same & cross unit)

- Addition with explicit target unit

- Weight vs length incompatibility

- Null & invalid input handling

- Zero, negative & large values

- Round-trip conversion precision

🚀 **Architectural Impact:**

- UC9 proves the architecture from UC1–UC8 scales cleanly to new categories.

- No changes required to Length classes

- Weight follows the same standalone unit pattern

- System is ready for future categories (Volume, Temperature, etc.)
