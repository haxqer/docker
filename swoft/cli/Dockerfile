# @description php image base on the debian 9.x
#
#                       Some Information
# ------------------------------------------------------------------------------------
# @link https://hub.docker.com/_/debian/      alpine image
# @link https://hub.docker.com/_/php/         php image
# @link https://github.com/docker-library/php php dockerfiles
# @see https://github.com/docker-library/php/tree/master/7.2/stretch/cli/Dockerfile
# ------------------------------------------------------------------------------------
# @build-example docker build . -f Dockerfile -t haxqer/swoft:cli
#
FROM haxqer/swoft:base

ENV VERSION="v0.1.1"

RUN curl -o /tmp/swoftcli.phar https://github.com/swoft-cloud/swoft-cli/releases/download/${VERSION}/swoftcli.phar -L \
    && mv /tmp/swoftcli.phar /usr/local/bin/swoftcli \
    && chmod a+x /usr/local/bin/swoftcli
