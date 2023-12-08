import sympy as sp

def integrate_expression():
    # Define the symbolic variable
    x = sp.symbols('x')

    # Ask the user to input a mathematical expression
    expression_str = input("Enter a mathematical expression in terms of 'x': ")

    try:
        # Parse the input expression into a symbolic expression
        expr = sp.sympify(expression_str)

        # Ask for the lower and upper limits of the definite integral
        a = float(input("Enter the lower limit of the integral: "))
        b = float(input("Enter the upper limit of the integral: "))

        # Calculate the definite integral
        definite_integral = sp.integrate(expr, (x, a, b), manual=True)

        # Display the result
        print("The definite integral of the expression is:")
        sp.pprint(definite_integral)

    except (sp.SympifyError, TypeError):
        print("Invalid input. Please enter a valid mathematical expression.")

if __name__ == "__main_2_":
    integrate_expression()
