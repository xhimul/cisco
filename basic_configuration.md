## Router have 3 types terminal
- 1. User Execution Mode: `Router>enable`
- 2. User Privileage Mode: `Router#configure terminal`  [show, monitoring, save config, ping]
- 3. Global Configuration Mode: `Router(config)#`

- `Router>enable`
- `Router#configure terminal`



### 3. User Configuration Mode: Router(config)#

#### Router Name Change
- `Router(config)#hostname testrouter1`

#### Password Assign [for user execution mode]:
- `Router(config)#line console 0`
- `Router(config-line)#password cisco`
- `Router(config-line)#login`


### 2. User Privileage Mode: Router#

#### See Running Configuration:
- `Router#show running-config`

#### See Startup Configuration:
- `Router#show startup-config`

#### Save Running to Startup:
- `Router#copy running-config startup-config`

#### Password Assign [for user previleage mode]:
- Router(config)#enable password ccna

#### Password Encrypt [for user previleage mode]:
- `Router(config)#service password-encryption`

#### Password Hash Encrypt [for user previleage mode]:
- `Router(config)#enable secret abcd` [hash hncription password get the preference]

#### Jump to Priviledge Mode:
- `Router(config)#Ctrl+z`

#### IP Address Assign in Serial Interface:
- `Router>enable`
- `Router#configure terminal`
- `Router(config)#interface serial 0/0/0`
- `Router(config-if)#ip address 20.0.0.1 255.0.0.0`
- `Router(config-if)#clock rate 64000`
- `Router(config-if)#no shutdown`

## Static IP Route:
#### IP Address Assign in R1:
- `Continue with configuration dialog? [yes/no]: no'
- `Router>enable`
- `Router#configure terminal`
- `Router#hostname R1
- `R1(config)#interface fastEthernet 0/0`
- `R1(config-if)#ip address 20.0.0.1 255.0.0.0`
- `R1(config-if)#no shutdown`
- `R1(config)#interface serial 0/0/0`
- `R1(config-if)#ip address 30.0.0.1 255.0.0.0`
- `R1(config-if)#clock rate 64000`
- `R1(config-if)#no shutdown`
- `R1(config)#ip route 20.0.0.0 255.0.0.0 30.0.0.2`
- `R1(config)#Ctrl+z`
- `R1#show ip route`
- `R1#show running-config`
- `R1#copy running-config startup-config`
- `R1#show startup-config`
- `R1#exit`

#### IP Address Assign in R2:
- `Continue with configuration dialog? [yes/no]: no'
- `Router>enable`
- `Router#configure terminal`
- `Router#hostname R2
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

#### Show Routing Table:

#### Create Static Route:
