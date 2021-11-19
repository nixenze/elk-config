# Ansible Role for Logstash

An Ansible Role that installs [Logstash](https://www.elastic.co/logstash/) version 7.14.0 on CentOS 8 Stream

All Logstash nodes deployed by this role are independent to each other. But they work on the same tasks, providing high availibility.

This Logstash nodes will recieve incoming events and send data out to Elasticsearch cluster deployed by Elasticsearch role

## Requirements

This role is written to be deployed on minimum 2 CentOS 8 Stream nodes or more with identical hardware configuration (vCPU, Ram, Storage, etc).
Updated to support Development mode. In situation of testing where Elasticsearch, Kibana and Logstash are deployed together on a single host. The role can detect such situation and change to Development mode. It is recommended to have a host with minimum 8 GB Ram when testing.

In order to use the whole ELK stack, it is required to install Elasticsearch first before Kibana. 

## Role Description
- Install Elasticsearch `7.14.0` configured to connect to Elasticsearch cluster deploy by Elasticsearch Ansible role
- Copy configuration files to `/etc/logstash/`
- Open port `5044`

## Variables

There is no variable available to user right now.
