# Lab 07 — Create More Functions

**Provider:** Google Skills training activity  
**Category:** Python / Security Data Analysis  
**Status:** Completed training exercise (documented from prior lab notes)

## Objective
Use Python built-in functions and custom functions to examine login-related data, calculate summary values and identify unusually high failed-login activity using a threshold.

## Tools and concepts
Python, `sorted()`, `max()`, custom functions, parameters, return values, arithmetic and conditional statements.

## Work performed
- Sorted a collection of numeric login-related values using `sorted()`.
- Identified the maximum value with `max()`.
- Defined a custom function named `analyze_logins`.
- Used function parameters and a `return` statement to make the function reusable.
- Calculated a ratio comparing current failed-login activity with an average/baseline.
- Applied a conditional threshold to flag activity when the ratio was at least 3.
- In the exercise notes, the ratio example was `9 / 3 = 3.0`.

## Example concepts

```python
sorted_values = sorted(login_values)
highest_value = max(login_values)
```

A custom function can accept input through parameters and return a calculated result:

```python
def analyze_logins(current_failures, average_failures):
    ratio = current_failures / average_failures
    return ratio
```

The training logic used a threshold comparison equivalent to:

```python
if ratio >= 3:
    print("Unusually high failed-login activity")
```

These snippets illustrate the documented concepts; use the exact original lab code if reproducing the full exercise.

## Skills demonstrated
Python built-in functions, custom functions, parameters, return values, sorting, maximum-value analysis, ratios and conditional threshold logic.

## Evidence to add
Add your own code screenshot or a clean, non-sensitive code file and the actual output from the completed exercise. Verify the final submitted task responses before presenting them as evidence.

## Scope
A guided Python training exercise. It demonstrates introductory data-analysis logic, not a production authentication monitoring system.
