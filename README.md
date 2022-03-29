```
sudo docker-compose up -d
```
```
sudo docker run -v "${PWD}/script:/opt/script" --network monitoring --rm \
-ti --link prometheus -e K6_PROMETHEUS_REMOTE_URL=http://prometheus:9090/api/v1/write norgefajardo/k6:v0.37.0  run opt/script/script.js -o output-prometheus-remote
```
