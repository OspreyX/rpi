
.. _webcam:

Webcam Surveillance
---------------------

Since the RPi has two **USB slots** (model A & B) or even four (model B+) it is easy to connect and use a webcam with it. Modern, simple webcams---even with infrared light---start below 10 USD. More professional equipment can, of course, also be used.

This small project **focuses on the software side** of setting up an automated webcam surveillance system and not on the hardware side (which is probably determined by your specific purpose and maybe budget). I am using a rather small, simple USB webcam with infrared light to have some basic night filming capabilities available.


Installing Motion
~~~~~~~~~~~~~~~~~~~~

There is an excellent off-the-shelve, open source software called **Motion** available (cf. http://www.lavrsen.dk/foswiki/bin/view/Motion/WebHome). It is installed as follows::

    sudo apt-get install motion

You find Motion **configuration files** generally in the directory ``/etc/motion``. We will only need the one called ``motion.conf``. You should make a **new folder** like::

    mkdir /home/pi/motion

and **copy** the configuration file to it::

    sudo cp /etc/motion/motion.conf /home/pi/motion

You should also create another folder like::

    mkdir /home/pi/motion/media

That's already it for the installation of Motion.


Basic Configurations
~~~~~~~~~~~~~~~~~~~~~~~~~

Motion is a powerful and mature system. However, in what follows we are mainly interested in the following **capabilities**:

* **detect a motion** defined by the number of pixels changed
* take **single pictures** and store them locally or do something else (e.g. sending by email, putting on a remote FTP server)
* make **video recordings** and store them locally or do something else (e.g. email, FTP)


