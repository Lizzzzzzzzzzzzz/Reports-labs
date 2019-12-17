~~~~
                                                    Лабораторна робота №4     

Автор:Прохорчук Дмитро Сергійович
Група:ІПЗ-13
Варіант:18

                                           Завдання

18.	Визначте загальну кількість слів у тексті, загальну кількість різних слів (без повторів) та кількість унікальних слів, що зустрічаються тільки один раз. Знайдіть найкоротше слово в тексті



print("Визначити загальну кількість слів у тексті - 1")
print("Визначити загальну кількість різних слів - 2")
print("Визначити кількість унікальних слів - 3")
print("Визначити найкоротше слово у тексті - 4")

def first(text):
    s = text.split()
    l = len(s)
    print(l)
    return l

def second(text):
    s = text.split()
    s = set(s)
    l = len(s)
    print(l)
    return l

def third(text):
    word_list = text.split()

    from collections import defaultdict
    word_count_dict = defaultdict(int)

    for word in word_list:
        word_count_dict[word] += 1

    lis = []
    for key, value in word_count_dict.items():
        if value == 1:
            lis.append(key)

    print(lis)


def fourth(text):
    s = text.split()
    idLongestWord = 0
    for i in range(1, len(s)):
        if len(s[idLongestWord]) > len(s[i]):
            idLongestWord = i
    return s[idLongestWord]

com = (input("Введіть номер команди"))
text = str(input("Введіть текст"))

if com == "1":
    print(first(text))
elif com == "2":
    print(second(text))
elif com == "3":
    print(third(text))
elif com == "4":
    print(fourth(text))



~~~~
                                            
                                            