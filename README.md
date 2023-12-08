import sympy as sp

def integrate_expression():
    # Define the symbolic variable
    x = sp.symbols('x')



       
        a = float(input("Enter the lower limit of the integral: "))
        b = float(input("Enter the upper limit of the integral: "))


        definite_integral = sp.integrate(expr, (x, a, b), manual=True)


        print("The definite integral of the expression is:")
        sp.pprint(definite_integral)

    except (sp.SympifyError, TypeError):
        print("Invalid input. Please enter a valid mathematical expression.")

if __name__ == "__main_2_":
    integrate_expression()
