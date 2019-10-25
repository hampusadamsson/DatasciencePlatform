
FROM python:3.7.0

RUN pip install mlflow
RUN pip install psycopg2

EXPOSE 5000

RUN mkdir /mlflow
RUN mkdir -p /server
WORKDIR /server
COPY . /server

RUN chmod +x wait-for-it.sh

RUN mkdir /mlflow-artifacts/
RUN chmod 777 /mlflow-artifacts

CMD ./wait-for-it.sh database:5432 -- mlflow server \
    --backend-store-uri postgresql://admin:secret@database:5432/mlflow \
    --default-artifact-root /artifacts/ \
    --host 0.0.0.0

