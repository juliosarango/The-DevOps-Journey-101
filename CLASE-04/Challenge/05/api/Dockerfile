FROM python:3.10-alpine
RUN pip install flask
COPY ./src/* /app
COPY ./start /start

RUN sed -i 's/\r//' /start && \
    chmod +x /start

WORKDIR /app