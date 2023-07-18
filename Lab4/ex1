# Kласс Airline:
# Пункт назначения,
# Номер рейса,
# Тип самолета,
# Время вылета,
# Дни недели.
# Функции- члены реализуют запись и считывание полей (проверка корректности).
# Создать список объектов. Вывести:
# a) список рейсов для заданного пункта назначения;
# б) список рейсов для заданного дня недели;.
import prettytable


class Airline:
    __airline_name = "BUTTERFLY"

    def __init__(self, aircraft_type, destination, flight_number,
                 departure_time, days_of_the_week):
        self.__aircraft_type = aircraft_type
        self.__destination = destination
        self.__flight_number = flight_number
        self.__departure_time = departure_time
        self.__days_of_the_week = days_of_the_week

    def get_destination(self):
        return self.__destination

    def set_destination(self, destination):
        self.__destination = destination
        return

    def get_flight_number(self):
        return self.__flight_number

    def set_flight_number(self, flight_number):
        self.__flight_number = flight_number
        return

    def get_aircraft_type(self):
        return self.__aircraft_type

    def set_aircraft_type(self, aircraft_type):
        self.__aircraft_type = aircraft_type
        return

    def get_departure_time(self):
        return self.__departure_time

    def set_departure_time(self, departure_time):
        self.__departure_time = departure_time
        return

    def get_days_of_the_week(self):
        return self.__days_of_the_week

    def set_days_of_the_week(self, days_of_the_week):
        self.__days_of_the_week = days_of_the_week
        return

    @staticmethod
    def change_airline_name(new_name):
        Airline.__airline_name = new_name

    @classmethod
    def airline_test(cls):
        test = cls("test", "test", 111, "00.00",
                   {"Пн": False, "Вт": False, "Ср": False, "Чт": False, "Пт": False, "Сб": False, "Вс": False})
        return test

    def days(self):
        str_days = ""
        for i in self.get_days_of_the_week():
            if self.get_days_of_the_week()[i] and str_days.__eq__(""):  # чтобы избежать запятой вначале
                str_days = i
            elif self.get_days_of_the_week()[i]:
                str_days = str_days + "," + i
        return str_days

    def __str__(self):
        return f"Пункт назначения: {self.__destination}\n" \
               f"Номер рейса: {self.__flight_number}\n" \
               f"Тип самолета: {self.__aircraft_type}\n" \
               f"Время вылета: {self.__departure_time}\n" \
               f"Дни недели: {self.days()} "

    def __gt__(self, other):
        return self.__departure_time > other.__departure_time

    def __lt__(self, other):
        return self.__departure_time < other.__departure_time

    def __eq__(self, other):
        return self.__departure_time == other.__departure_time

    def __ne__(self, other):
        return self.__departure_time != other.__departure_time


def set_days(flight_number):
    days = {"Пн": False, "Вт": False, "Ср": False, "Чт": False, "Пт": False, "Сб": False, "Вс": False}
    print(f"В какие дни недели состоятся вылеты рейса {flight_number}? Ввводите \"Y\" или \"N\"")
    for i in days:
        flag = True
        while flag:
            answer = str(input(f"День недели {i}:")).upper()
            if answer == "Y":
                days[i] = True
                flag = False
            elif answer == "N":
                days[i] = False
                flag = False
            else:
                print("Повторите ввод: ")
    return days


def all_days():
    return {"Пн": True, "Вт": True, "Ср": True, "Чт": True, "Пт": True, "Сб": True, "Вс": True}


def weekend_days():
    return {"Пн": False, "Вт": False, "Ср": False, "Чт": False, "Пт": False, "Сб": True, "Вс": True}


# некоррекно работает в этом случае: вызываются все методы, независимо от n
# def switch(n):
#     switcher = {1: all_flight(flight_list), 4: end()}
#     return switcher.get(n, "Значение некорректно")


def all_flight(list):
    table = prettytable.PrettyTable(["Пункт назначения", "Номер рейса", "Тип самолета", "Время вылета", "Дни недели"])

    for i in list:
        table.add_row([str(i.get_destination()), str(i.get_flight_number()), str(i.get_aircraft_type()),
                       str(i.get_departure_time()), str(i.days())])
    print(table)
    return True


def flight_in_destination(list):
    table = prettytable.PrettyTable(["Пункт назначения", "Номер рейса", "Тип самолета", "Время вылета", "Дни недели"])
    destination = str(input("Введите город назначения"))
    for i in list:
        if i.get_destination().upper().__eq__(destination.upper()):
            table.add_row([str(i.get_destination()), str(i.get_flight_number()), str(i.get_aircraft_type()),
                           str(i.get_departure_time()), str(i.days())])
    print(table)
    return True


def flight_in_days(list):
    table = prettytable.PrettyTable(["Пункт назначения", "Номер рейса", "Тип самолета", "Время вылета", "Дни недели"])

    flag = True
    while flag:
        day = str(input("Введите день недели (\"Пн\", \"Вт\", \"Ср\", \"Чт\", \"Пт\", \"Сб\", \"Вс\")")).upper()
        if day in ["ПН", "ВТ", "СР", "ЧТ", "ПТ", "СБ", "ВС"]:
            day = str(day[0].upper()) + str(day[1].lower())
            for i in list:
                if i.get_days_of_the_week()[day]:
                    table.add_row([str(i.get_destination()), str(i.get_flight_number()), str(i.get_aircraft_type()),
                                   str(i.get_departure_time()), str(i.days())])
            print(table)
            flag = False
        else:
            print("Повторите ввод")
    return True


def end():
    print("By by")
    return False


if __name__ == '__main__':

    flight_list = []
    # flight_list.append(Airline("BOEING", "Vilnus", 1111, "12.00", set_days(1111)))
    flight_list.append(Airline("BOEING", "Vilnus", 2222, "13.00", weekend_days()))
    flight_list.append(Airline("BOEING", "Vilnus", 3333, "14.00", all_days()))
    flight_list.append(Airline("BOEING", "Warshaw", 1122, "12.00", all_days()))
    flight_list.append(Airline("BOEING", "Warshaw", 2232, "13.00", weekend_days()))
    flight_list.append(Airline("BOEING", "Warshaw", 3323, "14.00", all_days()))
    # print(flight_list[0])

    flag = True
    while flag:
        try:
            print("1. Просмотреть все рейсы")
            print("2. Проверить рейсы по пункту назначения")
            print("3. Проверить рейсы по дню недели")
            print("4. Закончить работу")
            select = int(input("Выберите пункт меню_ "))
            # flag = switch(select)
            if select == 1:
                all_flight(flight_list)
            elif select == 2:
                flight_in_destination(flight_list)
            elif select == 3:
                flight_in_days(flight_list)
            elif select == 4:
                # print(flight_list[0] > flight_list[1])
                end()
                flag = False
            else:
                print("Такого пункта меню нет")
        except:
            print("Некорректный ввод")
