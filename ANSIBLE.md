## Setup

`sudo apt-get update`

Install python  dependencies  
`sudo apt-get install python-minimal virtualenv python-dev build-essential`

## Invetory

Ansible works against multiple systems in your infrastructure at the same time. It does this by selecting portions of systems listed in Ansible’s inventory file, which defaults to being saved in the location /etc/ansible/hosts. You can specify a different inventory file using the -i <path> option on the command line.

Not only is this inventory configurable, but you can also use multiple inventory files at the same time (explained below) and also pull inventory from dynamic or cloud sources, as described in Dynamic Inventory.
see more  ()[]
