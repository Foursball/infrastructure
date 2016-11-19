FROM fluent/fluentd:latest

COPY fluent.conf /fluentd/etc/fluent.conf

# Allow fluentd to forward to elasticsearch
RUN gem install --no-ri --no-rdoc fluent-plugin-elasticsearch
