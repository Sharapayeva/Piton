# Удалить в списке все числа, которые повторяются более двух раз.
# Найти подмножество данного множества чисел такое,
# что сумма его элементов равна заданному числу.

import random

n = int(input('Укажите размер списка: '))
A = [random.randint(0, 20) for _ in range(n)]
list_elements = []
print(f'A: {A}')
for i in range(0, len(A) - 1):
    for j in range(i + 1, len(A)):
        if A[i] == A[j]:
            list_elements.append(A[i])
for i in range(len(list_elements)):
    for j in range(len(A) - 1, -1, -1):
        if A[j] == list_elements[i]:
            A.pop(j)
# print(list_elements)
print(f'A: {A}')
list_elements2 = []
m = int(input('Укажите число: '))
for i in range(0, len(A) - 1):
    list_elements2.clear()
    list_elements2.append(A[i])
    for j in range(i + 1, len(A)):
        if A[i] + A[j] == m:
            list_elements2.append(A[j])
            print(list_elements2)

