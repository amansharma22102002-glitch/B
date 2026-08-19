# Basic Calculator — GUI App (Python + Tkinter)

A simple desktop calculator built with Python's built-in **Tkinter** GUI toolkit.
This project takes the logic of a typical command-line Python calculator and gives
it a clickable, windowed interface.

![Calculator preview](calc_mockup.png)

## Features

- **Equation display** — shows the expression as you build it, and the final result
- **Clickable buttons** — digits `0–9`, decimal point, and parentheses
- **Core operations** — addition (`+`), subtraction (`-`), multiplication (`*`), division (`/`)
- **Clear (`C`)** — resets the display instantly
- **Equals (`=`)** — evaluates the expression and shows the result
- Basic error handling (e.g. division by zero)

## Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core language |
| Tkinter | GUI toolkit (built into the Python standard library) |
| VS Code | Development environment |
| GitHub | Version control & hosting |

## Getting Started

### Prerequisites
- Python 3.8 or later. Tkinter ships with most standard Python installs.
  - On Debian/Ubuntu, if Tkinter is missing: `sudo apt install python3-tk`
  - On Windows/macOS, Tkinter is included with the official Python installer.

### Run it

```bash
git clone https://github.com/<your-username>/basic-calculator.git
cd basic-calculator
python calculator.py
```

A window titled **"Basic Calculator"** will open.

## Project Structure

```
basic-calculator/
├── calculator.py     # Main application script
└── README.md         # This file
```

## How It Works

The app is built around a single `Calculator` class:

| Method | Responsibility |
|---|---|
| `__init__` | Creates the window and calls the build methods |
| `_build_display()` | Creates the read-only display bound to a `StringVar` |
| `_build_buttons()` | Lays out digits & operators on a grid using `tk.Button` |
| `on_button_click()` | Routes a click to append, clear, or calculate |
| `append_to_expression()` | Builds up the expression string as keys are pressed |
| `calculate()` | Safely evaluates the expression and displays the result or an error |

## Example

```
Input:  12 + 7 * 2
Press:  =
Output: 26
```

## Possible Improvements

- Keyboard input support (typing instead of clicking)
- Percentage (`%`) and memory (`M+`, `M-`, `MR`) keys
- Packaging as a standalone `.exe` / `.app`

## License

This project is free to use for learning purposes.
