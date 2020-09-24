This file explain how wordpress automate using ansible

1. First create one directory on Ansible host
- create vars folder. In that created one yml file that include with mysql password, wordpress password and variable details
- create template folder. In that created J2 template of docker-compose that will copy on installation node.
- create main yaml file

|-- templates
|   |-- docker-compose.yaml
|   `-- docker-compose.yml.j2
|-- vars
|   `-- myvars.yml
`-- wordpress.yml

encrypt vars/myvars.yml

# ansible-vault encrypt vars/myvars.yml ( provide password that will use at the time of decypt)

2. Inside wordpress.yml file
- first create directory on installation node
- copy docker compose template with name docker-compose.yaml inside that directory
- execute docker-compose
Above three steps will execute on installation node.

ansible-playbook -i ../inventory --ask-vault-pass wordpress.yml

3. Test wordpress 
- execute "docker ps " to see deployed container of mysql and wordpress
- test connect from browser using node IP or localhost:<port>. Here Port number that you provide in compose file.
- if webpage get open successful then project done.
