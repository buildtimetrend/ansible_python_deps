# ansible_python_deps
Ansible role to install python dependencies for various python versions

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
        - python_deps_extra_libs : ['package-foo', 'package-bar']
        - python_deps_requirements : ['/path/to/requirements.txt', '/path/to/requirements_test.txt']

## License

Licensed under the MIT License. See the LICENSE file for details.
