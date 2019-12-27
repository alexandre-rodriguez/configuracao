## Spring Tool Suite
### Instalação
1. Fazer download do arquivo compactado do [Spring Tool Suite](https://spring.io/tools/) (versão no momento do tutorial: **4.5.0**)
2. Descompactar o arquivo no diretório de sua preferência, por exemplo: `~/desenvolvimento/sts`
### Configuração
1. Configurar o java no arquivo `~/desenvolvimento/sts/sts-4.5.0/SpringToolSuite4.ini`
   Incluir as linhas abaixo. (**Obs.:** a inclusão só é necessária, se o java não foi configurado conforme [configuração do java](java.md#configuração))
   
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





----
voltar ao [README](README.md)
