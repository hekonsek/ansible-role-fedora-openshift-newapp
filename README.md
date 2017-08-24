# Ansible role: New application operation for OpenShift Origin on Fedora

Deploys new application into OpenShift. Optionally exposes deployed service to the outside world.

## Compatibility

This playbook has been tested against Fedora 26.

## Installation 

    ansible-galaxy install hekonsek.fedora-openshift-newapp,0.2

## Variables

- `app_image` - coordinates of Docker image that should be used for application.
- `app_name` - name of the application to be used.
- `app_expose` - if application service should be exposed to the outside world via router. Also ensures that appropriate local DNS
entry has been added to `/etc/hosts`.
- `router_host` - host name used by router to expose services to the outside world. Default value is `router.default.svc.cluster.local`.

## Example playbook

    - hosts: localhost
      remote_user: root
      roles:
        - { role: "hekonsek.fedora-openshift-newapp,0.2,
            vars: { app_image: "my/dockerimage:0.0", app_name: myapp, 
                    app_expose=true, router_host: "example.com" }

## License

Apache 2.0
