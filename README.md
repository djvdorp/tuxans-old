# TuxAns

## About this project

What is **TuxAns**?
- **TuxAns** is an Ansible-port of the famous [TuxLite](http://tuxlite.com) shell scripts.
It is mainly free collection of shell scripts for rapid deployment of LAMP and LNMP stacks (Linux, Apache/Nginx, MySQL and PHP) for Debian and Ubuntu.

Who made the original **TuxLite**?
- Matt did! To contact him, email: *"s" at "tuxlite" dot "com"*

Are **TuxAns** and/or **TuxLite** free?
- Yes, the scripts are completely free and will remain free in the spirit of open source software. Use it as many times as you want, share it with others but do give credit where its due.

Can I donate to **TuxLite**?
- Yes, please see the [TuxLite Donate page](http://tuxlite.com/donate/).

What is ported in **TuxAns** (compared to **TuxLite**) at this time?
- All functionality, except for the "dbgui", "domain.sh" and "varnish.sh" parts of the script. (WIP)

Why **Ansible** and not *superCoolDevOpsToolB*?
- It only uses SSH for configuring. **NO AGENTS!** (Python dependency is only for data gathering)

## Installation instructions 

### Host node

How to use Ansible on Host (where you provision from):

1. Install python and pip
2. Install requirements.txt (pip install -r requirements.txt)
3. Install sshpass:

```
cd ~/Downloads
curl -O -L http://downloads.sourceforge.net/project/sshpass/sshpass/1.05/sshpass-1.05.tar.gz
tar xvzf sshpass-1.05.tar.gz
cd sshpass-1.05

./configure
make
sudo make install
```
Then run ansible on hosts in inventory (ansible-playbook main.yml -vvvv)

### Client node

How to make Node ready for Ansible:

1. Install bare OS
2. ssh as root
3. apt-get update && apt-get upgrade && apt-get install python