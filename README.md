IPython GEANT4 Linac
====================

A GEANT4 Linac written purely in the python environment using IPython notebook. An example of the ipython notebook running the GEANT4 code can be seen [here](http://nbviewer.ipython.org/github/SimonBiggs/ipython-geant4-linac/blob/master/main.ipynb).


Easy install on Windows, Mac, or Linux via Docker
=================================================
First install docker, generic instructions found [here](https://docs.docker.com/installation/). If you are on Windows these are the steps:
 
 * Download and run [docker-install.exe](https://github.com/boot2docker/windows-installer/releases/download/v1.3.1/docker-install.exe)
 * Run Boot2Docker from within the program menu (or desktop)
 * Press [Enter] when asked for an SSH keyphrase
 * Copy the following into the docker window:
   * `docker run -p 8888:8888 simonbiggs/geant4-examples`
   * On your first run this will download GEANT4
 * Once downloaded type `192.168.59.103:8888` into a [chrome](https://www.google.com/chrome/browser/) or [firefox](https://www.mozilla.org/firefox/new/) browser
 

Details
=======
If you are within windows and would like to use this repo first follow the steps given in [tips for virtualbox](#tips-for-virtualbox) to create an Ubuntu virtual machine, then follow the steps given within [setting up the environment](#setting-up-the-environment) in order to download and install python3.4 scipy stack, boost, and Geant4 9.6.3 with its python3.4 environment.




Setting up the environment
==========================

Assuming you have Ubuntu 14.04 64-bit LTS follow the steps given here to create a working environment. This will download and install:

 * Python 3.4 scipy stack
 * All boost-dev
 * Geant4 9.6.3 with python3.4 environment
 * All required dependencies for the above three items

Open terminal (ctrl + alt + T) and copy and paste (ctrl + shift + V) in the following lines, followed by enter, then your password:

    sudo apt-get -y install git; \
    mkdir ~/github; \
    cd ~/github; \
    git clone https://github.com/SimonBiggs/ipython-geant4-linac.git; \
    sudo ~/github/ipython-geant4-linac/install.sh; \
    sudo reboot

NOTE: This will take quite some time and use quite a bit of internet data. 

If you know what you are doing you should read through the install.sh before running it in case there are any options that disagree with your environment. 

The above method is for you if:

 * you are starting from scratch, 
 * don't mind where things are installed, 
 * and wouldn't know where to begin installing Geant4 


Once complete type:

    cd ~/github/ipython-geant4-linac
    ipython3 notebook
    
This will open up the notebook


Tips for virtualbox
===================
Download [Ubuntu 14.04 64-bit LTS](http://www.ubuntu.com/download/desktop/thank-you?version=14.04.1&architecture=amd64)

Download Virtualbox. If you are on Windows with antivirus use [version 2.3.12](http://download.virtualbox.org/virtualbox/4.3.12/VirtualBox-4.3.12-93733-Win.exe).

Install Virtualbox -- follow wizard

Create new virtual machine

 * >= 50 gb hard drive
 * >= 4 gb ram
 * Increase video memory
 * Increase number of cpus
 * Insert Ubuntu iso into virtual cd drive

Install Ubuntu 14.04 64-bit LTS inside the virtualbox


Boot new Ubuntu machine

Open terminal (ctrl + alt + T) and copy and paste (ctrl + shift + V) in the following lines, followed by enter, then your password:

    sudo apt-get update; \
    sudo apt-get -y upgrade; \
    sudo apt-get -y install build-essential dkms; \
    sudo reboot

(Virtualbox menu) || Devices > Insert Guest aditions CD Image

Allow the cd to autorun > follow prompts

    sudo reboot

(Virtualbox menu) || Machine > Settings > General > Advanced (Tab) > Enable bidirectional shared clipboard and drag 'n' drop
