# FASE2-VPN
Monitoramento VPN FASE 2 Fortigate
1° Passo: Add o template anexado no projeto
2° Passo: Crie um host NO Zabbix com o mesma nomenclatura do Firewall Fortigate. Ex: FW-02 (Nome que está no meu FW)
3° Passo: Add o IP do Firewall com a interface SNMP
4° Passo: Crie uma regra de descoberta com a chave: MM-NB-PE07BD75, tipo: Agent SNMP, Snmp OID: discovery[{#SNMPVALUE},.1.3.6.1.4.1.12356.101.12.2.2.1.3]
5° Passo: Criei um protótipo de item com a chave: fgVpnTunEntStatus[{#SNMPVALUE}], tipo: agente snmp, snmp OID: 1.3.6.1.4.1.12356.101.12.2.2.1.20.{#SNMPINDEX}, numero inteiro sem sinal

Feito:

Agora é só esperar o monitoramento coletar a informações de toda fase 2 que vc possui no seu Firewall Avançado (Fortigate)
