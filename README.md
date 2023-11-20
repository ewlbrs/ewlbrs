# Программа "Калькулятор эмодзи"

# Описание программы
print("Калькулятор эмодзи")
print("Программа позволяет выполнять операции (+, -, *, /, **, //, %) над эмодзи")

# Функции для выполнения операций над эмодзи
# Словарь с определениями эмодзи
emojis = {
    "🐱": "кот",
    "😭": "слёзы",
    # добавьте сюда другие эмодзи и их определения
}
`

После этого можно приступить к написанию функций для операций:

```python
# Функция для сложения двух эмодзи
def add_emoji(emoji1, emoji2):
    if emoji1 in emojis and emoji2 in emojis:
        return emojis[emoji1] + " + " + emojis[emoji2]
    else:
        return "Некорректные эмодзи"

# Функция для вычитания двух эмодзи
def subtract_emoji(emoji1, emoji2):
    if emoji1 in emojis and emoji2 in emojis:
        return emojis[emoji1] + " - " + emojis[emoji2]
    else:
        return "Некорректные эмодзи"

# Функция для умножения двух эмодзи
def multiply_emoji(emoji1, emoji2):
    if emoji1 in emojis and emoji2 in emojis:
        return emojis[emoji1] + " * " + emojis[emoji2]
    else:
        return "Некорректные эмодзи"

# Функция для деления двух эмодзи
def divide_emoji(emoji1, emoji2):
    if emoji1 in emojis and emoji2 in emojis:
        return emojis[emoji1] + " / " + emojis[emoji2]
    else:
        return "Некорректные эмодзи"

# Функция для целочисленного деления двух эмодзи
def divide_floor_emoji(emoji1, emoji2):
    if emoji1 in emojis and emoji2 in emojis:
        return emojis[emoji1] + " // " + emojis[emoji2]
    else:
        return "Некорректные эмодзи"

# Функция для определения остатка от деления двух эмодзи
def modulus_emoji(emoji1, emoji2):
    if emoji1 in emojis and emoji2 in emojis:
        return emojis[emoji1] + " % " + emojis[emoji2]
    else:
        return "Некорректные эмодзи"

# Функция для возведения эмодзи в степень
def power_emoji(emoji, power):
    if emoji in emojis:
        return emojis[emoji] + " ** " + str(power)
    else:
        return "Некорректное эмодзи"
# Основная часть программы

# Запрос у пользователя эмодзи и операции
emoji1 = input("Введите первое эмодзи: ")
emoji2 = input("Введите второе эмодзи: ")
operation = input("Введите операцию (+, -, *, /, **, //, %): ")

# Выполнение операции
result = ""
if operation == "+":
    result = add_emoji(emoji1, emoji2)
elif operation == "-":
    result = subtract_emoji(emoji1, emoji2)
elif operation == "*":
    result = multiply_emoji(emoji1, emoji2)
elif operation == "/":
    result = divide_emoji(emoji1, emoji2)
elif operation == "//":
    result = divide_floor_emoji(emoji1, emoji2)
elif operation == "%":
    result = modulus_emoji(emoji1, emoji2)
elif operation == "**":
    power = int(input("Введите степень: "))
    result = power_emoji(emoji1, power)
else:
    result = "Некорректная операция"

# Вывод результата
