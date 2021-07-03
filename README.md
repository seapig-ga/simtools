# simtools #
## Introduction ##
These are a collection of tools that are useful in my environment for setting
up simh emulators. If useful to you, great. If you have improvements, fine.
If you have complaints, too bad.

## Environment ##
My environment consists of:
* Various Debian based Linux (Ubuntu LTS versions) and Raspbian systems
* Several Windows 10 systems
* A Synology NAS providing storage for all the systems
* VAX and PDP-11 simulations

The disk images and simulator .ini files are all located on a common NFS
mounted share on the Synology.  This allows me to run the sims on any 
convenient system with minimal work.
__TODO: Need locking to prevent multiple copies from being run__

The main thing that is being done, is that the ethernet interfaces are being
set up as tap devices on a bridge with the actual ethernet device of the host
system.  This gets around a problem that the host and guest systems could not
interact with each other if the simulation was using the host ethernet device
via libpcap or vde.

## Tools ##
The tools that I use are bash scripts. 

__addtap__ creates the tap devices (and bridge, if neccessary).  It must be
run as root.

__mkemu__ creates and populates the directory for the particular simulation.
It uses template files for the various types of systems.

__is100install.ini__ is a simh .ini file for installing an InfoServer 100
instance. 

## References ##
Should be a boat-load.  I'll update them as I come across them again.

### Bridge/tap/tun ###
* Some info from the HECnet mailing list
* Other Internet references

### InfoServer Installation ###
(https://www.9track.net/simh/infoserver "9track.net InfoServer Software on Simh")


