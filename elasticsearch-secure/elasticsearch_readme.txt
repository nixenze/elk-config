Elasticsearch 7.8 (three nodes cluster)

included files : index_template (folder), ilm(folder)
program path: /etc/elasticsearch/

instruction (if needed):
install elasticsearch
#open port 9200 9300 -> 
firewall-cmd --add-port={9200/tcp,9300/tcp} --permanent
firewall-cmd --reload
systemctl enable elasticsearch


edit config files

- jvm.options

edit -Xms and -Xmx to half of available ram
example if ram 8gb set
 -Xms4g
 -Xmx4g

- elasticsearch.jvm
#change node name to elastic-$number such as elastic-1 elastic-2 
cluster.name: elastic
node.name: elastic-$number
#if it is a first node, name as elastic-1
node.master: true
node.data: true

network.host: $node ip
http.port: 9200

#for the first node and first startup only
cluster.initial_master_nodes: ["elastic-1"]
#

discovery.seed_hosts: ["elastic-1", "elastic-2", "elastic-3"]


#after node start

##set index lifecycle manager(ilm)
curl to any elastic node by using command in ilm folder
(edit host url before curl) 

##set index template
do the same step as ilm by using files in index_template folder







