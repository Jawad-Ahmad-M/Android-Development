# Android Calculator App

This Android calculator app is implemented in Java and provides basic arithmetic functionality with a clean and simple user interface.

---

## Features

- **Basic Arithmetic Operations:** Addition (`+`), subtraction (`-`), multiplication (`*`), and division (`/`).
- **Decimal Number Support:** Allows users to input decimal numbers via the dot (`.`) button.
- **Operator Precedence:** Correctly handles multiplication and division before addition and subtraction.
- **Clear and Delete:**  
  - **Clear (AC):** Resets the calculator input and internal state.  
  - **Delete (DEL):** Deletes the last entered character.
- **Input Display:** Shows the current input or result dynamically in a `TextView`.
- **Error Handling:** Detects invalid expressions and division by zero, providing feedback with Android Toast messages.
- **Precision:** Results are rounded to 8 decimal places and trailing zeros are removed for cleaner display.

---

## How It Works

1. **Initialization:**  
   Buttons for digits, operators, clear, delete, and equals are linked with `findViewById` and assigned a common click listener.

2. **User Input:**  
   When a button is pressed, the corresponding character (digit, operator, or decimal point) is appended to the current expression string shown in the display.

3. **Expression Parsing and Calculation:**  
   When the equals button is pressed:
   - The full expression string is parsed to separate numbers and operators.
   - Multiplication and division operations are performed first.
   - Then addition and subtraction operations are applied.
   - The final result is displayed, formatted to remove unnecessary trailing zeros.

4. **Clearing and Deleting:**  
   - Clear resets the input to `"0"` and clears stored numbers and operators.  
   - Delete removes the last character from the current input string.

---

## Code Highlights

- Uses a `TextView` (`solution_tv`) to show the current expression and results.
- Implements `View.OnClickListener` to handle button clicks efficiently.
- Uses `BigDecimal` for precise floating-point calculations and rounding.
- Manages operators and numbers via lists during expression evaluation.
- Provides feedback on errors via `Toast`.

---

## Limitations

- No support for parentheses or complex mathematical functions.
- Input validation is basic and may require enhancement for robustness.
- UI design is simple and can be improved for better user experience.

---

## Summary

This project demonstrates a functional calculator app for Android supporting basic arithmetic operations with operator precedence, decimal handling, and user-friendly features such as clear and delete. It provides a good foundation for further expansion into a more advanced calculator.

---

*Feel free to extend the app by adding scientific functions, parentheses handling, or improving UI/UX!*
