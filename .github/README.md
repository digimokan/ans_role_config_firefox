# ans_role_config_firefox

Install and configure the Firefox browser.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_config_firefox.svg?label=release)](https://github.com/digimokan/ans_role_config_firefox/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Supported Operating Systems](#supported-operating-systems)
* [Quick Start](#quick-start)
    * [Use From Playbook](#use-from-playbook)
* [Role Options](#role-options)
* [Role Dependencies](#role-dependencies)
* [Contributing](#contributing)

## Purpose

* Install the [Firefox](https://www.mozilla.org/en-US/firefox/) browser.
* Configure default browser settings.
* Install and configure select browser extensions.

## Supported Operating Systems

* Arch Linux.

## Quick Start

### Use From Playbook

1. Create `requirements.yml` in ansible project root, and add this content:

   ```yaml
   # requirements.yml
   - src: https://github.com/digimokan/ans_role_config_firefox
   ```

2. From the project root directory, install/download the role:

   ```shell
   $ ansible-galaxy install --role-file requirements.yml --roles-path ./roles --force-with-deps
   ```

   * _NOTE:_ `--force-with-deps` _ensures subsequent calls download updates_

3. Include the role like any local role, from the project playbook:

   ```yaml
   # playbook.yml
   - hosts: localhost
     connection: local
     tasks:
       - name: "Install and configure the Firefox browser"
         ansible.builtin.include_role:
           name: ans_role_config_firefox
         vars:
           user_name: "my_user_name"
   ```

## Role Options

See the role `defaults` file, for overridable vars:

  * [defaults/main.yml](../defaults/main.yml)

## Role Dependencies

* [ans_role_config_unofficial_packages](https://github.com/digimokan/ans_role_config_unofficial_packages)

Define these _required_ vars for the role:

  * `user_name`: name of primary Firefox user to configure the application for

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_config_firefox/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

