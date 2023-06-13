FROM python:3.10-alpine
COPY ./app.py .
COPY ./entrypoint .
RUN pip install flask redis
RUN chmod +x ./entrypoint
ENTRYPOINT [ "./entrypoint" ]