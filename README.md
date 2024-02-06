# Azure/Sentinel Live Attack Lab

## Overview
This project focuses on setting up a domain controller running active directory on a Windows 2019 Server along with a Windows 10 host connected to that domain controller in Azure. For the purposes of this lab, the domain controller will connect to the internet and intranet, but the host will only have an internet connect through the domain controller. The host will have the firewall taken down to allow outside connections. Event ID 4625 is used to track the failed logins and a PowerShell script utilizes an API (https://ipgeolocation.io/) to transform the IP address into the country, city, state, province, local currency, latitude and longitude, company detail, ISP lookup, language, and zip code. The PowerShell script then appends this data to a custom log that is imported by Sentinel which is utilized to create a heat map of all of the failed login attempts.

## Project Tasks
1. Windows Server 2019 Installation
Installed Windows Server 2019 with dual NIC configuration.
Configured one NIC for external access and another for internal access.
2. Active Directory Setup
Added Active Directory Domain Services role.
Established the domain as "Mydomain.com."
3. User Account Creation
Created a Domain Admin account with the username "a-dcrouch."
Ran a PowerShell script to generate 1002 user accounts in the Organizational Unit "_Users."
Usernames are based on the first letter of the first name and the last name.
All accounts share the password "Password1."
4. Network Configuration
Added Remote Access/Routing role for client internet access through the DC using NAT via the Internet NIC.
Configured DHCP Server role to assign IP addresses within the range of 172.16.0.100-200.
5. Windows 10 Host Configuration
Created a Windows 10 Host configured to use the intranet NIC.
Confirmed DHCP server functionality and successful client lease assignment within the specified IP range.
Verified the Domain Controller as the default gateway and confirmed internet access.
6. Domain Join and User Login
Successfully joined the domain with the Windows 10 Host.
Verified the ability to log in using one of the user accounts created via the PowerShell script.
Before and After
Before: [Screenshot or description of initial state]
After: [Screenshot or description of final configured state]
Conclusion
This project showcases the step-by-step implementation of an Active Directory Lab, demonstrating domain setup, user account creation, network configuration, and successful domain join and user login. The detailed documentation provides a comprehensive guide for understanding and replicating the environment.
