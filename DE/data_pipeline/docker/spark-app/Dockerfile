FROM bde2020/spark-python-template:3.3.0-hadoop3.3
	  
ENV ENABLE_INIT_DAEMON=false

RUN wget https://repo1.maven.org/maven2/org/apache/hadoop/hadoop-aws/3.3.2/hadoop-aws-3.3.2.jar \
&& wget https://repo1.maven.org/maven2/com/amazonaws/aws-java-sdk-bundle/1.11.1026/aws-java-sdk-bundle-1.11.1026.jar \
&& wget https://repo1.maven.org/maven2/org/postgresql/postgresql/9.4.1207/postgresql-9.4.1207.jar \
&& mv hadoop-aws-3.3.2.jar /spark/jars/ \
&& mv aws-java-sdk-bundle-1.11.1026.jar /spark/jars/ \
&& mv postgresql-9.4.1207.jar /spark/jars/

COPY ./loaders.py /app
ENV SPARK_APPLICATION_PYTHON_LOCATION=/app/loaders.py