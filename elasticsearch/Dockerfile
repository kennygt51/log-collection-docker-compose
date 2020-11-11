FROM docker.elastic.co/elasticsearch/elasticsearch:7.9.3

COPY ./config/elasticsearch.yml /usr/share/elasticsearch/config/elasticsearch.yml

RUN elasticsearch-plugin install analysis-kuromoji
