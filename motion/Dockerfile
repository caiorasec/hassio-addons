
FROM homeassistant/armhf-base

# Add env
ENV LANG C.UTF-8

# Setup base
RUN apk upgrade --no-cache --available \
 && apk add --no-cache --repository http://nl.alpinelinux.org/alpine/edge/testing \
        jq motion

# Copy data
COPY run.sh /
COPY motion.conf /etc/

RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
