# Домашнее задание к занятию «Базы данных» Фадеев Михаил

---
### Легенда

Заказчик передал вам [файл в формате Excel](https://github.com/netology-code/sdb-homeworks/blob/main/resources/hw-12-1.xlsx), в котором сформирован отчёт. 

На основе этого отчёта нужно выполнить следующие задания.

### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:

- какие данные хранятся в этих таблицах;
- какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

Приведите решение к следующему виду:

Сотрудники (

- идентификатор, первичный ключ, serial,
- фамилия varchar(50),
- ...
- идентификатор структурного подразделения, внешний ключ, integer).

### Решение:

Сотрудники (

идентификатор, первичный ключ, serial,

фамилия varchar(50),

имя varchar(50),

отчество varchar(50),

дата найма date,

идентификатор адреса, внешний ключ, integer,

идентификатор структурного подразделения, внешний ключ, integer,

идентификатор проекта, integer)/

---

Адрес (

идентификатор, первичный ключ, serial,

идентификатор субъекта, внешний ключ, integer,

идентификатор города, integer,

Адрес varchar(50))



Субъект(

идентификатор, первичный ключ, serial,

Субъект varchar(100))



Город(

идентификатор, первичный ключ, serial,
Город varchar(50))



Должность (

идентификатор, первичный ключ, serial,

Должность varchar(50),

Описание varchar(50),

идентификатор проекта, внешний ключ, integer)

Структурное подразделение (

идентификатор, первичный ключ, serial,

Подразделение varchar(50),

Описание varchar(50),

идентификатор должности, внешний ключ, integer,

идентификатор тип подразделения, внешний ключ, integer)



Тип подразделения (

идентификатор, первичный ключ, serial,

Тип подразделения varchar(50),

идентификатор структурного подразделения, внешний ключ, integer)



Проект (

идентификатор, первичный ключ, serial,

Проект varchar(100))



Оклад (

идентификатор сотрудника, внешний ключ, integer,

идентификатор должности, внешний ключ, integer,

оклад float)


