Project Overview

​I built a virtual pentesting lab using VirtualBox to test security tools and practice network assessments in a self-contained setup.

Setting it up on a private network keeps the traffic isolated while making it easy to plug in more target VMs down the road.

​Core Objectives

​Install VirtualBox and spin up a Kali Linux instance.

​Route the Kali VM through a custom NAT Network with a fixed IP and reliable DNS access.

​Save base-state snapshots so the VM can be reverted if anything breaks.

​Keep detailed setup notes to serve as a baseline for future lab builds.

​Primary Uses

​The lab serves as a safe sandboxed environment for hands-on ethical hacking tasks, such as: 
​Running network scans and mapping open ports 
​Finding system vulnerabilities and sniffing network traffic

​Testing web app exploits and trying out new security utilities

Key Takeaways

Setting up this project gave me some solid, practical experience with building virtual environments for security testing. Here are the main things I walked away with:The difference between NAT and a NAT Network: I finally got a clear look at how these two differ in practice. Standard NAT is fine for a single isolated VM, but a NAT Network is what actually lets multiple virtual machines on the same subnet talk to each other while still sharing internet access. It’s pretty much essential if you want to build a realistic, multi-machine lab.

VirtualBox network configuration:  I got to spend some time mapping out how virtual network adapters actually handle traffic. Testing different adapter modes showed me exactly how configuration choices change the communication boundaries between the guest machines, my host computer, and the outside internet.

Static IP Configuration: I practiced manually setting up and verifying IPv4 addresses, subnet masks, default gateways, and DNS settings right inside Kali Linux. Getting this right is huge for making sure lab machines can actually find each other and talk consistently. 

The Power of VM Snapshots: I learned the hard way (or just realized) how critical it is to take a clean snapshot before running anything risky or experimental. It saves a ton of time by giving you a reliable, known-good restore point to jump back to if a lab exercise completely breaks the system.

The Value of Documentation: This project really drove home why keeping track of your steps matters. Taking notes on commands, configurations, error messages, and their solutions isn't just extra work—it's a massive part of running a professional security project and making sure you can replicate your results later.
