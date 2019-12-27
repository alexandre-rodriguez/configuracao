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





----
voltar ao [README](README.md)
