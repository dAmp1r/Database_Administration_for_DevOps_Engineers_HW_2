# Database_Administration_for_DevOps_Engineers_HW_2

*SQL - Горубнов Д.Н.*

Задание 1.
```
version: '3.7'

services:
  postgres:
    image: postgres:12
    environment:
      - POSTGRES_PASSWORD=postgres
      - POSTGRES_PASSWORD=admin
    volumes: 
      - /home/gorbunov/hw_sql/db:/var/lib/postgres/data
      - /home/gorbunov/hw_sql/backup:/var/postgres_backup
    ports: 
      - 5432:5432

```
Задание 2.

- ![](https://github.com/dAmp1r/Database_Administration_for_DevOps_Engineers_HW_2/blob/main/21.png)             
- ![](https://github.com/dAmp1r/Database_Administration_for_DevOps_Engineers_HW_2/blob/main/22.png)            
  ![](https://github.com/dAmp1r/Database_Administration_for_DevOps_Engineers_HW_2/blob/main/23.png)
- ```select distinct grantee from information_schema.role_table_grants where table_catalog = 'test_db';```
- ![](https://github.com/dAmp1r/Database_Administration_for_DevOps_Engineers_HW_2/blob/main/24.png)

Задание 3.
 
```select count (*) from orders;```                            
```select count (*) from clients;```                       
![]()              

Задание 4.

- ```test_db=# update clients set order_id = '3' where id = '1';```               
- ```test_db=# update clients set order_id = '4' where id = '2';```                
- ```test_db=# update clients set order_id = '5' where id = '3';```          
- ```select last_name from clients where order_id is not null;```           
- ![]()                 
  
Задание 5.

- ![]()                              
- cost указывает время затраченое на получение первой записи и всем записей, rows - кол-во проверяемых строк, width - средний размер строки в байтах, указание применение фильтра

Задание 6.

```pg_dump -U postgres -p test_db > /var/postgres_backup/test_db.sql```
```postgres=# create user "test-admin-user" with password 'admin';```
```postgres=# create user "test-simple-user" with password 'admin';```
```postgres=# create database test_db;```
```psql -U postgres -d test_db -f test_db.sql```
![]()

