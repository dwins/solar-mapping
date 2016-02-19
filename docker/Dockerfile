FROM ubuntu:14.04.3
RUN apt-get update -y
RUN apt-get install -y \
    postgresql-9.3-postgis-2.1 \
    postgresql-9.3 \
    python-imaging \
    tilestache \
    nginx \
    uwsgi \
    osmosis \
    imposm
COPY pg_hba.conf.ex /etc/postgresql/9.3/main/pg_hba.conf
RUN service postgresql start && \
    sudo -u postgres psql -c 'create database fsgis' && \
    sudo -u postgres psql fsgis -c 'create extension postgis'
CMD service postgresql start && service nginx start && service uwsgi start && bash
# CMD echo hello
