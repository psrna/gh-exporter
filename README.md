# gh-exporter
GitHub metrics exporter to MP / Prometheus metrics

```bash
GH_TOKEN=YOUR_GH_TOKEN mvn clean package quarkus:dev

curl http://0.0.0.0:8080/metrics/ 2>/dev/null | grep gh_
```

## Docker image
https://hub.docker.com/r/rostasvo/gh-exporter

```
docker pull rostasvo/gh-exporter

docker run --env GH_TOKEN=ea768c5fa8c89310027903a116b33aa5cc94f7f5 -i --rm -p 8080:8080 rostasvo/gh-exporter:1.0-SNAPSHOT
```