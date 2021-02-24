# Configure remote host as docker context

## Setup

```sh
pip install -U pip-tools ansible
ansible-galaxy install -f -r requirements.yml -p roles/
cp config.yml.example config.yml
vim inventory
```

## Playbooks

```sh
# initial run as root user (e.g. for Digital Ocean)
ansible-playbook -u root -vv main.yml
```

## Docker Context

```sh
docker context create copelco-docker --docker "host=ssh://copelco@142.93.32.206"
docker context use copelco-docker
```
