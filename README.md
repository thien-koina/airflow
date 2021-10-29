# airflow
Develop ETL process in Airflow

First run to init db
```
chmod +x ./airflow.sh
./airflow.sh
```

Install Posgres
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

```
airflow db init

airflow users create \
    --username admin \
    --firstname Peter \
    --lastname Parker \
    --role Admin \
    --email spiderman@superhero.org

airflow webserver --port 8080

airflow scheduler
```