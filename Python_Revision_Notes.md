# 🐍 Python Revision Notes

> Yeh notes un concepts ka summary hai jo maine khud practice karke seekha!

---

## 📌 Table of Contents
1. [Even / Odd](#1-even--odd)
2. [Sum 1 to N](#2-sum-1-to-n)
3. [Factorial](#3-factorial)
4. [Prime Number](#4-prime-number)
5. [Maximum in List](#5-maximum-in-list)
6. [String Reverse](#6-string-reverse)
7. [Sets - Symmetric Difference](#7-sets---symmetric-difference)
8. [Leap Year](#8-leap-year)

---

## 1. Even / Odd

**Concept:** `%` operator remainder deta hai. Agar remainder `0` ho toh Even!

```python
n = int(input())
if n % 2 == 0:
    print("even")
else:
    print("odd")
```

---

## 2. Sum 1 to N

**Concept:** Loop mein har number ko `sum` mein add karte jao.

```python
n = int(input())
sum = 0
for i in range(1, n+1):
    sum += i
print(sum)
```

---

## 3. Factorial

**Concept:** Loop mein har number ko `factorial` se multiply karte jao.  
`0! = 1` aur `1! = 1` — yeh special cases hain!

```python
n = int(input())
factorial = 1
if n == 0 or n == 1:
    print(1)
else:
    for i in range(1, n+1):
        factorial *= i
    print(factorial)
```

---

## 4. Prime Number

**Concept:** Ek `is_prime` flag rakho. Agar koi number divide kar de toh `False` kar do aur `break` karo.

```python
n = int(input())
is_prime = True

for i in range(2, n):
    if n % i == 0:
        is_prime = False
        break

if is_prime:
    print("Prime")
else:
    print("Not Prime")
```

---

## 5. Maximum in List

**Concept:** Pehle element ko `maximum` maan lo. Phir har element se compare karo — agar bada mile toh update karo.

```python
numbers = [3, 7, 1, 9, 4]
maximum = numbers[0]

for i in numbers:
    if i > maximum:
        maximum = i

print(maximum)
```

---

## 6. String Reverse

**Concept:** Peeche se loop chalao aur characters add karte jao.

```python
# Tarika 1 - range peeche se
string = "hello"
result = ""
for i in range(len(string)-1, -1, -1):
    result = result + string[i]
print(result)

# Tarika 2 - Slicing (sabse simple!)
string = "hello"
print(string[::-1])
```

---

## 7. Sets - Symmetric Difference

**Concept:** Jo elements sirf ek set mein hain (dono mein nahi) — unka count nikalo.

```python
n = int(input())
english = set(input().split())

m = int(input())
french = set(input().split())

result = english.symmetric_difference(french)
print(len(result))
```

> **Shortcut:** `english ^ french` bhi same kaam karta hai!

---

## 8. Leap Year

**Concept:** Teen conditions check karo in order:
- 400 se divide → Leap Year ✅
- 100 se divide → Leap Year NAHI ❌
- 4 se divide → Leap Year ✅

```python
def is_leap(year):
    return year % 4 == 0 and (year % 100 != 0 or year % 400 == 0)
```

---

## 📝 Important Operators

| Operator | Kaam | Example |
|----------|------|---------|
| `%` | Remainder nikalna | `7 % 2 = 1` |
| `+=` | Add karke assign | `sum += i` |
| `*=` | Multiply karke assign | `factorial *= i` |
| `//` | Integer division | `7 // 2 = 3` |
| `**` | Power | `2 ** 3 = 8` |

---

## 📝 Important Concepts

| Concept | Use |
|---------|-----|
| `range(1, n+1)` | 1 se n tak loop |
| `range(n-1, -1, -1)` | Peeche se loop |
| `break` | Loop band karo |
| `is_prime = True` | Flag variable |
| `set.symmetric_difference()` | Sirf ek mein wale elements |

---

*Keep practicing! 💪🚀*
