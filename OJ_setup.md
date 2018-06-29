# OJ Setup Tutorial

## Install the KVM Virtual Machines on the Server

- Recommendation for Server OS: CentOS 7
- Recommendation for Guest OS: CentOS for OJ web and Ubuntu for OJ judger

First make sure the server support `VT-X`. If not, switch it on in BIOS.
Then follow the [Server World](https://www.server-world.info/en/note?os=CentOS_7&p=kvm&f=1) 
to install a KVM virtual machine with CentOS and Ubuntu system respectively.

After doing so, you will need to change the MAC address of the network interface so that the virtual machine get the
IP address that the domain is pointed to. The MAC address can be obtained from the TA.


## Implement the VJ4 OJ System

### Web End

You can just follow the README here:

[https://github.com/edwardfang/vj4] (https://github.com/edwardfang/vj4)

Note that the `mongodb` and `rabbitmq` are easier to install using Docker. 

Also, the documentation of the repo may not be so good, so you may need to read the source code 
to find the features or develop some new features.

There is a good web interface for mongodb too. It's [mongo-express](https://github.com/mongo-express/mongo-express).
You can implement via Docker as well.

### Judge Server

This can be easily done by following the tutorial here:
[https://github.com/vijos/jd4#usage](https://github.com/vijos/jd)
