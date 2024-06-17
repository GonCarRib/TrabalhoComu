```
Edifício 1 (E1)

    ALUNOS: vlan 10
        Necessidade: 130 IPs
        Sub-rede: 192.168.0.0/24 (256 endereços, 254 utilizáveis)

    PROFESSORES: vlan 20
        Necessidade: 3 IPs
        Sub-rede: 192.168.1.0/29 (8 endereços, 6 utilizáveis, 192.168.1.1 a 192.168.1.6)

    TELEFONES: vlan 70
        Necessidade: 4 IPs
        Sub-rede: 192.168.1.8/29 (8 endereços, 6 utilizáveis, 192.168.1.9 a 192.168.1.14)

    IMPRESSORAS: Vlan 100
        Necessidade: 3 IPs
        Sub-rede: 192.168.1.16/29 (8 endereços, 6 utilizáveis, 192.168.1.17 a 192.168.1.22)

    CCTV: Vlan 90
        Necessidade: 5 IPs
        Sub-rede: 192.168.1.24/29 (8 endereços, 6 utilizáveis, 192.168.1.25 a 192.168.1.30)

    AVAC: Vlan 120
        Necessidade: 3 IPs
        Sub-rede: 192.168.1.32/29 (8 endereços, 6 utilizáveis, 192.168.1.33 a 192.168.1.38)

    CONVIDADOS: Vlan 80
        Necessidade: 5 IPs
        Sub-rede: 192.168.1.48/28 (16 endereços, 14 utilizáveis, 192.168.1.49 a 192.168.1.62)

Edifício 2 (E2)
    TVs: Vlan 110
        Necessidade: 7 IPs
        Sub-rede: 192.168.2.0/28 (16 endereços, 14 utilizáveis, 192.168.2.1 a 192.168.2.14)

    CCTVs: Vlan 90
        Necessidade: 11 IPs
        Sub-rede: 192.168.2.16/28 (16 endereços, 14 utilizáveis, 192.168.2.17 a 192.168.2.30)

    TELEFONES: vlan 70
        Necessidade: 38 IPs
        Sub-rede: 192.168.2.64/26 (64 endereços, 62 utilizáveis, 192.168.2.65 - 192.168.2.126)

    ALUNOS: vlan 10
        Necessidade: 100 IPs
        Sub-rede: 192.168.2.128/25 (128 endereços, 126 utilizáveis, 192.168.2.129 a 192.168.2.254)

    PROFESSORES: vlan 20
        Necessidade: 11 IPs
        Sub-rede: 192.168.3.0/28 (16 endereços, 14 utilizáveis, 192.168.3.1 a 192.168.3.14)

    PC GESTÃO: vlan 30
        Necessidade: 10 IPs
        Sub-rede: 192.168.3.16/28 (16 endereços, 14 utilizáveis, 192.168.3.17 a 192.168.3.30)

    PC ACADÊMICO: vlan 50
        Necessidade: 13 IPs
        Sub-rede: 192.168.3.32/28 (16 endereços, 14 utilizáveis, 192.168.3.33 a 192.168.3.46)

    PC INFORMÁTICA: vlan 40
        Necessidade: 4 IPs
        Sub-rede: 192.168.3.48/29 (8 endereços, 6 utilizáveis, 192.168.3.49 a 192.168.3.54)

    AVAC: Vlan 120
        Necessidade: 8 IPs
        Sub-rede: 192.168.3.112/28 (16 endereços, 14 utilizáveis, 192.168.3.113 - 192.168.3.126)

    IMPRESSORAS: Vlan 100
        Necessidade: 15 IPs
        Sub-rede: 192.168.3.64/27 (32 endereços, 30 utilizáveis, 	192.168.3.65 - 192.168.3.94)

    PC CONVIDADO: vlan 80
        Necessidade: 3 IPs
        Sub-rede: 192.168.3.104/29 (8 endereços, 6 utilizáveis, 192.168.3.105 a 192.168.3.110)



```

```
DataCenter (DC)
    ServInternos
      Necessidade: 7 IPs
      Sub-rede: 192.168.1.129/28 (16 endereços, 14 utilizáveis, 192.168.1.130 a 192.168.1.145)

```
```
Ip Ineterfaces de cada router
    RT-DC
    192.168.1.201/30 G0/1/0
    192.168.1.205/30 G0/2/0

    RT-1
    192.168.1.209/30 G0/0/0
    192.168.1.213/30 G0/1/0
    

    RT-2
    192.168.1.217/30 G0/0/0
    192.168.1.221/30 G0/1/0
    

```




