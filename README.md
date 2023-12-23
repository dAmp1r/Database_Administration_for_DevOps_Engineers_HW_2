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

Задание 4.

Задание 5.

Задание 6.
