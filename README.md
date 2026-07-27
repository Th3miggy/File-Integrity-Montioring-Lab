# File-Integrity-Montioring-Lab

## Objective

In this lab our goal is to establish a SIEM on our Ubuntu machine get our windows machine add as an endpoint and setup file integrity montioring on the endpoint and final test the montioring by creating and deleting files to see if they created event logs on our Wazuh Dashboard.

### Skills Learned

- Advanced understanding of SIEM concepts and practical application.
- Proficienet in SIEM setup as a control and a endpoint.
- Better understanding of File integrity montioring application.

### Tools Used

- Security Information and Event Management (SIEM) system namely Wazuh and Open source SIEM.
- Notpad or other text editor to note which directory we want to monitor.
- a Linux ubuntu machine to act as our manager and a windows device to be our endpoint.

## Steps
Below will be steps and images to document the process of completing this lab.

Ref 1: First step in the lab is to confirm the IP on our Ubuntu machine and windows machines as they will both be needed in the setup of the SIEM. we can do this by using ifconfig on our ubuntu machine and ipconfig on our windows machine.

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2022-11-27.png?raw=true)

Ref 2: Next we will head to the Wazuh and find the manager installer for ubuntu and run that script.

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2015-25-53.png?raw=true)

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2016-40-01.png?raw=true)




