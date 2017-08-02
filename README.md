# mybox_provisioning
Placeholder for the required files when provisioning a virtual box thru Vagrant
1. Installing Vagrant \
To begin with the provisioning, you should first find the appropriate package for your system and download it. 
2. Installing VirtualBox \
VirtualBox is also required to be present in your system before proceeding with the provisioning proper.  Please download and install it.
3. Installing a base box thru Vagrant \
When both VirtualBox and Vagrant are installed, you may now begin building a virtual box. 

$ vagrant init rivillar/mybox --box-version 1.0 \
$ vagrant up \

To test if you are able to login please enter the command below: 

$ vagrant ssh

Once you are able to login, please exit and go back to your host machine.

You now have a minimally installed virtual box.  You may now proceed with customizing the newly-installed box. 

4. We need to keep 3 important files to provision a successful box as per the requirement:

- a new modified Vagrantfile 
- a file called phpinfo.php 
- a file called bootstrap.sh

5. Please ensure that these 3 files are in your present working directory.  Your base directory (present working directory) and these 3 files should have 755 permission. 

6. After putting them in place, we need to reload the newly-built virtual box. 

$ vagrant reload --provision

7. Test if php and apache are working as required.  Access the default homepage from your host machine's browser. 

enter the url http://localhost:8888/phpinfo.php or http://127.0.0.1:8888/phpinfo.php

At this point, you should be able to see the php homepage.

