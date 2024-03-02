class Person:
    def __init__(self, name, surname, qualification=1):
        self.name = name
        self.surname = surname
        self.qualification = qualification

    def __str__(self):
        return f"Имя: {self.name}\nФамилия: {self.surname}\nКвалификация: {self.qualification}"

    def __del__(self):
        print(f"До свидания, мистер {self.name} {self.surname}.")

# Создание трех экземпляров класса Person
person1 = Person("Иван", "Иванов", 3)
person2 = Person("Петр", "Петров", 2)
person3 = Person("Сидор", "Сидоров", 1)

# Вывод информации о сотрудниках
print("Информация о сотрудниках:")
print(person1)
print(person2)
print(person3)

# Увольнение сотрудника с наименьшей квалификацией
weakest_link = min(person1, person2, person3, key=lambda person: person.qualification)
print(f"\nУвольнение самого слабого звена: {weakest_link.name} {weakest_link.surname}")
del weakest_link

# Функция input() для ожидания нажатия Enter
input()
