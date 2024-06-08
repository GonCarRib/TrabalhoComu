Para dividir a rede 192.168.250.0/23 de forma que cada grupo tenha espaço suficiente, incluindo uma folga de 30%, exceto para os alunos que devem caber em um /24, precisamos calcular o número de IPs necessários para cada grupo e ajustar conforme necessário. 

Aqui estão os passos:

1. **Calcular o número de IPs necessários com a folga de 30%:**
   - Impressoras: 14 * 1.3 = 19
   - CCTVs: 13 * 1.3 = 17
   - TV: 6 * 1.3 = 8
   - AVAC: 9 * 1.3 = 12
   - Telefone: 33 * 1.3 = 43
   - Convidado: 6 * 1.3 = 8
   - Professor: 11 * 1.3 = 15
   - Alunos: 230 (sem folga, mas dentro de um /24 que fornece 256 IPs)
   - Gestão: 7 * 1.3 = 10
   - Acadêmicos: 10 * 1.3 = 13
   - Informática: 4 * 1.3 = 6

2. **Converter para potências de 2:**
   - Impressoras: 32 (5 bits)
   - CCTVs: 32 (5 bits)
   - TV: 16 (4 bits)
   - AVAC: 16 (4 bits)
   - Telefone: 64 (6 bits)
   - Convidado: 16 (4 bits)
   - Professor: 32 (5 bits)
   - Alunos: 256 (8 bits)
   - Gestão: 16 (4 bits)
   - Acadêmicos: 16 (4 bits)
   - Informática: 8 (3 bits)

3. **Ajustar os tamanhos das sub-redes:**
   - Impressoras: /27
   - CCTVs: /27
   - TV: /28
   - AVAC: /28
   - Telefone: /26
   - Convidado: /28
   - Professor: /27
   - Alunos: /24
   - Gestão: /28
   - Acadêmicos: /28
   - Informática: /29

4. **Dividir a rede 192.168.250.0/23:**
   - A rede 192.168.250.0/23 possui 512 IPs (9 bits de host).

Agora vamos dividir a rede:

**Divisão da rede 192.168.250.0/23:**

1. **Alunos:**
   - 192.168.250.0/24 (256 IPs)

2. **Impressoras:**
   - 192.168.251.0/27 (32 IPs)

3. **CCTVs:**
   - 192.168.251.32/27 (32 IPs)

4. **Telefone:**
   - 192.168.251.64/26 (64 IPs)

5. **Professor:**
   - 192.168.251.128/27 (32 IPs)

6. **TV:**
   - 192.168.251.160/28 (16 IPs)

7. **AVAC:**
   - 192.168.251.176/28 (16 IPs)

8. **Convidado:**
   - 192.168.251.192/28 (16 IPs)

9. **Gestão:**
   - 192.168.251.208/28 (16 IPs)

10. **Acadêmicos:**
    - 192.168.251.224/28 (16 IPs)

11. **Informática:**
    - 192.168.251.240/29 (8 IPs)

Somando todos, utilizamos 496 IPs dos 512 disponíveis no espaço de endereço 192.168.250.0/23.
