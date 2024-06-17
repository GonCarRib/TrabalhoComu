# Trabalho de Comunicaçao
 192.168.0.0/22
## Vlans
E1
```

en
conf t
vlan 10
name Alunos
exit
vlan 20
name Profs
exit
vlan 30
name ConcDeGestao
exit
vlan 40
name Informatica
exit
vlan 50
name ServAcademicos
exit
vlan 60
name GestaoRede
exit
vlan 70
name Telefone
exit
vlan 80
name Convidados
exit
Vlan 90
name CCTV
exit
Vlan 100
name Printer
exit
Vlan 110
name TV
exit
Vlan 120
name AVAC
exit
Vlan 130
name ServInte
exit
Vlan 947
name Native
exit

```


Total:

```
Impressoras: 14
CCTVs: 13
TV: 6
AVAC: 9
Telefone: 33
Convidado: 6
Professor: 11
Alunos: 230
Gestão: 7
Acadêmicos: 10
Informática: 4
```
```
access-list 101 permit tcp 192.168.0.0 0.0.0.255 host 192.168.1.133 eq 80
access-list 101permit tcp 192.168.2.128 0.0.0.127 host 192.168.1.133 eq 80
access-list 101 permit tcp 192.168.1.0 0.0.0.7 host 192.168.1.133 eq 80
access-list 101 permit tcp 192.168.3.0 0.0.0.15 host 192.168.1.133 eq 80
access-list 101 permit tcp 192.168.3.16 0.0.0.15 host 192.168.1.133 eq 80
access-list 101 permit tcp 192.168.3.32 0.0.0.15 host 192.168.1.133 eq 80
access-list 101 permit tcp 192.168.3.48 0.0.0.7 host 192.168.1.133 eq 80
access-list 101 deny   tcp any host 192.168.1.133 eq 80
access-list 101 deny ip any any


int g0/1
ip access-group 101 out
​```
