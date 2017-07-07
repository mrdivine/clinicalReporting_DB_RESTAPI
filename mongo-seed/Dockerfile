FROM mongo

COPY clinical_reporting_db_dump_noNaN.json /clinical_reporting_db_dump_noNaN.json
CMD mongoimport --host mongodb --db clinical_reporting --collection biograph_genes --type json --file /clinical_reporting_db_dump_noNaN.json --drop
