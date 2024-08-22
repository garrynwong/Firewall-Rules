<h1>Firewall Rules & Inspecting Traffic</h1>

 ### [ ]()

<h2>Description</h2>
Project consists of inspecting network traffic and setting inbound and outbound rules in Windows Firewall.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Windows Firewall</b>
- <b>Command Line Tools</b>
- <b>Network Protocols</b>
- <b>WirsShark</b>

<h2>Environments Used </h2>

- <b>Windows 11, Windows Server 2022</b>

<h2>Program walk-through:</h2>


<h1>Inspecting Network Traffic</h1>

<h3>Step 1:  </h3>
<p> Ping the domain controller from the client; then filter and observe ICMP packets only in Wireshark </p>

![1](https://github.com/user-attachments/assets/bdfcedef-da30-4820-b518-ef3e61923649)


____


<h3>Step 2:</h3>
<p> set a firewall rule on the server to block/deny inbound ICMP v4 traffic; then ping the domain controller from the client</p>

- custom rule type
- all programs
- icmp v4
- any ip addresses
- block the connection
- check boxes for domain, private, public
- name = block icmp v4 traffic

![2](https://github.com/user-attachments/assets/9f0f06e1-4bc0-4a1d-b0aa-35f7e1e4c8ab)


![3](https://github.com/user-attachments/assets/29ecf21a-1a04-465b-a70a-4e0bc3d2cdf1)

____

wireshark is showing that no response was found for ping and cmd is request timed out

![4](https://github.com/user-attachments/assets/ffd85b6a-d12d-49c8-990d-eb8d0de75cb4)


____
now disable the firewall rule to allow icmp v4 traffic

![5](https://github.com/user-attachments/assets/86204ee9-7273-4fc4-9cd7-ae584dcfc7f2)

![6](https://github.com/user-attachments/assets/53d3cc09-23ef-4437-a1bc-2b911ce6070f)


____


<h3>Step 3: </h3>
<p>SSH into the domain controller; then filter and observe SSH traffic only in Wireshark. make sure to have an ssh server running such as OpenSSH Server</p>


- ssh (USERNAME)@(HOSTNAME)
- ENTER PASSWORD FOR USERNAME

![7](https://github.com/user-attachments/assets/2eb02079-de1c-44b9-837a-71f956783b23)

____

- to verify ssh connection, use commands to navigate through the drive

to navigate into a directory
- cd (FOLDER NAME)

to navigate to the previous directory
- cd.. 

to check contents of the current directory
- dir




![8](https://github.com/user-attachments/assets/e0aa7a19-595c-423f-8eaa-535f7c38332f)


____

to end ssh session
- exit


![9](https://github.com/user-attachments/assets/eb461205-b4b2-4e4c-8634-d6cca90afcee)



____



<h3>Step 4: </h3>
<p>request a new ip address from DHCP via ipconfig /renew; then filter and observe DHCP traffic only in Wireshark</p>


![10](https://github.com/user-attachments/assets/99589e9d-b002-4175-8172-07cfcb7b208c)



____


<h3>Step 5: </h3>
<p>initiate DNS traffic via "nslookup (DOMAIN NAME)"; then filter and observe DNS traffic only in Wireshark</p>


![11](https://github.com/user-attachments/assets/0f986437-e9ae-4ca3-bcbc-640e25707b08)


____



<h2> Final Thoughts </h2>

<p> In closing, the "Firewall Rules & Inspecting Traffic" project streamlines our  .</p>
