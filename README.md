# SSH Switch Configuration

### Objective

Simulate a console connection to a switch using Packet Tracer and understand and configure basic switch settings

### Skills Learned

- Learn to configure hostname, IP addresses, and passwords and setting up SSH
- Practice using show commands to verify switch configurations

### Tools Used

- Cisco Packet Tracer

### Steps

*Ref 1: Simulating the console connection using packet tracer. Using the blue console cable to connect the switch (console) to the pc (RS 232)*

![image](https://github.com/user-attachments/assets/d9022095-f27e-4564-a242-853d3803004e)

*Ref 2: Access the PC terminal to begin entering the command prompts to configure the switch*

![image](https://github.com/user-attachments/assets/396c1fd2-f75e-4be8-8ac1-9c7dcec92a88)

*Ref 3: Switch>enable (to get to privilaged exec role) then enter Switch#sh running-config. Should notice there's nothting configured since its a new switch*

![image](https://github.com/user-attachments/assets/7033fb60-7d17-4a26-9235-7bc84f4be793)

*Ref 4: To find the version of our switch enter Switch#sh version; 15.0(2)* 

![image](https://github.com/user-attachments/assets/cfe28d88-4fdc-4c3c-ba3e-8956244c18a9)

*Ref 5: Assign the switch hostname, enter Switch#config t > Switch(config)#hostname Switch01. Configure password encryption, Switch01(config)#service password-encryption (use this command to use encrypted that is stored in our configuration file because by default the password that's set on CISCO switches are stored in plain txt and configuration. This adds to the layer of protection when we are setting up passwords so they are encrypted. And to prevent anyone from easily reading the passwords when viewing the configuration file. Assign a secret password for privileged exec mode access, Switch01(config)#enable secret homelab. This sets up an encrypted password for our homelab*

![image](https://github.com/user-attachments/assets/26f8bd49-7050-45cb-b266-bc007cf3cab8)

*Ref 6: Won't be able to get privileged exec mode access without entering the password we created*

![image](https://github.com/user-attachments/assets/310a2619-8e99-4879-861d-4789accdfa00)

*Ref 7: Preventing unwanted DNS lookups, Switch01(config)# no ip domain-lookup. Disable DNS lookup to prevent the switch from wasting time trying to resolve incorrect commands and domain names.*

![image](https://github.com/user-attachments/assets/2106688a-8964-4df1-b508-d3542e89d170)

*Ref 8: Configure a MOTD (Message of the Day) banner. This banner is useful because it's used to communicate important information such as legal disclaimer or security policies. Switch01#conf t > Switch01(config)#banner motd # "Unauthorized access is strictly prohibited. #"*

![image](https://github.com/user-attachments/assets/750904a8-8252-42fd-9d6d-8ed559fe5ade)

*Ref 9: Configuring an IP address on Bill. VLAN1 is a default VLAN on most switches and when we assign an IP address to VLAN 1, it allows us to remotely manage the switch so we don't have to connect to our console cable anymore. Once we have configured our remote connection to the switch and we have given it an IP address.*

![image](https://github.com/user-attachments/assets/f3fc08d7-4323-4135-9f8f-0fc65bd5c9ab)

