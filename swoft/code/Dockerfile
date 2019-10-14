# @description php image base on the debian 9.x
#
#                       Some Information
# ------------------------------------------------------------------------------------
# @link https://hub.docker.com/_/debian/      alpine image
# @link https://hub.docker.com/_/php/         php image
# @link https://github.com/docker-library/php php dockerfiles
# @see https://github.com/docker-library/php/tree/master/7.2/stretch/cli/Dockerfile
# ------------------------------------------------------------------------------------
# @build-example docker build . -f Dockerfile -t haxqer/swoft:code
#
FROM haxqer/swoft:base

ENV SWOFT_HOME="/var/www/swoft" \
    SWOFT_VERSION="v2.0.6.1"

RUN mkdir -p ${SWOFT_HOME} \
    && curl -o /tmp/swoft.tar.gz https://github.com/haxqer/swoft/archive/bas-${SWOFT_VERSION}.tar.gz -L \
    && tar xzf /tmp/swoft.tar.gz -C ${SWOFT_HOME}/ --strip-components 1 \
    && rm -f /tmp/swoft.tar.gz \
    && cd ${SWOFT_HOME} \
    && composer install \
    && composer clearcache

WORKDIR ${SWOFT_HOME}
EXPOSE 18306 18307 18308

