# How-to

1#
How to Install PostgreSQL 9.5 on Ubuntu 16.04 and 14.04 LTS    // http://eax.me/postgresql-install/

Step 1: Add PostgreSQL Apt Repository
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ `lsb_release -cs`-pgdg main" >> /etc/apt/sources.list.d/pgdg.list'
wget -q https://www.postgresql.org/media/keys/ACCC4CF8.asc -O - | sudo apt-key add -

Step 2: Install PostgreSQL 
sudo apt-get update
sudo apt-get install postgresql postgresql-contrib

Step 3: Connect to PostgreSQL 
sudo -u postgres psql

Command:
1. Создадим тестовую базу данных и тестового пользователя:
postgres=# CREATE DATABASE test_database;
CREATE DATABASE

postgres=# CREATE USER test_user WITH password 'qwerty';
CREATE ROLE

postgres=# GRANT ALL privileges ON DATABASE test_database TO test_user;
GRANT

2.Теперь попробуем поработать с созданной базой данных от имени test_user:
psql -h localhost test_database test_user






