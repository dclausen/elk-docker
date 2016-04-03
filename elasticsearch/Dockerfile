# Pull base image.
FROM elasticsearch:2.2.1

# Set install version
ENV ES_PKG_NAME elasticsearch-2.2.1
ENV ES_HEAP_SIZE=2g

# Config
ADD elasticsearch.yml /usr/share/elasticsearch/config/elasticsearch.yml

RUN mkdir /data && chown -R elasticsearch:elasticsearch /data

VOLUME /data
