# mybox_provisioning
Placeholder for the required files when provisioning a virtual box thru Vagrant
1. Installing Vagrant \
To begin with the provisioning, you should first find the appropriate package for your host system and download it. 
2. Installing VirtualBox \
VirtualBox is also required to be present in your host system before proceeding with the provisioning proper.  Please download and install it.
3. Installing a base box thru Vagrant \
When both VirtualBox and Vagrant are installed, you may now begin building a virtual box. 

$ vagrant init rivillar/mybox --box-version 1.0 \

A new file call Vagrantfile will be created in your present working directory.  We need to replace this with the modified Vagrantfile provided.

4. Copy the bootstrap.sh and phpinfo.php in your present working directory.  

These files can be found in https://gist.github.com/rivillar/8f94a8b10de185eebfaf1dc1df42d380.

Please ensure that these 3 files and your present working directory have 755 permission.

Start up your system:

$ vagrant up 

To test if you are able to login please enter the command below: 

$ vagrant ssh

Once you are able to login, please exit and go back to your host machine.  

5. Test if php and apache are working as required.  Access the default homepage from your host machine's browser. 

enter the url http://localhost:8888/phpinfo.php or http://127.0.0.1:8888/phpinfo.php

At this point, you should be able to see the required homepage successfully. 
