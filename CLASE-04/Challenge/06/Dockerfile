FROM python:3.10-alpine
COPY ./requirements.txt .
RUN pip install -r requirements.txt

COPY ./app.py /app/
COPY ./pokeapi.py /app/
COPY ./templates /app/templates/
COPY ./start /start

RUN sed -i 's/\r//' /start && \
    chmod +x /start

WORKDIR /app