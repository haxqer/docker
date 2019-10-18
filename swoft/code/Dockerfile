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

ENV SWOFT_HOME="/var/www/swoft" 

RUN mkdir -p ${SWOFT_HOME} \
    && curl -o ${SWOFT_HOME}/composer.json https://raw.githubusercontent.com/haxqer/swoft/master/composer.json -L \
    && cd ${SWOFT_HOME} \
    && composer install \
    && composer clearcache

WORKDIR ${SWOFT_HOME}
EXPOSE 18306 18307 18308

