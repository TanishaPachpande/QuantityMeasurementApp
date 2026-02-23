# QuantityMeasurementApp

## ✅ UC14 – Temperature Support with Selective Arithmetic
📌 **Overview:**

UC14 adds Temperature measurement support to the system.

Unlike length, weight, and volume:

✅ Temperature supports equality & conversion

❌ Temperature does NOT support arithmetic (add, subtract, divide)

🛠 **Key Changes:**

1️⃣ Refactored IMeasurable

Added:

- Default method: supportsArithmetic()

- Default method: validateOperationSupport(String operation)

- Functional Interface: SupportsArithmetic

By default → arithmetic allowed
Temperature overrides → arithmetic NOT allowed

✔ Backward compatible
✔ Existing units unchanged

2️⃣ Created TemperatureUnit Enum

Supports:

- CELSIUS

- FAHRENHEIT

- KELVIN

Implements:

 - Non-linear conversion formulas

 - Arithmetic support = false

 - Clear UnsupportedOperationException messages

3️⃣ Updated Quantity<U>

Before performing:

- add()

- subtract()

- divide()

System checks:

 - unit.validateOperationSupport(operation)

 - If unsupported → throws meaningful exception.

🌡 **Temperature Conversions:**

- °F = (°C × 9/5) + 32

- °C = (°F − 32) × 5/9

- K = °C + 273.15


❌ Unsupported Operations
new Quantity<>(100, CELSIUS).add(...)
→ UnsupportedOperationException

Clear error message explains why.

🧠 **Key Concepts:**

- Interface Segregation Principle (ISP)

- Default methods in interfaces

- Functional Interfaces & Lambdas

- Non-linear conversion handling

- Capability-based design

- Backward-compatible refactoring
