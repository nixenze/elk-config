# Ansible Role for Logstash

An Ansible Role that installs [Logstash](https://www.elastic.co/logstash/) version 7.9.2 on RedHat/CentOS

All Logstash nodes deployed by this role are independent to each other. But they work on the same tasks, providing high availibility.

This Logstash nodes will recieve incoming events and send data out to Elasticsearch cluster deployed by Elasticsearch role

## Requirements

This role is written to be deployed on minimum 2 CentOS 7 nodes or more with identical hardware configuration (vCPU, Ram, Storage, etc).

## Role Description
- Install Elasticsearch `7.9.2` configured to connect to Elasticsearch cluster deploy by Elasticsearch Ansible role
- Copy configuration files to `/etc/logstash/`
- Open port `5044`

## Variables

Available variables are listed below, along with default values:


| Variable                                | Default Value            | Notes                                            |
| ----------------------------------------|--------------------------|--------------------------------------------------|
| `logstash_heap_size`               | `4g`                     | Config this variable to be half of your available system memory.<br>E.g. `4g` for a node with 8gb memory       |

