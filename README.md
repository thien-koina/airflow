# airflow
Develop ETL process in Airflow

# Install Posgres
```
sudo apt update
sudo apt install postgresql postgresql-contrib
sudo -u postgres psql

CREATE ROLE ubuntu;
CREATE DATABASE airflow;
GRANT ALL PRIVILEGES on database airflow to ubuntu;
ALTER ROLE ubuntu WITH LOGIN;
ALTER ROLE ubuntu SUPERUSER;
ALTER ROLE ubuntu CREATEDB;
GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA public to ubuntu;
```

# Init Database
```
airflow db init

airflow users create \
    --username admin \
    --firstname Thien \
    --lastname Pham \
    --role Admin \
    --email thienph3@gmail.com

airflow webserver --port 8080

airflow scheduler

airflow celery worker
```