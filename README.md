# Ansible role to install PHP Composer from source on Debian

[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-php-composer-blue.svg)](https://galaxy.ansible.com/mejo-/php-composer/) [![Build Status](https://travis-ci.org/mejo-/ansible-role-php-composer.svg?branch=master)](https://travis-ci.org/mejo-/ansible-role-php-composer)

A very simple role to install latest PHP Composer from source on Debian
systems.

Additionally, it installs a daily cronjob to update PHP Composer.

# Defaults

```
php_version_default: "{{ '5' if ansible_distribution_major_version|int <= 8 else '7.0' }}"

# Packages to be installed before composer
php_composer_deps:
  - "php{{ php_version_default }}-cli"

# The path where the composer binary is installed
php_composer_path: /usr/local/bin
```

# License

This Ansible role is licensed under the GNU GPLv3 or later.

# Author

Copyright 2017 Jonas Meurer <jonas@freesources.org>
