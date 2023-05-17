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
Navigate to the ip address of your ubuntu servers, see how we've deployed a web server in a single command.

You can remove all the configuration we applied with previous command by using this one:
```
ansible-navigator run undo-ubuntu-web-server.yml
```
Having your web servers up and running run the following command to demonstrate how to edit files and, therefore, change configuration.
```
ansible-navigator run add-info-to-index.yml
```
Last, demonstrate the different behaviour of this two playbooks:
```
ansible-navigator run idempotency.yml
ansible-navigator run not-idempotency.yml
```
Look at the content of those two playbooks, see that the "command" module is not idempotent while the "file" module is idempotent. That explains the different behaviour of two playbooks that apparently are doing the same tasks.
