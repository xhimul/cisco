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

#### IP Address Assign in Interface:
- `Router(config)#interface fastEthernet 0/0`
- `Router(config-if)#ip address 10.0.0.1 255.0.0.0`
- `Router(config-if)#no shutdown`

#### IP Address Assign in Serial Interface:
- `Router(config)#interface serial 0/0/0`
- `Router(config-if)#ip address 20.0.0.1 255.0.0.0`
- `Router(config-if)#clock rate 64000`
- `Router(config-if)#no shutdown`


#### Show Routing Table:

#### Create Static Route:
