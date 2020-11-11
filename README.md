# log-collection-docker-compose
nginxのアクセスログをFilebeats -> Logstash -> ElasticSearchで連携してKibanaから参照する仕組みを、
docker-composeを使って構築するサンプルです

# Getting Started
- まずはじめに`shared-network`という名前でdocket networkを作成しておきます
```
docker network create shared-network
```

- 全てのコンポーネントで`docker-compose up -d`します
```
cd nginx
docker-compose up -d
cd ../beats
docker-compose up -d
cd ../logstash
docker-compose up -d
cd ../elasticsearch
docker-compose up -d
cd ../kibana
docker-compose up -d
```

- nginxのアクセスログを出力します
```
curl http://localhost:8080
```

- Kibanaからログを参照します

http://localhost:5601
