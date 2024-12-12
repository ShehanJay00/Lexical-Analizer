# Lexical-Analizer

## Overview
This repository contains a simple lexical analyzer implemented in Python without using built-in libraries such as `re` for regular expressions. The purpose of this project is to tokenize arithmetic expressions into distinct components called **tokens**, such as identifiers, numbers, operators, parentheses, and other symbols.

## Features
- Tokenizes arithmetic expressions into:
  - Identifiers (e.g., variables like `x`, `y`, `result`)
  - Numbers (e.g., `10`, `20`)
  - Operators (`+`, `-`, `*`, `/`)
  - Parentheses (`(`, `)`)
  - Assignment (`=`)
  - Semicolon (`;`)
- Fully implemented without using regex or external libraries.
- Handles both simple and complex expressions.
- Includes comprehensive test cases.

## Expected Output
For an input string like:
```plaintext
x = 10 + 20 * (30 / y);
```
The lexer produces the following tokens:
```plaintext
('IDENTIFIER', 'x')
('ASSIGNMENT', '=')
('NUMBER', '10')
('OPERATOR', '+')
('NUMBER', '20')
('OPERATOR', '*')
('PARENTHESIS', '(')
('NUMBER', '30')
('OPERATOR', '/')
('IDENTIFIER', 'y')
('PARENTHESIS', ')')
('SEMICOLON', ';')
```

## Implementation
### How It Works
1. The input string is processed character by character.
2. Tokens are identified based on their type (e.g., letter, digit, operator).
3. The lexer builds tokens and outputs them in the format `(TOKEN_TYPE, VALUE)`.

### Token Types
- **IDENTIFIER**: Variables (e.g., `x`, `result`).
- **NUMBER**: Numeric values (e.g., `10`, `20`).
- **OPERATOR**: Arithmetic operators (`+`, `-`, `*`, `/`).
- **PARENTHESIS**: Parentheses (`(`, `)`).
- **ASSIGNMENT**: Assignment operator (`=`).
- **SEMICOLON**: Semicolon (`;`).

### Key Functions
- `is_letter(char)`: Checks if a character is a letter.
- `is_digit(char)`: Checks if a character is a digit.
- `lexer(input_string)`: Tokenizes the input string into tokens.

## Usage
### Clone the Repository
```bash
git clone https://github.com/ShehanJay00/Lexical-Analizer.git
cd lexical-analyzer
```

### Run the Code
1. Ensure you have Python installed.
2. Run the `lexer.py` file:
   ```bash
   python lexer.py
   ```
3. Modify the `input_string` variable in the script to test different expressions.

### Example Input
```python
input_string = "x = 10 + 20 * (30 / y);"
```

### Example Output
```plaintext
('IDENTIFIER', 'x')
('ASSIGNMENT', '=')
('NUMBER', '10')
('OPERATOR', '+')
('NUMBER', '20')
('OPERATOR', '*')
('PARENTHESIS', '(')
('NUMBER', '30')
('OPERATOR', '/')
('IDENTIFIER', 'y')
('PARENTHESIS', ')')
('SEMICOLON', ';')
```

## Test Cases
The repository includes multiple test cases to validate the correctness of the lexer:
- **Basic expressions**: `x = 10;`
- **Complex expressions**: `result = a * (b + c / d);`

To add your own test cases, modify the `input_string` in the script.


## Contribution
Feel free to contribute by:
- Adding new features.
- Reporting issues.
- Providing additional test cases.

## License
This project is licensed under the [MIT License](LICENSE).

---

Thank you for visiting this repository! Happy coding! 🎉

