import datetime

a = 0


def tribonacci(n):
    global a
    a += 1
    if n in (1, 2):
        return 0
    elif n == 3:
        return 1
    return tribonacci(n - 1) + tribonacci(n - 2) + tribonacci(n - 3)


n = 5
t1 = datetime.datetime.now()
print(f"Для числа {n} :")
print(tribonacci(n))
t2 = datetime.datetime.now()
print(str((t2 - t1).total_seconds())+" секунд")
print(f"кол-во обращений: {a}")

