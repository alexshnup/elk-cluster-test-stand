# Elasticsearch Kibana Logstash and Filebeat 

This project sets up a Docker-based ELK (Elasticsearch, Logstash, Kibana) stack, enhanced with Filebeat for log shipping and a dummy service for generating JSON-formatted test logs for Filebeat.

It's designed for easy deployment and testing of log collection, search, and visualization capabilities. The configuration includes two Elasticsearch nodes for data resilience, Kibana for data exploration, and a dummy service to simulate real-time log data generation.

```
docker-compose up -d
```



## Send test logs to Logstash using Curl
```
curl -XPOST http://localhost:8080 -H 'Content-Type: application/json' -d '{
  "message": "This is a test log message",
  "timestamp": "'$(date --iso-8601=seconds)'"
}'
```