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
![2023-04-14_11-28-18](https://user-images.githubusercontent.com/122459067/231989161-97c95d95-7543-4af9-967d-95d2116cac3d.png)

##### Step 2: Disable DNS lookup.
![2023-04-14_10-55-08](https://user-images.githubusercontent.com/122459067/231981221-1b4f3910-d8c6-4ca8-9b44-fc794c436fa7.png)

![2023-04-14_10-56-57](https://user-images.githubusercontent.com/122459067/231981568-13d33962-6146-4363-be27-b5dd5c7e2f4b.png)

![2023-04-14_10-58-18](https://user-images.githubusercontent.com/122459067/231981887-65dca5e6-439c-4835-b2ca-47be969293f9.png)

##### Step 3: Configure basic settings for each router.

###### a.	Configure host names as shown in the topology.

###### b.	Configure the interface IP addresses as shown in the IP addressing table.

![2023-04-14_11-07-48](https://user-images.githubusercontent.com/122459067/231984168-6f4f3f80-764c-4895-9311-ba41a5d4617b.png)

![2023-04-14_11-08-38](https://user-images.githubusercontent.com/122459067/231984318-c172ef7e-d4a7-4dbb-80d8-cc97cf3f1551.png)

![2023-04-14_11-09-14](https://user-images.githubusercontent.com/122459067/231984455-a5fc0541-fe64-4ff0-b600-cd379b6b6532.png)

##### Step 4: Configure static routes on R1, R2, and R3.
###### a.	To achieve end-to-end IP reachability, proper static routes must be configured on R1, R2 and R3. R1 and R3 are stub routers, and as such, only need a default route pointing to R2. R2, behaving as the ISP, must know how to reach R1’s and R3’s internal networks before end-to-end IP reachability is achieved. Below is the static route configuration for R1, R2 and R3. On R1, use the following command:

![2023-04-14_11-12-25](https://user-images.githubusercontent.com/122459067/231985220-19236b41-4e0c-4605-be16-0582b66ee388.png)

###### b.	On R2, use the following commands.

![2023-04-14_11-13-47](https://user-images.githubusercontent.com/122459067/231985568-6986cea8-6f4a-4650-9f5a-0f697317ed1f.png)

###### c.	On R3, use the following command.

![2023-04-14_11-14-35](https://user-images.githubusercontent.com/122459067/231985823-c6a57bdc-aae0-49e2-97c8-04d214dfcaa1.png)

##### Step 5: Configure S3.

![2023-04-14_11-44-29](https://user-images.githubusercontent.com/122459067/231993048-1158deab-9982-4b21-a01b-9f2c704e1e49.png)

##### Step 6: Configure PC host IP settings.

![2023-04-14_11-52-40](https://user-images.githubusercontent.com/122459067/231995011-396ce395-3a56-4ff7-8a70-06e9279868cb.png)

![2023-04-14_11-54-30](https://user-images.githubusercontent.com/122459067/231995871-17127d5b-b0e4-4ba4-a6bf-60b3fc6ef932.png)

![2023-04-14_11-56-26](https://user-images.githubusercontent.com/122459067/231996349-f73089f5-b8a4-4ced-9453-8f265935e4ff.png)

##### Step 7: Verify basic network connectivity.

###### a.	Ping from R1 to R3. If the pings are not successful, troubleshoot the basic device configurations before continuing.

![2023-04-14_11-58-24](https://user-images.githubusercontent.com/122459067/231996849-9a51a634-b1de-4581-830b-c98c345f6f79.png)

###### b.	Ping from PC-A on the R1 LAN to PC-B and PC-C on the R3 LANs. If the pings are not successful, troubleshoot the basic device configurations before continuing.

![2023-04-14_12-00-17](https://user-images.githubusercontent.com/122459067/231997302-9b7eda10-7501-470d-bad1-f802a4025989.png)

##### Step 8: Configure a user account, encrypted passwords and crypto keys for SSH.
###### Note: Passwords in this task are set to a minimum of 10 characters, but are relatively simple for the benefit of performing the lab. More complex passwords are recommended in a production network.
###### a.	Configure a minimum password length using the security passwords command to set a minimum password length of 10 characters.
###### b.	Configure a domain name.
###### c.	Configure crypto keys for SSH
###### d.	Configure an admin01 user account using algorithm-type scrypt for encryption and a password of cisco12345.
###### e.	Configure line console 0 to use the local user database for logins. For additional security, the exec-timeout command causes the line to log out after 5 minutes of inactivity. The logging synchronous command prevents console messages from interrupting command entry.
###### f.	Configure line aux 0 to use the local user database for logins.
###### g.	Configure line vty 0 4 to use the local user database for logins and restrict access to SSH connections only.
###### h.	Configure the enable password with strong encryption.

![2023-04-14_12-04-40](https://user-images.githubusercontent.com/122459067/231999097-6fcd0881-780a-4e86-b5c5-e11799869aac.png)

##### Step 9:  Save the basic running configuration for all three routers.

![2023-04-14_12-06-31](https://user-images.githubusercontent.com/122459067/231999626-801839b2-3e6d-45fc-9e5a-19aaf4c140cc.png)

![2023-04-14_12-07-26](https://user-images.githubusercontent.com/122459067/231999869-18018d3d-6469-467a-b2f7-1d8cd9faf70f.png)

![2023-04-14_12-08-01](https://user-images.githubusercontent.com/122459067/231999992-2651eb23-cfa1-4ab8-bf79-c67b22c65384.png)

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
