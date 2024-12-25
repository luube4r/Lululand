# Lululand

## Overview  
**Lululand** is a virtual network created to serve as a hands-on learning and testing environment for cybersecurity concepts and techniques. Developed as part of my journey as a Network Security major, Lululand allows me to apply and refine the knowledge and skills I gain throughout my studies and career.  

The network operates within Oracle VM VirtualBox and is designed to facilitate experimentation, testing, and practice. Lululand is equipped with:  
- An **OPNsense firewall**.  
- Three internal virtual machines:  
  - **Kali Linux** for offensive security testing.  
  - **Ubuntu** for server or application hosting.  
  - **Windows 11** for endpoint simulation and analysis.  

## Project Goals  
The primary goals of Lululand include:  
1. **Penetration Testing**: Conducting simulated cyberattacks using an external virtual machine as a malicious actor to:  
   - Analyze traffic flows within the network.  
   - Identify vulnerabilities and areas of weakness.  
   - Develop threat intelligence and mitigation strategies.  
2. **Service Expansion**:  
   - Implementing additional services such as a web server for hosting or application testing.  
3. **Skill Enhancement**: Refining my network monitoring, intrusion detection, and secure system design abilities.  

## Future Plans  
In addition to the current setup, I aim to:  
- Develop a scenario to design the network infrastructure, optimizing its ability to effectively manage and implement changes to the network's security configuration.  
- Successfully configure and host a website on a designated machine within the network, ensuring proper accessibility and security measures.  
- Explore the firewall's IDS/IPS and web proxy capabilities.  

## Technical Setup  
- **Virtualization Platform**: Oracle VM VirtualBox
- **Firewall**: OPNsense Firewall
- **Internal Machines**:  
  - Kali GNU/Linux
  - Ubuntu
  - Windows 10  

## How To 
1. Install the latest version of **Oracle VirtualBox** or any type 2 hypervisor that you are familiar with.
   - [VirtualBox Download Page](https://www.oracle.com/virtualization/technologies/vm/downloads/virtualbox-downloads.html#vbox).
2. Download the latest ISO images for the OPNsense Firewall, and the Kali Linux, Ubuntu, and Windows 11 machines.
   - [OPNsense Firewall Download Page](https://opnsense.org/download/).
   - [Kali Linux](https://www.kali.org/get-kali/#kali-installer-images).
   - [Ubuntu](https://ubuntu.com/download/desktop#how-to-install-OracularOriole).
   - [Windows 11](https://www.microsoft.com/en-us/software-download/windows11).
3. **Creating OPNsense Firewall VM**
   - Enter a name for the VM and the OPNsense ISO image. Change the type to BSD and the version to FreeBSD.
   - Set base memory to 2048 MB and processors to 2.
   - Set disk size to 16 GB.
   - Go to the firewall VM's settings, and go to network. Enable adapter 1 and attach it to NAT, and enable adapter 2 and attach it to an internal network (intnet or network name of your choosing).
5. **Firewall Configuration**
   - Boot up the firewall.
   - Log into the firewall using the login: 'installer' and password: 'opnsense'.
   - Choose the default keymap setting.
   - Choose Install (UFS).
   - Choose VBox hard disk and confirm your choice.
   - After the installation is finished, change the root password, then complete the installation.
   - Let the VM reboot. Once the VBox graphic appears, click on 'Devices' in the window menu, go to optical drives, and click 'Remove disk from virtual drive'.
   - Log in to the firewall using 'root' as the login and the password you made.
   - Enter 1 to assign the WAN and LAN interface.
   - Set the WAN interface to 'em0' (NAT interface) and the LAN interface to 'em1' (internal network interface).
   - Enter 2 to set the LAN interface's IPv4 address (static (not DHCP)) and subnet mask.
   - You can activate the DHCP server on the LAN and create client address ranges to your liking. 
   - Select yes for web GUI options.
6. Now your firewall should be properly configured. At this point, you can start setting up other VMs like Windows 11, Ubuntu, Kali Linux, etc, and connecting them to your internal network.
7. After creating new machines in VBox, enter the network settings and attach adapter 1 to your internal network.
8. Once you've completed the installation of the new VM on your network, open a web browser on the VM and access the firewall's web GUI. Once you've completed the configurations(some of which do not have to be redone because they were done in previous steps), enter the dashboard and now your VM and any other VM on the network should have access to the Internet!
9. At this point you can explore your firewall's capabilities, add more VMs, and expand your virtual space(to the capabilities of your host machine).

## Acknowledgments
I used LS111 Cyber Security Education's [Virtual Cyber Security Lab Building Series](https://youtube.com/playlist?list=PLjjkJroii8DDb0QZpWLo978VXcLp8-xW3&si=0fDDPFpa2xgNOL0L) on YouTube to guide the making of this project.

## Contributions
This project is a personal endeavor aimed at self-education and skill-building. However, suggestions and feedback are welcome. Feel free to open an issue or submit a pull request with recommendations.  
