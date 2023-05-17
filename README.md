# ansible-ubuntu-example
An example of what can Ansible do when automating Ubuntu environments

# WIP

## How to use

Install ansible-navigator in a RHEL machine that has access to your Ubuntu systems.

Change inventory file so all ip addresses, users and passwords are up to date.

In your RHEL system with ansible-navigator installed clone this repo and run this command:
```
podman login registry.redhat.io
```

Then change into the directory for this Github repo and run the playbook:
```
ansible-navigator run do-ubuntu-web-server.yml
```
