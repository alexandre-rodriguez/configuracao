[TOC]

# Configuração de ambiente de desenvolvimento
## Java
### Instalação
1. Fazer download do arquivo compactado do [java JDK](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html?ssSourceSiteId=otnpt) (versão no momento do tutorial: **jdk1.8.0_231**)
2. Descompactar o arquivo no diretório de sua preferência, por exemplo: `~/desenvolvimento/java`
### <a name="java-configuracao"></a>Configuração
1. Configurar o java
   ```shell
   sudo update-alternatives --install /usr/bin/java java <diretorio-instalacao-java>/jdk1.8.0_231/bin/java 1000

   sudo update-alternatives --install /usr/bin/javac javac <diretorio-instalacao-java>/jdk1.8.0_231/bin/javac 1000
   ```
2. Para verificar a versão instalada
   ```shell
   java -version
   ```

## Git
### Instalação
1. Executar o comando
   ```shell
   sudo apt install git
   ```
2. Verificar a versão instalada
   ```shell
   git --version
   ```
### Configuração
1. Configurar as variáveis de ambiente do git
   ```shell
   git config --global user.name "<nome do usuário>"

   git config --global user.email "<email do usuário>"
   ```
2. Listar as configurações do git
   ```shell
   git config --list
   ```

## Maven
### Instalação
1. Fazer download do arquivo compactado do [Maven](https://maven.apache.org/download.cgi) (versão no momento do tutorial: **apache-maven-3.6.3**)
2. Descompactar o arquivo no diretório de sua preferência, por exemplo: `~/desenvolvimento/maven`
3. editar o arquivo `~/.profile` e incluir as linhas abaixo no final do arquivo:
   ```shell
   export M3_HOME=<diretorio-instalacao-maven>/apache-maven-3.6.3
   export MAVEN_HOME=<diretorio-instalacao-maven>/apache-maven-3.6.3
   export PATH=${M3_HOME}/bin:${PATH}
   ```
4. Carregar as configurações acima:
   ```shell
   source ~/.profile
   ```
5. Verificar a versão instalada
   ```shell
   mvn --version
   ```

## NVM
### Instalação
1. Fazer o download e instalar o [NVM](https://github.com/nvm-sh/nvm) com o comando abaixo (versão no momento do tutorial: **v.35.2**):
   ```shell
   wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
   ```
2. Verificar a versão instalada
   ```shell
   nvm --version
   ```
### Uso
1. Instalar a última release do Node.js:
   ```shell
   nvm install node
   ```
2. Para listar as versões disponíveis do Node.js  para instalação:
   ```shell
   nvm ls-remote
   ```
3. Para listar as versões instaladas do Node.js:
   ```shell
   nvm ls
   ```
4. Definir uma versão padrão do Node.js:
   ```shell
   nvm alias default <versão>
   ```
5. Usar uma versão do Node.js:
	```shell
	nvm use <versão>
	```
6. Para saber qual a versão atual do Node.js
	```shell
	nvm current
	```
7. Para saber qual a versão sendo utilizada do Node.js
   ```shell
   node --version
   ```
8. Para saber qual a versão sendo utilizada do NPM
   ```shell
   npm --version
   ```

## Mysql
### Instalação
1. Fazer download do pacote do repositório apt do [MySQL](https://dev.mysql.com/downloads/repo/apt/)
2. Instalar o pacote do repositório usando dpkg:
   ```shell
   sudo dpkg -i mysql-apt-config_0.8.14-1_all.deb
   ```
3. Atualizar as listas de pacotes dos repositórios do sistema:
   ```shell
   sudo apt update
   ```
4. Instalar o MySQL Server:
   ```shell
   sudo apt install mysql-server
   ```
5. Executar o script para configurar instalação segura:
   ```shell
   sudo mysql_secure_installation
   ```
   - Responder as seguintes perguntas
     - **"Would you like to setup VALIDATE PASSWORD component?"** com um <kbd>ENTER</kbd>
     - **"Change the password for root?"** com um  <kbd>ENTER</kbd>
     - **"Remove anonymous users?"** com um `Y`
     - **"Disallow root login remotely?"** com um `Y`
     - **"Remove test database and access to it?"** com um  <kbd>ENTER</kbd>
     - **"Reload privilege tables now?"** com um `Y`
6. Instalar o MySQL Workbench
   ```shell
   sudo apt install mysql-workbench-community
   ```
### Comandos
1. Verificar o status do serviço:
   ```shell
   sudo systemctl status mysql
   ```
2. Para iniciar o MySQL
   ```shell
   sudo systemctl start mysql
   ```
3. Para parar o MySQL
   ```shell
   sudo systemctl stop mysql
   ```
4. Habilitar inicialização automática do MySQL Server
   ```shell
   sudo systemctl enable mysql
   ```
5. Testar a instalação do MySQL Server acessando o servidor pelo terminal:
    ```shell
    mysql -u root -p
    ```

## Eclipse
### Instalação
1. Fazer download do arquivo compactado do [Eclipse](https://www.eclipse.org/downloads/packages/) (versão no momento do tutorial: **Eclipse IDE 2019-12 R**)
2. Descompactar o arquivo no diretório de sua preferência, por exemplo: `~/desenvolvimento/eclipse`
### Configuração
1. Configurar o java no arquivo `~/desenvolvimento/eclipse/eclipse-jee-2019-12-R/eclipse.ini`
   Incluir as linhas abaixo. (**Obs.:** a inclusão só é necessária, se o java não foi configurado conforme <a href="#java-configuracao">configuração do java</a>)
   
   ```shell
   -vm
   <diretorio-instalacao-java>/bin/java
   ```
2. Criar o arquivo `~/.local/share/applications/eclipse.desktop` com o seguinte conteúdo (**Obs.:** Esse arquivo é criado para fixar o eclipse na barra lateral)
   ```shell
   [Desktop Entry]
   Name=Eclipse
   Comment=Eclipse
   Exec=<diretorio-instalacao-eclipse>/eclipse
   Icon=<diretorio-instalacao-eclipse>/icon.xpm
   Terminal=false
   Type=Application
   ```

## Spring Tool Suite
### Instalação
1. Fazer download do arquivo compactado do [Spring Tool Suite](https://spring.io/tools/) (versão no momento do tutorial: **4.5.0**)
2. Descompactar o arquivo no diretório de sua preferência, por exemplo: `~/desenvolvimento/sts`
### Configuração
1. Configurar o java no arquivo `~/desenvolvimento/sts/sts-4.5.0/SpringToolSuite4.ini`
   Incluir as linhas abaixo. (**Obs.:** a inclusão só é necessária, se o java não foi configurado conforme [configuração do java](#java-configuracao))
   
   ```shell
   -vm
   <diretorio-instalacao-java>/bin/java
   ```
2. Criar o arquivo `~/.local/share/applications/sts.desktop` com o seguinte conteúdo (**Obs.:** Esse arquivo é criado para fixar o Spring Tool Suite na barra lateral)
   ```shell
   [Desktop Entry]
   Name=STS
   Comment=Spring Tool Suite
   Exec=<diretorio-instalacao-sts>/SpringToolSuite4
   Icon=<diretorio-instalacao-sts>/icon.xpm
   Terminal=false
   Type=Application
   Categories=Development;IDE;Java;
   StartupWMClass=Spring Tool Suite 4
   ```

## Visual Studio Code
### Instalação
1. Fazer download do arquivo compactado do [Visual Studio Code](https://code.visualstudio.com/download) (versão no momento do tutorial: **1.41**)
2. Descompactar o arquivo no diretório de sua preferência, por exemplo: `~/desenvolvimento/sts`
### Configuração
1. Configurar o java no arquivo `~/desenvolvimento/sts/sts-4.5.0/SpringToolSuite4.ini`
   Incluir as linhas abaixo. (**Obs.:** a inclusão só é necessária, se o java não foi configurado conforme [configuração do java](#java-configuracao))
   
   ```shell
   -vm
   <diretorio-instalacao-java>/bin/java
   ```
2. Criar o arquivo `~/.local/share/applications/sts.desktop` com o seguinte conteúdo (**Obs.:** Esse arquivo é criado para fixar o Spring Tool Suite na barra lateral)
   ```shell
   [Desktop Entry]
   Name=STS
   Comment=Spring Tool Suite
   Exec=<diretorio-instalacao-sts>/SpringToolSuite4
   Icon=<diretorio-instalacao-sts>/icon.xpm
   Terminal=false
   Type=Application
   Categories=Development;IDE;Java;
   StartupWMClass=Spring Tool Suite 4
   ```
