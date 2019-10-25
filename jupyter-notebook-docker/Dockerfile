FROM jupyter/scipy-notebook

RUN conda install --quiet --yes \
    'pysftp' \
    'mlflow' \
    'psycopg2'

COPY . /home/jovyan/work

USER root
RUN mkdir /artifacts
RUN chown jovyan /artifacts -R
