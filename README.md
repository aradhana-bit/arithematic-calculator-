-
-
-
-
# arithematic-calculator-




def arithmetic_calculator():
    print("=== Simple Arithmetic Calculator ===")
    print("Supported operations: +, -, *, /, ** (exponentiation)")
    
    while True:
        try:
            # Get first number
            num1 = float(input("Enter the first number: "))
            
            # Get operation
            operation = input("Enter the operation (+, -, *, /, **): ").strip()
            
            # Get second number
            num2 = float(input("Enter the second number: "))
            
            # Perform calculation based on operation
            if operation == '+':
                result = num1 + num2
            elif operation == '-':
                result = num1 - num2
            elif operation == '*':
                result = num1 * num2
            elif operation == '/':
                if num2 == 0:
                    print("Error: Division by zero is not allowed!")
                    continue
                result = num1 / num2
            elif operation == '':
                result = num1 ** num2
            else:
                print("Error: Invalid operation! Please use +, -, *, /, or **.")
                continue
            
            # Display result
            print(f"Result: {num1} {operation} {num2} = {result}")
            
            # Ask if user wants to continue
            again = input("Do you want to perform another calculation? (y/n): ").strip().lower()
            if again != 'y':
                print("Thanks for using the calculator!")
                break
                
        except ValueError:
            print("Error: Please enter valid numbers!")
        except Exception as e:
            print(f"An unexpected error occurred: {e}")

# Run the calculator
if _name_ == "_main_":
    arithmetic_calculator()
