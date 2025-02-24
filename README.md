# Project
This lab simulates real-world cyber attacks and endpoint detection/response. Following Eric Capuano's guide, I’ll use VMs to replicate threat and victim machines. The attacker machine will run Sliver as a C2 framework to target a Windows endpoint protected by LimaCharlie (EDR).

Eric Capuano's Guide: https://blog.ecapuano.com/p/so-you-want-to-be-a-soc-analyst-intro
# Setup
Machines:

Attacker: Ubuntu Server with Sliver installed as the C2 framework.

Endpoint: Windows 11 with Microsoft Defender disabled (and other settings adjusted).

Tools:

Sliver: Primary attack tool on the Ubuntu machine.

LimaCharlie: EDR solution on the Windows machine, with a sensor linked to the endpoint and Sysmon logs imported for monitoring.


![image](https://github.com/user-attachments/assets/6a93b00b-df68-4222-96c4-2084560a158d)

![image](https://github.com/user-attachments/assets/7bf99267-b1b1-40ec-b023-6e0b61f008df)
# Attack
I generate a payload using Sliver and implant it onto the Windows host. Once the malware is executed on the endpoint, a command-and-control (C2) session can be established.
With a live C2 session established, the attacker can now explore the target machine, check privileges, gather host information, and assess the security measures in place.


![image](https://github.com/user-attachments/assets/60ba5db6-adac-4749-9446-e72594ab2869)
![image](https://github.com/user-attachments/assets/9f7a9db3-4410-4bc4-9f8c-61fc9b9ee265)

With a live C2 session established, the attacker can now explore the target machine, check privileges, gather host information, and assess the security measures in place.
