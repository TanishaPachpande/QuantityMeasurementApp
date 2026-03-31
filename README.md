
# QuantityMeasurementApp

## Project Overview

The **Quantity Measurement App** is a Test-Driven Development (TDD)-based project designed to demonstrate how to build scalable and maintainable software by starting simple and progressively adding complexity through Use Cases (UCs).  
The application focuses on converting and comparing measurements across different quantities (length, weight, volume, temperature, etc.) while following clean design principles and incremental development. 

---

## 📜 Development Methodology

This project follows the **TDD cycle**:

1. Write a failing test.
2. Write the minimal code to pass the test.
3. Refactor without breaking tests.

This approach ensures:

- Safety
- Maintainability
- Scalability

### Git Workflow

We followed a professional branching strategy:

- `main` → stable production code  
- `dev` → integration branch  
- `feature/UCx-*` → individual feature branches

Each UC is:

- Developed in a feature branch
- Tested locally
- Pushed via Pull Request
- Merged into `dev` once complete and verified

---

## 🔍 Use Case Implementation

Below are the major use cases (UCs) implemented in this app:

### UC1 — Basic Length Equality Check

- Compares two length values for equality regardless of the unit.

- Accepts values like 1 foot and 12 inches and returns equal or not equal.

- Handles null / invalid inputs safely.

- Ensures type safety so only length-to-length comparisons are allowed.

- This is where the system began — the simplest equality feature.

### UC2 — Support for Additional Length Units

- Introduced support for more units (e.g., centimeters, inches, meters).

- Extended conversion logic while maintaining correct comparisons.

- Refactoring was started to remove duplication from UC1 logic.

- This extends UC1 by enabling more units for comparison and conversion.

### UC3 — Refactor to Generic Length Class

- Refactored multiple individual unit classes into a single generic length class.

- Introduced unit enums and base interfaces.

- Reduced code duplication and improved maintainability.

- This step shifts from specific classes to a reusable base structure for lengths.

### UC4 — Extensible Unit Architecture (Open-Closed Design)

- Reorganized unit conversion logic to be easily extensible.

- Adds a framework so new units can be added without modifying core logic.

- Encourages modularity and clean extension of features.

- This enables the app to scale to new unit types without changing old code.

### UC5 — Unit Conversion Between Different Units

- Implements conversion APIs between units like feet → inches, inches → cm, etc.

- Centralized conversion factors and logic into reusable routines.

- Ensures reliable “convert from A to B” functionality.

- This introduces real conversion as opposed to just comparing values.

### UC6 & UC7 — Arithmetic Operations (Addition / Subtraction)

- UC6 introduced addition of two measurement quantities.

- Supports mix of units (e.g., 1 ft + 2 inches) with a target unit.

- Ensures correct normalization and rounding before summing.

### UC7 added subtraction and potential domain validations (e.g., negative results).

- These UCs extend the system from comparison to full arithmetic support.

### UC8 — Architectural Refactor for Separation of Concerns

- Separated core logic from enums and interfaces.

- Split converters, models, and helper utilities into layers.

- Prepared code for adding completely new categories (weight, volume, etc.).

- Reinforced SOLID design principles.

- This ensures cleaner project layering before adding new domains.

### UC9 — Weight Measurement and Conversions

- Introduced weight category with units like grams, kilograms, pounds, ounces.

- Implemented conversion logic and comparison for Weight types.

- Maintains the generic structure defined earlier.

- Ensures that weight quantities can be compared and converted like lengths.

- This adds a whole new domain beyond length.

### UC10 — Generic Quantity Measurement Framework

- The system now supports any measurable type (length, weight, volume, temperature).

- Refactored shared logic into generic interfaces and processors.

- Means adding categories no longer repeats major logic.

- This is the most important architectural shift — the system now truly supports multiple dimensional categories.

### UC11 — Volume Measurement

- Introduced volume category (e.g., liters, gallons, milliliters).

- Uses generic engine from UC10 to handle conversion & comparison.

- Maintains consistent behavior with other categories.

- Expands measurement domains further.

### UC12 — Division & Edge Case Handlings

- Added division operations allowing e.g., ratio computations.

- Ensures safe behavior for division by zero.

- Also validates edge cases like invalid unit combinations.

- This adds deeper mathematical support to the framework.

### UC13 — Centralized Arithmetic Logic

- Moved addition, subtraction, division, and comparison logic into a central shared module.

- Removes duplication across categories.

- Improves testability and clarity.

- Helps enforce the Don’t Repeat Yourself (DRY) principle.

### UC14 — Temperature Measurements

- Adds support for temperature units (Celsius, Kelvin, Fahrenheit).

- Temperature conversion involves non-linear formulas (not simple scale factors).

- Arithmetic operations like addition/subtraction must be treated appropriately or disabled for temperature.

- Shows that the system can handle complex domain logic (not just linear unit conversions).
