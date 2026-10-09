[README-codelab1-oct26.md](https://github.com/user-attachments/files/33263496/README-codelab1-oct26.md)
# BMI Calculator

A simple C++ console program that calculates a user's Body Mass Index (BMI) from their height and weight, then classifies the result into a standard health category.

Created as part of the Programming Skills Portfolio assessment for CodeLab II (Bath Spa University).

## Features

- Validated user input for height (metres) and weight (kg), rejecting non-numeric and non-positive values
- Calculates BMI using the standard formula: `weight / (height * height)`
- Classifies the result into one of four categories: underweight, healthy weight, overweight, obese
- Allows the user to repeat the calculation as many times as they like
- Output formatted to one decimal place

## How It Works

The program is split into three functions, each with a single responsibility:

| Function | Purpose |
|---|---|
| `getMeasurements(double&, double&)` | Prompts for and validates height and weight, writing results directly into the caller's variables via reference parameters |
| `calculateBMI(double, double)` | Applies the BMI formula and returns the result |
| `classifyBMI(double)` | Maps the BMI value onto a category and returns it as a string |

`main()` ties these together in a loop, letting the user calculate BMI repeatedly until they choose to stop.

## Example Output

```
Enter height in metres: 1.75
Enter weight in kg: 70
Your BMI is: 22.9
Category: healthy weight

Calculate again? (y/n): n
Thank you for using the BMI calculator.
```

## Build & Run

```bash
g++ -o bmi_calculator main.cpp
./bmi_calculator
```

## Author

Tara ([TaraaaYah](https://github.com/TaraaaYah))
