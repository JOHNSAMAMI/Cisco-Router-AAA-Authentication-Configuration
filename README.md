# Cisco-Router-AAA-Authentication-Configuration

Project Overview
This project involved the configuration of Authentication, Authorization, and Accounting (AAA) on Cisco routers to enhance administrative security and management. The focus was on implementing both local and server-based AAA authentication methods using TACACS+ and RADIUS protocols.
Business Understanding
In a secure network environment, protecting access to devices is crucial. AAA provides a comprehensive framework for managing user access and ensuring that only authorized personnel can make configuration changes. By implementing AAA, organizations can enforce security policies, track user activities, and reduce the risk of unauthorized access to critical network infrastructure.
Tools and Frameworks Used
•	Packet Tracer: A network simulation tool used for configuring and testing Cisco routers.
•	Cisco IOS Commands: Utilized for executing configurations on routers.
Project Description
The project involved configuring AAA authentication on three routers (R1, R2, and R3) using local accounts and TACACS+/RADIUS servers. Below is a breakdown of the key configurations performed:
Topology and Addressing Table:
•	Configured routers R1, R2, and R3 with respective IP addresses, ensuring connectivity.
•	Included TACACS+ and RADIUS servers with pre-defined user accounts for authentication.
Objectives and Configuration Steps:
Part 1: Local AAA Authentication on R1
1.	Test Connectivity: Verified connectivity between devices (PC-A, PC-B, and PC-C) through successful pings.
2.	Local User Account Creation: Configured a local user account on R1 with username Admin1 and password admin1pa55.
3.	Enable AAA: Enabled AAA on R1 and configured it to use the local database for console access.
4.	Console Configuration: Configured the console line to use the defined AAA authentication method.
5.	Verification: Verified successful login through the local AAA database from R1 console.
Part 2: Local AAA Authentication for vty Lines on R1
1.	Domain Name and Crypto Key: Set domain name to ccnasecurity.com and generated a 1024-bit RSA key.
2.	Named List for vty Lines: Created a named AAA method list called SSH-LOGIN to authenticate SSH logins using local AAA.
3.	VTY Line Configuration: Configured the vty lines to use the SSH-LOGIN method and restrict access to SSH only.
4.	Verification: Verified SSH connectivity to R1 from PC-A, confirming successful authentication.
Part 3: Server-Based AAA Authentication Using TACACS+ on R2
1.	Backup Local Database Entry: Configured a local username Admin2 with password admin2pa55 for backup purposes.
2.	TACACS+ Server Configuration: Verified that R2 was set up as a TACACS+ client, configured with server IP and secret key.
3.	AAA Configuration on R2: Enabled AAA and configured all logins to authenticate using TACACS+, falling back to the local database if necessary.
4.	Console Line Configuration: Configured the console line to utilize the TACACS+ authentication method.
5.	Verification: Verified successful logins using the AAA TACACS+ server from R2.
Part 4: Server-Based AAA Authentication Using RADIUS on R3
1.	Backup Local Database Entry: Configured a local username Admin3 with password admin3pa55 for backup purposes.
2.	RADIUS Server Configuration: Verified that R3 was set up as a RADIUS client with the correct server IP and secret key.
3.	AAA Configuration on R3: Enabled AAA and configured logins to authenticate using the RADIUS server, with a fallback to the local database.
4.	Console Line Configuration: Configured the console line to use the defined RADIUS authentication method.
5.	Verification: Verified successful logins using the AAA RADIUS server from R3.
6.	Final Check: Confirmed 100% completion by reviewing project requirements.
Conclusion: The successful implementation of AAA on the routers improved the overall security posture of the network by ensuring that only authorized users can access and configure devices. By combining local and server-based authentication methods, the network can maintain a robust security framework, significantly reducing the risk of unauthorized access and ensuring accountability.


