## **🚀 Deploy de API na Nuvem com Azure DevOps**

Este repositório contém um projeto que demonstra o **deploy de uma API na nuvem** utilizando **Azure DevOps** com um agente **self-hosted**. O objetivo é mostrar como automatizar a implantação de uma aplicação utilizando pipelines personalizados.

---

## **📌 Tecnologias Utilizadas**

- **Linguagem:** C#/.NET 8.0
- **Azure DevOps:** Para versionamento, CI/CD e gerenciamento de pipeline
- **Azure Web App:** Hospedagem da API na nuvem
- **Agente Self-Hosted:** Para execução de jobs no pipeline sem necessidade de agente gerenciado

---

### Pré-requisitos

- **.NET 8 SDK** instalado
- **Conta no Azure** (com permissões para realizar deploy)
- **Docker (caso deseje testar via container)

---

## **📺 Instalação e Uso**

Para rodar o projeto localmente, siga os passos abaixo:

1. **Clone o repositório:**
   ```sh
   git clone https://github.com/seu-usuario/seu-repo.git
   ```
2. **Acesse a pasta do projeto:**
   ```sh
   cd nome-do-projeto

   ```
3. **Restaure os pacotes do .NET:**
   ```sh
   dotnet restore
   ```
4. **Compile a aplicação no modo Release:**
   ```sh
   dotnet build -c Release
   ```
4. **Publique a aplicação:**
   ```sh
   dotnet publish -c Release -o out
   ```
4. **Execute a aplicação localmente:**
   ```sh
   dotnet run --project APITempoDIO.csproj
   ```
Caso deseje testar via Docker, execute:

1. **Criação da imagem Docker:**
   ```sh
   docker build -t meuapp:latest .
   ```
2. **Execução do container:**
   ```sh
   docker run -p 8080:8080 -p 8081:8081 meuapp:latest
   ```
---

Após rodar a aplicação, acesse o **Swagger** para testar os endpoints.

 **📌 Swagger UI:**  
[http://localhost:8080/swagger](http://localhost:8080/swagger)

---

## **🛠 Funcionalidades**

- ✅ **Pipeline de CI/CD no Azure DevOps**
- ✅ **Deploy automatizado em Azure Web App**
- ✅ **Uso de agente self-hosted para execução de jobs**
- ✅ **Integração com Azure Container Registry (opcional, se usou)**
- ✅ **Monitoramento e logs da aplicação via Azure**
---

## **🔧 Configuração do Agente Self-Hosted**

Se deseja utilizar um **agente self-hosted** no Azure DevOps, siga estes passos:

1. **Baixe e instale o agente:**
   ```powershell
   mkdir agent ; cd agent
   Invoke-WebRequest -Uri https://vstsagentpackage.azureedge.net/agent/4.248.0/vsts-agent-win-x64-4.248.0.zip -OutFile agent.zip
   ```
2. **Extraia e configure:**
   ```powershell
   Expand-Archive -Path agent.zip -DestinationPath $PWD
   ./config.cmd
   ```
3. **Inicie o agente:**
   ```powershell
   ./run.cmd
   ```

---

## **Autor** 👨🏻‍💻
<p>
    <img 
      align=left 
      margin=10 
      width=80 
      src="https://avatars.githubusercontent.com/u/79777133?v=4"
    />
    <p>&nbsp&nbsp&nbspEduardo Ramos<br>
    &nbsp&nbsp&nbsp
    <a 
        href="https://github.com/edugramosf">
        GitHub
    </a>
    &nbsp;|&nbsp;
    <a 
        href="https://www.linkedin.com/in/eduardo-ramos-code/">
        LinkedIn
    </a>
    &nbsp;|&nbsp;
    <a 
        href="https://www.dio.me/users/edugramosf">
        DIO
    </a>
    &nbsp;|&nbsp;</p>
</p>
<br/><br/>
<p>
