FROM ubuntu:14.04.4
RUN apt-get update -y
RUN apt-get install -y \
    python-imaging \
    tilestache \
    uwsgi
CMD service uwsgi start && bash
