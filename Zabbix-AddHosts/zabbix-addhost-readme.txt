Zabbix Add/Modify Host Ansible script

Prepare the Ansible environment: 
	•	Ansible plugin need to be installed “community.zabbix.zabbix_host”
	•	This plugin will help us to Create/update/delete Zabbix hosts.
	•	To install it use:
ansible-galaxy collection install community.zabbix
	•	Modify the ansible script “zabbix-addhosts.yml” for below parameters
	•	hosts
	•	remote_user
	•	server_url
	•	login_user
	•	login_password
	•	host_groups
	•	link_templates 
	•	Updating an already onboarded existing hosts – hostgroups and link_templates which are linked in the current state needs to be mentioned.  
	•	Add servers to be updated in the servers.csv file in the below format:
"server.example.com,x.x.x.x"
	•	Place all below files in the same folder
	•	servers.csv
	•	zabbix-addhost-ansible.sh
	•	zabbix-addhosts.yml
 Steps to run the script:

	•	Change the permissions on “zabbix-addhost-ansible.sh”
chmod +x zabbix-addhost-ansible.sh
	•	Run the script as below
sh zabbix-addhost-ansible.sh


