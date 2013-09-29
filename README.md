#OIP

## About

OIP is a visualization in which individual machine IPs are placed randomly on a display, and packets are visualized as different sized dots flowing from one machine to another.

### Architecture

OIP is primarily a server/client architecture. The server analyzes traffic on a given port, and streams summaries to clients over a udp session. The packets are encrypted using a shared AES key. The server should have two interfaces. One of them should be connected to a mirror interface, and the other should be used for the client connections.

The client can also be used as a stand-alone app by reading pcap files.

### License
License GPLv3 project: so enjoy and have fun.

You need to install these on debian-based distros
-------------------------------------------------
- apt-get install libcrypto++-dev libsdl-image1.2-dev libpcap-dev libsdl1.2-dev libfreetype6-dev g++ make


## Introduction

This is an update and modification of the forked OIP project from /eldraco on https://github.com/eldraco/oip to run on OS X Mountain Lion.

Original source code on: https://it.wiki.usu.edu/OIP

## How-To

### Command line

#### Parameters

1. -e argument to speed up the analysis of pcap files:
    -e 1000 is normal
    -e 100 is 10x faster
    -e 10 is 100x faster

2. -c argument to give the pcap file name in the command line:
    If you give a pcap file name, the analysis starts right away.

3. Pause/Play the capture by pressing the letter p.

#### Color code:

    On packet-balls:
        - Red for UDP
        - Green for TCP
        - White for ICMP

    On hosts:
        - Unknown still

### GUI

You can use the mouse and the keyboard.

Keyboard keys:
    - ! to open the menu
    - , to start displaying the capture (Load button).
    - p to pause and play the capture


## Installation

### Quick setup:

1. Checkout the master branch 
    `git clone git@github.com:markich/oip.git`

2. Type
    `make`
    Note: If you have any dependency error, just install them.

3. Modifiy the oip.conf file to suite your needs (Optional).

## Authors

1. Original code: Rian Shelley (Utah State Univeristy)

2. Forked code for Debian: Sebastian Garcia (eldraco@gmail.com) and Vojtech Uhlir (wojtyla@agents.felk.cvut.cz) (Czech Technical University)

3. Forked code for OS X: Marcos Jes&ucute;s Vivar (marcosjvivar@gmail.com) (Universidad F.A.S.T.A.)
