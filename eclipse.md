## Eclipse
### Instalação
1. Fazer download do arquivo compactado do [Eclipse](https://www.eclipse.org/downloads/packages/) (versão no momento do tutorial: **Eclipse IDE 2019-12 R**)
2. Descompactar o arquivo no diretório de sua preferência, por exemplo: `~/desenvolvimento/eclipse`
### Configuração
1. Configurar o java no arquivo `~/desenvolvimento/eclipse/eclipse-jee-2019-12-R/eclipse.ini`
   Incluir as linhas abaixo. (**Obs.:** a inclusão só é necessária, se o java não foi configurado conforme [configuração do java](java.md#configura--o))
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
   
3. Alterar as configurações do eclipse (Window &#10145; Preferences)

   - General &#10145; Editors &#10145; Text Editors &#10145; Spelling
       - Desmarcar `Enable spell checking`

   - General &#10145; Workspace
       - Text File Enconding &#10145; Other: `UTF-8`
       - New Text File Line Delimiter &#10145; Other: `Unix`
   
   - Validation
      - Marcar `Suspend all validators`
   
   - Web  &#10145; CSS Files
      - Enconding: `ISO 10646/Unicode(UTF-8)`
   
   - Web  &#10145; HTML Files
      - Encondig: `ISO 10646/Unicode(UTF-8)`
   
   - Web  &#10145; JSP Files 
      - Enconding: `ISO 10646/Unicode(UTF-8)`
   
   - XML &#10145; XML Files
      - Encondig: `ISO 10646/Unicode(UTF-8)`

4. Criar uma **User Library** para o **Hibernate**

   **Obs.:** Não será necessário quando utilizamos o maven 

   - Fazer download do [hibernate](https://hibernate.org/orm/releases/5.1/) (versão utilizada: **hibernate-release-5.1.17.Final**)

   - Descompactar o arquivo no diretório de sua preferência, por exemplo: `~/desenvolvimento/libs`

   - No Eclipse, criar a User Library  (Window &#10145; Preferences &#10145; Java &#10145; Build Path &#10145; User Library) 

     - Clicar em **New...**

     - Definir um User library name: `hibernate-release-5.1.17.Final`

     - Clicar em **OK**

     - Clicar em **Add External JARs...**

     - Navegar até `~/desenvolvimento/libs/hibernate-release-5.1.17.Final/lib/jpa` e selecionar o arquivo `hibernate-entitymanager-5.1.17.Final.jar`

     - Clicar em **Add External JARs...**

     - Navegar até `~/desenvolvimento/libs/hibernate-release-5.1.17.Final/lib/required` e selecionar todos os arquivos

       ![configuracao-hibernate-eclipse](/home/alexandre/Documentos/configuracao/configuracao-hibernate-eclipse.png)

5. Criar uma **Driver Definition** para o **MySQL** 

   **Obs.:** Não será necessário quando utilizamos o maven 

   - Fazer download do [MySQL Connector](https://dev.mysql.com/downloads/connector/j/5.1.html) (versão utilizada: **mysql-connector-java-5.1.48, Plataform Independent**)

   - Descompactar o arquivo no diretório de sua preferência, por exemplo: `~/desenvolvimento/libs`

   - No Eclipse, criar a Driver Definition (Window &#10145; Preferences &#10145; Data Management &#10145; Connectivity &#10145; Driver Definitions)

     - Clicar em **Add...**
- Filtrar por Vendor: `MySQL`
     - Selecionar `MySQL JDBC Driver - versão 5.1` em **Available driver templates**
- Clicar na aba **JAR List**
     - Remover os jars listados em **Driver files**
- Clicar em **Add JAR/Zip...**
     - Navegar até `~/desenvolvimento/libs/mysql-connector-java-5.1.48`e selecionar o arquivo `mysql-connector-java-5.1.48-bin.jar` 
- Clicar em **OK**
     - Clicar em **Apply and Close**





----
voltar ao [README](README.md)
