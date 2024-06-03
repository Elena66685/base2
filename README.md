1. Создать таблицу для хранения фамилии, имени, отчества, email, логина, пароля, *роль(внешний ключ) и адреса(город)
```dtd
create table test
(
  id integer primary key autoincrement,
  name text not null,
  patronymic text not null,
  surname text not null,
  email text not null,
  login text not null,
  city text not null,
  password text not null,
  role_id integer not null,
  foreign key (role_id) references role (id)
)
```
2. Заполнить таблицу данными 5-10 записей
```dtd
INSERT INTO test (name, patronymic, surname, email, login, city, password, role_id) values
('Николай', 'Васильевич', 'Сидоров', 'fgh.mail', 'вася', 'Нижний Новгород', 'fgh', 1),
('Надежда', 'Васильевна', 'Сидорова', 'ffgnm.mail', 'надя', 'Москва', 'sdfgh', 2),
('Мария', 'Александровна', 'Белкина', 'cvbn.mail', 'белка', 'Казань', 'rtyui', 3),
('Александр', 'Валерьевич', 'Ступнев', 'asd.mail', 'кабан', 'Семенов', 'uiop', 3),
('Юлия', 'Матвеевна', 'Зуйкова', 'zxcvb.mail', 'киса', 'Городец', 'bnm', 1);
```
3. Вывести все записи из таблицы с данными пользователя
```dtd
SELECT * FROM test
```
4. Вывести только тех пользователей которые проживают в Москве
```dtd
SELECT * FROM test where city = 'Москва'
```
5. Вывести только продавцов
```dtd
SELECT * FROM test where role_id = 2
```
