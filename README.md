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
