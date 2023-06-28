# Usage

`docker-compose up --build`

`docker-compose exec pg_master psql -U postgres`

`create table test_table (id integer) ;`

`insert into test_table (id) values (1000) ;`

`select * from test_table ;`

`\q`

`exit`

`docker-compose exec pg_slave psql -U postgres`

`select * from test_table ;`

Результаты select должны быть идентичными в master и slave базах

и еще insert into запрос в  slave базе должен возращать ошибку, так как это только на чтение. 
