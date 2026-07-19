# dictionary-assignment
dictionary assignment
# ==========================================
# Question 1 — Student Profile System
# ==========================================

student = {
    "name": "Ali",
    "age": 20,
    "city": "Karachi",
    "hobbies": ["Reading", "Cricket", "Gaming"],
    "skills": ["Python", "MS Office", "Communication"]
}

print("===== Question 1 =====")
print("Student Name:", student["name"])
print("First Hobby:", student["hobbies"][0])
print("Total Skills:", len(student["skills"]))


# ==========================================
# Question 2 — Student Marks System
# ==========================================

marks = {
    "math": 85,
    "english": 78,
    "science": 90,
    "computer": 88
}

print("\n===== Question 2 =====")
print("Math:", marks["math"])
print("English:", marks["english"])
print("Science:", marks["science"])
print("Computer:", marks["computer"])

total = sum(marks.values())
average = total / len(marks)

print("Total Marks:", total)
print("Average Marks:", average)


# ==========================================
# Question 3 — Grade Checking System
# ==========================================

print("\n===== Question 3 =====")

if average >= 80:
    grade = "A"
elif average >= 70:
    grade = "B"
elif average >= 60:
    grade = "C"
else:
    grade = "Fail"

print("Final Grade:", grade)

if average >= 60:
    print("Status: Passed")
else:
    print("Status: Failed")


# ==========================================
# Question 4 — Attendance Management System
# ==========================================

attendance = {
    "total_classes": 100,
    "attended_classes": 82
}

print("\n===== Question 4 =====")

attendance_percentage = (attendance["attended_classes"] / attendance["total_classes"]) * 100

print("Attendance Percentage:", attendance_percentage, "%")

if attendance_percentage < 75:
    print("Short Attendance")
else:
    print("Eligible For Exam")


# ==========================================
# Question 5 — Fee Management System
# ==========================================

student["fee_paid"] = True

print("\n===== Question 5 =====")

if student["fee_paid"]:
    print("Fee Cleared")
else:
    print("Fee Pending")


# ==========================================
# Question 6 — Skills Management System
# ==========================================

print("\n===== Question 6 =====")

student["skills"].append("Graphic Designing")
student["skills"].remove("MS Office")

print("Updated Skills:", student["skills"])
print("Total Skills:", len(student["skills"]))


# ==========================================
# Question 7 — Login Authentication System
# ==========================================

login = {
    "username": "admin",
    "password": "12345"
}

print("\n===== Question 7 =====")

username = input("Enter Username: ")
password = input("Enter Password: ")

if username == login["username"] and password == login["password"]:
    print("Login Successful")
else:
    print("Invalid Credentials")


# ==========================================
# Question 8 — Address Management System
# ==========================================

student["address"] = {
    "area": "Gulshan",
    "street": "Street 5",
    "house_number": "A-123"
}

print("\n===== Question 8 =====")

print("Complete Address:")
print(
    student["address"]["house_number"],
    student["address"]["street"],
    student["address"]["area"]
)

student["address"]["area"] = "North Nazimabad"
student["address"]["zip_code"] = "74700"

print("Updated Address:", student["address"])


# ==========================================
# Question 9 — Multiple Students Database
# ==========================================

students = {
    "student1": {
        "name": "Ali",
        "city": "Karachi",
        "marks": 450
    },
    "student2": {
        "name": "Ahmed",
        "city": "Lahore",
        "marks": 470
    }
}

print("\n===== Question 9 =====")

print("Student1 Name:", students["student1"]["name"])
print("Student2 Marks:", students["student2"]["marks"])

students["student2"]["city"] = "Islamabad"

print("Updated Student2 City:", students["student2"]["city"])


# ==========================================
# Question 10 — Final Student Report Card System
# ==========================================

print("\n===================================")
print("      STUDENT REPORT CARD")
print("===================================")

print("Name:", student["name"])
print("Age:", student["age"])
print("City:", student["city"])

print("\nMarks")
for subject, mark in marks.items():
    print(subject.capitalize(), ":", mark)

print("\nTotal:", total)
print("Average:", average)
print("Grade:", grade)

print("\nAttendance:", round(attendance_percentage, 2), "%")

if attendance_percentage >= 75:
    print("Attendance Status: Eligible For Exam")
else:
    print("Attendance Status: Short Attendance")

if student["fee_paid"]:
    print("Fee Status: Fee Cleared")
else:
    print("Fee Status: Fee Pending")

print("\nSkills:", student["skills"])

print("\nAddress:")
for key, value in student["address"].items():
    print(key.capitalize(), ":", value)

print("\n===================================")
print("End of Report Card")
print("===================================")
