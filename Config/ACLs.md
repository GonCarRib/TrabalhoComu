# RT-1

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

!ConcGestao -> Alunos Ed2
permit ip 192.168.3.16 0.0.0.15 192.168.2.128 0.0.0.127
permit icmp 192.168.3.16 0.0.0.15 192.168.2.128 0.0.0.127


int g0/1.10
ip access-group R2AclG01_10Out Out

------------------------------------------------------------

!RT-2 G0/1.20 out
ip access-list extended R2AclG01_20Out

!Alunos do Ed1 -> Professores Ed2
permit ip 192.168.0.0 0.0.0.255 192.168.3.0 0.0.0.15
permit icmp 192.168.0.0 0.0.0.255 192.168.3.0 0.0.0.15

!Professores do Ed1 -> Professores Ed2
permit ip 192.168.1.0 0.0.0.7 192.168.3.0 0.0.0.15
permit icmp 192.168.1.0 0.0.0.7 192.168.3.0 0.0.0.15

!Alunos do Ed2 -> Professores Ed2
permit ip 192.168.2.128 0.0.0.127 192.168.3.0 0.0.0.15
permit icmp 192.168.2.128 0.0.0.127 192.168.3.0 0.0.0.15

!Informatica do Ed2 -> Professores Ed2
permit ip 192.168.3.48 0.0.0.7 192.168.3.0 0.0.0.15
permit icmp 192.168.3.48 0.0.0.7 192.168.3.0 0.0.0.15

!Academico do Ed2 -> Professores Ed2
permit ip 192.168.3.32 0.0.0.15 192.168.3.0 0.0.0.15
permit icmp 192.168.3.32 0.0.0.15 192.168.3.0 0.0.0.15

!ConcGestao Ed2 -> Professores Ed2
permit ip 192.168.3.16 0.0.0.15 192.168.3.0 0.0.0.15
permit icmp 192.168.3.16 0.0.0.15 192.168.3.0 0.0.0.15


int g0/1.20
ip access-group R2AclG01_20Out Out

------------------------------------------------------------

!RT-2 G0/1.30 out
ip access-list extended R2AclG01_30out

!Informatica do Ed2 -> CooncGestao Ed2
permit ip 192.168.3.48 0.0.0.7 192.168.3.16 0.0.0.15
permit icmp 192.168.3.48 0.0.0.7 192.168.3.16 0.0.0.15


int g0/1.30
ip access-group R2AclG01_30Out Out

------------------------------------------------------------

!RT-2 G0/1.50 out
ip access-list extended R2AclG01_50Out

!Informatica do Ed2 -> Academico Ed2
permit ip 192.168.3.48 0.0.0.7 192.168.3.32 0.0.0.15
permit icmp 192.168.3.48 0.0.0.7 192.168.3.32 0.0.0.15


int g0/1.50
ip access-group R2AclG01_50Out Out

------------------------------------------------------------

!RT-2 G0/1.70 out
ip access-list extended R2AclG01_70Out

!Informatica do Ed2 -> Telefone do Ed2
permit ip 192.168.3.48 0.0.0.7 192.168.2.64 0.0.0.63
permit icmp 192.168.3.48 0.0.0.7 192.168.2.64 0.0.0.63


!Telefone do Ed1 -> Telefone do Ed2
permit ip 192.168.1.8 0.0.0.7 192.168.2.64 0.0.0.63
permit icmp 192.168.1.8 0.0.0.7 192.168.2.64 0.0.0.63



int g0/1.70
ip access-group R2AclG01_70Out Out

------------------------------------------------------------

!RT-2 G0/1.80 out
ip access-list extended R2AclG01_80Out

!Informatica do Ed2 -> Convidados do Ed2
permit ip 192.168.3.48 0.0.0.7 192.168.3.104 0.0.0.7
permit icmp 192.168.3.48 0.0.0.7 192.168.2.104 0.0.0.7


int g0/1.80
ip access-group R2AclG01_80Out Out

------------------------------------------------------------

!RT-2 G0/1.90 out
ip access-list extended R2AclG01_90Out

!Informatica do Ed2 -> Convidados do Ed2
permit ip 192.168.3.48 0.0.0.7 192.168.2.17 0.0.0.15
permit icmp 192.168.3.48 0.0.0.7 192.168.2.17 0.0.0.15


int g0/1.90
ip access-group R2AclG01_90Out Out

------------------------------------------------------------

!RT-2 G0/1.100 out
ip access-list extended R2AclG01_100Out

!Informatica do Ed2 -> Convidados do Ed2
permit ip 192.168.3.48 0.0.0.7 192.168.3.65 0.0.0.31
permit icmp 192.168.3.48 0.0.0.7 192.168.3.65 0.0.0.31


int g0/1.100
ip access-group R2AclG01_100Out Out

------------------------------------------------------------




```

# RT-DC
```
!Router DC g0/1.130 out
ip access-list extended RDcAclG01_130Out

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
ip access-group RDcAclG01_130Out out
```
