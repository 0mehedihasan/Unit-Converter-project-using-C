# Unit Converter — C Console Application

A feature-rich, menu-driven unit converter built in C for the Windows console. Supports **8 conversion categories** with over **60 individual conversions**, including length, time, temperature, mass, electric current, area, volume, and currency.

---

## Table of Contents

- [Features](#features)
- [Supported Conversions](#supported-conversions)
- [Screenshots](#screenshots)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Building](#building)
  - [Running](#running)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

---

## Features

- **8 conversion categories** accessible through an interactive menu
- **Continuous operation** — perform multiple conversions without restarting
- **Formatted console UI** — custom colors (red background / white text) and large readable font
- **Two-decimal precision** on all calculated results

---

## Supported Conversions

| Category | Conversions |
|---|---|
| **Length** | Meter ↔ Centimeter, Kilometer ↔ Meter, Meter ↔ Millimeter, Inch ↔ Meter |
| **Time** | Seconds ↔ Minutes, Seconds ↔ Hours, Minutes ↔ Hours, Hours ↔ Days, Days ↔ Weeks, Days ↔ Months, Days ↔ Years |
| **Temperature** | Fahrenheit ↔ Celsius, Celsius ↔ Kelvin, Fahrenheit ↔ Kelvin |
| **Mass** | Gram ↔ Kilogram, Gram ↔ Milligram |
| **Electric Current** | Ampere ↔ Milliampere, Kiloampere ↔ Milliampere |
| **Area** | Circle, Rectangle, Triangle, Square |
| **Volume** | Liter ↔ Milliliter, Liter ↔ Centiliter, Liter ↔ Deciliter, Liter ↔ Hectoliter |
| **Currency** | BDT ↔ USD, EUR, INR, GBP, JPY, RUB, CHF, SEK, AUD, CAD (fixed rates) |

---

## Screenshots

After launching, the program presents a numbered main menu:

```
========================================================
|              WELCOME TO UNIT CONVERTER               |
========================================================

1. Length Converter
2. Time Converter
3. Temperature Converter
4. Mass Converter
5. Current Converter
6. Area Converter
7. Volume Converter
8. Currency Converter

Enter your choice (1-8):
```

Select a category, then choose a specific conversion from the sub-menu, enter a value, and the result is displayed instantly.

---

## Getting Started

### Prerequisites

| Requirement | Details |
|---|---|
| **Operating System** | Windows (the project uses the Windows Console API via `Windows.h`) |
| **Compiler** | Any C compiler that supports the Windows API — for example **GCC (MinGW)** or **MSVC** |
| **IDE (optional)** | [Code::Blocks](http://www.codeblocks.org/) — a `.cbp` project file is included |

### Building

**Option A — GCC (MinGW)**

```bash
gcc -o unit_converter "unit converter final project/main updated.c" -lm
```

**Option B — Code::Blocks**

1. Open `CODE BLOCKS ALL FILE/unit_conversion.cbp` in Code::Blocks.
2. Click **Build → Build and Run** (or press <kbd>F9</kbd>).

### Running

```bash
./unit_converter.exe
```

The converter launches in the current console window with custom formatting.

---

## Usage

1. Run the executable.
2. Choose a conversion category (1–8) from the main menu.
3. Choose the specific conversion from the sub-menu.
4. Enter the value you want to convert.
5. View the result.
6. When prompted **"Do you want to continue? [y/n]"**, press `y` to perform another conversion or `n` to exit.

---

## Project Structure

```
.
├── CODE BLOCKS ALL FILE/       # Code::Blocks project (early version)
│   ├── main.c                  # Source (basic version)
│   ├── unit_conversion.cbp     # Code::Blocks project file
│   └── unit_conversion.layout  # Code::Blocks layout file
│
├── SOURCE CODE/                # Intermediate version with Windows API enhancements
│   ├── main.c
│   └── unit_converter.c
│
├── unit converter final project/   # Final version (recommended)
│   ├── main.c                      # Near-final source
│   ├── main updated.c              # ✅ Latest source with bug fixes
│   └── UNIT CONVERTER sdp REPORT.pdf  # Project report
│
├── LICENSE                     # MIT License
└── README.md                   # This file
```

> **Tip:** The recommended source file to build and use is **`unit converter final project/main updated.c`** — it contains the latest bug fixes and improvements.

---

## Contributing

Contributions are welcome! Here are some ideas for improvement:

- **Cross-platform support** — replace `Windows.h` calls with portable alternatives so the project runs on Linux and macOS.
- **Modular design** — refactor the single `main()` function into smaller, reusable functions.
- **Input validation** — add checks for non-numeric or out-of-range input.
- **Live currency rates** — fetch exchange rates from an API instead of using fixed values.
- **Additional units** — add conversions for speed, data storage, pressure, energy, etc.

### How to Contribute

1. **Fork** this repository.
2. **Create a branch** for your feature or fix:
   ```bash
   git checkout -b feature/my-improvement
   ```
3. **Commit** your changes with a clear message:
   ```bash
   git commit -m "Add input validation for length converter"
   ```
4. **Push** to your fork and open a **Pull Request**.

Please make sure your code compiles without warnings before submitting.

---

## License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

Copyright © 2022 Md. Mehedi Hasan