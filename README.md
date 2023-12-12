import math

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return 'Error! Division by zero is not allowed'
    else:
        return x / y

def square(x):
    return x ** 2

def square_root(x):
    return math.sqrt(x)

print("Select operation:")
print("1. Addition")
print("2. Subtraction")
print("3. Multiplication")
print("4. Division")
print("5. Square")
print("6. Square Root")

while True:
    choice = input("Enter choice(1/2/3/4/5/6): ")

    if choice in ('1', '2', '3', '4', '5', '6'):
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))

        if choice == '1':
            print(num1, "+", num2, "=", add(num1, num2))

        elif choice == '2':
            print(num1, "-", num2, "=", subtract(num1, num2))

        elif choice == '3':
            print(num1, "*", num2, "=", multiply(num1, num2))

        elif choice == '4':
            print(num1, "/", num2, "=", divide(num1, num2))

        elif choice == '5':
            print(num1, "^2 =", square(num1))

        elif choice == '6':
            print("Square root of", num1, "=", square_root(num1))
            
        next_calculation = input("Do you want to continue calculation (yes/no): ")
        if next_calculation == "no":
          print("Exiting the calculator")
          break

    else:
        print("Invalid Input")
