FROM ubuntu:14.04

# Dependencies
RUN apt-get update -y && \
    apt-get install -y -qq \
    nginx-full \
    wget \
    vim

# Kibana
RUN mkdir -p /opt/kibana
RUN wget https://download.elasticsearch.org/kibana/kibana/kibana-4.4.2-linux-x64.tar.gz -O /tmp/kibana.tar.gz && \
 tar zxf /tmp/kibana.tar.gz && mv kibana-4.4.2-linux-x64/* /opt/kibana/

# Configs
COPY kibana.yml /opt/kibana/config/kibana.yml

EXPOSE 5601

CMD /opt/kibana/bin/kibana
