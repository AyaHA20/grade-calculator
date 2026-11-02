# Student Grade Calculator

A simple Python application that calculates the average grade of a student
and determines whether the student passes.

## Installation

```bash
pip install -r requirements.txt
```

## Run Tests

```bash
pytest -v
```

## Run Linting

```bash
flake8 .
```

## Usage

```python
from calculator import calculate_average, is_passing, get_grade_category

average = calculate_average([12, 14, 9])  # 11.67
is_passing(average)                       # True (passing grade is 10 or more)
get_grade_category(average)               # "Average"
```

| Average        | Category    |
|----------------|-------------|
| 16 or higher   | Excellent   |
| 12 – 15.99     | Good        |
| 10 – 11.99     | Average     |
| below 10       | Fail        |

`calculate_average` raises `ValueError` if the grades list is empty.
