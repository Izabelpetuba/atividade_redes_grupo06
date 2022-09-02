CONFIGURAÇÃO DAS VMS
---------------------

PARTE 1: CONFIGURAÇÃO DAS NICS:
------------------------------------
  - Vamos logar na VM, para isso iremos alterar a NICs para o modo 'Rede interna', igualando à rede que nomeamos no passo anterior, lembra? Sim, 'labredes'.
  
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
  'sudo apt install net-tools -y'
  
  ![9f6d76ff-4a91-48ce-ad6e-a20ab78c4a7f](https://user-images.githubusercontent.com/103438135/188140969-81a60c4e-3a22-4705-b7ea-7792ce55f0eb.jpg)
  
  - Depois de finalizada, digite 'ifconfig' que é um meio de você conferir se sua instalação foi efetivada e se esta está apta para o uso.
  
  - Por sua vez use o comando abaixo para organizar as interfaces que poderíamos vir a utlizar e por sua vez definindo seu local de instalação:
  
      cat /etc/netplan/01-netcfg.yaml
  
