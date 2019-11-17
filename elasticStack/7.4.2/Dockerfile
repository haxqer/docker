FROM elasticsearch:7.4.2

ENV PLUGIN_IK_VERSION="7.4.2" \
    PLUGIN_IK_PATH=/usr/share/elasticsearch/plugins/ik \
    LIB_MYSQL_VERSION="8.0.18" \
    LIB_PATH="/usr/share/logstash/logstash-core/lib/jars"

RUN yum install unzip -y \
    && curl -o /tmp/es-ik.zip https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v${PLUGIN_IK_VERSION}/elasticsearch-analysis-ik-${PLUGIN_IK_VERSION}.zip -L \
    && mkdir -p ${PLUGIN_IK_PATH} \
    && unzip /tmp/es-ik.zip -d ${PLUGIN_IK_PATH} \
    && rm -f /tmp/es-ik.zip \
    && curl -o ${LIB_PATH}/mysql-connector-java-${LIB_MYSQL_VERSION}.jar https://repo1.maven.org/maven2/mysql/mysql-connector-java/${LIB_MYSQL_VERSION}/mysql-connector-java-${LIB_MYSQL_VERSION}.jar


