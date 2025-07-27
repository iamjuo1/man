.PHONY: man secrets-view secrets-edit shared-roles
.PHONY: setup
.DEFAULT_GOAL = man

man:
	less README

secrets-view:
	ansible-vault view group_vars/all.yml

secrets-edit:
	ansible-vault edit group_vars/all.yml

setup: shared-roles
	ansible-playbook -i hosts.ini main.yml --ask-vault-pass

shared-roles:
	ansible-galaxy install -r requirements.yml
