# Project 13: Centralized Logging with ELK & Filebeat

A demonstration of centralized logging in Kubernetes using the ELK Stack (Elasticsearch, Logstash, Kibana) and Filebeat.

## Overview

This project deploys a complete logging pipeline alongside a demo application across two namespaces:

- **Demo Application (`demo-app` namespace):**
  - **Frontend (`frontend.yaml`):** Demo frontend web service.
  - **Backend (`backend.yaml`):** Demo backend service.
- **Logging Pipeline (`ELK` namespace):**
  - **Filebeat (`filebeat.yaml`):** DaemonSet that discovers and collects container logs from Kubernetes nodes, forwarding them to Logstash.
  - **Logstash (`logstash.yaml`):** Filters and parses raw log lines using Grok patterns, forwarding structured log entries (`app-logs-*` index) to Elasticsearch.
  - **Elasticsearch (`elasticsearch.yaml`):** Single-node search and analytics engine that indexes and stores log data.
  - **Kibana (`kibana.yaml`):** Web interface for querying, analyzing, and visualizing logs stored in Elasticsearch.
