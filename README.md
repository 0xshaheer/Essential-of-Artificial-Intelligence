# Essential-of-Artificial-Intelligence
```markdown
# Artificial Intelligence Lab Reports

This repository contains Python lab work completed as part of the **Artificial Intelligence Lab** course at HITEC University, Taxila.  
Each lab demonstrates fundamental Python programming concepts with clear solutions and outputs.

---

## Lab 01 - Python Basics

### Question 1: Table of a Number
```python
num = int(input("Enter a number: "))
for i in range(1, 11):
    print(f"{num} x {i} = {num * i}")
```
**Sample Output:**
```
Enter a number: 8
8 x 1 = 8
8 x 2 = 16
...
8 x 10 = 80
```

---

### Question 2: Prime Number Check
```python
num = int(input("Enter a number: "))
if num > 1:
    for i in range(2, num):
        if num % i == 0:
            print(num, "is not a prime number.")
            break
    else:
        print(num, "is a prime number.")
else:
    print(num, "is not a prime number.")
```
**Sample Output:**
```
Enter a number: 5
5 is a prime number.
```

---

### Question 3a: Numbers 1–10 with While Loop
```python
i = 1
while i <= 10:
    print(i)
    i += 1
```
**Sample Output:**
```
1
2
3
...
10
```

---

### Question 3b: Even Numbers 1–20
```python
i = 1
while i <= 20:
    if i % 2 == 0:
        print(i)
    i += 1
```
**Sample Output:**
```
2
4
6
...
20
```

---

### Question 4: Harshad Number
```python
num = int(input("Enter a number: "))
sum_of_digits = sum(int(digit) for digit in str(num))
if num % sum_of_digits == 0:
    print(num, "is a Harshad Number.")
else:
    print(num, "is not a Harshad Number.")
```
**Sample Output:**
```
Enter a number: 45
45 is a Harshad Number.
```

---

## Lab 02 - Lists, Tuples, Sets, Dictionaries

### Question 1: Count Strings with Same First & Last Character
```python
sample_list = ['abc', 'xyz', 'aba', '1221', 'xyzzyx', 'aa', '12']
count = 0
for s in sample_list:
    if len(s) >= 2 and s[0] == s[-1]:
        count += 1
print("Expected Result:", count)
```
**Sample Output:**
```
Expected Result: 4
```

---

### Question 2: Sum and Product of Tuple
```python
numbers = (1, 2, 4, 2, 6)
sum_numbers = sum(numbers)
product = 1
for n in numbers:
    product *= n
print("Sum is:", sum_numbers)
print("Product is:", product)
```
**Sample Output:**
```
Sum is: 15
Product is: 96
```

---

### Question 3: Largest Number in List
```python
numbers = [1, 2, 4, 2, 6]
largest = max(numbers)
print("Largest number is:", largest)
```
**Sample Output:**
```
Largest number is: 6
```

---

### Question 4: Remove Empty Tuples
```python
L = [(), ('',), ('a', 'b'), (), ('a', 'b', 'c'), (), ('d',)]
result = [t for t in L if t]
print("Result:", result)
```
**Sample Output:**
```
Result: [('',), ('a', 'b'), ('a', 'b', 'c'), ('d',)]
```

---

### Question 5: Dictionary of Squares
```python
n = int(input("Enter a number: "))
d = {}
for x in range(1, n + 1):
    d[str(x)] = x * x
print(d)
```
**Sample Output:**
```
Enter a number: 4
{'1': 1, '2': 4, '3': 9, '4': 16}
```

---

### Question 6: Number to Words
```python
num = input("Enter a number: ")
words = {
    '0': 'Zero', '1': 'One', '2': 'Two', '3': 'Three', '4': 'Four',
    '5': 'Five', '6': 'Six', '7': 'Seven', '8': 'Eight', '9': 'Nine'
}
for digit in num:
    print(words[digit], end=' ')
```
**Sample Output:**
```
Enter a number: 43
Four Three
```

---

## 👨‍💻 Author
- **Shaheer Ahmad**  
- Roll No: 23-CYS-009  
- Department of Cyber Security, HITEC University, Taxila

