Logstash 7.8

included file: pipeline.yml, conf (pipeline config folder)

program path: /etc/logstash/

instruction (if needed):
install logstash
install java: yum install java-11-openjdk-devel
install jdbc: yum install mysql-connector-java
systemctl enable logstash
//delete the pipeline config in conf.d
//then put files in conf folder into conf.d

edit config files

- jvm.options

edit -Xms and -Xmx to half of available ram
example if ram 8gb set
 -Xms4g
 -Xmx4g


- pipeline.yml
replace this file with provided pipeline.yml file


- logstash.yml add monitoring (legacy method) change elasticsearch urls in hosts
xpack.monitoring.enabled: true
xpack.monitoring.elasticsearch.hosts: ["http://change_me-1:9200,"http://change_me-2:9200", ...(add more if any)]
