# Ansible role python_deps
Ansible role to install python dependencies for various python versions in a Debian based distro.

[![Version](https://img.shields.io/github/release/buildtimetrend/ansible_python_deps.svg)](https://github.com/buildtimetrend/ansible_python_deps/releases/latest)
[![Build Status](https://travis-ci.org/buildtimetrend/ansible_python_deps.svg)](https://travis-ci.org/buildtimetrend/ansible_python_deps)
[![Galaxy](http://img.shields.io/badge/galaxy-buildtimetrend.python__deps-blue.svg)](https://galaxy.ansible.com/buildtimetrend/python_deps/)

## Role Variables

Available variables are listed below, along with default values:

    python_deps_python_version : ''
    python_deps_extra_libs : []
    python_deps_requirements : ['requirements.txt']

## Example Playbook

    - hosts: all
      roles:
        - { role: python_deps}
        - { role: python_deps, python_deps_python_version: "3" }

      vars:
        python_deps_extra_libs : ['package-foo', 'package-bar']
        python_deps_requirements : ['/path/to/requirements.txt', '/path/to/requirements_test.txt']

## License

Licensed under the MIT License. See the LICENSE file for details.
