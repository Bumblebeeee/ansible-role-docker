Ansible Role: install_docker
=========

Installing the latest Docker CE on Ubuntu with the option to add docker shared volume plugin

Requirements
------------

None

Role Variables
--------------

```
# defaults file for install_docker
pre_packages:
  - apt-transport-https
  - ca-certificates
  - curl
  - gnupg-agent
  - software-properties-common

packages:
  - docker-ce
  - docker-ce-cli
  - containerd.io

docker_volume_netshare_type: nfs
docker_volume_netshare_params: ""
```

```
# vars file for install_docker
docker_user: 
  - vagrant
# Choose if docker-volume-netshare is also included
include_docker_volume_netshare: false

```

Dependencies
------------

None

Example Playbook
----------------

See `tests/test.yml`

```
- hosts: all
  become: yes
  roles:
  - install_docker
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
