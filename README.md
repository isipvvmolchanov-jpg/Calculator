print("Категории: 1. Арифметика | 2. Сравнение | 3. Логика")

category = input("Выберите категорию (1-3): ").strip()

try:
    # ШАГ 1: АРИФМЕТИЧЕСКИЕ ОПЕРАТОРЫ
    if category == "1":
        op = input("Оператор (+, -, *, /, //, %, **): ").strip()
        n1 = float(input("Первое число: "))
        n2 = float(input("Второе число: "))

        if op in ["/", "//", "%"] and n2 == 0:
            print("Ошибка: Деление на ноль!")
        elif op == "+": print(f"Результат: {n1 + n2}")
        elif op == "-": print(f"Результат: {n1 - n2}")
        elif op == "*": print(f"Результат: {n1 * n2}")
        elif op == "/": print(f"Результат: {n1 / n2}")
        elif op == "//": print(f"Результат: {n1 // n2}")
        elif op == "%": print(f"Результат: {n1 % n2}")
        elif op == "**": print(f"Результат: {n1 ** n2}")
        else: print("Ошибка: Неверный оператор!")

    # ШАГ 2: ОПЕРАТОРЫ СРАВНЕНИЯ
    elif category == "2":
        op = input("Оператор (==, !=, >, <, >=, <=): ").strip()
        n1 = float(input("Первое число: "))
        n2 = float(input("Второе число: "))

        if op == "==": print(f"Результат: {n1 == n2}")
        elif op == "!=": print(f"Результат: {n1 != n2}")
        elif op == ">": print(f"Результат: {n1 > n2}")
        elif op == "<": print(f"Результат: {n1 < n2}")
        elif op == ">=": print(f"Результат: {n1 >= n2}")
        elif op == "<=": print(f"Результат: {n1 <= n2}")
        else: print("Ошибка: Неверный оператор!")

    # ШАГ 3: ЛОГИЧЕСКИЕ ОПЕРАТОРЫ
    elif category == "3":
        op = input("Оператор (and, or, not): ").strip().lower()

        if op == "not":
            v = input("Введите значение (True/False): ").strip().title() == "True"
            print(f"Результат: {not v}")
        elif op in ["and", "or"]:
            v1 = input("Первое значение (True/False): ").strip().title() == "True"
            v2 = input("Второе значение (True/False): ").strip().title() == "True"
            print(f"Результат: {v1 and v2 if op == 'and' else v1 or v2}")
        else: print("Ошибка: Неверный оператор!")

    else:
        print("Ошибка: Неверная категория!")

except ValueError:
    print("Ошибка: Неверный ввод данных (нужно число или True/False)!")
