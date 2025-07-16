# Student-Grades-Management-System


# # STUDENT GRADE MANAGEMENT SYSTEM

# # This project make on DIctionary.
# # Student name is Key and his Marks are Value.

# """
# What we do in this project?
# 1. Add    --->     Student name add
# 2. Update --->     Existing student name update
# 3. Delete
# # 4. View
# # 5. Exit
# # """

# # """ What is Dictinary? ---> collection - key+value = pair = data

# # left-side = key
# # right-side = value
# # {key1:value1, key2:value2}

# # """

# # # Create a dictioanry
# # student = {
# #     "Sadaqat": 200,
# #     "Daniyal": 100
# # }

# # # Accessing a element. In dictionary we use KEY for accessing and element.
# # print(student["Sadaqat"])

# # # Update
# # student["Daniyal"] = 180
# # print(student["Daniyal"])

# # # Delete
# # del student["Daniyal"]
# # print(student)



# Initialising Dictionary
student_grades = { }

# Create a function with the name of add_student
def add_student(name, grade):  # Pass the parameter name and grade as a key and value
    student_grades[name] = grade
    # [Rizy] = 100
    print(f"Added {name} with a {grade}")
    # Added Rizy with a 100

# Create a function with the name of Update_student
def update_student(name, grade):
    if name in student_grades: # Memebership operator's help check it either student availbe in dict or not?
        student_grades[name]  = grade
        # Rizy = 200  ---> for suppose 
        print(f"{name} with marks are update {grade}")
    else:
        print(f"{name} is not found!")

# Delete a Student
def delete_student(name):
    if name in student_grades:
        del student_grades[name]
        print(f"{name} has been successfully deleted")
    else:
        print(f"{name} is not found!")
        

# View All Students
def display_all_student():
    if student_grades:
        for name, grade in student_grades.items(): # we use the item() method for dictionaries data 
            print(f"{name} : {grade}")
        else:
            print("No student found/Added")
# Now we use MAIN LOGIC
def main():
    while True:
        print('\n Student Grades Management System')
        print("1. Add Student")
        print("2. Update Student")
        print("3. Delete Student")
        print("4. View Student")
        print("5. Exit")

        choice = int(input("Enter your choice = "))
        if choice == 1:
            name = input("Enter student name = ")
            grade = int(input("Enter student grade = "))
            add_student(name, grade)   # call the function

        elif choice == 2:
             name = input("Enter student name = ")
             grade = int(input("Enter student grade = "))
             update_student(name, grade)

        elif choice == 3:
             name = input("Enter student name = ")
             delete_student(name)

        elif choice == 4:
            display_all_student()

        elif choice == 5:
            print("Closing the Prograaam....")
            break

        else:
            print("Invalid choice")

if __name__ == "__main__":
    main()
