# Troubleshooting Guide

This guide provides solutions to common issues that you may encounter while setting up and using Cloud Monitoring & Performance Tracking for MongoDB using Prometheus and Grafana.

## Problem: Prometheus Scrape Failures

- **Solution**: Check Prometheus's configuration in `prometheus.yml`.
- Ensure that MongoDB Exporter is reachable from Prometheus.
- Verify any firewall settings that might be blocking communication.

## Problem: Grafana Data Source Connection Issues

- **Solution**: Double-check the Prometheus data source configuration in Grafana.
- Confirm the Prometheus server's URL is correctly entered.
- Verify network connectivity between Grafana and Prometheus.

## Problem: MongoDB Exporter Not Collecting Metrics

- **Solution**: Review the `start-mongodb-exporter.sh` script.
- Ensure the MongoDB URI and authentication details are accurate.
- Check MongoDB Exporter logs for any errors.

## Problem: Alerts Not Triggering

- **Solution**: Inspect the `alerting-rules.yml` configuration for alert expressions.
- Check if metric values meet the conditions set in alerting rules.
- Verify that alert notifications are properly configured.

## Problem: Missing or Inaccurate Metrics

- **Solution**: Confirm MongoDB Exporter is properly configured to expose desired metrics.
- Ensure MongoDB queries are generating expected metrics.
- Validate configuration by manually querying the MongoDB Exporter's `/metrics` endpoint.

## Conclusion

Troubleshooting is a crucial aspect of setting up monitoring. Identifying and resolving issues promptly helps maintain a reliable monitoring environment for your MongoDB database.
