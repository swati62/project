# project
 A simple calculator using python
def add(a,b):
    return a+b
def subtract(a,b):
    return a-b
def multiply(a,b):
    return a*b
def divide(a,b):
    return a/b
operator_dict={
    "+":add,
    "-":subtract,
    "*":multiply,
    "/":divide
}
choose="n"
while choose=="n":
    a=int(input("Enter first number:"))
    for symbol in operator_dict:
        print(symbol)
    choose_symbol=input("Pick an operator:")
    b=int(input("Enter next number:"))
    calculator_func=operator_dict[choose_symbol]
    result=calculator_func(a=a,b=b)
    print(f"{a}{choose_symbol}{b}={result}")
    print(f"Enter 'y' to contiune calculation with {result} or 'n' to start new calculation or 'x' to exit!")
    choose=input("")
    if choose=="y":
        a=result
        choose_symbol=input("Pick an operator:")
        b=int(input("Enter your number:"))
        calculator_func=operator_dict[choose_symbol]
        result=calculator_func(a=a,b=b)
        print(f"{a}{choose_symbol}{b}={result}")
        print(f"Enter 'y' to contiune calculation with {result} or 'n' to start new calculation or 'x' to exit!")
        choose=input("")
    elif choose=="n":
        continue
    elif choose=="x":
        break
    else:
        try_again=input("Type 'try' to try again:")
        if try_again=="try":
            continue
        else:
            break
print("thanyou!")

