
From the directory where this file(readme.txt) is present, run the following command - 

	docker run -it -p 8888:8888 -v "${PWD}":/home/jovyan/work quay.io/jupyter/pyspark-notebook:spark-3.5.2

This will launch the pyspark notebook environment on 8888 port.

You might also need to add additional jars to spark jars folder. This can be done via login into terminal as root in docker container

docker exec -u root -it <containerid> bash

cd /usr/local/spark/jars
wget https://repo1.maven.org/maven2/org/apache/iceberg/iceberg-spark-runtime-3.5_2.12/1.9.0/iceberg-spark-runtime-3.5_2.12-1.9.0.jar

Restart kernel if needed.
