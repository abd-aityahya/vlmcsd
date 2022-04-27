FROM alpine:latest as builder
WORKDIR /root
RUN apk add --no-cache git make build-base && \
    git clone --branch main --single-branch https://github.com/abd-aityahya/vlmcsd.git && \
    cd vlmcsd/ && \
    make

FROM alpine:latest
WORKDIR /root/
COPY --from=builder /root/vlmcsd/bin/vlmcsd /usr/bin/vlmcsd
EXPOSE 1700/tcp
CMD [ "/usr/bin/vlmcsd", "-D", "-d" ]
