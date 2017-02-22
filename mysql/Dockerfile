FROM mysql:5.7
MAINTAINER ucpwang <ucpwang@gmail.com>

ENV MYSQL_ROOT_PASSWORD redmine
ENV MYSQL_DATABASE      redmine
ENV MYSQL_USER          redmine
ENV MYSQL_PASSWORD      redmine
ENV TZ                  Asia/Seoul

# for mysql `SYSTEM` timazone config
RUN echo $TZ | tee /etc/timezone
RUN dpkg-reconfigure --frontend noninteractive tzdata

CMD ["mysqld", "--character-set-server=utf8mb4", "--collation-server=utf8mb4_unicode_ci"]
EXPOSE 3306
