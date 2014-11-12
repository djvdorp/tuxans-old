# tuxans

## About this project

What is **tuxans**?
- **tuxans** is an Ansible-port of the famous [TuxLite](http://tuxlite.com) shell scripts.
It is mainly free collection of shell scripts for rapid deployment of LAMP and LNMP stacks (Linux, Apache/Nginx, MySQL and PHP) for Debian and Ubuntu.

Who made the original **TuxLite**?
- Matt did! To contact him, email: *"s" at "tuxlite" dot "com"*

Are **tuxans** and/or **TuxLite** free?
- Yes, the scripts are completely free and will remain free in the spirit of open source software. Use it as many times as you want, share it with others but do give credit where its due.

Can I donate to **TuxLite**?
- Yes, please see the [TuxLite Donate page](http://tuxlite.com/donate/).

What is ported in **tuxans** (compared to **TuxLite**) at this time?
- All functionality, including the Database GUI (now as a separate shell script, ```dbgui.sh```), ```domain.sh```, ```varnish.sh``` and ```wordpress.sh```. These scripts will be in ```/usr/local/src/tuxlite/ ```
- Removed: AWstats (use Analytics), TMPDD/TMPFS securing, MySQL optimization.

Why **Ansible** and not *superCoolDevOpsToolB*?
- It only uses SSH for configuring. **NO AGENTS!** (Python dependency is only for data gathering)

## Installation instructions 

### Host node

How to use Ansible on Host (where you provision from):

1. Install ```python``` and ```pip```
2. Install ```requirements.txt``` (```pip install -r requirements.txt```)
3. Run ansible on hosts in inventory (```ansible-playbook main.yml -vvvv```)

### Client node

How to make Node ready for Ansible (which you provision):

1. Install bare OS (Ubuntu 14.04 LTS recommended, but all Ubuntu and Debian supported)
2. Open ssh session as ```root```
3. ```apt-get update && apt-get upgrade && apt-get install python```