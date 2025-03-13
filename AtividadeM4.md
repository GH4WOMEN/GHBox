# Laboratório – Módulo 4: Modern Development

## Objetivo
Esta atividade tem como objetivo colocar em prática os conceitos básicos do GitHub Codespaces e do GitHub Actions, uma poderosa ferramenta de automação oferecida pelo GitHub para construir, testar e implantar seu código.

## Pré- Requisitos:
- Um repositório no GitHub

> Caso ainda não tenha um repositório criado, seguir os passos abaixo de criação de repositório. **Caso já tenha um criado, pular para o passo 2**.

### 1. Criar um Repositório no GitHub:
1.	Crie um repositório no GitHub (assim como vocês fizerem nas atividades anteriores caso ainda não tenha um criado)
2.	Nomeie o repositório como "gh-actions-webapp-seunome"
3.	Selecione a opção para inicializar o repositório com um arquivo README.md.
![image](https://github.com/user-attachments/assets/dce5b3c4-f22a-4c39-b7b7-22d8effa3348)

4.	Selecione a opção para inicializar o repositório com um arquivo .gitignore e selecione o template do VisualStudio.

![image](https://github.com/user-attachments/assets/24f953c2-f8fe-49d5-b5f7-a8227a732735)

### 2.	Criar o Código da Aplicação:

#### 1.	Inicialize um Codespace.
  1. Clique no botão “Code”
     
     ![image](https://github.com/user-attachments/assets/a414e37c-d3b2-4fe5-bb7e-fe791a8a2300)

  2. Selecione a aba "Codespaces"

   ![image](https://github.com/user-attachments/assets/b72c588e-88e6-46b7-86e2-0231789a2d10)

  4.	Clique no botão “Create codespace on main”.

   ![image](https://github.com/user-attachments/assets/dce11fd1-a7d3-417a-b476-f4cb76cc3ecf)

 Aguarde até que o setup esteja completo.

#### 2.	Crie uma aplicação dotnet core wepapp usando a lista de comandos abaixo: (executar os comandos no terminal)
  1.	**Criar o webapp:** ```dotnet new webapp -n github4women```
  2.	**Baixar as dependências:** ```dotnet restore **/*.csproj```
  3.	**Compilar o webapp:** ```dotnet build **/*.csproj --no-restore```
  4.	**Rodar o wepapp:** ```dotnet run --project **/*.csproj```

  ![image](https://github.com/user-attachments/assets/a68aca0a-cbd4-4657-aee6-d1fae06fc09e)

> Observação: O Codespace dá a opção de abrir o browser com o webapp rodando. Para isso clique no botão **Open in Browser**. Para parar a execução do webapp precione as teclas “ctrl+c”.

> ![image](https://github.com/user-attachments/assets/718a3b9e-4c93-4bee-b6f9-7beaf58152fb)


#### 3.	Criar o arquivo de Workflow:
1.	Crie um arquivo YAML para definir o workflow. Nomeie-o como dotnet-build.yml e salve-o na pasta **.github/workflows** do seu repositório. (precisa estar na raíz do repositório)
 
 ![image](https://github.com/user-attachments/assets/96654320-a97a-4501-9e4a-827331a49f24)

> Observação: Você pode continuar usando o codespace para realizar esse passo.

#### 4.	Configurar o Workflow:
  1.	O arquivo YAML do workflow deve ser configurado para executar os passos para fazer o build de uma aplicação .NET:
     Exemplo de um workflow:

  ```yaml
      name: .NET

      on:
        push:
          branches: [ "main" ]
        pull_request:
          branches: [ "main" ]
      
      jobs:
        buildapp:
          runs-on: ubuntu-latest
  
          steps:
          - uses: actions/checkout@v4
          - name: Setup .NET
            uses: actions/setup-dotnet@v4
            with:
              dotnet-version: 8.0.x
          - name: Restore dependencies
            run: dotnet restore **/*.csproj
            working-directory: ${{ github.workspace }}
          - name: Build
            run: dotnet build **/*.csproj
  ```


#### 5.	Executar o Workflow:
  1.	Faça um push das alterações para o repositório no GitHub.
     
   ![image](https://github.com/user-attachments/assets/4744a0c7-27fd-468f-920d-c5ed02139256)

  2.	Verifique se o workflow é acionado corretamente.
  
   ![image](https://github.com/user-attachments/assets/ded0574a-73bd-44af-ad0c-e7ad144b9bcb)

 
#### 6.	Verificar o Log do Workflow:
  1.	Após a execução do workflow, verifique o log gerado.

  ![image](https://github.com/user-attachments/assets/599570c4-e01d-49b2-b4e6-b3d602fc2a12)

 Parabéns por finalizar o conteúdo desta aula! 😸💙
