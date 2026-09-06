# 🔢 Python Pattern & Loop Programs

A collection of **Python programming practice programs** focused on nested loops, number patterns, alphabet patterns, binary patterns, and different types of star patterns.
This repository is designed to strengthen **logical thinking and loop-based problem-solving skills** in Python.

---

## 📌 Project Overview

Pattern programs are an excellent way to understand how loops work and how the output of one iteration depends on the current row and column.

This collection covers:

* Even number patterns
* Sequential number patterns
* Alphabet patterns
* Repeated alphabet patterns
* Binary number patterns
* Increasing star patterns
* Decreasing star patterns
* Right-aligned star patterns
* Pyramid patterns
* Diamond/star pyramid patterns
* Nested `for` loops
* Conditional statements inside loops

---

## 🛠️ Technologies Used

* **Python 3**
* `for` loops
* Nested loops
* `range()`
* `if-else`
* `chr()`
* Arithmetic operators
* `print()` with `end`

---

# 📂 Programs Included

## 1. Even Number Pattern

### Code

```python
num = 2

for i in range(1, 6, 1):
    for j in range(1, i + 1):
        print(num, end=" ")
        num = num + 2
    print()
```

### Output

```text
2
4 6
8 10 12
14 16 18 20
22 24 26 28 30
```

### Concept

The variable `num` starts at `2` and increases by `2` after every iteration.

```python
num = num + 2
```

This generates consecutive even numbers.

---

# 2. Sequential Number Pattern

### Code

```python
num = 1

for i in range(1, 6, 2):
    for j in range(1, i + 1):
        print(num, end=" ")
        num = num + 1
    print()
```

### Concept

The program demonstrates how a variable can retain its value between iterations of nested loops.

The `num` variable is incremented continuously:

```text
1 → 2 → 3 → 4 → 5 → ...
```

---

# 3. Increasing Alphabet Pattern

### Code

```python
for i in range(1, 6, 1):
    for j in range(i):
        print(chr(65 + j), end=" ")
    print()
```

### Output

```text
A
A B
A B C
A B C D
A B C D E
```

### Concept

The `chr()` function converts an ASCII value into a character.

```text
65 → A
66 → B
67 → C
68 → D
69 → E
```

Therefore:

```python
chr(65 + j)
```

generates consecutive alphabets.

---

# 4. Repeated Alphabet Pattern

### Code

```python
for i in range(1, 6, 1):
    for j in range(i):
        print(chr(64 + i), end=" ")
    print()
```

### Output

```text
A
B B
C C C
D D D D
E E E E E
```

### Concept

Unlike the previous pattern, the alphabet depends on the **row number `i`**.

For example:

```text
i = 1 → chr(65) → A
i = 2 → chr(66) → B
i = 3 → chr(67) → C
```

The same character is printed repeatedly within each row.

---

# 5. Binary Number Pattern

### Code

```python
for i in range(1, 6, 1):
    for j in range(1, i + 1):
        if (i + j) % 2 == 0:
            print(1, end=" ")
        else:
            print(0, end=" ")
    print()
```

### Output

```text
1
0 1
1 0 1
0 1 0 1
1 0 1 0 1
```

### Concept

The program uses:

```python
(i + j) % 2
```

to determine whether the sum of the row and column numbers is even or odd.

If:

```text
(i + j) % 2 == 0
```

the program prints `1`.

Otherwise, it prints `0`.

This creates an alternating binary pattern.

---

# 6. Increasing Star Pattern

### Code

```python
for i in range(1, 5, 1):
    for j in range(i):
        print("*", end=" ")
    print()
```

### Output

```text
*
* *
* * *
* * * *
```

### Concept

The number of stars increases according to the current row number.

---

# 7. Decreasing Star Pattern

### Code

```python
for i in range(5, 0, -1):
    for j in range(i):
        print("*", end=" ")
    print()
```

### Output

```text
* * * * *
* * * *
* * *
* *
*
```

### Concept

The reverse `range()`:

```python
range(5, 0, -1)
```

generates:

```text
5, 4, 3, 2, 1
```

Therefore, the number of stars decreases on each row.

---

# 8. Right-Aligned Increasing Triangle

### Code

```python
for i in range(1, 6, 1):
    for j in range(5 - i):
        print(" ", end=" ")

    for j in range(i):
        print("*", end=" ")

    print()
```

### Output

```text
        *
      * *
    * * *
  * * * *
* * * * *
```

### Concept

This pattern uses **two inner loops**:

1. The first loop prints spaces.
2. The second loop prints stars.

The number of spaces decreases while the number of stars increases.

---

# 9. Right-Aligned Decreasing Triangle

### Code

```python
for i in range(5, 0, -1):
    for j in range(5 - i):
        print(" ", end=" ")

    for j in range(i):
        print("*", end=" ")

    print()
```

### Output

```text
* * * * *
  * * * *
    * * *
      * *
        *
```

### Concept

This is the reverse version of the previous pattern.

As the number of stars decreases, the number of leading spaces increases.

---

# 10. Full Pyramid Pattern

### Code

```python
for i in range(1, 6, 1):

    for j in range(5 - i):
        print(" ", end=" ")

    for j in range(2 * i - 1):
        print("*", end=" ")

    print()
```

### Output

```text
        *
      * * *
    * * * * *
  * * * * * * *
* * * * * * * * *
```

### Concept

The number of stars in each row follows:

```text
2 × i − 1
```

Therefore:

```text
i = 1 → 1 star
i = 2 → 3 stars
i = 3 → 5 stars
i = 4 → 7 stars
i = 5 → 9 stars
```

This produces a centered pyramid.

---

# 11. Diamond Pattern

### Code

```python
for i in range(1, 6, 1):
    for j in range(5 - i):
        print(" ", end=" ")

    for j in range(2 * i - 1):
        print("*", end=" ")

    print()

for i in range(4, 0, -1):
    for j in range(5 - i):
        print(" ", end=" ")

    for j in range(2 * i - 1):
        print("*", end=" ")

    print()
```

### Output

```text
        *
      * * *
    * * * * *
  * * * * * * *
* * * * * * * * *
  * * * * * * *
    * * * * *
      * * *
        *
```

### Concept

The diamond consists of two sections:

### Upper Half

```python
range(1, 6)
```

creates the increasing pyramid.

### Lower Half

```python
range(4, 0, -1)
```

creates the decreasing pyramid.

Combining both sections creates a complete diamond.

---

# 🧠 Important Python Concepts

## 1. Nested `for` Loops

A nested loop is a loop inside another loop.

```python
for i in range(...):
    for j in range(...):
        print(...)
```

The outer loop generally controls the **rows**, while the inner loop controls the **elements within each row**.

---

## 2. `range()`

The general syntax is:

```python
range(start, stop, step)
```

Example:

```python
range(1, 6, 1)
```

produces:

```text
1 2 3 4 5
```

Reverse range:

```python
range(5, 0, -1)
```

produces:

```text
5 4 3 2 1
```

---

## 3. `chr()`

The `chr()` function converts an integer into its corresponding character.

```python
chr(65)
```

returns:

```text
A
```

Examples:

```text
chr(65) → A
chr(66) → B
chr(67) → C
chr(68) → D
chr(69) → E
```

---

## 4. Modulus `%`

The modulus operator returns the remainder of a division.

```python
10 % 2
```

returns:

```text
0
```

While:

```python
11 % 2
```

returns:

```text
1
```

This is useful for identifying even/odd values and generating alternating patterns.

---

## 5. `print()` and `end`

Normally:

```python
print("*")
print("*")
```

produces:

```text
*
*
```

Using:

```python
print("*", end=" ")
```

allows multiple values to appear on the same line:

```text
* * * * *
```

---

# 📊 Pattern Summary

| #  | Pattern                  | Main Concept                    |
| -- | ------------------------ | ------------------------------- |
| 1  | Even Numbers             | Nested loops + increment        |
| 2  | Sequential Numbers       | Counter variable                |
| 3  | Alphabet Triangle        | `chr()` + nested loops          |
| 4  | Repeated Alphabets       | Row-based `chr()`               |
| 5  | Binary Pattern           | `%` + conditional statements    |
| 6  | Increasing Stars         | Nested loops                    |
| 7  | Decreasing Stars         | Reverse `range()`               |
| 8  | Right-Aligned Triangle   | Spaces + stars                  |
| 9  | Right-Aligned Decreasing | Reverse loops + spaces          |
| 10 | Full Pyramid             | `2*i-1` logic                   |
| 11 | Diamond                  | Increasing + decreasing pyramid |

---

# 🎯 Learning Objectives

By practicing these programs, you will develop an understanding of:

* Nested loops
* Loop control
* Forward and reverse iteration
* Number patterns
* Alphabet patterns
* Binary patterns
* Conditional statements inside loops
* ASCII/Unicode character conversion
* Space management
* Pyramid and diamond logic
* Problem-solving using mathematical formulas

---

# 🚀 Recommended Next Practice

After completing these programs, try creating:

* Hollow square
* Hollow pyramid
* Number pyramid
* Floyd's Triangle
* Pascal's Triangle
* Diamond number pattern
* Hollow diamond
* Butterfly pattern
* Alphabet pyramid
* Palindrome number pattern

---

## 👨‍💻 Author

**Pranay Vishwanath Jadhao**

This repository is created as part of **Python programming practice** to improve logical thinking, loop concepts, and pattern-based problem solving.

---

## 📄 License

This project is created for **educational and learning purposes**.


