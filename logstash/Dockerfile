ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/logstash/logstash:${ELK_VERSION}

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
RUN logstash-plugin install logstash-filter-geoip

RUN logstash-plugin install logstash-filter-mutate

RUN logstash-plugin install logstash-filter-useragent

COPY ./plugins-data/GeoLite2-City.mmdb /usr/share/logstash/GeoLite2-City.mmdb