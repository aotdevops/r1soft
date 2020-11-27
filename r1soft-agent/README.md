Automation

I have done multiple of them. 
1. Installation backup agent (r1soft) on different platforms. Our company uses a backup tool that is called r1soft. It uses client - server architecture. To take a backup of the system, agent needs to be installed on remote systems. So I created ansible playbook that installs agent on remote systems. The playbook I created can actually sort the OS type and install packages accordingly. It is one of the robust playbooks I have created. You can check out my github account for that. I have a repository called r1soft.

It became reusable playbook. I documented it and we are using it to automate the installation of backup agent. 


Version 1 
Overall the project supposed to have the following things in it. 
1. It needs to 
     Pre-steps
       i) enable r1soft repo depending on OS type
       ii) add hosts to the inventory 
    a) install r1soft agent on centos 6 
    b) run r1soft    /  enable r1soft
    c) open port 1167 using iptables 
    d) enroll the machine into r1soft server
  
1. It needs to 
    a) install r1soft agent on centos 7
    b) run r1soft    /  enable r1soft
    c) open port 1167 using firewalld 
    d) enroll the machine into r1soft server

Our company also uses fedora 26.  So I had to create another playbook for that. 
    a) install r1soft agent on Fedora 26
    b) run r1soft    /  enable r1soft
    c) open port 1167 using firewalld 
    d) enroll the machine into r1soft server


Another playbook
It needs to install r1soft agent on Debian family
    a) install r1soft agent on Debian.
    b) run r1soft    /  enable r1soft
    c) open port 1167 using ufw 
    d) enroll the machine into r1soft server

It needs to install r1soft agent on Debian family
    a) install r1soft agent on Ubuntu
    b) run r1soft    /  enable r1soft
    c) open port 1167 using ufw 
    d) enroll the machine into r1soft server



Version 2 
I combined all of them into  1 playbook 
