class TribonacciIterator:
    def __init__(self, n):
        self.n = n
        self.current = 1
        self.a = 0
        self.b = 0
        self.c = 1
        self.lst = [self.a, self.b, self.c]

    def __iter__(self):
        return self

    def __next__(self):
        if self.current in (1, 2):
            self.current += 1
            return 0
        elif self.current == 3:
            self.current += 1
            return 1
        elif self.n >= self.current:
            x = sum(self.lst)
            self.lst[0], self.lst[1], self.lst[2] = self.lst[1], self.lst[2], x
            self.current += 1
            return x
        else:
            raise StopIteration


def tribonacciIteratorGenerator():
    a = 0
    b = 0
    c = 1
    current = 1
    while True:
        if current in (1, 2):
            current += 1
            yield 0
        elif current == 3:
            current += 1
            yield 1
        else:
            x = a + b + c
            a, b, c = b, c, x
            current += 1
            yield x


if __name__ == '__main__':
    it = TribonacciIterator(10)
    for i in it:
        print(i)
    itg = tribonacciIteratorGenerator()
    for i in range(50):
        print(f'{i+1}-й элемент последовательности: {next(itg)}')





