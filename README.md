Ansible role: packer
=========

An Ansible role that installs Hashicorps Packer

Requirements
------------

On the host must `unzip` being installed. If not installed it will be installed by the role.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

	packer_version: 0.10.1

The version which should be installed.

	packer_sha256sum: c78a986708d48b69b42f02ca9e4a7974a9b7c453d65e9be6785e013af08ff90b

The sha256sum of the downloaded zip file.

	packer_base_url: https://releases.hashicorp.com/packer

Base URL from Hashicorps mirror.

	packer_arch: amd64

Architecture which should be used.

	packer_download_cache: /tmp/packer.zip

Destination where the zip file should be cached.

	packer_path: /opt/packer

Info file where the version is being stored

Dependencies
------------

None

Example Playbook
----------------

    - hosts: buildservers
      roles:
         - { role: craneworks.packer, packer_version: 0.10.1, packer_sha256sum: c78a986708d48b69b42f02ca9e4a7974a9b7c453d65e9be6785e013af08ff90b }

License
-------

CC-BY - https://creativecommons.org/licenses/by/3.0/


