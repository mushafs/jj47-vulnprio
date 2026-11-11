# logstash/
Logstash pipeline(s) that read `/var/ossec/logs/alerts/alerts.json` and ship to Elasticsearch, plus enrichment dictionaries.
Credentials live in the Logstash keystore only. Never commit them.
Owner: Noor (M-SIEM).
