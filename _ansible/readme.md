http://adeira-tmp.s3-website.eu-central-1.amazonaws.com/



Important! Run ansible-playground from this folder because of ansible.cfg.
AWSCLI must be installed.

	ansible-playbook deploy.yml

Or specify inventory file:

	ansible-playbook --inventory-file=_ansible/production _ansible/deploy.yml [-t deploy]

Possible command options:

	--check     (dry run)
	--verbose



ansible webservers -i _ansible/production -m setup
ansible webservers -i _ansible/production -m setup -a 'filter=ansible_distribution'
ansible all -i _ansible/production -m ping
ansible all -i _ansible/production -a "uname -r"
