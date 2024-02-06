# Sentinel-Live-Attack-Lab

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Active Directory Lab Project</title>
</head>

<body>

    <h1>Active Directory Lab Project</h1>

    <h2>Overview</h2>

    <p>This project focuses on setting up a robust Active Directory environment using Windows Server 2019. The configuration includes dual NICs, one for external access and one for internal access. The Active Directory Domain is established as "Mydomain.com," with specific roles, including Active Directory Domain Services, Remote Access/Routing, and DHCP Server. A PowerShell script is utilized to create a designated Organizational Unit and generate 1002 user accounts for testing purposes.</p>

    <h2>Project Tasks</h2>

    <h3>1. Windows Server 2019 Installation</h3>

    <ul>
        <li>Installed Windows Server 2019 with dual NIC configuration.</li>
        <li>Configured one NIC for external access and another for internal access.</li>
    </ul>

    <h3>2. Active Directory Setup</h3>

    <ul>
        <li>Added Active Directory Domain Services role.</li>
        <li>Established the domain as "Mydomain.com."</li>
    </ul>

    <h3>3. User Account Creation</h3>

    <ul>
        <li>Created a Domain Admin account with the username "a-dcrouch."</li>
        <li>Ran a PowerShell script to generate 1002 user accounts in the Organizational Unit "_Users."</li>
        <li>Usernames are based on the first letter of the first name and the last name.</li>
        <li>All accounts share the password "Password1."</li>
    </ul>

    <h3>4. Network Configuration</h3>

    <ul>
        <li>Added Remote Access/Routing role for client internet access through the DC using NAT via the Internet NIC.</li>
        <li>Configured DHCP Server role to assign IP addresses within the range of 172.16.0.100-200.</li>
    </ul>

    <h3>5. Windows 10 Host Configuration</h3>

    <ul>
        <li>Created a Windows 10 Host configured to use the intranet NIC.</li>
        <li>Confirmed DHCP server functionality and successful client lease assignment within the specified IP range.</li>
        <li>Verified the Domain Controller as the default gateway and confirmed internet access.</li>
    </ul>

    <h3>6. Domain Join and User Login</h3>

    <ul>
        <li>Successfully joined the domain with the Windows 10 Host.</li>
        <li>Verified the ability to log in using one of the user accounts created via the PowerShell script.</li>
    </ul>

    <h2>Before and After</h2>

    <p>Before: [Screenshot or description of initial state]</p>
    <p>After: [Screenshot or description of final configured state]</p>

    <h2>Conclusion</h2>

    <p>This project showcases the step-by-step implementation of an Active Directory Lab, demonstrating domain setup, user account creation, network configuration, and successful domain join and user login. The detailed documentation provides a comprehensive guide for understanding and replicating the environment.</p>

</body>

</html>
