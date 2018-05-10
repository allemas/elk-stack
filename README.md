#ELK Stack
Run ELK (Elasticsearch, Logstash, Kibana) stack with Docker and Docker Compose. _based on (https://github.com/deviantony/docker-elk)_
Centralized log management allow you to visualize alerts,log and messages to discover app's states and issues.

## Requirements
 - Docker
 - Docker compose

## Usage
###Build the stack
``` $ docker-compose build ```
###Start
Verbose mode
``` $ docker-compose up ```
Daemon mode
``` $ docker-compose up -d```

*Port Forwarding*

Give Kibana a few seconds to initialize, then access http://localhost:5601 with your browser.
- 5000: Logstash TCP input.
- 9200: Elasticsearch HTTP
- 9300: Elasticsearch TCP transport
- 5601: Kibana

Test the stack
``` $ nc localhost 5000 < /path/to/logfile.log ```
