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





----
voltar ao [README](README.md)
