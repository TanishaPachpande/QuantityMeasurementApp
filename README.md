# QuantityMeasurementApp

## ✅ UC10 – Generic Quantity (Multi-Category Support)
📌 **Overview:**

UC10 replaces QuantityLength and QuantityWeight with a single generic class:

- Quantity<U extends IMeasurable>

- All unit enums (LengthUnit, WeightUnit) now implement IMeasurable.

🎯 **Purpose:**

- Remove duplicate classes

- Follow DRY & SRP

- Support unlimited measurement categories

- Keep strong type safety

⚙️ **What It Handles:**

- The generic Quantity class provides:

  - equals()

  - convertTo()

  - add()

  - add(targetUnit)

Works for both Length and Weight.

🔒 **Type Safety:**

- Quantity<LengthUnit> ≠ Quantity<WeightUnit>

- Cross-category equality returns false

🚀 **Scalability:**

To add a new category:

- Create enum implementing IMeasurable

- Use Quantity<NewUnit>

✔ No new Quantity class
✔ No duplicate logic
✔ All previous UCs preserved
