1) Структура, просмотр
    1)  `mysql -u username` - вход в среду mysql
    2) ==`mysql --local-infile=1 -u root -p` - запуск с возможностью импортировать данные==
    3) ==`SET GLOBAL local_infile = 1;` - решение проблемы с доступом к локальным файлам==
	4)  `CREATE DATABASE name` - создание базы данных 
	5) `USE name` - использование базы данных
	6) `CREATE TABLES sectorname (rowname type(capasity), etc...)` - создание таблиц внутри базы
	7) `SHOW TABLES` - вывод таблиц
	8) `DESCRIBE sectorname` - вывод таблицы по ее названию
2) Загрузка локальных данных 
	1) `LOAD DATA LOCAL INFILE "filename" INTO TABLE sectorname` - загрузка локального файла в сектор таблицы
	2) `SELECT * FROM sectorname` - выбрать и показать все данные из сектора
	3) `INSERT INTO sectorname (rownames...) VALUE ("name","name",...etc);` - вставка в таблицу значений в ручную (если не указано имя столбца или название в соответствующем столбце, вставится NULL)
	4) `DELETE FROM sectorname WHERE rowname="name";` - удаление из таблицы строки с определенным значением
	5) `UPDATE sectorname SET ...` - поменять файл с определенными параметрами
	6) 