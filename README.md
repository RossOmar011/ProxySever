# ProxySever
Project Title: Proxy Server Setup and Configuration
Description: A project detailing the steps to set up a SOCKS proxy server using a Linux server, Akamai cloud services, and Ubuntu. This setup ensures secure data transmission and location masking for clients.

Requirements:

Linux server (e.g., Ubuntu).

Cloud hosting with Anode by Akamai.

SSH access to the server.

Client machine (e.g., Windows with Firefox browser).

Steps:

Server Setup:

Create a server in your cloud environment with your desired region.

Retrieve SSH access credentials after server creation.

SSH Access:

Open your terminal on the client PC.

Paste your SSH credentials into the terminal and accept all fingerprints.

Install the OpenSSH server:

bash
sudo apt install openssh-server
Client Configuration:

On Windows, open Firefox and check your current IP address via whatmyip.com.

Launch Windows PowerShell and connect to the proxy server using the SOCKS proxy configuration:

bash
ssh -D 1337 -N -C root@<proxy-server-IP>
(Flags: SOCKS proxy, no remote commands, compress data over a timeline). Accept all fingerprints.

Firefox Proxy Setup:

Go to Firefox Settings -> Network Settings -> Manual Proxy Configuration.

Set the SOCKS host to localhost and add the port 1337.

Verification:

Return to whatmyip.com and confirm your IP location has changed.

Future Enhancements:

Automate the setup process using scripts.

Add support for additional proxy protocols (e.g., HTTP, HTTPS)
