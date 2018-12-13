.. title: Installing the latest version of Texlive (2016 right now) on Ubuntu without a headache
.. slug: installing-the-latest-version-of-texlive-2016-right-now-on-ubuntu-without-a-headache
.. date: 2016-11-04 21:50:19 UTC-05:00
.. tags: Ubuntu, LaTeX
.. category: 
.. link: 
.. description: 
.. type: text

Texlive is the most convenient way to get up and running with LaTeX on Linux (specifically Ubuntu, in this case) systems. A simple :code:`sudo apt-get install texlive` does the trick - however, there's an important catch: Debian versions of texlive traditionally lag behind. Ubuntu 14.04 and 16.04 ship with the 2013 and 2015 versions respectively. So, when I had to look into updating texlive on my 14.04 system, I had no recourse but to try to attempt installing 'vanilla' texlive straight from CTAN, and of course, risk the consequences!


Turns out that installing texlive on CTAN can be a complicated mess of steps that need to be done in exactly the right order - but I came across this supremely helpful `Github repo`_ from Scott Kostyshak that makes everything super simple. One simply needs to clone this repository, and follow the steps in the readme, and things work smoothly (I've tested this on my Ubuntu 14.04 system).

Here are the steps::

    git clone https://github.com/scottkosty/install-tl-ubuntu
    cd install-tl-ubuntu
    sudo ./install-tl-ubuntu

NOTE: If you have the Debian version of texlive already installed (2013 in the case of Ubuntu 14.04 - to check your texlive version, say 'tex --version' at the terminal), you will need to remove it with :code:`sudo apt-get remove --purge texlive*` first.

.. _Github repo: https://github.com/scottkosty/install-tl-ubuntu
 