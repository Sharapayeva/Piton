"""
3	Даны три числа a, b и c. Найти среднее геометрическое этих чисел,
если все они отличны от нуля, и среднее арифметическое в противном случае.
"""
import random

arr = [random.randint(0, 10) for _ in range(3)]
haveZeroValue = False
print(arr)
for i in range(len(arr)):
    if arr[i] == 0:
        haveZeroValue = True
        break
if haveZeroValue:
    sum = 0
    for i in range(len(arr)):
        sum += arr[i]
    avg = sum / len(arr)
    print(f'Среднее арифметическое: {avg}')
else:
    mlt = 1
    for i in range(len(arr)):
        mlt *= arr[i]
    avg = mlt ** (1 / len(arr))
    print(f'Среднее геометрическое: {avg}')
