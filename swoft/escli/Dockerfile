# @description php image base on the debian 9.x
#
#                       Some Information
# ------------------------------------------------------------------------------------
# @link https://hub.docker.com/_/debian/      alpine image
# @link https://hub.docker.com/_/php/         php image
# @link https://github.com/docker-library/php php dockerfiles
# @see https://github.com/docker-library/php/tree/master/7.2/stretch/cli/Dockerfile
# ------------------------------------------------------------------------------------
# @build-example docker build . -f Dockerfile -t haxqer/swoft:escli
#
FROM haxqer/swoft:base

ENV SWOFT_HOME="/var/www/swoft"
ENV VERSION="v0.1.3"

RUN mkdir -p ${SWOFT_HOME} \
    && curl -o ${SWOFT_HOME}/composer.json https://raw.githubusercontent.com/haxqer/swoft/master/composer-es.json -L \
    && cd ${SWOFT_HOME} \
    && composer install \
    && composer clearcache

RUN curl -o /tmp/swoftcli.phar https://github.com/swoft-cloud/swoft-cli/releases/download/${VERSION}/swoftcli.phar -L \
    && mv /tmp/swoftcli.phar /usr/local/bin/swoftcli \
    && chmod a+x /usr/local/bin/swoftcli

# install zsh
RUN apt-get install -y zsh \
    && sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"

RUN echo "PROMPT='%#docker \${ret_status} %{\$fg[cyan]%}%c%{\$reset_color%} \$(git_prompt_info)'" >> /root/.zshrc

# install common tools
RUN apt install -y iputils-ping

WORKDIR ${SWOFT_HOME}


