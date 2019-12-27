## Visual Studio Code
### Instalação
1. Fazer download do arquivo compactado do [Visual Studio Code](https://code.visualstudio.com/download) (versão no momento do tutorial: **1.41**)
2. Descompactar o arquivo no diretório de sua preferência, por exemplo: `~/desenvolvimento/VSCode`
### Configuração
1. Criar o arquivo `~/.local/share/applications/vscode.desktop` com o seguinte conteúdo (**Obs.:** Esse arquivo é criado para fixar o Visual Studio Code na barra lateral)

 ```shell
   [Desktop Entry]
   Name=VSCode
   Comment=Visual Studio Code
   Exec=/home/alexandre/desenvolvimento/VSCode/code
   Icon=/home/alexandre/desenvolvimento/VSCode/resources/app/resources/linux/code.png
   Terminal=false
   Type=Application
   Categories=Development;IDE;Java;
   StartupWMClass=code
   ```





----
voltar ao [README](README.md)
