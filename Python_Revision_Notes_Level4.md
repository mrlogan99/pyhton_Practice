# 🐍 Python Revision Notes - Level 4

---

## 1. List Sort (Selection Sort)

**Concept:** Minimum nikalo, result mein daalo, list se hatao — repeat karo!

```python
numbers = [64, 34, 25, 12, 22]
result = []

while len(numbers) != 0:
    minimum = numbers[0]
    for i in numbers:
        if i < minimum:
            minimum = i
    result.append(minimum)
    numbers.remove(minimum)

print(result)
# Output: [12, 22, 25, 34, 64]
```

---

## 2. Second Largest Number

**Concept:** Sort karo phir last se doosra element lo!

```python
numbers = [64, 34, 25, 12, 22]
result = []

while len(numbers) != 0:
    minimum = numbers[0]
    for i in numbers:
        if i < minimum:
            minimum = i
    result.append(minimum)
    numbers.remove(minimum)

print(result[-2])  # second largest
# Output: 34
```

---

## 3. Most Frequent Character

**Concept:** Har character ka count nikalo, sabse zyada wala store karo!

```python
string = "hello"
max_count = 0
result = ""

for char in string:
    count = string.count(char)
    if count > max_count:
        max_count = count
        result = char

print(result)
# Output: l
```

---

## 4. Duplicate Numbers Ka Sum

**Concept:** Pehle duplicates dhundho, phir unka sum nikalo!

```python
numbers = [1, 2, 3, 2, 4, 1, 5]
duplicates = []
total = 0

for i in numbers:
    if numbers.count(i) > 1 and i not in duplicates:
        duplicates.append(i)

for i in duplicates:
    total += i

print(total)
# Output: 3  (1 + 2 = 3)
```

---

## 5. Square Check in List

**Concept:** Har number ka square nikalo aur check karo list mein hai ya nahi!

```python
numbers = [2, 3, 4, 6, 9]

for i in numbers:
    if i ** 2 in numbers:
        print(True)
        break
else:
    print(False)

# Output: True  (3**2 = 9 list mein hai!)
```

---

## 📝 New Concepts Seekhe

| Concept | Use | Example |
|---------|-----|---------|
| `while len(list) != 0` | List empty hone tak loop | Sort karna |
| `list.remove(x)` | List se element hatao | `numbers.remove(minimum)` |
| `list[-1]` | Last element | Largest |
| `list[-2]` | Last se doosra | Second Largest |
| `string.count(x)` | Character kitni baar aaya | Most frequent |
| `**` | Power/Square | `3 ** 2 = 9` |
| `for/else` | Break nahi aaya toh else | Square check |

---

> ⚠️ **Important:** `for/else` ka matlab — agar loop mein `break` nahi aaya toh `else` execute hoga!

---

*Keep practicing! 💪🚀*
