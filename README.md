IPython GEANT4 Linac
====================

A GEANT4 Linac written purely in the python environment using IPython Notebook. An example of the IPython Notebook running the GEANT4 code can be seen [here](http://nbviewer.ipython.org/github/SimonBiggs/ipython-geant4-linac/blob/master/main.ipynb). 

Note, the methods outlined below will likely use upwards of 2 GB of data and about 1-2 hours computer time.

If you have any trouble getting this to work first try running `docker pull simonbiggs/geant4-examples` in case I have released an update. If you are still having trouble then feel free to [contact me](mailto:mail@simonbiggs.net) I am more than happy to help.

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


Linux
=====
Install docker using the method for your os described [here](https://docs.docker.com/installation/). An example for Ubuntu 14.10 is by typing within the terminal:

    sudo apt-get install docker.io
    
Once installed run the following command within terminal as root (sudo):

    docker run -p 8888:8888 simonbiggs/geant4-examples

Once downloaded type `localhost:8888` into a [chrome](https://www.google.com/chrome/browser/) or [firefox](https://www.mozilla.org/firefox/new/) browser.

Be warned that if you use the docker method of installation data will not be saved once you stop the docker process, therefore you need to download the .ipynb files to your computer. These can be uploaded again by dragging and dropping into the browser window when you next start up docker.
