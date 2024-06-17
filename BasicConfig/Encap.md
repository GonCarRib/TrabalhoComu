## E1
```

int g0/0.11
description AlunosE1
encapsulation dot1q 10
ip address 192.168.0.1 255.255.255.0

int g0/0.21
description ProfsE1
encapsulation dot1q 20
ip address 192.168.1.1 255.255.255.248

int g0/0.71
description TelefoneE1
encapsulation dot1q 70
ip address 192.168.1.9 255.255.255.248

int g0/0.81
description ConvidadosE1
encapsulation dot1q 80
ip address 192.168.1.49 255.255.255.240

```
## E2
```
int g0/0.12
description AlunosE2
encapsulation dot1q 10
ip address 192.168.2.129 255.255.255.128

int g0/0.22
description ProfsE2
encapsulation dot1q 20
ip address 192.168.3.1 255.255.255.240

int g0/0.32
description ConcDeGestaoE2
encapsulation dot1q 30
ip address 192.168.3.17 255.255.255.240


int g0/0.42
description InformaticaE2
encapsulation dot1q 40
ip address 192.168.3.49 255.255.255.248

int g0/0.52
description AcademicosE2
encapsulation dot1q 50
ip address 192.168.3.33 255.255.255.240

int g0/0.72
description TelefoneE2
encapsulation dot1q 70
ip address 192.168.2.41 255.255.255.192

int g0/0.82
description ConvidadosE2
encapsulation dot1q 80
ip address  192.168.3.105 255.255.255.248

```

## RC
```
int g0/0.130
description ServInternos
encapsulation dot1q 130
ip address 192.168.1.130 255.255.255.240

```

```
g0/1 
200.10.10.1/30

RT ISP
g0/0
200.10.10.1/30
```

```
rt isp
g0/2
200.10.10.5 /30


rt www
g0/0
200.10.10.6 /30
```

```
rt isp
g0/1
200.10.10.9 /30

rt cloud
g0/0
200.10.10.10 /30
```
```
REde www
200.20.20.0 /24
rt www
g0/1
rt.200.20.20.1 /24

pc
rt.200.20.20.2 /24
```

```
REde cloud
200.30.30.0 /24
rt cloud
g0/1
rt.200.30.30.1 /24

pc
rt.200.30.30.2 /24
```
