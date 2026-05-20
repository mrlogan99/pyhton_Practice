# 🐍 Python Revision Notes - Level 2 & 3

---

## Level 2 - List Questions

### 1. Maximum in List (without max())

**Concept:** Pehle element ko maximum maan lo, phir har element se compare karo.

```python
numbers = [3, 7, 1, 9, 4]
maximum = numbers[0]

for i in numbers:
    if i > maximum:
        maximum = i

print(maximum)
# Output: 9
```

---

### 2. String Reverse (without reverse())

**Concept:** Peeche se loop chalao ya slicing use karo.

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
# Output: olleh
```

---

### 3. Duplicate Elements Hatao

**Concept:** Nayi list banao, `not in` se check karo, `append` karo.

```python
numbers = [1, 2, 3, 2, 4, 1, 5]
result = []

for i in numbers:
    if i not in result:
        result.append(i)

print(result)
# Output: [1, 2, 3, 4, 5]
```

---

### 4. Even/Odd Alag Karo

**Concept:** Do alag lists banao aur `%` operator se check karo.

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8]
even = []
odd = []

for i in numbers:
    if i % 2 == 0:
        even.append(i)
    else:
        odd.append(i)

print("Even:", even)
print("Odd:", odd)
# Output:
# Even: [2, 4, 6, 8]
# Odd:  [1, 3, 5, 7]
```

---

## Level 3 - Problem Solving

### 1. FizzBuzz

**Concept:** Sabse specific condition pehle check karo — order matter karta hai!

```python
n = int(input())
for i in range(1, n+1):
    if i % 3 == 0 and i % 5 == 0:  # pehle FizzBuzz!
        print("FizzBuzz")
    elif i % 3 == 0:
        print("Fizz")
    elif i % 5 == 0:
        print("Buzz")
    else:
        print(i)
```

> ⚠️ **Important:** `FizzBuzz` pehle check karo warna kabhi print nahi hoga!

---

### 2. Palindrome Check

**Concept:** String ko reverse karo aur original se compare karo.

```python
string = input()
rev_str = string[::-1]

if string == rev_str:
    print("Palindrome")
else:
    print("Not Palindrome")

# madam  → Palindrome ✅
# hello  → Not Palindrome ✅
```

---

### 3. Two Sum

**Concept:** Nested loops se har do numbers ka sum check karo.

```python
numbers = [2, 7, 11, 15]
target = 9

for i in range(len(numbers)):
    for j in range(i+1, len(numbers)):  # i+1 kyunki same element dobara nahi
        if numbers[i] + numbers[j] == target:
            print([i, j])

# Output: [0, 1]  (2 + 7 = 9)
```

---

## 📝 New Concepts Seekhe

| Concept | Use | Example |
|---------|-----|---------|
| `not in` | List mein nahi hai check | `if i not in result` |
| `append()` | List mein add karo | `result.append(i)` |
| `[::-1]` | String/List reverse | `"hello"[::-1]` |
| Nested Loop | Loop ke andar loop | Two Sum problem |
| `i+1` in range | Same element skip karo | `range(i+1, n)` |

---

*Keep practicing! 💪🚀*
