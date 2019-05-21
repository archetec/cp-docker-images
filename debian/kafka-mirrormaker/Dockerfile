FROM confluentinc/cp-kafka

# allow arg override of required env params
ARG MM_CONSUMER_BOOTSTRAP_SERVERS
ENV MM_CONSUMER_BOOTSTRAP_SERVERS=${MM_CONSUMER_BOOTSTRAP_SERVERS}
ARG MM_PRODUCER_BOOTSTRAP_SERVERS
ENV MM_PRODUCER_BOOTSTRAP_SERVERS=${MM_PRODUCER_BOOTSTRAP_SERVERS}

VOLUME ["/var/lib/${COMPONENT}/data", "/etc/${COMPONENT}/secrets"]

COPY include/etc/confluent/docker /etc/confluent/docker

CMD ["/etc/confluent/docker/run"]
