# Ansible Role for Kibana

An Ansible Role that installs [Kibana](https://www.elastic.co/kibana) version 7.9.2 on RedHat/CentOS

Kibana deployed by this role is configured to connect to Elasticsearch cluster deploy by Elasticsearch role

## Requirements

1 CentOS 7 node

## Role Description
- Install Kibana `7.9.2` configured to connect to Elasticsearch cluster deploy by Elasticsearch Ansible role
- Copy configuration files to `/etc/kibana/`
- Open port `5601`
- Upload Kibana saved object (Dashboards, mapping, etc)

## Variables

None.
