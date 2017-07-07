FROM alpine:3.3
ENV TERM xterm

RUN apk add --update musl python3 py-pip bash ca-certificates
RUN pip install --upgrade pip
RUN rm /var/cache/apk/*

ADD ./requirements.txt /
RUN pip install -r requirements.txt

WORKDIR /api

CMD ["python", "/app/run.py"]
EXPOSE 8000 5000 8080 9001
