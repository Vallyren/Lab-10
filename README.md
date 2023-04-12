# Lab10
## Configure ZPFs
### Topology
![2023-04-10_15-46-27](https://user-images.githubusercontent.com/122459067/230904037-00127cfa-1985-4c49-831f-03cab464ca5f.png)
### IP Addressing Table
![2023-04-10_15-47-36](https://user-images.githubusercontent.com/122459067/230904167-467a2b1e-129b-4ca8-bf72-fab867cc2aec.png)
### Objectives
#### Part 1: Basic Device Configuration
In this part of this lab, you set up the network topology and configure basic settings, such as the interface IP addresses, static routing, device access, and passwords.
Note: All tasks should be performed on routers R1, R2, and R3. The procedures are shown for only one of the routers.

##### Step 1: Cable the network as shown in the topology.
![2023-04-10_16-44-27](https://user-images.githubusercontent.com/122459067/230913195-7e8fdb62-3d23-4037-9a70-eceaa15b297e.png)

##### Step 2: Disable DNS lookup.
![2023-04-10_16-46-14](https://user-images.githubusercontent.com/122459067/230913485-ed1ac971-1525-4802-8a4e-7c176fb70565.png)

![2023-04-10_16-47-38](https://user-images.githubusercontent.com/122459067/230913707-c9f73a9a-e231-4e24-97ab-34dcb60192ad.png)

![2023-04-10_16-48-35](https://user-images.githubusercontent.com/122459067/230913878-3fe3a496-8917-4ee6-a655-a1525b0879fe.png)

##### Step 3: Configure basic settings for each router.

###### a.	Configure host names as shown in the topology.

###### b.	Configure the interface IP addresses as shown in the IP addressing table.

![2023-04-10_16-55-50](https://user-images.githubusercontent.com/122459067/230915362-16ad92ab-cb4f-4893-8b46-07f60e36532a.png)

![2023-04-10_16-56-39](https://user-images.githubusercontent.com/122459067/230915485-38c42c4f-f3f0-43c7-b9f5-fdf508c1a7cd.png)

![2023-04-10_16-57-20](https://user-images.githubusercontent.com/122459067/230915616-bf5f6ee9-9e05-4794-b88c-020f35f7db21.png)

##### Step 4: Configure static routes on R1, R2, and R3.
###### a.	To achieve end-to-end IP reachability, proper static routes must be configured on R1, R2 and R3. R1 and R3 are stub routers, and as such, only need a default route pointing to R2. R2, behaving as the ISP, must know how to reach R1’s and R3’s internal networks before end-to-end IP reachability is achieved. Below is the static route configuration for R1, R2 and R3. On R1, use the following command:

![2023-04-10_17-32-37](https://user-images.githubusercontent.com/122459067/230922226-9d2088ce-dc60-4c98-9a78-b7940fd16878.png)

###### b.	On R2, use the following commands.

![2023-04-10_17-34-14](https://user-images.githubusercontent.com/122459067/230922523-b6e3472b-76fd-4199-90b2-b158ff778d00.png)

###### c.	On R3, use the following command.

![2023-04-10_17-35-25](https://user-images.githubusercontent.com/122459067/230922753-f3246f68-f14e-4899-adb2-243166920cdf.png)

##### Step 5: Configure S3.

![2023-04-10_17-40-29](https://user-images.githubusercontent.com/122459067/230924584-0e3ccbc7-3e5a-4fd7-a23b-cf17974b1dc7.png)

![2023-04-10_17-44-24](https://user-images.githubusercontent.com/122459067/230924599-9847d0f0-95ec-4198-b476-07f564b8effa.png)

##### Step 6: Configure PC host IP settings.

![2023-04-10_16-52-13](https://user-images.githubusercontent.com/122459067/230920417-541ab9eb-2096-49bc-ac9b-276e6907cce5.png)

![2023-04-10_17-25-14](https://user-images.githubusercontent.com/122459067/230920825-6a9174fd-ba50-4547-98ed-b013cc048a75.png)

![2023-04-10_17-26-27](https://user-images.githubusercontent.com/122459067/230921020-cffe3c99-8a22-490b-bbfc-c1efb976e5f0.png)

##### Step 7: Verify basic network connectivity.

###### a.	Ping from R1 to R3. If the pings are not successful, troubleshoot the basic device configurations before continuing.

![2023-04-10_17-48-19](https://user-images.githubusercontent.com/122459067/230925367-21fb1a3f-af86-4c30-9e63-581f82d2e73f.png)

###### b.	Ping from PC-A on the R1 LAN to PC-B and PC-C on the R3 LANs. If the pings are not successful, troubleshoot the basic device configurations before continuing.

![2023-04-10_17-51-17](https://user-images.githubusercontent.com/122459067/230925913-f92afae6-6cae-4b42-a9ff-43108842096b.png)

##### Step 8: Configure a user account, encrypted passwords and crypto keys for SSH.
###### Note: Passwords in this task are set to a minimum of 10 characters, but are relatively simple for the benefit of performing the lab. More complex passwords are recommended in a production network.
###### a.	Configure a minimum password length using the security passwords command to set a minimum password length of 10 characters.
###### b.	Configure a domain name.
###### c.	Configure crypto keys for SSH

![2023-04-12_15-03-15](https://user-images.githubusercontent.com/122459067/231451482-bdc9deb9-8cce-4724-b5c2-9ca8ff35f0ed.png)

###### d.	Configure an admin01 user account using algorithm-type scrypt for encryption and a password of cisco12345.

![2023-04-12_15-05-31](https://user-images.githubusercontent.com/122459067/231451927-25e5ad5d-1c2b-4abc-95fc-f7f9c87b8f27.png)

###### e.	Configure line console 0 to use the local user database for logins. For additional security, the exec-timeout command causes the line to log out after 5 minutes of inactivity. The logging synchronous command prevents console messages from interrupting command entry.

![2023-04-12_15-08-29](https://user-images.githubusercontent.com/122459067/231452449-c79b4083-2e43-4944-a791-3489c3548fe4.png)

###### f.	Configure line aux 0 to use the local user database for logins.

![2023-04-12_15-09-55](https://user-images.githubusercontent.com/122459067/231452806-c3822088-b544-43b7-b9ec-72c937b3b077.png)

###### g.	Configure line vty 0 4 to use the local user database for logins and restrict access to SSH connections only.

![2023-04-12_15-11-28](https://user-images.githubusercontent.com/122459067/231453192-54cd1b4a-a477-4f21-a380-5a7f2bf2fabc.png)

###### h.	Configure the enable password with strong encryption.

![2023-04-12_15-13-15](https://user-images.githubusercontent.com/122459067/231453629-4d63e081-90da-4566-8a7e-d46df1ad8b14.png)

##### Step 9:  Save the basic running configuration for all three routers.

![2023-04-12_15-14-49](https://user-images.githubusercontent.com/122459067/231457029-9ec9f396-54b5-4d57-bec8-d15cb23bb6be.png)

![2023-04-12_15-15-40](https://user-images.githubusercontent.com/122459067/231457055-47ee53c4-8220-43f1-9bbe-a924c40a0ae2.png)

![2023-04-12_15-28-26](https://user-images.githubusercontent.com/122459067/231457095-c13446a3-f5dd-4d1c-9bf7-9e46f5e24db9.png)

#### Part 2: Configuring a Zone-Based Policy Firewall (ZPF)

##### Step 1: Verify end-to-end network connectivity.

###### a.	Ping from R1 to R3 using both of R3’s G0/0/1 interface IP addresses (192.168.3.1 and 192.168.33.1).

![2023-04-12_16-46-48](https://user-images.githubusercontent.com/122459067/231477734-d73b9e5c-98b0-47da-b973-dc1d1336a942.png)

###### b.	Ping from PC-A on the R1 LAN to PC-C on the R3 conference room LAN.

![2023-04-12_16-47-50](https://user-images.githubusercontent.com/122459067/231478040-1dc276ee-95f7-4ae5-bbd3-a65403ca0e67.png)

###### c.	Ping from PC-A on the R1 LAN to PC-B on the R3 internal LAN.

![2023-04-12_16-48-44](https://user-images.githubusercontent.com/122459067/231478257-dfba8aba-cf0f-4d5b-852c-d2ca1440de5d.png)

##### Step 2: Display the R3 running configurations.

###### a.	Issue the show ip interface brief command on R3 to verify the correct IP addresses were assigned. Use the Address Table to verify the addresses.

![2023-04-12_16-51-12](https://user-images.githubusercontent.com/122459067/231479059-54bd2eea-7c7e-4e0d-b870-85c3b7ffbffc.png)

![2023-04-12_16-51-34](https://user-images.githubusercontent.com/122459067/231479104-f67021ea-fcae-4fbf-b42b-73ab65a94693.png)

###### b.	Issue the show ip route command on R3 to verify it has a static default route pointing to R2’s G0/0/1 interface.

![2023-04-12_16-53-08](https://user-images.githubusercontent.com/122459067/231479900-7ca8184c-ed50-4217-8c5b-5288fa6cdce8.png)

###### c.	Issue the show run command to review the current basic configuration on R3.

![2023-04-12_16-56-06](https://user-images.githubusercontent.com/122459067/231480430-1dd1a5d0-28d7-4fa5-be5b-f3a6d8fec761.png)

![2023-04-12_16-56-27](https://user-images.githubusercontent.com/122459067/231480461-d8857502-8cce-4b6d-9b29-de3844474ca3.png)

##### Step 3: Creating the security zones.

###### A security zone is a group of interfaces with similar security properties and requirements. For example, if a router has three interfaces connected to internal networks, all three interfaces can be placed under the same zone named “internal”. Because all security properties are configured to the zone instead of to the individual router interfaces, the firewall design is much more scalable.
###### In this lab, the R3 site has three interfaces; one connected to an internal trusted network, one connected to the conference room network and another connected to the internet. Because all three networks have different security requirements and properties, we will create three different security zones.
###### Security zones are created in global configuration mode, and the command allows for zone name definition. In R3, create three zones named INSIDE, CONFROOM and INTERNET:

![2023-04-12_16-59-32](https://user-images.githubusercontent.com/122459067/231481389-7b53743a-7280-4424-9f4b-8eab35f7d03d.png)

##### Step 4: Creating Security Policies

###### a.	Create an inspect class-map to match traffic to be allowed from the INSIDE zone to the INTERNET zone. Because we trust the INSIDE zone, we allow all the main protocols.
###### b.	Similarly, create a class-map to match the traffic to be allowed from the CONFROOM zone to the INTERNET zone. Because we do not fully trust the CONFROOM zone, we must limit what the server can send out to the Internet:
###### c.	Now that the class-maps are created, you can create the policy-maps.

![2023-04-12_17-08-37](https://user-images.githubusercontent.com/122459067/231483956-7db65ee6-6cf3-4243-9383-176ccf7491b2.png)

##### Step 5: Create the Zone Pairs

###### a.	Creating the zone-pairs:
###### b.	Verify the zone-pairs were correctly created by issuing the show zone-pair security command. Notice that no policies are associated with the zone-pairs yet. The security policies will be applied to zone-pairs in the next step.

![2023-04-12_17-11-07](https://user-images.githubusercontent.com/122459067/231484505-985d28e0-6607-41fa-8084-b67c8325af53.png)

##### Step 6: Applying Security Policies

###### a.	As the last configuration step, apply the policy-maps to the zone-pairs
###### b.	Issue the show zone-pair security command once again to verify the zone-pair configuration. Notice that the service-polices are now displayed:

![2023-04-12_17-15-54](https://user-images.githubusercontent.com/122459067/231485975-07fa0878-3f26-46a4-b6cd-4b90b5c13f8b.png)

###### c.	To obtain more information about the zone-pairs, their policy-maps, the class-maps and match counters, use the show policy-map type inspect zone-pair command

![2023-04-12_17-32-05](https://user-images.githubusercontent.com/122459067/231490688-431900da-de1f-484c-8107-f7e93c2fae25.png)

##### Step 7: Assign Interfaces to the Proper Security Zones

###### a.	Assign R3’s G0/0 to the CONFROOM security zone:



###### b.	Assign R3’s G0/1 to the INSIDE security zone:

###### c.	Assign R3’s S0/0/1 to the INTERNET security zone:
