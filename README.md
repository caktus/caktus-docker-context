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
ansible-playbook deploy.yml
```

## Docker Context

```sh
docker context create copelco-docker --docker "host=ssh://copelco@142.93.32.206"
docker context use copelco-docker
```

## Update requirements

```
pip-compile --upgrade requirements.in
pip-sync requirements.txt
```
