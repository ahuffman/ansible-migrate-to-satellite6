# Migrate Satellite 5 clients to Satellite 6  
## Purpose  
To provide a method to painlessly move Satellite 5 clients to Satellite 6 by making use of Ansible playbooks.

## Usage
There's a few ways you could use this playbook.  
### Modifying the variables  
If you would like to update the required variables `sat6server`,`activationkey`, and `organization` simply edit the playbook under the 'vars' section and plug-in the valid values for your environment.  You will also want to change `hosts: all` to a specific group.  
  
You could then run:  
ansible-playbook mig2sat6.yml -u root -k

### Passing variables at runtime  
If you would rather just pass the variables at runtime, then you can run:  
ansible-playbook mig2sat6.yml -e "sat6server=mysat6server.mydomain.com activationkey=myactivationkey organization=myorganization" --limit mygroupofhosts -u root -k

## Author
[Andrew J. Huffman](https://github.com/ahuffman)

## License
[MIT](LICENSE)
