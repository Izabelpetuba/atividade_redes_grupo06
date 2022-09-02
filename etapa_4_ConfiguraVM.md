CONFIGURAÇÃO DAS VMS
---------------------

PARTE 1: CONFIGURAÇÃO DAS NICS:
------------------------------------
  - Vamos logar na VM, para isso iremos alterar a NICs para o modo `Rede interna`, igualando à rede que nomeamos no passo anterior, lembra? Sim, `labredes`.
  
  ![3b0d25ec-08c4-424d-a66a-4a87cf064a33](https://user-images.githubusercontent.com/103438135/188139114-530be4c9-aa85-4593-b186-7f90b5d7aea0.jpg)

- Depois de confirmar, apenas inicie a máquina!

PARTE 2: LOGIN NA VM
-------------------------
  - Depois de iniciar a Vm, iremos logar como usuário administrador:
  
  |usuário: administrador|
  |---------------------|
  |senha: adminifal      |
  
  
 ![0bff0a38-cea2-460d-af4c-e86c14c9bd40](https://user-images.githubusercontent.com/103438135/188140452-2127f973-9b8d-4b02-99ba-89ec8b24f00e.jpg)
 
 - Agora que você está logado (lembre-se no seu Pc deve ter duas VMs, o processo de uma aplique a outra), iremos instalar os requisitos para fazer nosso trabalho, digite o comando:
 
  `sudo apt install net-tools -y`
  
  ![9f6d76ff-4a91-48ce-ad6e-a20ab78c4a7f](https://user-images.githubusercontent.com/103438135/188140969-81a60c4e-3a22-4705-b7ea-7792ce55f0eb.jpg)
  
  - Depois de finalizada, digite `ifconfig` que é um meio de você conferir se sua instalação foi efetivada e se esta está apta para o uso.
  
  - Por sua vez use o comando abaixo para organizar as interfaces que poderíamos vir a utlizar e por sua vez definindo seu local de instalação:
  
      `cat etc/netplan/01-netcfg.yaml`

      
  
PARTE 3: CONFIGURAÇÃO DOS ENDERSÇOS DE IP NA INTERFACE DA REDE
--------------------------------------------------------------

  - Efetue os seguintes comandos:
      `sudo nano /etc/netplan/01-netcfg.yaml` 
       - efetue este comando em todas as VMs.
       
       - Modifique o endereço de IP:
       `adresses: [192.168.13.IP/28]`
       - LEMBRE-SE DOS IPS DE SUA VM!!!!!
       
       - Por fim, depois de ter feito as modificações corrertas, salve-as atráves do atalho `ctrl+S` e depois `ctrl+x`
       
       
PARTE 4: CONFIGURE AS VMS

- Exemplo retirado da VM3:

![f9e6b9eb-ddc5-4351-ac45-a5916745a1af](https://user-images.githubusercontent.com/103438135/188144258-e618b906-0444-4f61-be1a-960f600b08e6.jpg)

Como o processo e as configurações são as mesmas, abaixo  seguem os IPS das VMs em coesão à seus respectivos PCs:
  - Lembre-se o gateway é o mesmo em todas as VMs!
  
  - PC1: 
    - VM1: addresses: [192.168.13.81/28]
    - VM2: addresses: [192.168.13.82/28]
  - PC2:
    -  VM1: addresses: [192.168.13.83/28]
    -  VM2: addresses: [192.168.13.84/28]
  - PC 3: (imagem acima)
  - PC4:
    -  VM1: addresses: [192.168.13.87/28]
    -  VM2: addresses: [192.168.13.88/28]

Lembre-se de salvar suas edições com `ctrl+S+X` em seguida utilize: 
  `sudo netplan apply`
  `ifconfig -a `
  
Por fim ping entre suas VMs de um mesmo PC (faça em todos) , como mostra a imagem:
![ad5edb1e-7cb7-4281-8a20-4cbb871fda78](https://user-images.githubusercontent.com/103438135/188148722-817c229d-24ca-4788-9070-cf2eca0534c4.jpg)
