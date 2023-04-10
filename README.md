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
