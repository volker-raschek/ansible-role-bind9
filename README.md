# bind9-role

[![Build Status](https://drone.cryptic.systems/api/badges/volker.raschek/bind9-role/status.svg)](https://drone.cryptic.systems/volker.raschek/bind9-role)
[![Ansible Role](https://img.shields.io/ansible/role/d/58170)](https://galaxy.ansible.com/volker_raschek/bind9_role)

With following role can be bind installed and configured.

## Installation

```bash
ansible-galaxy install volker_raschek.bind9_role
```

## Supported distributions

- Arch Linux
- Rocky Linux 8
- Ubuntu 20.04

## Features

- Installing bind/named
- Configuring bind/named
  - TSIG-Keys
  - Simple Zones
  - Zones with different views
  - DYNDNS

## Configuring

In the default directory are examples how to configure `named`. Copy the
defaults into your `host_vars` or `group_vars` and adapt the examples.

## Individual host-templates

Each host has his own zones templates. Store the template in
`templates/<hostname>/etc/named/zones/<name-of-view>/zone.conf`. For example:
`templates/ns1.example.com/etc/named/zones/internal/db.de.example`.
