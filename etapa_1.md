IDENTIFICAR OS ENDEREÇOS IPs DA REDE E NOME DOS HOSTs
------------------------------------------------------

  Antes de iniciar o desenvolvimento do projeto é válido destacar que devemos criar uma tabela, afim de organizar os IPs de cada VM utilizada, oito ao todo. Destacamos, também que este grupo utilizou a Sub-rede, subdivisão lógica de uma rede de IPs, 192.168.13.[81-88]. Portanto, a partir desta Sub-rede podemos determinar alguns requisitos utilizados ao longo deste trabalho, sendo eles:
  
|   Sub-rede |  192.168.13.[81-88] |
| --- | --- |
|    Rede    |     192.168.13.81   |
|  Broadcast |     192.168.13.88   |
|   Gateway  |     192.168.13.00   |

  Por consoante,é válido reforçar que as VMs presentes nos quatro computadores utilizadas foram divididas da seguinte forma:
  
| VM |  Aluno |
| --- | --- |
| PC1| Izabel |
| PC2| Amauri |
| PC3| Kamilla|
| PC4| Viviane|

  A partir desta divisão, formaremos uma tabela conferindo cada IP de rede e nome de Hosts a seus respectivos usuários:
  
  Tabela 1: Identificação de endereços de IP e nome de seus respevtivos Hosts:
  
  | DESCRIÇÃO  |        IP      |       IP    |              FQN               |   Aliase |
  | ---------- | -------------- | ----------- | ------------------------------ | ---------|
  |   VM1-PC1  |  192.168.13.81 | srv-vm1-pc1 | vm1-pc1.grupo6-913.ifalara.net | Izabel1  |
  |   VM1-PC2  |  192.168.13.82 | srv-vm2-pc1 | vm2-pc1.grupo6-913.ifalara.net | Izabel2  |
  |   VM2-PC1  |  192.168.13.83 | srv-vm1-pc2 | vm1-pc2.grupo6-913.ifalara.net | Amauri1  |
  |   VM2-PC2  |  192.168.13.84 | srv-vm2-pc2 | vm2-pc2.grupo6-913.ifalara.net | Amauri2  |
  |   VM3-PC1  |  192.168.13.85 | srv-vm1-pc3 | vm1-pc3.grupo6-913.ifalara.net | Kamila1  | 
  |   VM3-PC2  |  192.168.13.86 | srv-vm2-pc3 | vm2-pc3.grupo6-913.ifalara.net | Kamila2  |
  |   VM4-PC1  |  192.168.13.87 | srv-vm1-pc4 | vm1-pc4.grupo6-913.ifalara.net | viviane1 |
  |   VM4-PC2  |  192.168.13.88 | srv-vm2-pc4 | vm2-pc4.grupo6-913.ifalara.net | viviane2 |
  
CONFIGURAÇÕES DE HARDWARE
---------------------------------

![imagem1_png](https://user-images.githubusercontent.com/103438135/188125574-96ffb5c4-5c0e-47fc-9c0c-6dafd584f6c7.png)

Esta foi a configuração utilizada em todas as máquinas, atente-se à:
 - Memória principal;
 - Memória de vídeo;
 - CPU;
 - Controladora;
 - Porta SATA/
 - Software utilizado na máquina: Linux e VirtualBox;
 - Softaware da VM: Net-tools, open ssh server;
 - Rede física: 
      -> 4 computadores - 8 VMs;
      -> 4 Cabos para os conectar ao switch;
