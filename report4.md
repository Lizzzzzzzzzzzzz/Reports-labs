
~~~~
                                                    Лабораторна робота №4     

Автор:Прохорчук Дмитро Сергійович
Група:ІПЗ-13
Варіант:18
~~~~
                                                          Завдання
~~~~
18.Обчислити значення функції у, розвинувши функцію sh(x) у ряд Тейлора. Аргумент х 
змінюється від -2 до 2 з кроком 0.5. Визначити похибку y 
~~~~                                                                                



![схема  до завдання]()

~~~~
import math

def fact(n):
    factorial = 1
    while n > 1:
        factorial *= n
        n -= 1
    return factorial;

def sinh(x):
    acc = float(input("Введіть точність"))
    sum = x
    item = x #елемент ряду
    i = 2 #счетчик цикла
    n = 1
    while abs(item) > acc:
        item *= (x**(2*n+1)) / fact (2*n+1)
        sum += item
        i += 2
    return sum

arg = float(input("Введіть значення аргументу"))
count = -2
x = 1

while (count <=  0):
    res = sinh(3*arg) + sinh(arg)
    print(res)
    print(math.sin(arg))
    count += 0.5

while (count <= 2):
    res = sinh(arg) / sinh(arg**arg)
    print(res)
    print(math.sin(arg))
    count += 0.5
~~~~    

                                                    Текстові данні                                                    
~~~~
   

                                                    Тестування 
import unittest
from laba4 import sinh as sh


class TestSinh(unittest.TestCase):
    def test_sinh(self):
        self.assertEqual(sh(1.3), 0.966184951612734)
        self.assertEqual(sh(2.15), 0.8368987907984977)


if __name__ == '__main__':
    unittest.main()

Ran 2 test in 3.489s

OK