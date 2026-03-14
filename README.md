# Essential-of-Artificial-Intelligence

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


# Lab 03 -Python-Functions

````

### Question 1: Factorial of a Number
 
def factorial(n):
    if n < 0:
        return "Factorial not defined"
    fact = 1
    for i in range(1, n + 1):
        fact *= i
    return fact

num = int(input("Enter a number: "))
print("Factorial:", factorial(num))
````

**Sample Output**

```
Enter a number: 5
Factorial: 120
```

---

### Question 2: Unique Elements from List

```python
def unique_list(lst):
    unique = []
    for item in lst:
        if item not in unique:
            unique.append(item)
    return unique

sample_list = [1,2,3,3,4,4,5,3,7,5]
print("Unique List:", unique_list(sample_list))
```

**Sample Output**

```
Unique List: [1, 2, 3, 4, 5, 7]
```

---

### Question 3: First n Even Numbers with Sum and Product

```python
def even_numbers(n):
    evens = []
    for i in range(1, n + 1):
        evens.append(i * 2)
    return evens

def sum_product(numbers):
    s = sum(numbers)
    p = 1
    for i in numbers:
        p *= i
    return s, p

n = int(input("Enter value of n: "))
evens = even_numbers(n)
print("Even Numbers:", evens)

s, p = sum_product(evens)
print("Sum:", s)
print("Product:", p)
```

**Sample Output**

```
Enter value of n: 5
Even Numbers: [2, 4, 6, 8, 10]
Sum: 30
Product: 3840
```

---

### Question 4: Match Two Strings

```python
def match_strings(str1, str2):
    if str1 == str2:
        return "Strings are matched"
    else:
        return "Strings are not matched"

s1 = input("Enter first string: ")
s2 = input("Enter second string: ")

print(match_strings(s1, s2))
```

**Sample Output**

```
Enter first string: hello
Enter second string: hello
Strings are matched
```

---

### Question 5: User Login System

```python
def login():
    username = "admin"
    password = "1234"

    user = input("Enter username: ")
    pwd = input("Enter password: ")

    if user == username and pwd == password:
        print("Login Successful")
    else:
        print("Invalid username or password")

login()
```

**Sample Output**

```
Enter username: admin
Enter password: 1234
Login Successful
```

---

## Lab 04 - Object Oriented Programming in Python
### Question 1: Circle Class (Area and Perimeter)

```python
class Circle:
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.1416 * self.radius * self.radius

    def perimeter(self):
        return 2 * 3.1416 * self.radius

c = Circle(5)

print("Area:", c.area())
print("Perimeter:", c.perimeter())
```

**Sample Output**

```
Area: 78.54
Perimeter: 31.416
```

---

### Question 2: Implement pow(x,n) Without Built-in Function

```python
class Power:
    def power(self, x, n):
        result = 1
        if n >= 0:
            for i in range(n):
                result *= x
        else:
            for i in range(-n):
                result *= x
            result = 1 / result
        return result

p = Power()

print(p.power(2,3))
print(p.power(2,-2))
```

**Sample Output**

```
8
0.25
```

---

### Question 3: Star Pattern

```python
def pattern(n):
    for i in range(1, n+1):
        print("*" * i)

pattern(5)
```

**Sample Output**

```
*
**
***
****
*****
```

---

### Task: Employee Management System (Inheritance)

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age


class Job:
    def __init__(self, designation, salary):
        self.designation = designation
        self.salary = salary


class Employee(Person, Job):
    def __init__(self, name, age, designation, salary):
        Person.__init__(self, name, age)
        Job.__init__(self, designation, salary)

    def display(self):
        print("Name:", self.name)
        print("Age:", self.age)
        print("Designation:", self.designation)
        print("Salary:", self.salary)


emp = Employee("Shaheer Ahmad", 22, "Cyber Security Intern", 50000)
emp.display()
```

**Sample Output**

```
Name: Shaheer Ahmad
Age: 22
Designation: Cyber Security Intern
Salary: 50000
```

---

## 👨‍💻 Author

* **Shaheer Ahmad**
* Roll No: 23-CYS-009
* Department of Cyber Security
* HITEC University, Taxila



