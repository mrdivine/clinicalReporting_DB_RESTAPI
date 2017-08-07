FROM mongo

COPY /driver_db_dump.json /driver_db_dump.json

CMD mongoimport --host mongodb --db clinical_reporting --collection biograph_genes --jsonArray --file /driver_db_dump.json --drop
