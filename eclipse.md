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
	
	General &#10145; Editors &#10145; Text Editors &#10145; Spelling
		Desmarcar `Enable spell checking`
	
	General &#10145; Workspace
		Text File Enconding &#10145; Other: `UTF-8`
		New Text File Line Delimiter &#10145; Other: `Unix`
	
	
	
	Validation
		Marcar `Suspend all validators`
	
	
	
	Web  &#10145; CSS Files
		Enconding: `ISO 10646/Unicode(UTF-8)`
	
	Web  &#10145; HTML Files
		Encondig: `ISO 10646/Unicode(UTF-8)`
	
	Web  &#10145; JSP Files 
		Enconding: `ISO 10646/Unicode(UTF-8)`	
	
	
	
	XML &#10145; XML Files
		Encondig: `ISO 10646/Unicode(UTF-8)`

4. Criar uma **Library** para o **hibernate** (Window &#10145; Preferences &#10145; Java &#10145; Build Path &#10145; User Libraries)

   ```java
   //TODO
   ```

5. Criar um **Driver Definitions** para o **MySQL** (Window &#10145; Preferences &#10145; Data Management &#10145; Connectivity &#10145; Driver Definitions)

   ```java
   //TODO
   ```



----
voltar ao [README](README.md)
