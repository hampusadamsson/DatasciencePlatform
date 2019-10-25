# FROM rastasheep/ubuntu-sshd
# FROM inspectorio/mlflow


# USER root
# RUN apt-get update
# RUN apt-get install -y supervisor

# COPY runner.sh /usr/local/bin/runner.sh
# COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

# CMD ["/usr/bin/supervisord"]

###############

FROM ubuntu:16.04

RUN apt-get update && apt-get -y install cron

COPY cron /etc/cron.d/cron

RUN chmod 0644 /etc/cron.d/cron

RUN crontab /etc/cron.d/cron

# RUN touch /var/log/cron.log

# CMD cron && tail -f /var/log/cron.log

CMD ["cron", "-f"]

