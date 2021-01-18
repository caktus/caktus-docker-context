# copelco-docker

## Setup

```sh
pip install -U pip-tools
pip-sync requirements.txt
ansible-galaxy install -f -r requirements.yml -p roles/
```

## Playbooks

```sh
# setup
ansible-playbook playbooks/deploy.yml
```

## Update requirements

```
pip-compile --upgrade requirements.in
pip-sync requirements.txt
```
