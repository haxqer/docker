FROM logstash:7.4.2

ENV LIB_MYSQL_VERSION="8.0.18" \
    LIB_PATH="/usr/share/logstash/logstash-core/lib/jars"

RUN curl -o ${LIB_PATH}/mysql-connector-java-${LIB_MYSQL_VERSION}.jar https://repo1.maven.org/maven2/mysql/mysql-connector-java/${LIB_MYSQL_VERSION}/mysql-connector-java-${LIB_MYSQL_VERSION}.jar


