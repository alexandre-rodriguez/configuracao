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
1. Configurar o git para conectar ao GitHub utilizando SSH.
   - Seguir as instruções do [Help do GitHub](https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh).
2. Configurar as variáveis de ambiente do git
   ```shell
   git config --global user.name "<nome do usuário>"

   git config --global user.email "<email do usuário>"
   ```
3. Listar as configurações do git
   ```shell
   git config --list
   ```





----
voltar ao [README](README.md)
