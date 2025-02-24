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
#

![image](https://github.com/user-attachments/assets/60ba5db6-adac-4749-9446-e72594ab2869)
![image](https://github.com/user-attachments/assets/9f7a9db3-4410-4bc4-9f8c-61fc9b9ee265)
![image](https://github.com/user-attachments/assets/d548259d-d9e0-48f2-849f-bb064e53f499)

#
On the attack machine, we can simulate credential theft by dumping LSASS memory. Meanwhile, in LimaCharlie, we can monitor the sensors, analyze telemetry, and create detection rules to identify this sensitive process.

![image](https://github.com/user-attachments/assets/2a3def04-0ae5-4a89-b786-d4737e39286f)
![image](https://github.com/user-attachments/assets/ccab791e-1a62-45c8-b310-3d2cb3205b3e)
![image](https://github.com/user-attachments/assets/ee074a10-368f-4fb3-a064-7d066f1d362d)
![image](https://github.com/user-attachments/assets/c448b9ff-34a4-4e33-9614-544ab1bf3d48)

#
To take it further, I’ll simulate a ransomware attack by attempting to delete volume shadow copies from the Ubuntu machine. Using LimaCharlie, I’ll observe the telemetry, write rules to detect and block the attack, and ensure the same attack fails if attempted again.

![image](https://github.com/user-attachments/assets/1e3fa0f7-456a-4b4e-8693-66c4710d09ce)
![image](https://github.com/user-attachments/assets/8431b07f-cc4e-4c19-944b-79c4456f36fc)
![image](https://github.com/user-attachments/assets/cd81e4a7-e4fa-40fa-a508-ccdd8684f79b)
![image](https://github.com/user-attachments/assets/d5d88761-3d07-466e-98b4-701bf8f4304c)




