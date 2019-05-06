## Setup (Using PiP and Virtual Enviroment)

`sudo apt-get update`

Install python  dependencies  

`sudo apt-get install python-minimal virtualenv python-dev build-essential`

Create a virtual environment (create a folder first)

`virtualenv myenv`

Excute the enviroment 
- ./script runs the script as an executable file, launching a new shell to run it
- source script reads and executes commands from filename in the current shell environment

`source venv27/bin/activate`



Verify if python is installed on recent created enviroment

`which python`

Install Ansible with pip insid the env

`pip install ansible`

Installing other packages from ansible git repository
`pip install git+https://github.com/ansible/ansible`

## FACTS
JSON with a collection of host's information 


[see more](https://www.middlewareinventory.com/blog/ansible-facts-list-how-to-use-ansible-facts/)

## Playbooks
Playbooks are Ansible’s configuration, deployment, and orchestration language. They can describe a policy you want your remote systems to enforce, or a set of steps in a general IT process.

If Ansible modules are the tools in your workshop, playbooks are your instruction manuals, and your inventory of hosts are your raw material.

## Invetory

Ansible works against multiple systems in your infrastructure at the same time. It does this by selecting portions of systems listed in Ansible’s inventory file, which defaults to being saved in the location /etc/ansible/hosts. You can specify a different inventory file using the -i <path> option on the command line.

Not only is this inventory configurable, but you can also use multiple inventory files at the same time (explained below) and also pull inventory from dynamic or cloud sources, as described in Dynamic Inventory.
 
[see more](https://docs.ansible.com/ansible/2.3/intro_inventory.html)


## What Is a Virtual Environment?
At its core, the main purpose of Python virtual environments is to create an isolated environment for Python projects. This means that each project can have its own dependencies, regardless of what dependencies every other project has.

In our little example above, we’d just need to create a separate virtual environment for both ProjectA and ProjectB, and we’d be good to go. Each environment, in turn, would be able to depend on whatever version of ProjectC they choose, independent of the other.

The great thing about this is that there are no limits to the number of environments you can have since they’re just directories containing a few scripts. Plus, they’re easily created using the virtualenv or pyenv command line tools.

## Dynamic Inventory 
Used when hots availabilty can change over time via  custom scripts or plugins.
` inventory plugin vs script pluging `

## Magic Variables
Whether or not you define any variables, you can access information about your hosts with the Special Variables Ansible provides, including “magic” variables, facts, and connection variables. Magic variable names are reserved - do not set variables with these names. The variable environment is also reserved.

## PATCH FILE 
Patch is a command that is used to apply patch files to the files like source code, configuration. Patch files holds the difference between original file and new file. In order to get the difference or patch we use diff tool.

## Import vs Include 
