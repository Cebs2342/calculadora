print("\033[34m""calculadora.")

def suma(num1, num2):
    return num1 + num2

def resta(num1, num2):
    return num1 - num2

def multiplicacion(num1, num2):
    return num1 * num2

def division(num1, num2):
    return num1 / num2
#agregamos un bucle que solo nos deja elegir las 5 opciones
while True:
    # Menú principal
    print("\033[37m""Por favor, elige una operación:")
    print("\033[37m""1. Suma")
    print("\033[37m""2. Resta")
    print("\033[37m""3. Multiplicación")
    print("\033[37m""4. División")
    print("\033[37m""5. Salir")
#Que opcion quieres elegir
    opcion = input("\033[32m""Ingresa una opción (1/2/3/4/5): ")
#Damos los resultados segun la opcion que se tomo
    if opcion == '5':
        print("¡Hasta luego!")
        break

    elif opcion in ['1', '2', '3', '4']:
        while True:
            try:
                num1 = float(input("Ingresa el primer número: "))
                num2 = float(input("Ingresa el segundo número: "))
                break
            except ValueError:
                print("\033[37m""Error: Ingresa un número válido.")

        if opcion == '1':
            print(num1, "+", num2, "=", suma(num1, num2))

        elif opcion == '2':
            print(num1, "-", num2, "=", resta(num1, num2))

        elif opcion == '3':
            print(num1, "*", num2, "=", multiplicacion(num1, num2))

        elif opcion == '4':
            if num2 != 0:
                print(num1, "/", num2, "=", division(num1, num2))
            else:
                print("\033[31m""Error no se puede una División por cero")

    else:
        print("\033[31m"" Opción inválida. Por favor, elige una opción válida.")
