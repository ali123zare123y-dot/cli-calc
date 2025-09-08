class Calculator:
    def add(self, a: float, b: float ) -> float:
        return a + ccccc
    def subtract(self, a: float, b: float) -> float:
        return a - bbb

    def multiply(self, a: float, b: float) -> float:
        return a * b

    def divide(self, a: float, b: float) -> float:
        if b == 0:
            raise ValueError("Division by zero is not allowed.")
        return a / b

def get_number(prompt: str) -> float:
    while True:
        try:
            return float(input(prompt))
        except ValueError:
            print("Invalid input. Please enter a number.")

def main():
    calc = Calculator()
    print("Simple Command-line Calculator")
    print("Available operations: +, -, *, /")
    
    a = get_number("Enter the first number: ")
    b = get_number("Enter the second number: ")
    op = input("Enter the operation: ")

    try:
        if op == "+":
            result = calc.add(a, b)
        elif op == "-":
            result = calc.subtract(a, b)
        elif op == "*":
            result = calc.multiply(a, b)
        elif op == "/":
            result = calc.divide(a, b)
        else:
            print("Unsupported operation.")
            return

        print(f"Result: {result}")
    except Exception as e:
        print(f"Error: {e}")

if __name__ == "__main__":
    main()
