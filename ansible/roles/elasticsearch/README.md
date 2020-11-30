# Ansible Role for Elasticsearch

An Ansible Role that installs [Elasticsearch](https://www.elastic.co/elasticsearch/) version 7.9.2 on RedHat/CentOS

All Elasticsearch nodes deployed with this Ansible Role will be configured as both Master and Data role (Elasticsearch role, not to be confused with Ansible Role).

## Requirements

This role is written to be deployed on minimum 2 CentOS 7 nodes or more with identical hardware configuration (vCPU, Ram, Storage, etc).

## Role Description
- Install Elasticsearch `7.9.2` configured as `Master` and `Data` node
- Copy configuration files to `/etc/elasticsearch/`
- Open port `9200`, `9300`
- Upload index template and lifecycle configuration to the stack

## Variables

Available variables are listed below, along with default values:


| Variable                                | Default Value            | Notes                                            |
| ----------------------------------------|--------------------------|--------------------------------------------------|
| `elasticsearch_heap_size`               | `4g`                     | Config this variable to be half of your available system memory.<br>E.g. `4g` for a node with 8gb memory       |

