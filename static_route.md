## Router have 3 types terminal
- A. User Execution Mode: `Router>enable`
- B. User Privileage Mode: `Router#configure terminal` [show, monitoring, save config, ping]
- C. Global Configuration Mode: `Router(config)#` [ip, route, password, encryption, hash encryption]

## Static IP Route:
#### IP Address Assign in R1:
- `Continue with configuration dialog? [yes/no]: no` [manual configuration]
- `Router>enable` [go to privilege mode]
- `Router#configure terminal` [go to global configuration mode]
- `Router(config)#hostname R1` [change hostname]
- `R1(config)#banner motd "Welcome"`
- `R1(config)#line console 0` [go to line console for set password at user previleage mode]
- `R1(config-line)#password cisco` [password is cisco]
- `R1(config-line)#login` [password needed at login]
- `R1(config-line)#exec-timeout 1`
- `R1(config-line)#exit`
- `R1(config)#enable password ccna` [password at global configuration mode]
- `R1(config)#service password-encryption` [all password will be normal encription, it's not required if use hash encryption]
- `R1(config)#enable secret abcd` [hash encription password at global configuration mode, hash encryption is best and get preference]
- `R1(config)#interface fastEthernet 0/0`
- `R1(config-if)#ip address 20.0.0.1 255.0.0.0`
- `R1(config-if)#no shutdown`
- `R1(config)#interface serial 0/0/0`
- `R1(config-if)#ip address 30.0.0.1 255.0.0.0`
- `R1(config-if)#clock rate 64000`
- `R1(config-if)#no shutdown`
- `R1(config)#ip route 20.0.0.0 255.0.0.0 30.0.0.2`
- `R1(config)#Ctrl+z`
- `R1#show version`
- `R1#show flash`
- `R1#show clock`
- `R1#show route`
- `R1#show running-config`
- `R1#show startup-config`
- `R1#copy running-config startup-config`
- `R1#exit`

#### IP Address Assign in R2:
- `Continue with configuration dialog? [yes/no]: no` [manual configuration]
- `Router>enable` [go to privilege mode]
- `Router#configure terminal` [go to global configuration mode]
- `Router#hostname R2` [change hostname]
- `R2(config)#banner motd "Welcome"`
- `R2(config)#line console 0` [password at user previleage mode]
- `R2(config-line)#password cisco` [password is cisco]
- `R2(config-line)#login` [password needed at login]
- `R2(config-line)#exec-timeout 1 30`
- `R2(config-line)#exit`
- `R2(config)#enable password ccna` [password at global configuration mode]
- `R2(config)#service password-encryption` [all password will be normal encription, it's not required if use hash encryption]
- `R2(config)#enable secret abcd` [hash encription password at global configuration mode, hash encryption is best and get preference]
- `R2(config)#interface fastEthernet 0/0`
- `R2(config-if)#ip address 20.0.0.1 255.0.0.0`
- `R2(config-if)#no shutdown`
- `R2(config)#interface serial 0/0/0`
- `R2(config-if)#ip address 30.0.0.2 255.0.0.0`
- `R2(config-if)#no shutdown`
- `R1(config)#ip route 10.0.0.0 255.0.0.0 30.0.0.1`
- `R2(config)#Ctrl+z`
- `R2#show ip route`
- `R2#show running-config`
- `R2#copy running-config startup-config`
- `R2#show startup-config`
- `R2#exit`

##### Remove ip route:
- `R1(config)#no ip route 210.0.0.0 255.0.0.0 30.0.0.2`
