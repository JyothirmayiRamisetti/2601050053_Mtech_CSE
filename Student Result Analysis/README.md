# 🎓 STUDENT RESULT PROCESSING

## 📌 PROBLEM STATEMENT

A college has thousands of student marks and wants to calculate **grades, class averages, toppers, and pass percentages**.

### QUESTION

Identify the smaller computational tasks involved and explain how you would decompose the problem.

---

# 💡 SOLUTION

The appropriate Computational Thinking method for this problem is **Decomposition**.

## 🔹 What is Decomposition?

**Decomposition** means breaking a large and complex problem into **smaller, simple, and manageable tasks**.

Each smaller task can be solved separately to obtain the final solution.

---

# 📝 EXAMPLE

Suppose there are **3 students** with their marks:

| STUDENT | MATHS | SCIENCE | ENGLISH |
|---------|------:|--------:|--------:|
| A | 80 | 70 | 90 |
| B | 60 | 65 | 70 |
| C | 90 | 95 | 85 |

---

# 🔨 APPLY DECOMPOSITION

We break the large result-processing problem into smaller tasks:

### Task 1
Enter the marks of each student.

### Task 2
Calculate total marks.

### Task 3
Calculate percentage and assign grades.

### Task 4
Calculate the class average.

### Task 5
Compare marks and find the topper.

### Task 6
Count passed students and calculate pass percentage.

---

# 📊 RESULTS

- **Student A Total = 240**
- **Student B Total = 195**
- **Student C Total = 270**
- **Topper = Student C**
- **Class Average = 235 marks**
- **Pass Percentage = 100%**

---

# ⚙️ ALGORITHM

### Step 1
Start.

### Step 2
Enter student marks.

### Step 3
Calculate total and percentage.

### Step 4
Assign grades.

### Step 5
Check pass/fail.

### Step 6
Calculate class average.

### Step 7
Find topper.

### Step 8
Calculate pass percentage.

### Step 9
Display the result.

### Step 10
Stop.

---
# 💻 PYTHON CODE

```python
students = {
    "A": [80, 70, 90],
    "B": [60, 65, 70],
    "C": [90, 95, 85]
}

totals = {}

for name, marks in students.items():

    # Calculate total and percentage
    total = sum(marks)
    percentage = total / 3

    # Assign grade
    if percentage >= 90:
        grade = "A+"
    elif percentage >= 75:
        grade = "A"
    elif percentage >= 60:
        grade = "B"
    elif percentage >= 50:
        grade = "C"
    else:
        grade = "F"

    totals[name] = total

    print(name, "Total =", total,
          "Percentage =", percentage,
          "Grade =", grade)

# Class average
average = sum(totals.values()) / len(students)

# Topper
topper = max(totals, key=totals.get)

# Pass percentage
passed = sum(total >= 150 for total in totals.values())
pass_percentage = (passed / len(students)) * 100

print("\nClass Average =", average)
print("Topper =", topper)
print("Pass Percentage =", pass_percentage, "%")


INPUT

The student marks are:
A = [80, 70, 90]
B = [60, 65, 70]
C = [90, 95, 85]

OUTPUT

A Total = 240 Percentage = 80.0 Grade = A
B Total = 195 Percentage = 65.0 Grade = B
C Total = 270 Percentage = 90.0 Grade = A+

Class Average = 235.0
Topper = C
Pass Percentage = 100.0 %

TIME COMPLEXITY

Let n = number of students.

Each student is processed once.

Time Complexity = O(n)


