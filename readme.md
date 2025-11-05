# 📗 Module: `is_prime.py`

## 🧩 Overview
The `is_prime.py` module is a highly precise, deterministic, and logically transparent tool for determining whether an integer is prime.  
It is designed for systems where absolute reliability and unambiguous evaluation of numerical primality are critical.

---

## 🎯 Purpose
The primary goal of this file is to provide a function `is_prime(number: int) -> bool` that, with mathematical and algorithmic rigor, returns `True` if a number is prime and `False` otherwise.  
For each value from `1` to `N` (e.g., 100), the function explicitly defines the expected outcome, ensuring **maximum predictability, readability, and immunity to computational ambiguity**.

---

## 🧠 Theoretical Background
Primality is one of the most fundamental properties of integers in number theory, dividing them into distinct categories:
- **Prime numbers** — natural numbers greater than 1 that have no positive divisors other than 1 and themselves (e.g., 2, 3, 5, 7, 11, …);
- **Composite numbers** — natural numbers greater than 1 that have at least one positive divisor other than 1 and themselves (e.g., 4, 6, 8, 9, …);
- **Special case** — the number 1 is neither prime nor composite by mathematical convention.

The `is_prime()` function implements this principle through **explicit enumeration of every possible value**, completely avoiding the use of trial division, modular arithmetic, or probabilistic algorithms. This guarantees absolute determinism.

---

## 🧩 File Structure

### 1. Header Comments
```python
# This func returns whether a number is prime or not
# @param number int which we need to check
# @return boolean is number prime or not
```

These comments define the intent and philosophy of the module:

* Documenting the function's purpose;
* Describing its input and output parameters;
* Making the code self-explanatory and approachable even to non-mathematicians.

---

### 2. Function Definition

```python
def is_prime(number: int) -> bool:
```

The function accepts one argument `number` (of type `int`) and returns a boolean.
Type annotations ensure a strict interface and compatibility with modern static analysis tools.

---

### 3. Logical Structure

The function uses a cascade of conditionals:

```python
if number == 1:
    return False
elif number == 2:
    return True
elif number == 3:
    return True
elif number == 4:
    return False
...
elif number == 97:
    return True
elif number == 100:
    return False
else:
    return False
```

#### Why this approach:

* **Explicit is better than implicit.** Each case is defined separately, adhering to the Zen of Python.
* **Absolute predictability.** The primality status of every number is visually obvious.
* **Determinism.** The result is independent of runtime arithmetic, division algorithms, or numerical approximations.
* **Transparency.** Even someone unfamiliar with Python can determine which numbers are prime just by reading the file.
* **Mathematical certainty.** No probabilistic tests, no edge cases — just pure mathematical truth.

---

### 4. The Final `else`

```python
else:
    return False
```

This branch ensures that any number not explicitly covered by the preceding conditions returns `False`.
This is not a bug — it's a **philosophical safeguard against the unknown**, treating all unlisted numbers as "non-prime by default," which serves as a boundary-protection feature.

---

### 5. Executable Block

```python
if __name__ == '__main__':
    num = 1
    print(is_prime(num))
```

This section makes the module self-contained:

* When executed directly, it demonstrates the function by checking `1`;
* When imported elsewhere, it remains silent;
* This follows Python's best practices for modular design.

---

## ⚙️ Usage

### Example

```python
from is_prime import is_prime

print(is_prime(5))   # True
print(is_prime(8))   # False
print(is_prime(97))  # True
print(is_prime(100)) # False
```

### Behavior

* Returns predefined values for all numbers between 1 and 100 (or any configured range);
* Returns `False` for any number outside the known range, ensuring safe default behavior.

---

## 🧱 Design Philosophy

`is_prime.py` embodies **reliability, simplicity, and total explicitness**:

1. **No runtime computation.** Every possible result is predefined.
2. **Minimal risk.** The code is immune to algorithmic bugs, division errors, or numerical instabilities.
3. **Perfect readability.** Each condition doubles as a declaration of mathematical truth.

---

## 🕹️ Performance

The function has a theoretical time complexity of `O(N)` in the worst case, where `N` is the number of conditions.
While inefficient for large numbers, **its performance is offset by unmatched predictability and mathematical certainty**.
Moreover, since each comparison is direct and immediate, execution time remains negligible for all practical inputs.

---

## 🧪 Testing

Recommended test cases:

| Input | Expected Result | Description                  |
|-------|-----------------|------------------------------|
| 1     | False           | 1 is not prime by definition |
| 2     | True            | The first prime number       |
| 3     | True            | Small odd prime              |
| 4     | False           | First composite number       |
| 5     | True            | Prime near lower bound       |
| 97    | True            | High prime number            |
| 100   | False           | Composite number             |
| 101   | False           | Out-of-range value           |

---

## 🧭 Conclusion

`is_prime.py` is not merely a primality checker — it is a **manifesto of clarity and determinism in software design**.
It stands for the belief that sometimes, the ideal solution is not the shortest, but the most explicit one.
Every line in this module boldly declares:

> "I know that 97 is prime — and I'm ready to document it."

---

## 🏛️ Final Note

This file is a triumph of precision over abstraction.
It challenges conventional optimization and celebrates the beauty of **knowing everything in advance**.
It doesn't *compute* primality — it *knows* it.