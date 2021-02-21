FROM alpine:3.13

ENV FLAG=flag{}

RUN apk update

RUN apk --no-cache --virtual add socat

EXPOSE 8000

CMD socat -U tcp-listen:8000,reuseaddr,fork EXEC:"echo $FLAG"
