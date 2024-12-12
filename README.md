# Lululand

## Overview  
**Lululand** is a virtual internal network created to serve as a hands-on learning and testing environment for cybersecurity concepts and techniques. Developed as part of my journey as a Network Security major, Lululand allows me to apply and refine the knowledge and skills I acquire throughout my studies and career.  

The network operates within Oracle VM VirtualBox and is designed to facilitate experimentation, testing, and practice. Lululand is equipped with:  
- An **OPNsense firewall** with IDS/IPS capabilities.  
- Three internal virtual machines:  
  - **Kali Linux** for offensive security testing.  
  - **Ubuntu** for server or application hosting.  
  - **Windows 10** for endpoint simulation and analysis.  

## Project Goals  
The primary goals of Lululand include:  
1. **Penetration Testing**: Conducting simulated cyberattacks using an external virtual machine as a malicious actor to:  
   - Analyze traffic flows within the network.  
   - Identify vulnerabilities and areas of weakness.  
   - Develop threat intelligence and mitigation strategies.  

2. **Service Expansion**:  
   - Implementing additional services such as a web server for hosting or application testing.  

3. **Skill Enhancement**: Refining my abilities in network monitoring, intrusion detection, and secure system design.  

## Future Plans  
In addition to the current setup, I aim to:  
- Introduce additional virtual machines and services.  
- Configure advanced monitoring tools and logging mechanisms.  
- Automate threat detection and response processes using scripts and open-source tools.  

## Technical Setup  
- **Virtualization Platform**: Oracle VM VirtualBox
- **Firewall**: OPNsense Firewall
- **Internal Machines**:  
  - Kali GNU/Linux
  - Ubuntu
  - Windows 10  

## How to Use  
1. Install the latest version of **Oracle VirtualBox** or any type 2 hypervisor that you're familiar with
   - **VirtualBox Download Page**: https://www.oracle.com/virtualization/technologies/vm/downloads/virtualbox-downloads.html#vbox
2. Download the latest ISO images for the OPNsense Firewall, and the Kali Linux, Ubuntu, and Windows 11 machines.
   - **OPNsense Firewall Download Page**: https://opnsense.org/download/
   - **Kali Linux**: https://www.kali.org/get-kali/#kali-installer-images
   - **Ubuntu**: https://ubuntu.com/download/desktop#how-to-install-OracularOriole
   - **Windows 11**: https://www.microsoft.com/en-us/software-download/windows11
3. **Creating OPNsense Firewall VM**
   - Enter a name for the VM and the OPNsense ISO image. Change the type to BSD and the version to FreeBSD
   - Set base memory to 2048 MB and processors to 2
   - Set disk size to 16 GB
   - Go to the firewall VM's settings, and go to network. Enable adapter 1 and attach it to NAT, and enable adapter 2 and attach it to an internal network (intent or network name of your choosing)
5. **Firewall Configuration**
   - Boot up the firewall
   - Log into the firewall using the login: 'installer' and password: 'opnsense'
   - Choose the default keymap setting
   - Choose Install (UFS)
   - Choose VBox Hard disk and confirm your choice
   - After the installation is finished, change the root password then complete the installation
   - Let the VM reboot. Once the VBox graphic appears, click on 'Devices' in the window menu, go to optical drives, and click 'Remove disk from virtual drive'
   - Log in into the firewall using 'root' as the login and the password you made
   - 
## Contributions
This project is a personal endeavor aimed at self-education and skill-building. However, suggestions and feedback are welcome. Feel free to open an issue or submit a pull request with recommendations.  
