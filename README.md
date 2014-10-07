IPython GEANT4 Linac
====================

A GEANT4 Linac written purely in the python environment using IPython notebook.




How to install
==============

Assuming you have Ubuntu 14.04 64-bit LTS follow these steps to create a working environment:

Open terminal (ctrl + alt + T)

    sudo apt-get -y install git
    
    mkdir ~/github
    cd ~/github
    git clone https://github.com/SimonBiggs/ipython-geant4-linac.git
    
    sudo ~/github/ipython-geant4-linac/install.sh

NOTE: This will take quite some time and use quite a bit of internet data

Once complete type:

    cd ~/github/ipython-geant4-linac
    ipython3 notebook
    
This will open up the notebook


Tips for virtual box
====================
Download Ubuntu 14.04 64-bit LTS
Install virtualbox -- follow wizard
Install Ubuntu 14.04 64-bit LTS inside the virtualbox


Boot new Ubuntu machine

Open terminal (ctrl + alt + T)

    sudo apt-get update
    sudo apt-get -y upgrade

    sudo apt-get -y install build-essential dkms
    sudo reboot

(Virtualbox menu) || Devices > Insert Guest aditions CD Image

Allow the cd to autorun > follow prompts

    sudo reboot

(Virtualbox menu) || Machine > Settings > General > Advanced (Tab) > Enable bidirectional shared clipboard and drag 'n' drop
