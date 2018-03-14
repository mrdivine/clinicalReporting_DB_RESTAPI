# clinicalReporting_DB_RESTAPI
Used docker-compose to set up the MongoDB and attached Eve REST API

command line usage is as follows:

```docker-compose run --service-ports ClinicalReportR -t /data/<VCF FILE> -p jwp```

* `-t`: input file name. This should be in the data volume of ClinicalReportR service.
* `-p`: output format to save the results.
	* `j` to save report in JSON format
	* `w` to save report in DOCX format
	* `p` to save report in PDF format

Note that ClinicalReportR and clinicalReporting_DB_RESTAPI should have the same parent directory.

To test the functionality, point your browser to the following link:

http://localhost:5000/biograph_genes?where={%22meta_information.symbol%22:%20%22EGFR%22}


have fun
