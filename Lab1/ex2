# 1 Шестизначный автобусный билет считается удачным, если сумма его цифр делится на 7.
# Могут ли два билета подряд быть удачными?

# l = list()

def sUm(x):
    sum = 0
    num = x
    while num != 0:
        sum += num % 10
        num //= 10
    return sum


for i in range(1, 1000000):
    if sUm(i) % 7 == 0 and sUm(i + 1) % 7 == 0:
        print(f'Найденная пара:   {i} & {i + 1}')
        # l.append(i)
        # l.append(i + 1)
        # l.append(' ')
# print(l)
