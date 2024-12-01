# Домашнее задание по теме "Зачем нужно наследование"

Если вы решали старую версию задачи, проверка будет производиться по ней.

Ссылка на старую версию [тут](https://docs.google.com/document/d/1VXN2VXriHikKE3KBOmGvhw50lgEFcI4Oa6oUr9YXGWA/edit?usp=sharing).

Цель: применить базовые знания о наследовании классов для решения задачи

# Задача "Съедобное, несъедобное":

Разнообразие животного мира давно будоражит умы человечества. Царства,
классы, виды... Почему бы и нам не попробовать выстроить что-то подобное
используя наследования классов?

Необходимо описать пример иерархии животного мира, используя классы и
принцип наследования.

Создайте:

2 класса родителя: Animal, Plant
Для класса Animal атрибуты alive = True (живой) и fed =
False (накормленный), name - индивидуальное название каждого животного.
Для класса Plant атрибут edible = False (съедобность), name -
индивидуальное название каждого растения

4 класса наследника: 
Mammal, Predator для Animal.
Flower, Fruit для Plant.

У каждого из объектов класса Mammal и Predator должны быть атрибуты и
методы:
eat(food) - метод, где food - это параметр, принимающий объекты классов
растений.

Метод eat должен работать следующим образом:

Если переданное растение (food) съедобное - выводит на экран "<self.name>
съел <food.name>", меняется атрибут fed на True.

Если переданное растение (food) не съедобное - выводит на экран
"<self.name> не стал есть <food.name>", меняется атрибут alive на False.
Т.е если животному дать съедобное растение, то животное насытится, если не
съедобное - погибнет.

У каждого объекта Fruit должен быть атрибут edible = True (переопределить
при наследовании)

Создайте объекты классов и проделайте действия затронутые в примере
результата работы программы.

Пункты задачи:
1. Создайте классы Animal и Plant с соответствующими атрибутами и
   методами
2. Создайте(+унаследуйте) классы Mammal, Predator, Flower, Fruit с
   соответствующими атрибутами и методами. При необходимости
   переопределите значения атрибутов.
3. Создайте объекты этих классов.

Пример результата выполнения программы:

Выполняемый код(для проверки):
```
a1 = Predator('Волк с Уолл-Стрит')
a2 = Mammal('Хатико')
p1 = Flower('Цветик семицветик')
p2 = Fruit('Заводной апельсин')

print(a1.name)
print(p1.name)

print(a1.alive)
print(a2.fed)
a1.eat(p1)
a2.eat(p2)
print(a1.alive)
print(a2.fed)
```

\# Что произошло: Хищник попытался съесть цветок и погиб, млекопитающее
съело фрукт и насытилось.

Вывод на консоль:
```
Волк с Уолл-Стрит
Цветик семицветик
True
False
Волк с Уолл-Стрит не стал есть Цветик семицветик
Хатико съел Заводной апельсин
False
True
```

Примечания:
> 1. Помните, обращаясь к атрибутам объекта текущего класса используйте
     параметр self.
> 2. Передавая объекты классов Fruit и Flower в метод eat, так же можно
     обращаться к их атрибутам внутри.
> 3. Обращайте внимание на то, где атрибут класса, а где атрибут объекта.

Файл module_6_1.py и загрузите его на ваш GitHub репозиторий и пришлите
ссылку на него.

Успехов!
