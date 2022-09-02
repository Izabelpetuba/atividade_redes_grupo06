USANDO O TERMINAL...
----------------------------

  A partir do passo anterior, basicamente a parte organizacional do trabalho, nesta em questão utilizaremos as máquinas propriamente ditas, detacamos que em razão dos passos a serem seguidos são iguais em todas as máquinas, utilizamos apenas imagens de uma máquina, mas reforçamos que estes serão iguais em todas as máquinas, independendo de sua VM.
  
  PASSO 1. LOGIN NA REDE:
  -----------------------
  - Abra o seu terminal e digite o seguinte comando: `su redes`
      Este comando é usado para mudar o usuário:
      
       | Senha: admin@Lab92|
       |----------------- |
       
      - Usuário anterior: aluno@LABREDES-VM.
      - Usuário atual (após o login): redes@LABREDES-VM
     
     ![alterarU](https://user-images.githubusercontent.com/103438135/188128649-df344876-3253-483d-9d62-017c542ea3b3.jpg)

PASSO 2. CRIAÇÃO DA PASTA LABREDES
---------------------------------
- Verifique se a pasta labredes e suas dependentes existem: `/labredes`
     ![diretorio](https://user-images.githubusercontent.com/103438135/188129214-654112c5-ee5b-4487-8403-6ff6aa7eccfd.jpg)
     
 - Criação o diretório: 
      -> Primeiro entre na raiz de seu diretório, digite o seguinte comando:  `cd /`
      -> Depois digite o comando `sudo mkdir /labredes` 
      
 - Agora que você entrou no diretório, crie as subpastas `images` e `original`:
 
      ![WhatsApp Image 2022-09-02 at 08 38 29](https://user-images.githubusercontent.com/103438135/188131736-dc4b106d-f438-4b4d-83bf-d52d80c2344c.jpeg)

 - Criar diretório pra máquina virtual, mas primeiro entre no diretório `cd /labredes` novamente:
      ![WhatsApp Image 2022-09-02 at 08 43 26](https://user-images.githubusercontent.com/103438135/188132541-63a56f37-159e-4eee-aa4e-79a32de2f148.jpeg)

  - No nosso trabalho:
  
  | PC1 | sudo mkdir izabel |
  |-----| ----------------- |
  | PC2 | sudo mkdir Amauri |
  | PC3 | sudo mkdir Kamila |
  | PC4 | sudo mkdir Viviane|
  
  - Adicione os integrantes do seu grupo de redes, para isso continue no terminal:
  
  ![2cda9312-6560-459e-be3a-acbafa3347dc](https://user-images.githubusercontent.com/103438135/188137083-1ec7c63e-3dfc-4783-b88e-5d2925aca272.jpg)

  Respectivamente, efetuamos a adição do aluno ao grupo de redes, seguida pela modificação de pertencimento, e por sua vez a alteração de proprietário.
  
  - Por fim, verificaremos a existencia das pastas e subpastas desenvolvidas.
  
    
  ![b590beb7-fb2a-4014-8c3f-57db86bbc970](https://user-images.githubusercontent.com/103438135/188137784-5f097083-64a0-4b84-8ace-f7a42a835c4e.jpg)
