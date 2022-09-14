SSH
-----
  Depois dos cabos estarem conectados, vamos conetar as VMs pelo meio lógico.
  
  PARTE 1: NOMEANDO O HOSTNAME:
  ----------------------------------
  
  - digite o código `sudo hostnamectl set-hostnaem <hostname>`
  
    1) VMs PC1:
    
        - VM1 PC1:
        ```sudo hostnamectl set-hostname srv-vm1-pc1```
        
        - VM2 PC1:
        ```sudo hostnamectl set-hostname srv-vm2-pc1```
      
      
    2) VMs PC2:
    
        - VM1 PC2:
        ```sudo hostnamectl set-hostname srv-vm1-pc2```
        
       - VM2 PC2:
        ```sudo hostnamectl set-hostname srv-vm2-pc2```
        
        
    3) VMs PC3:
    
        - VM1 PC3:
        ```sudo hostnamectl set-hostname srv-vm1-pc3```
        
       - VM2 PC3:
        ```sudo hostnamectl set-hostname srv-vm2-pc3```
        
        
    4) VMs PC4:
    
        - VM1 PC4:
        ```sudo hostnamectl set-hostname srv-vm1-pc4```
        
       - VM2 PC4:
        ```sudo hostnamectl set-hostname srv-vm2-pc4```
        
  PARTE 2: Instalar o SSH:
  ----------------------------------
   Antes de conectar os PCs, mude a conexão das VMs, mude de ponto-a-ponto para modo Bridge.
   1) Verifique se a internet está funcionando, use os comandos:
   
   ```
    sudo apt update
    sudo apt upgrade -y
    ```
    
   2) Instalar SSH:
   
   ```
    sudo apt-get install openssh-server
    ```
   
   3) Verificar se o ssh está ativado:
   
   ``systemctl status ssh``
   
   ![WhatsApp Image 2022-09-14 at 17 16 18](https://user-images.githubusercontent.com/103438135/190253640-f3fc9a09-4eaf-4868-972d-14422959ec56.jpeg)

   4) Verifique as portas do sistema:
   
   ``netstat -an | grep LISTEN.``
   
   ![WhatsApp Image 2022-09-14 at 17 15 33](https://user-images.githubusercontent.com/103438135/190253465-0797561c-f611-436d-9bce-dd37c14a554c.jpeg)

   
   5)Agora, para certificarnos que o controle de acesso do sistema estão exercendo corretamente sua funcionalidade, o comando ```` deve ser inserido para ativar o SSH no firewell UFW. Uma vez que ele isto for feito, as conexões SSH serão permitidas. Logo, use os comandos:
   
   ```
  sudo ufw allow ssh.
  sudo ufw status
  sudo ufw enable
  sudo ufw status
  ```
  
  ![WhatsApp Image 2022-09-14 at 17 17 40](https://user-images.githubusercontent.com/103438135/190253930-6ccbc1b1-250d-425e-9417-3959f63689aa.jpeg)

  
  6) Acessar uma vm remotamente:  
  
  Exemplo: $ ssh ``<user>``@``<ipServidorRemoto>``
  
  7) fazer login

  PARTE 3: ROTEIRO HOST-ONLY (SSH NO TERMINAL)
  ----------------------------------
* Abrir opção ``Host Network Manager`` dentro da aba ``Arquivo`` do Virtualbox ou ``ctrl + H``
* Criar novo adaptador de rede no botão ``Criar``
* Click na botão ``Propriedades`` --> ``Servidor DHCP`` --> click ``[]Habilitar Servidor``
* Entre em uma VM e digite ``ifconfig -a`` (necessita do ``sudo apt install net-tools`` antes de ser usado)
* Verifique se na saída do comando há o nome do adaptador de rede que foi criado
* Desligue a VM com ``sudo poweroff``
* Click no botão ``configurações`` --> ``Rede``
* Habilite um novo adaptador de rede clickando em ``Adaptador <n>`` --> ``[] Habilitar placa de rede``

* Iniciar VM
* Digite ``ifconfig -a``
* Verifique se na saída do comando há o nome do adaptador de rede que foi criado
* Execute ``cd /etc/netplan/``
* ``sudo nano <nome_do_arquivo>.yaml``
   * Adicione no arquivo:
      ```
      <nome_adaptador_de_rede>:
         dhcp4: true
      ```
* Execute ``sudo netplan apply``
* Verifique no ``ifconfig -a`` se as mudanças deram certo
* Abrir terminal do pc (sem ser da vm)
* ``ssh <user>@<ip>``

teste
---------------------

![WhatsApp Image 2022-09-02 at 09 13 11](https://user-images.githubusercontent.com/103438135/190254339-1cfdfe19-9dce-4ee9-b0fc-9e7039153f16.jpeg)
