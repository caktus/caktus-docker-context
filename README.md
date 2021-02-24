# copelco-docker

## Setup

```sh
pip install -U pip-tools ansible
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
