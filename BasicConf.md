```
en
conf t
hostname Admin
no ip domain-lookup
service password-encryption
banner motd #Unauthorized access is prohibited#
clock set 11:18:00 apr 24 2024
copy running-config startup-config  
```