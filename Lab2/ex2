# 1. В матрице найти номер строки, сумма чисел в которой максимальна.

import random
import numpy as np
def randList():
    return [random.randint(0, 5) for _ in range(5)]
A = np.array([randList(),
              randList(),
              randList(),
              randList()])
maxrow_index = 0
maxSum = sum(A[0])
for i in range(1, len(A)):
    #print(sum(A[i]))
    if sum(A[i]) > maxSum:
        maxrow_index = i
        maxSum = sum(A[i])

print(A)
print(f"Строка с максимальной суммой чисел: {maxrow_index+1}, сумма: {maxSum}")
