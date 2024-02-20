import random

num = int(input('Введите количество чисел: '))
numbers = [1,2,3,4]
lst = []
end_lst = []

for i in range(num):
    ind = random.choice(numbers)
    lst.append(ind)

print(lst)

def check(lst_of_numbers,x):
    end_lst = []
    new_lst = filter(lambda num: num == x,lst)
    for i in new_lst:
        end_lst.append(i)
    return end_lst

for i in range(1,5):
    part_of_end_lst = check(lst,i)
    end_lst.append(part_of_end_lst)

print(end_lst)
