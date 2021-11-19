# Ansible Role for Elasticsearch

An Ansible Role that installs [Elasticsearch](https://www.elastic.co/elasticsearch/) version 7.12.1 on CentOS 8 Stream

All Elasticsearch nodes deployed with this Ansible Role will be configured as both Master and Data role (Elasticsearch role, not to be confused with Ansible Role).

## Requirements

This role is written to be deployed on minimum 2 CentOS 8 Stream nodes or more with identical hardware configuration (vCPU, Ram, Storage, etc).
Updated to support Development mode. In situation of testing where Elasticsearch, Kibana and Logstash are deployed together on a single host. The role can detect such situation and change to Development mode. It is recommended to have a host with minimum 8 GB Ram when testing.

In order to use the whole ELK stack, it is required to install Elasticsearch first before Logstash or Kibana. 


## Role Description
- Install Elasticsearch `7.12.1` configured as `Master` and `Data` node
- Copy configuration files to `/etc/elasticsearch/`
- Open port `9200`, `9300`
- Upload index template and lifecycle configuration to the stack

## Variables

There is no variable available to user right now.