# my-first-project
My first coding project
students = []

def add_student():
    name = input("Enter student name: ")
    roll = input("Enter roll number: ")
    marks = float(input("Enter marks: "))

    student = {
        "name": name,
        "roll": roll,
        "marks": marks
    }

    students.append(student)
    print("Student added successfully!")

def display_students():
    if not students:
        print("No students found.")
    else:
        for student in students:
            print("-------------------")
            print("Name:", student["name"])
            print("Roll Number:", student["roll"])
            print("Marks:", student["marks"])

while True:
    print("\n===== STUDENT MANAGEMENT SYSTEM =====")
    print("1. Add Student")
    print("2. Display Students")
    print("3. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        add_student()
    elif choice == "2":
        display_students()
    elif choice == "3":
        print("Thank you!")
        break
    else:
        print("Invalid choice!")
