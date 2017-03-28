FROM rabbitmq:alpine

RUN rabbitmq-plugins enable --offline rabbitmq_management && \
    rabbitmq-plugins enable --offline rabbitmq_stomp && \
    rabbitmq-plugins enable --offline rabbitmq_web_stomp && \
    echo '[  { rabbit, [ { loopback_users, [ ] } ] }, { rabbitmq_web_stomp, [ {tcp_config, [{port, 15674}]}, {default_user, [{login, "guest"}, {passcode, "guest"}]}] }].' > /etc/rabbitmq/rabbitmq.config

EXPOSE 15671 15672 15674
