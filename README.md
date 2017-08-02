# Ansible role: New application operation for OpenShift Origin on Fedora

Deploys new application into OpenShift.

## Compatibility

This playbook has been tested against Fedora 25.

## Installation 

    ansible-galaxy install hekonsek.fedora-openshift-newapp,0.0

## Variables

- `app_image` - coordinates of Docker image that should be used for application.
- `app_name` - name of the application to be used.

## Example playbook

    - hosts: localhost
      remote_user: root
      roles:
        - { role: hekonsek.fedora-openshift-newapp,0.0, vars: { app_image: my/dockerimage:0.0, app_name: myapp }

## License

Apache 2.0
