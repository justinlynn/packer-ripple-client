Ripple Client Packer
====================
Uses packer (packer.io) to create a virtualbox ovf appliance which
serves the Ripple JS Client.

Installation of Dependencies
----------------------------
* Install RVM for the build tooling by following the installation instructions at http://rvm.io/
* Ensure packer is installed by following the installation instructions at http://www.packer.io/docs/installation.html
* Once RVM is installed, leave and reenter directory. RVM will prompt you to install the correct ruby version.
* Once installed, you'll need to run `bundle` to install the dependency manager for the chef cookbook which will configure ripple client.
* Once bundle has been run, you can run `librarian-chef` to install all cookbook dependencies. (You may visit https://github.com/applicationsonline/librarian-chef for more information)
* Librarian-chef will install all of the cookbook dependencies to cookbooks/

Building The VirtualBox OVF
---------------------------
* The packer definition file `ripple-client.json` contains all the information packer needs to build the OVF.
* Run packer with the build argument, passing in the ripple-client.json file. Run `packer` for documentation on parameter order and for more information.
* Once build is completed packer should spit out your .ovf file!
