# bind

With following role can be bind installed and configured.

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
