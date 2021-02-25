# Ansible Role for Logstash

An Ansible Role that installs [Logstash](https://www.elastic.co/logstash/) version 7.9.2 on RedHat/CentOS

All Logstash nodes deployed by this role are independent to each other. But they work on the same tasks, providing high availibility.

This Logstash nodes will recieve incoming events and send data out to Elasticsearch cluster deployed by Elasticsearch role

## Requirements

This role is written to be deployed on minimum 2 CentOS 7 nodes or more with identical hardware configuration (vCPU, Ram, Storage, etc).
Updated to support Development mode. In situation of testing where Elasticsearch, Kibana and Logstash are deployed together on a single host. The role can detect such situation and change to Development mode. It is recommended to have a host with minimum 8 GB Ram when testing.

## Role Description
- Install Elasticsearch `7.9.2` configured to connect to Elasticsearch cluster deploy by Elasticsearch Ansible role
- Copy configuration files to `/etc/logstash/`
- Open port `5044`

## Variables

There is no variable available to user right now.
