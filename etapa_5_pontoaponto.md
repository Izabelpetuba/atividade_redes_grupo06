MONTE UMA REDE PONTO A PONTO FÍSICA ENTRE SEUS 4 PCS E UMA LAN LÓGICA COM 8 VMs
-----------------------------------------------------------------------------

PARTE 1: CONEXÃO DOS CABOS ATRÁVES DO SWITCH
----------------------------------------------
![61f874bd-6c5a-4314-b730-0556afdd54ed](https://user-images.githubusercontent.com/103438135/188149443-f4e7ff3b-97a5-4b4e-b623-65ce2016d6a1.jpg)

  - Lembre-se de colocar sua VM em modo bridge, altere nas configurações da VM:

  ![3926ac14-2e7e-48be-9f48-81c28f212eae](https://user-images.githubusercontent.com/103438135/188149869-e203ce49-6926-4bb6-9077-723028954f9b.jpg)

  - Altere, também o endereço MAC,gerando outro endereço, afim de evitar a padronização intríssica dos endereços das VMs:
  
  ![d4bb334f-bc61-4494-b254-3fe1c68d511c](https://user-images.githubusercontent.com/103438135/188150442-32ddf242-8ebb-406f-ac85-f4d0d9ae2434.jpg)

- Configure a NIC: 
   ![8091b3f2-17cc-4e89-9606-45d12a2fe345](https://user-images.githubusercontent.com/103438135/188150660-c9b60c0a-e205-4428-9183-751efb34b710.jpg)
   
- Por fim, ping entre as VMs, verificando suas conexões.   
