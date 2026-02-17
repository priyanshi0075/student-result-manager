import json
FILE = "students.json"

def load_data():
    try:
        with open(FILE, "r") as f:
            return json.load(f)
    except:
        return {}

def save_data(data):
    with open(FILE, "w") as f:
        json.dump(data, f, indent=4)

def add_student():
    name = input("Enter student name: ")
    marks = int(input("Enter marks: "))
    data = load_data()
    data[name] = marks
    save_data(data)
    print("Student added successfully!")

def view_students():
    data = load_data()
    if not data:
        print("No records found.")
        return
    for name, marks in data.items():
        print(f"{name}: {marks}")

while True:
    print("\n1. Add Student")
    print("2. View Students")
    print("3. Exit")
    choice = input("Enter choice: ")

    if choice == "1":
        add_student()
    elif choice == "2":
        view_students()
    elif choice == "3":
        break
    else:
        print("Invalid choice")
