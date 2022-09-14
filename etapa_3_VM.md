CRIANDO A VM ````
--------------------

PASSO 1: BAIXE O ARQUIVO OVA E ISO:
------------------------------------
  - Execute o seguinte comando: 
  
    ``scp aluno@192.168.101.10:~/Public/iso-images/ubuntu-server-mini.ova /labredes/images/original``
    
  - Crie uma nova:
    1) Se os arquivos ``.iso`` não foram instalados:
      1.2) Clique em novo no VirtualBox:
      
      ![WhatsApp Image 2022-09-14 at 16 02 14 (1)](https://user-images.githubusercontent.com/103438135/190246913-464a5bc5-f529-4b31-bb6d-bf64c33c1ac7.jpeg)
      
      1.2) Defina o tamanho da máquina, é recomendável que toda as máquinas tenham o mesmo tamanho:
      
      ![WhatsApp Image 2022-09-14 at 16 04 41 (1)](https://user-images.githubusercontent.com/103438135/190247095-31d48b5d-1bbf-49c4-ba76-d76d2c4190b3.jpeg)
      
      1.3) Crie a máquina:
      
      ![WhatsApp Image 2022-09-14 at 16 05 47 (1)](https://user-images.githubusercontent.com/103438135/190247246-4dcc9838-d00c-473d-b4f9-6caa380766c6.jpeg)


    2) Verificar se foram baixados, vá no terminal e use os comandos: ``ls -la``, em seguida ultilize os comandos ``sudo apt install virtualbox-ext-pack``
    
![0cae298e-07d6-41bb-ad30-91326155f07c](https://user-images.githubusercontent.com/103438135/190246619-47e7c790-bfce-4ac6-bbb2-41c1ea3c1d2a.jpg)


PASSO 2: IMPORTAÇÃO DE VM:
------------------------------------
1) Acesse a opção importar Applience:

![WhatsApp Image 2022-09-14 at 16 19 00](https://user-images.githubusercontent.com/103438135/190243383-cff91b26-64cb-419e-b03c-ffdfad34ac88.jpeg)

2) Procure o caminho do arquivo que vamos importar, (clique na caixinha amarela) ultilize o comando ``Outos locais > Computador > images > original >`` e por fim selecione o arquivo ubuntu;

![487c66ef-3a56-49ad-a4c1-0c5e43a02e51](https://user-images.githubusercontent.com/103438135/190244717-08e40807-95ee-4e18-aef5-da723d45e70b.jpg)

3) Ou insira o endereço do arquivo, digitando ``/labredes/images/original/ubuntu-server-mini.ova``

![WhatsApp Image 2022-09-14 at 16 21 36](https://user-images.githubusercontent.com/103438135/190243886-dc15d0ce-9632-4eb8-8d6d-6f54d5714db8.jpeg)

4) Depois de carregar, modifique o diretório onde nosso arquivo será salvo, lembre do padrão ``/labredes/VM/turma/aluno`` colocando em seguida o nome da VM;

![WhatsApp Image 2022-09-14 at 16 29 35](https://user-images.githubusercontent.com/103438135/190245226-c73c66f3-ab86-40d8-bcc3-7ff204cb98e3.jpeg)

5) Mude o caminho da máquina: 

![WhatsApp Image 2022-09-14 at 16 30 40](https://user-images.githubusercontent.com/103438135/190245489-8971a6ce-8a63-4db0-a127-c119507f79df.jpeg)

Faça isso em todas as VMs ou as clone;
