FROM python:3.10-alpine
ENV LOCAL true
ENV PYTHONUNBUFFERED 1

RUN pip install requests
COPY ./consumer/* /app/
COPY ./start /start

RUN sed -i 's/\r//' /start && \
    chmod +x /start
    
WORKDIR /app