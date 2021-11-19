# Ansible Role for Kibana

An Ansible Role that installs [Kibana](https://www.elastic.co/kibana) version 7.12.1 on CentOS 8 Stream

Kibana deployed by this role is configured to connect to Elasticsearch cluster deploy by Elasticsearch role

## Requirements

1 CentOS 8 Stream node
Updated to support Development mode. In situation of testing where Elasticsearch, Kibana and Logstash are deployed together on a single host. The role can detect such situation and change to Development mode. It is recommended to have a host with minimum 8 GB Ram when testing.

In order to use the whole ELK stack, it is required to install Elasticsearch first before Kibana. 

## Role Description
- Install Kibana `7.12.1` configured to connect to Elasticsearch cluster deploy by Elasticsearch Ansible role
- Copy configuration files to `/etc/kibana/`
- Open port `5601`
- Upload Kibana saved object (Dashboards, mapping, etc)

## Variables

None.
