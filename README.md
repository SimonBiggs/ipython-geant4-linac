IPython GEANT4 Linac
====================

A GEANT4 Linac written purely in the python environment using IPython notebook. An example of the ipython notebook running the GEANT4 code can be seen [here](http://nbviewer.ipython.org/github/SimonBiggs/ipython-geant4-linac/blob/master/main.ipynb). 


Windows 7/8
===========
In order to install Geant4 within Windows you can use Docker. These are the steps to acheive this:

 * Download and run [docker-install.exe](https://github.com/boot2docker/windows-installer/releases/download/v1.3.1/docker-install.exe)
 * Run Boot2Docker from within the program menu (or desktop)
 * Press [Enter] when asked for an SSH keyphrase
 * Copy the following into the docker command window:
   * `docker run -p 8888:8888 simonbiggs/geant4-examples`
   * On your first run this will download GEANT4
 * Once downloaded type `192.168.59.103:8888` into a [chrome](https://www.google.com/chrome/browser/) or [firefox](https://www.mozilla.org/firefox/new/) browser
 
Be warned that if you use the docker method of installation data will not be saved once you close boot2docker, therefore you need to download the .ipynb files to your computer. These can be uploaded again by dragging and dropping into the browser window when you next start up docker.

Mac OS X
=======
In order to install Geant4 within Mac OS X you can use Docker. These are the steps to acheive this:

 * Download and run [Boot2Docker-1.3.1.pkg](https://github.com/boot2docker/osx-installer/releases/download/v1.3.1/Boot2Docker-1.3.1.pkg)
 * Run the newly installed Boot2Docker from within your applications folder
 * Copy the following into the docker terminal:
   * `docker run -p 8888:8888 simonbiggs/geant4-examples`
   * On your first run this will download GEANT4
 * Once downloaded type `192.168.59.103:8888` into a [chrome](https://www.google.com/chrome/browser/), [firefox](https://www.mozilla.org/firefox/new/), or safari browser

Be warned that if you use the docker method of installation data will not be saved once you close boot2docker, therefore you need to download the .ipynb files to your computer. These can be uploaded again by dragging and dropping into the browser window when you next start up docker.


Linux through docker
====================
Install docker using the method for your os described [here](https://docs.docker.com/installation/).

Run the following command within the terminal as root:
`docker run -p 8888:8888 simonbiggs/geant4-examples`

Once downloaded type `localhost:8888` into a [chrome](https://www.google.com/chrome/browser/) or [firefox](https://www.mozilla.org/firefox/new/) browser.

Be warned that if you use the docker method of installation data will not be saved once you stop the docker process, therefore you need to download the .ipynb files to your computer. These can be uploaded again by dragging and dropping into the browser window when you next start up docker.




Ubuntu 14.04 64-bit LTS
=======================

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
