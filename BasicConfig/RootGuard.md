Root Guard
```
E1-B2-S2(config)#interface gigabitEthernet 0/1
E1-B2-S2(config-if)#spanning-tree guard root
```
```
E1-B2-S1(config)#interface fastEthernet 0/1
E1-B2-S1(config-if)#spanning-tree guard root
```
```
E1-B2-S3(config)#interface f0/1 
E1-B2-S3(config-if)#spanning-tree guard root
```
```
E1-B1-S4(config)#interface gigabitEthernet 0/1
E1-B1-S4(config-if)#spanning-tree guard root
```
```
E2-B2-S1(config)#interface gigabitEthernet 0/1
E2-B2-S1(config-if)#spanning-tree guard root
```
```
E2-B2-S3(config)#interface gigabitEthernet 0/1
E2-B2-S3(config-if)#spanning-tree guard root
```
