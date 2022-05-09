# Homelab In A Box
...preamble, purpose, and general description.

##  Assumptions and Expectations
You are... you know how to... you have....

### Minimums
- Windows, Linux, or MAC with an SSH terminal installed.  Used as your console and remote management tool.
- github account - WITH uploaded SSH key.
- internet connectivity of at least 10mb speed and ability to download a few fairly large files
- one or more computing systems to be used as servers
- a dedicated router that is more than standard consumer grade (See Mikrotik or using an SBC as a router)

### Nice to haves
static IP address from ISP
greater than 10MB connectivity

## Preparation and Planning
- Network config and access...
- Access and IPs - external access, DNS, accounts you might need (a registrar, CDN, DynDNS, ...) etc..
- Hardware....  at least 1 machine that can even be an [[SBC]].  More power is always better, but one small Raspberry Pi would be enough.

## Network - the glue
either configure a router, or build one from an SBC and use a simple OpenWRT or similar.

## Lets Begin
### OS - A basic Linux server
Common to all nodes in our home lab Linux systems.  We are choosing a [Debian](https://www.debian.org/)  based distrobution for simplicity and coverage for multiple hardware options.  

If you are using a Raspberry Pi, it is recommended to use the [Raspberry Pi Configurator](https://www.raspberrypi.com/software/) and choose the default installation. 

If you are using another type of system, there will likely be a version of Debian or Ubuntu that is already available for it.  If you are using an AMD or Intel based system, simply follow the direction on the Ubuntu website for installing the latest LTS server version.
...
- enable ssh
- enable default pubkey from github account

### NAS - Network Attached Storage
If using SBCs - best to your OMV, otherwise it is strongly suggested to youe TrueNAS (is free now) on an Intel/AMD based system instead.
- install a NAS - including a drive (don't just use the SBC's SD card)
	- create a share for:
		- Portainer
		- NGiNX Proxy Manager
		- etc...  maybe we will just describe the process

### The Swarm - Docker cluster
- install Docker
- install Portainer (use the NAS for the volumes)

...
