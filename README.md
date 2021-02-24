# loki-docker-nginx-example

docker plugin install grafana/loki-docker-driver:latest --alias loki --grant-all-permissions

brew install promtail

wget https://raw.githubusercontent.com/grafana/loki/master/cmd/promtail/promtail-local-config.yaml

promtail -config.file=./config/promtail-local-config.yaml

docker run -d -v /var/log/:/var/log/ grafana/promtail:latest -config.file=./config/promtail-local-config.yaml