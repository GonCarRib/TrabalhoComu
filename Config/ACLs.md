#RT-1

# RT-2
```
!RT-2 G0/1.10 out
ip access-list extended R2AclG01_10Out

!Alunos do Ed1 -> Alunos Ed2 
permit ip 192.168.0.0 0.0.0.255 192.168.2.128 0.0.0.127
permit icmp 192.168.0.0 0.0.0.255 192.168.2.128 0.0.0.127

!Professores do Ed1 -> ALunos Ed2 
permit ip 192.168.1.0 0.0.0.7 192.168.2.128 0.0.0.127
permit icmp 192.168.1.0 0.0.0.7 192.168.2.128 0.0.0.127

!Professores do Ed2 -> Alunos Ed2
permit ip 192.168.3.0 0.0.0.15 192.168.2.128 0.0.0.127
permit icmp 192.168.3.0 0.0.0.15 192.168.2.128 0.0.0.127

!Informatica do Ed2 -> Alunos Ed2
permit ip 192.168.3.48 0.0.0.7 192.168.2.128 0.0.0.127
permit icmp 192.168.3.48 0.0.0.7 192.168.2.128 0.0.0.127

!Academico do Ed2 -> Alunos Ed2
permit ip 192.168.3.32 0.0.0.15 192.168.2.128 0.0.0.127
permit icmp 192.168.3.32 0.0.0.15 192.168.2.128 0.0.0.127

!Academico do ConcGestao -> Alunos Ed2
permit ip 192.168.3.16 0.0.0.15 192.168.2.128 0.0.0.127
permit icmp 192.168.3.16 0.0.0.15 192.168.2.128 0.0.0.127


int g0/1.10
ip access-group R2AclG01_10Out Out
```

# RT-DC
```
!Router DC g0/1.10 out
ip access-list extended RDcAclG01Out
!Alunos do Ed1 -> ServerWeb 
permit tcp 192.168.0.0 0.0.0.255 host 192.168.1.133 eq 80
permit tcp 192.168.0.0 0.0.0.255 host 192.168.1.133 eq 443

!Ed1 -> DHCP 
permit udp 192.168.0.0 0.0.3.255 host 192.168.1.131 eq bootps
permit udp 192.168.0.0 0.0.3.255 host 192.168.1.131 eq bootpc

!Alunos do Ed1 -> DNS 
permit udp 192.168.0.0 0.0.0.255 host 192.168.1.132 eq 53

!Alunos deny ligacao ha internet
deny ip 192.168.0.0 0.0.0.255 192.168.0.0 0.0.255.255

!Permitir alunos falarem com qualquer coisa
permit ip 192.168.0.0 0.0.0.255 any

deny tcp any any
deny udp any any
deny icmp any any

int g0/1.130
ip access-group RDcAclG01Out out
```
