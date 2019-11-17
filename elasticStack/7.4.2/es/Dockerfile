FROM elasticsearch:7.4.2

ENV PLUGIN_IK_VERSION="7.4.2" \
    PLUGIN_IK_PATH=/usr/share/elasticsearch/plugins/ik

RUN yum install unzip -y \
    && curl -o /tmp/es-ik.zip https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v${PLUGIN_IK_VERSION}/elasticsearch-analysis-ik-${PLUGIN_IK_VERSION}.zip -L \
    && mkdir -p ${PLUGIN_IK_PATH} \
    && unzip /tmp/es-ik.zip -d ${PLUGIN_IK_PATH} \
    && rm -f /tmp/es-ik.zip


