# Ansible role: f.lux

[![Build Status](https://travis-ci.org/danbohea/ansible-role-flux.svg?branch=master)](https://travis-ci.org/danbohea/ansible-role-flux)

Installs & configures f.lux on Mac OS X.


## Requirements

- Mac OS 10.9+


## Role Variables

All role default variables are listed below along with their respective default values.

```
flux_appdir: "/Applications"
```

Where to install the app. The value is passed to Homebrew Cask via the `--appdir` option.

```
flux_locationTextField: "ta126bu"
```

Your postal code. f.lux will use this to determine your Latitude & longitude.

```
flux_location: "50.976297,-2.838684"
```

Latitude & longitude. f.lux normally determines this for you but if you have the value from a previous installation enter it here.

```
flux_lateColorTemp: 3500
```

Color temperature for "Sunset".

```
flux_nightColorTemp: "{{ flux_lateColorTemp }}"
```

Color temperature for "Bedtime".


## Dependencies

- [danbohea.homebrew](https://galaxy.ansible.com/danbohea/homebrew)


## Example Playbook

```
- hosts: macbook
  connection: local

  roles:
    - role: ansible-role-flux
```

## License

MIT


## Author Information

This role was created by [Dan Bohea](http://bohea.co.uk) primarily for use with [Macsible](https://github.com/danbohea/macsible).
