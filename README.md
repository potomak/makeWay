# makeWay

makeWay will poison the gateway's IP entry for all hosts in the network. It will replace the victim's gateway ARP entry with the hosts own MAC address, disconnecting connection between gateway and the hosts. In a sense it is a DOS attack. As the name applies when you run it you will have all the bandwidth to your self.

Please do not abuse the software, i wrote it because i use a network where people abuse torrents, at times you can't even access your email account. I do not have access to gateway and i needed a way to control bandwidth.

## Installation

There are no pre build packages availible. For now you have to build it your self. **Only depency is pcap library**.

To build it from source

* use `make linux` on linux
* use `make darwin` on Mac OS X


## Usage

* `./makeWay en1 -t 600`
  
  inject packages every 10 minutes.
  
* `./makeWay en1`
  
  inject packages every 3 secods. (This renders the network useless for everyone except you.)
  
* `./makeWay en1 scan`
  
  just make an ARP Sweep to see whose online.
  
* `./makeWay en1 192.68.16.15`
  
  inject packages every 3 secods. (This renders the network useless for everyone except you and 192.168.16.15.)

## Supported OS's

* Linux - Debian Lenny, Ubuntu 8.10
* Mac OS X - Mac OS X 10.5
