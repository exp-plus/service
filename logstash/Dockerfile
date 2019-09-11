FROM logstash:7.3.1
ENV VERSION = 7.3.1

#安装input插件
RUN logstash-plugin install logstash-input-jdbc
RUN logstash-plugin install logstash-filter-aggregate
RUN logstash-plugin install logstash-filter-jdbc_streaming
RUN logstash-plugin install logstash-filter-mutate
RUN logstash-plugin install logstash-output-elasticsearch

# 复制 jar 包
# MySQL Connector/J 8.0 is highly recommended for use with MySQL Server 8.0, 5.7, 5.6, and 5.5. 
COPY ./mysql-connector-java-8.0.16.jar /usr/share/logstash/mysql-connector-java.jar