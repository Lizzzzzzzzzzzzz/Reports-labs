~~~~
                                               Лабораторна робота 5
Автор:Прохорчук Дмитро Сергійович
Група:ІПЗ-13
Варіант:18

                                               
                                          Завдання

18.	Обчислити ланцюговий дріб використавши рекурсію. Обчислити глибину рекурсії


def fraction(x, maxi=0x100):
    def recur(i):
        count = 0
        count += 1 
        return x**2 + (i / recur(i << 1) if i <= maxi else 0)

    return x / recur(2)

print(fraction(2))
~~~~  
