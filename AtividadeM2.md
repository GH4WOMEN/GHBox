# Laboratório – Módulo 2: Trabalhando com repositórios GitHub

A atividade a seguir visa consolidar o conhecimento apresentado na aula, abordando os seguintes tópicos:

- Criação de repositório
- Adição de arquivos
- Adição de branch
- Clone de repositório

### Requisitos:

- Conta GitHub

## 1. Criando Repositório

1. Acesse [github.com](https://github.com) no seu navegador e faça login em sua conta (clique no botão “Sign In” localizado no canto superior direito).

2. Clique no botão sinalizado com “+”, posicionado na parte superior da tela e selecione “New Repository” ou no botão "New" do lado esquerdo.

![image](https://github.com/user-attachments/assets/4661c003-746d-47f9-99b2-614821a45fcd)

3. Na página recém aberta, configure as seguintes informações:
   - **Repository Owner**
   - **Repository Name**
   - **Description**
   - **Defina a visibilidade do repositório:** público ou privado
     
![image](https://github.com/user-attachments/assets/dc823f19-f554-47f1-9564-54f8e32e00bc)

> Repare que na imagem não existe a opção “Internal”, isso ocorre pois tal opção está disponível apenas nas contas Enterprise. 

-  Avançando na página temos a seção “Initialize this repository with”, nela, trabalhamos itens como os arquivos README e .gitignore e o licenciamento. Nessa etapa:
- 	Marque a caixa de seleção “Add a README file”
- 	Selecione a opção “None” na lista suspensa de GitIgnore
- 	Selecione a opção MIT License na lista suspensa de licenças
   
![image](https://github.com/user-attachments/assets/4b44303e-8a02-4dee-8ed0-52508956a584)


4. Clique em “Create Repository”

Pronto, o novo repositório foi criado! 😃

Perceba que até essa etapa temos 2 arquivos no nosso repositório, são eles LICENSE e README.md, ambos localizados no ramo (branch) “main”.

## 2. Adicionando arquivos

Nesta etapa, adicionaremos novos arquivos, para isso abordaremos de duas maneiras distintas: através da interface e via linha de comando.

### 2.1 Adicionando arquivos através da interface

1. Ainda no seu navegador (tela do repositório criado), clique no botão sinalizado com “+” ou “Add file”, posicionado na parte central da tela e selecione “Upload Files”

**Informação:** Caso você não esteja na página do seu repositório, você poderá acessá-la através da url no seguinte padrão:

`github.com/<proprietario>/<nomeRepositorio>`

![image](https://github.com/user-attachments/assets/87559e91-9988-465e-a135-c2b6bc715613)


2. Na tela que for apresentada, arraste arquivos para a região mostrada ou clique no botão “Choose your files” para buscar arquivos através do explorador de arquivos do Windows. Adicione um arquivo.  

![image](https://github.com/user-attachments/assets/0e1f02ef-9708-44d9-bb98-586b288bb219)

3. Na sequência, adicione informações pertinentes na seção “Commit Changes”, nos campos abaixo:
   - Resumo de commit
   - Descrição extendida de commit

![image](https://github.com/user-attachments/assets/c5084d3c-b5a5-4faa-af65-df114584d0d3)

4. Abaixo dos campos, devemos escolher se o commit será direto na branch “main” ou se haverá a criação de uma nova branch para esse commit. Escolha pela criação de uma nova branch e dê um nome adequado

> Essa ação, além de criar uma nova branch com o arquivo selecionado, criará também um pull request, não abordaremos em detalhes qual o impacto da criação de um pull request. Por ora, vamos focar apenas que estamos adicionando um arquivo e criando uma nova branch ao mesmo tempo no nosso repositório.

5. A tela que temos agora é de abertura de um pull request. Adicione um título e uma descrição

![image](https://github.com/user-attachments/assets/b27fd468-b66c-4aed-88e3-bf7457af0139)

6. Clique no botão “Create pull request”, localizado logo abaixo da descrição e à direita

Pronto, ao término desses passos temos:

- 1 novo arquivo adicionado
- 1 nova branch
- 1 pull request

Alternativamente, é possível criar uma nova branch separadamente e inserir arquivos diretamente nela, sem gerar um pull request.

Explore essa possibilidade, acesse a página inicial, clique no link de branches, crie uma nova branch e adicione arquivos diretamente na branch (o procedimento é similar ao que já vimos nos passos acima).

### 2.2 Adicionando arquivos através de linhas de comando

#### Requisitos:

- Um repositório criado no github.com
- Software Git Bash já instalado ([Download aqui](https://git-scm.com/downloads)) ou outro terminal de sua escolha

> Substitua os termos entre “<>” que estarão presentes nas instruções abaixo pelas informações do seu repositório/caso.

Diversas vezes vamos nos referir a `<proprietario>` e `<nomeRepositorio>`, essas informações podem ser obtidas na url do seu repositório, conforme imagem abaixo:

![image](https://github.com/user-attachments/assets/df314028-167c-4dd8-9e7c-c6acf25b9b68)


Para este laboratório, os dados que serão utilizados como exemplo são:

- Proprietário: jovisisa
- Nome do repositório remoto (GitHub): gh4w

Antes de qualquer coisa, clonaremos o repositório do GitHub.

#### 2.2.1 Clone de repositório

Nesta etapa, clonaremos um repositório. A essência da clonagem de repositório é capturar um repositório remoto (criado no GitHub.com) e replicá-lo localmente. Ou seja, teremos um repositório git local igual ao existente remotamente, sendo esse repositório sua propriedade ou de outra pessoa.

1. Crie uma nova pasta em “Documentos”, essa será nossa pasta do repositório local git.
   - Abra o explorador de arquivos do Windows
   - Clique em “Documentos”

![image](https://github.com/user-attachments/assets/ccb73ff7-982f-47f0-a092-093d1877dafc)

2. Crie uma nova pasta com o nome gh4w (botão direito do mouse, selecione new e depois Folder)

![image](https://github.com/user-attachments/assets/66ab13f4-8709-4be2-84a1-31e580bfa56f)

3. Acesse a pasta e copie seu endereço

![image](https://github.com/user-attachments/assets/4c342d3c-350b-41ec-864f-3581ce004486)

4. Abra o Git Bash
   - Depois da instalação, vá até o menu iniciar e busque por Git Bash
   - Selecione Git Bash na lista de resultados, conforme figura abaixo:

![image](https://github.com/user-attachments/assets/fecd428c-b949-4cc3-96a5-d9e794b0054a)

> Aqui estamos usando o git bash, porém você pode usar outro terminal como powershell ou cmd

A tela que abrirá será semelhante a imagem a seguir, mas o conteúdo em verde serão as informações relativas à sua própria máquina:

![image](https://github.com/user-attachments/assets/9e2412ef-e01a-4a31-a465-08213976ff79)

5. Com o terminal aberto, execute o comando a seguir para acessar a pasta criada anteriormente. 
```sh
cd "<endereçoPasta>"
```

> O endereço da pasta estará na área de transferência, pois foi copiado no passo 2. Então basta digitar cd e abrir aspas duplas, control+v e fechar aspas duplas

Captura de tela do terminal com o comando: cd 

![image](https://github.com/user-attachments/assets/1de1539a-0dd6-45dd-9aae-fb069fceaa75)

5. Acesse github.com no seu navegador e vá até a página do seu repositório

6. Localize o botão “Code” e copie o link HTTPS

![image](https://github.com/user-attachments/assets/fb241a7d-f643-485f-8905-a03c1da10295)


 7. Execute o comando:
      
```sh
git clone <linkCopiado>
```

> O link copiado já está na área de transferência, digite o comando git clone, depois control + v e depois enter

Imagem mostrando o comando: "git clone https://github.com/jovisisa/gh4w.git" e sua resposta: "Cloning into 'gh4w'... remote: Enumerating objects: 19, done. remote: Counting objects: 100% (19/19), done. remote: Compressing objects: 100% (15/15), done. remote: Total 19 (delta 2), reused 3 (delta 0), pack-reused 0 Receiving objects: 100% (19/19), 7.85 KiB | 2.62 MiB/s, done. Resolving deltas: 100% (2/2), done."

![image](https://github.com/user-attachments/assets/1dd1b535-f888-4c33-987e-4b5bfe0f9fa2)

Pronto, temos o clone do nosso repositório do GitHub em um repositório local. 

A pasta que criamos no passo 1 agora deve conter uma pasta, que é o nosso repositório clonado, contendo todos os arquivos do nosso repositório remoto. 

Pasta local com os arquivos clonados do repositório remoto. Perceba que dentro da pasta criada em Documentos, a ação de clone gera uma pasta que é o repositório remoto

![image](https://github.com/user-attachments/assets/7547928c-1475-441b-b10f-a54a594ac6a1)
 
#### 2.2.2 Adicionando arquivo através de linha de comando  

1. Voltando ao terminal, execute o comando:  
```sh
cd <nomeRepositorio>
```

> O comando acima nos levará até nosso repositório git local, que é o nosso repositório clonado. Perceba que o terminal indicará que agora estamos no nosso repositório e na branch “main”

2. Como boa prática, não devemos fazer alterações direto na “main”, execute o comando a seguir para criar uma nova branch:
   
```sh
 git checkout -b <nomeBranchNova>
```

> O comando acima realiza a criação da nova branch e já nos coloca nessa nova branch, ou seja, as alterações feitas nos passos seguintes estarão nesse escopo.

Captura de tela do terminal mostrando o comando: "$ git checkout -b BranchExemplo", a resposta: "Switched to a new branch 'BranchExemplo'" e a indicação da nossa nova localização: "REDMOND+joasantos@DESKTOP-GV71ASL MINGW64 ~/Documents/gh4w/gh4w (BranchExemplo)"

![image](https://github.com/user-attachments/assets/acf177fd-c676-49d0-86c3-d5048c4b80ba)

3. Agora execute o comando:

```sh
touch <nomeDoArquivo>
```

> Como exemplo, o nome do arquivo será “meu_novo_arquivo.txt”. Esse comando adicionará esse arquivo (que é um .txt vazio) ao meu repositório na branch “BranchExemplo”

4. Agora execute o comando:

```sh
git add .
```

> Utilizando o “.” aplicaremos o comando add a todos os arquivos da pasta, para selecionar arquivos específicos basta substituir o “.” pelo nome dos arquivos com suas extensões, exemplo: git add arquivo1.txt arquivo2.js

![image](https://github.com/user-attachments/assets/bde97fb0-aae2-4f9a-b956-97daa0774967)

5. Em seguida, execute o comando:

```sh
git commit -m "<Descrição>" 
```

> Informação: Esse comando “comita” a alteração feita no repositório local, no nosso caso, a adição de 1 arquivo através do comando do passo 4 com o git add.

Perceba que o Git Bash detectará as alterações feitas e apontará que houve um arquivo alterado, ou seja, o arquivo que criamos na pasta no passo 3

![image](https://github.com/user-attachments/assets/51b20a7c-6731-41c7-b6bf-8063372f1b20)

6. Na sequência, execute o comando:

```sh
git push --set-upstream origin <nomeBranchNova>
```

> Imagem mostrando o comando: "$ git push --set-upstream origin BranchExemplo" e sua resposta: " Enumerating objects: 6, done. Counting objects: 100% (6/6), done. Delta compression using up to 8 threads Compressing objects: 100% (4/4), done. Writing objects: 100% (5/5), 635 bytes | 635.00 KiB/s, done. Total 5 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0) remote: Resolving deltas: 100% (1/1), done. remote: remote: Create a pull request for 'BranchExemplo' on GitHub by visiting: remote:      https://github.com/jovisisa/gh4w/pull/new/BranchExemplo remote: To https://github.com/jovisisa/gh4w.git * [new branch]      BranchExemplo -> BranchExemplo branch 'BranchExemplo' set up to track 'origin/BranchExemplo'."

![image](https://github.com/user-attachments/assets/e63eae22-1efb-47ee-92fa-54aa74b6817e)

> Note que o resultado até aqui é um pouco diferente da inserção de arquivos através da interface do GitHub, visto que não há uma criação automática de um pull request. Conforme já é sinalizado na resposta, que nos orienta a criar um pull request diretamente na interface do GitHub.

7. Acesse a página do seu repositório no navegador. Você receberá a indicação através de um banner de que ocorreram “pushes” na branch que foi criada no terminal, conforme a figura abaixo:  

Captura de tela da página inicial do repositório no GitHub, onde existe um banner com a inscrição: "BranchExemplo had recent pushes 6 minutes ago" ao lado de um botão com a inscrição: "Compare & pull request"

![image](https://github.com/user-attachments/assets/a700b061-1919-4070-bcb3-c4b15782b485)

Conforme mencionado anteriormente, o foco nesta atividade não são os pull requests, isso será abordado na próxima aula. Com isso encerramos a atividade. 🙂

Parabéns por finalizar o conteúdo desta aula! 😸💜
