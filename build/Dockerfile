FROM registry.access.redhat.com/ubi8/ubi-minimal:latest

ENV OPERATOR=/usr/local/bin/pocs-operator-sdk \
    USER_UID=1001 \
    USER_NAME=pocs-operator-sdk

# install operator binary
COPY build/_output/bin/pocs-operator-sdk ${OPERATOR}

COPY build/bin /usr/local/bin
RUN  /usr/local/bin/user_setup

ENTRYPOINT ["/usr/local/bin/entrypoint"]

USER ${USER_UID}
