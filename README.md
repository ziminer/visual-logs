visual-logs
===========

A Vagrant image to make post-mortem log visualization easier.

###Use case:  
You have a bunch of static log files and you want to analyze them.

###Solution:  
Use the logstash -> elasticsearch -> kibana stack, just like you would on a live system!

###Dependencies:  
Vagrant - http://www.vagrantup.com/downloads.html  
Ansible - http://docs.ansible.com/intro_installation.html#latest-releases-via-pip

###How To Set Up:  
1) Install Vagrant and Ansible  
2) Replace the ```logstash.conf``` file in ```ansible-playbook/roles/logstash/files``` with your own  
3) ```vagrant up```  
4) ```ifconfig``` to get the IP address - use this to navigate to Kibana

###How To Use:  
1) copy/move your logs to the ```logs/``` directory  
2) ```vagrant ssh```  
3) (if necessary) ```elasticsearchclear```  
4) ```stashlogs``` (CTRL-C when it's done)
